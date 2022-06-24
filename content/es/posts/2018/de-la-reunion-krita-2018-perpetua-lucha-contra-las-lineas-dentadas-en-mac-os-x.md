---
title: "De la reunión Krita 2018: Perpetua lucha contra las lineas dentadas en Mac OS X"
date: "2018-06-04"
categories: 
  - "uncategorized-es"
---

Hace dos semanas que tubimos una muy buena y motivante reunion in Deventer, donde varios miembros del equipo de Krita se juntaron y conocieron. Boud ya nos escribio un [artículo](https://krita.org/en/item/krita-2018-sprint-report) al respecto, por lo que trataremos de evitar repeticion y solo nos enfocaremos en uno de las metas de esta reunion... el corregir los problemas con las tabletas en Mac OS X.

[![](/images/posts/2018/krita_jagged_lines_on_osx.png)](/images/posts/2018/krita_jagged_lines_on_osx.png) Lineas dentadas causadas por la compresión de los eventos de entrada, relacionado con el uso del OpenGL.

### Compresión de los eventos de las tabletas

Desde la primera versión de Krita disponible para Mac OS X, hemos tenido un problema raro. Cuando el usuario pinta rápidamente, los trazos están dentados, también les llamamos torcidas, ésto sucede dado a que los eventos de tableta que vienen del stylus se perdían a cierto punto antes de llegar a Krita.

Debo mencionar que éste problema ya ha sucedido en Krita varias veces en Linux y Windows. En la mayoría de los casos era causado por una actualización de Qt que introducía o activaba la compresión de los eventos: una función especial de Qt que elimina eventos de movimientos extras del ratón o de las tabletas si el programa que los esta usando se hace muy lento al procesarlos a tiempo. Ésta función es necesaria para programas regulares que no se usan para arte digital de pintura, mismos que esperan una gran cantidad de eventos de movimiento y por lo tanto pueden ignorar alguno de ellos. El síntoma principal de ésta compresión son las lineas dentadas, mismas que desaparecen cuando se desactiva el OpenGL, y se ha reportado que en Mac OS X ésto también aplica. Ya he corregido éste problema muchas veces anteriormente en otros sistemas, lo cual me hizo sentir optimista mientras me dirigía a la reunión...

Sin embargo mi optimismo se hizo menos cuando en la reunión revise los recursos Qt: ¡No hay tales eventos de compresión en Mac OS x! Lo que me dejo conmocionado. Las pruebas mostraron que todos los eventos que llegaban a Qt eran entregados correctamente a Krita. Lo cual fue un poco inesperado. Parece que el Mac OS X mismo elimina los eventos si los programas no los aceptan a tiempo (y sigo creyendo que éste es el caso).

Por lo que no pudimos hacer nada al respecto con esta compresión: ya que sucede en alguna parte dentro del sistema operativo o en el controlador. La única manera posible de tratar de corregir ésto es haciendo la interfaz de Krita mucho mas rápida, sin embargo aun así todavía tenemos... OpenGL.

### El prevenir que OpenGL bloquee el proceso de la interfaz de Krita

El síntoma principal de la compresión, esta relacionado con el echo de que en ocasiones OpenGL necesita tiempo para cargar las texturas o para reproducir el lienzo. De manera muy simple, ésto es como se ve el proceso:

1. La imagen se carga en el pincel.
2. El proceso de la interfaz se carga con las texturas en el GPU usando glTexImage2D o glTexSubImage2D.
3. La interfaz llama al QOpenGLWidget::update() para comenzar un nuevo ciclo de reproducción.
4. Qt llama al QOpenGLWidget::paintGL() donde generamos _mipmaps_ para actualizar las texturas y reproducirlas en la pantalla.

Este método funciona bien en todas las plataformas excepto en Mac OS X, donde Krita reproduce las texturas con **mipmaps corrompidos**. Tiempo atrás, cuando encontramos este problema por primera vez, no la supimos entender por lo simplemente hicimos una compostura por encima del problema: añadimos glFinish() entre el cargar las texturas y el reproducirlas. Resolvió el problema con los mipmaps corrompidos, pero hizo el circuito de la reproducción mas lento. Nunca entendimos el por que rea necesario, pero resolvía el problema a cierto punto, y el método usado en Mac OS X se miraba de esta manera:

1. Actualizar la imagen.
2. Cargar las texturas.
3. **Llamar el glFinish() ( MUUUY LEEEENTOOO )**
4. Llamar el QOpenGLWidget::update()
5. Generar mipmas y reproducir las texturas.

Pusimos Krita a prueba con [apitrace](https://github.com/apitrace/apitrace) y resulto obvio que glFinish() es un verdadero problema. Bloquea los circuitos de eventos por largo plazo, haciendo que Mac OS X elimine los eventos de las tabletas. Por lo que tuvimos que eliminarlo, pero la pregunta es ¿Por qué era necesario para empezar? OpenGL garantiza que todas las llamadas del GPU sean ejecutadas en orden cronológico, entonces ¿Por qué se desacomodaban?

Me dedique casi dos días durante la reunión tratando de encontrar el por qué el glFinish() fue necesario a cierto punto. Le dedique otros dos días después de regresar a casa. Inclusive pensé que era un error de código en como se implementa  el protocolo de OpenGL en Mac OS X... pero resultó ser algo mucho mas simple.

Resulta que usamos dos contextos separados para OpenGL: uno (el de Qt) que carga las texturas, y el otro (el de QOpenGLWidget) que reproduce la imagen. Estos dos contextos se pueden compartir, por lo que supusimos que eran equivalentes, pero no lo son. Si bien, comparten todos los recursos, la manera en que procesan los comandos en fila del GPU no esta definida. En Linux y en Windows parecen compartir los comandos en fila por lo que son ejecutados en secuencia; pero en Mac OS X las filas están separadas, por lo que los comandos están reorganizados y últimamente producen mipmaps corruptos...

Ahora nuestro método realmente se mira así:

1. **\[openGL context 1\]** Actualizar la imagen.
2. **\[openGL context 1\]** Cargar las texturas.
3. **\[openGL context 2\]** Llamar al QOpenGLWidget::update()
4. **\[openGL context 2\]** Generar mipmaps y reproducir las texturas (reproduce mipmaps corruptos, ya que todavía no esta terminado)

Así que solo tenemos que mover el cargado al contexto correcto de OpenGL para que el error desapareciera. [La corrección](https://phabricator.kde.org/R37:fb43d4e5be6112c7d9df2ee3f33697d07a614ca6) ya está implementada en la rama principal de desarrollo, lo cual se lanzara en la versión de Krita 4.0.4

### La moraleja

Siempre tomar en cuenta cual contexto se usa en OpenGL para acceder el GPU. Si no se está dentro de QOpenGLWidget::paintGL(), el contexto resultara improvisado.

PS: Y por supuesto, esta corrección no a solucionado el problema con las tabletas completamente. Cierta compresión todavía sucede muy dentro de Mac OS X, pero ahora es muy difícil de notar :)

PPS: La reunión Krita 2018 fue patrocinada por KDE e.V. (viajes) y por la Fundación Krita (hospedaje y comida).

PPPS:

Apple a [descontinuado](https://developer.apple.com/macos/whats-new/) OpenGL...
