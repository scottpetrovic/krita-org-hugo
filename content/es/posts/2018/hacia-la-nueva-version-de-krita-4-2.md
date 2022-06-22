---
title: "¡Hacia la nueva versión de Krita: 4.2!"
date: "2018-10-04"
categories: 
  - "uncategorized-es"
---

El equipo de Krita esta trabajando arduamente en lo que será la nueva versión 4.2. En ésta ocasión presentamos un adelanto de lo que encontrarás en ella. Las descargas no están listas para la distribución publica, y **contienen** errores de código, más aun de los que encontraras en la versión estable y algunos de estos pueden producir la perdida de información en los documentos que se usen, por lo que se avisa el no usarlo para trabajos importantes. (También vamos a distribuir la versión 4.1.4 después de todo, ya que queremos remover algunos errores importantes para los usuarios de ésta serie)

\[caption id="attachment\_8252" align="aligncenter" width="850"\][![](/images/posts/2018/2018-fundraiser-hero2.png)](https://krita.org) ¡Apoyanos en nuestro evento para la recaudación de fondos!\[/caption\]

La version 4.2 se puede usar sin embargo para probar lo nuevo que vendrá incluido, lo cual es bastante y por lo que esperamos de tus respuestas. Ademas de lo que veras en esta versión de prueba, también habrá otras modificaciones que aun que no se han incluido en ésta, si estarán en la versión estable final.

## Lo que ya viene incluido

**Mascaras y selecciones**. Hemos realizado bastante trabajo mejorando las mascaras y las selecciones. De hecho, parte de las mejoras ya se pueden apreciar en krita 4.1.3, pero aun hay mas de lo que hemos logrado que vamos a incluir, tal como el hacer mas fácil pintar en las mascaras de selección y nuevas formas de mover y modificar las selecciones, así como un mejor desempeño del programa en general. La selección de opacidad ha recibido nuevas opciones.

https://youtu.be/gWv--Do9L0E

**Mascara de Gama**. Una de las nuevas funciones que mas nos han pedido, la mascara de gama ahora es parte del selector de color. Una [técnica descrita por James Gurney](http://gurneyjourney.blogspot.com/2011/09/part-1-gamut-masking-method.html) que te ayuda a usar colores de forma mas coordinada, ésta mascara funciona con los dos selectores, el artístico y el avanzado, inclusive se pude rotar la mascara en el selector.

![](/images/posts/2018/gamut-masking.png)

**Un desempeño mejorado**. Siempre estamos buscando las maneras de hacer de Krita un programa mas rápido, y la posibilidad de hacerlo siempre está presente con los avances de software. Ésta versión de prueba contiene el nuevo código de Andrey Kamakin hecho en su proyecto para el Google Summer of Code: avances de "La pequeña maquina", justo desde el centro del programa, en donde cada pixel es procesado. Aun hay trabajo por realizar, por lo que puede suceder los cierres del programa de manera inesperada al usar pinceles de gran tamaño. Ademas contiene otra porción del trabajo de Ivan Yossi del mismo evento, la creación de mascaras de pincel ahora usan las instrucciones de vectorizacion del procesador, lo cual resulta en un mejor desempeño y rapidez. Dmitry también estubo ocupado mejorando el desempeño de los estilos de las capas, especialmente la de estilo de trazado, lo que resulta ademas en un mejor reproducción visual. Las capas de llenado de color también actual mucho mas rápido.

**Estando al** **día** Por lo pronto solo en Linux, ya que aun estamos trabajando en el uso de ciertas partes del softaware para los otros sistemas. Al iniciar Krita ahora posee una vista de bienvenida en la cual ademas de abrir nuevos documentos o los últimos ya usados, también se pueden ver las noticias mas recientes directamente desde nuestra pagina. Por defecto la función esta desactivada para evitar que Krita se quiera conectar a nuestra pagina por el Internet cuando éste no está disponible, y solo se muestra un marco con la opción de activación justo arriba del mismo.

[![](/images/posts/2018/news_widget-1024x566.png)](https://krita.org/wp-content/uploads/2018/10/news_widget.png)

**Asistentes de dibujo con colores** Es posible el cambiar colores en los los asistentes de dibujo, los colores seleccionados son guardados con cada documento lo que permite mayor control por documento.

**Activación de la herramienta de transformación al "pegar"**. Cuando se usa la función de copiado/pegado en Krita, el resultado es una nueva capa justo encima de la que se ha seleccionado para el pegado, la mayoría del tiempo, el usuario deseará mover o modificar la parte copiada antes de pegarla permanentemente. Una nueva opción permite el activar la herramienta de transformación justo al momento de pegar.

**Herramienta de traslado mejorada** Las funciones de "deshacer/hacer" siempre presentaban dificultades con ésta herramienta, ahora funciona justo como es de esperar, tal ves un cambio pequeño, pero que ayuda bastante.

**Una mejor vista** Krita 4.2 tendrá muchas composturas las cuales mejoran el proceso de pintado, tales como la posibilidad de cambiar el tamaño de las vistas previas en el panel de capas, una mejor interacción con las paletas de color, hacer posible el traducir los controladores de Python, etc. Ademas hay nuevos modos de mezclado disponibles y mas por ser agregados. El controlador de G'MIC se ha actualizado a la ultima versión disponible.

\[video width="344" height="502" mp4="https://krita.org/wp-content/uploads/2018/08/resize-thumbnail.mp4"\]\[/video\]

**Bastantes composturas de errores** Ya casi estamos a las 200 composturas de errores de código incorporadas en lo que sera 2.4, y el numero sigue creciendo.

## Mas trabajos que estamos realizando

Lo anterior no significa que es todo, esperamos distribuir Krita 4.2 en diciembre, aun que no hemos propuesto la forma de la versión final todavía. Esto solo es una prueba de lo que vendrá.

Aun que solo es una muestra, el siguiente video muestra parte del trabajo que se está realizando el **editor de pinceles**, bajo la mano de nuestro experto en UX, Scott. Como se puede ver, el editor se ha condensado y se esta buscando la solución para poderlo poner en un panel o tenerlo como una ventana flotante, lo cual hará posible el mantenerlo abierto aun cuando se esta pintando.

https://youtu.be/2hWPzNFPIxY

Ademas la ventana de opciones de la **herramienta de texto** se ha mejorado,  y Dmitry está trabajando en hacerla mas correcta mientras que Scott la está haciendo mas fácil de usar.

https://youtu.be/pNsifPZJsjw

El proyecto de Michael de el evento Google Summer of Code no se ha integrado todavía, pero está planeado en incorporarse completamente en Krita 4.2. Su trabajo hará que al usar las paletas de colores sea algo mas estable y con mejor control, incluyendo la posibilidad de guardar las paletas en el documento KRA mismo..

Otra parte en la que se está trabajando es en el **organizador** **de los recursos**, el cual se usa internamente para manejar los aspectos de los pinceles, sus puntas, las gradientes y las texturas tales como el activarlos, desactivarlos, agruparlos, ponerles etiquetas, formar paquetes, etc. Ésto es un trabajo elaborado y toma tiempo, pero una vez terminado Krita sera mucho mas rápido, usará menos memoria poroporcionara un mejor manejor de los recursos.

### **Descargas**

¡Diviértete con la versión de prueba 4.2!

[![](/images/posts/2018/4.2-preview-1024x693.png)](https://www.krita.org)

### Windows

- 64 bits Windows: [krita-x64-4.2.0-preview-setup.exe](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x64-4.2.0-preview-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.0-preview.zip](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x64-4.2.0-preview.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x64-4.2.0-preview-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.0-preview-setup.exe](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x86-4.2.0-preview-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.0-preview.zip](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x86-4.2.0-preview.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x86-4.2.0-preview-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.0-preview-x86\_64.appimage](https://download.kde.org/unstable/krita/4.2.0-preview/krita-4.2.0-preview-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/unstable/krita/4.2.0-preview/gmic_krita_qt-x86_64.appimage).

(Si Firefox carga el enlace como texto en ves de descargar, simplemente has un clic a la derecha y usa la función de descargar.)

### OSX

- OSX disk image: [krita-4.2.0-preview.dmg](https://download.kde.org/unstable/krita/4.2.0-preview/krita-4.2.0-preview.dmg)

Nota: El panel de control táctil, los controladores G'MIC y Python no están disponibles en OSX.

### Código original

- Código original: [krita-4.2.0-preview.tar.gz](https://download.kde.org/unstable/krita/4.2.0-preview/krita-4.2.0-preview.tar.gz)

### md5sum

Para todas las descargas.

- [md5sum.txt](https://download.kde.org/unstable/krita/4.2.0-preview/md5sum.txt)
