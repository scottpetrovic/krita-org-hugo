---
title: "Krita 4.0 versión de prueba"
date: "2017-11-09"
categories: 
  - "uncategorized-es"
---

No hemos tenido la oportunidad de mostrar la version en desarrollo de Krita 4.0, las razones son multiples, mas que nada el estar continuamente mejorando y corrigiendo todas las versiones disponibles.

Entre los trabajos que se han estado realizando tenemos lo que hemos añadido de la versión en desarrollo a las estables 3.2 y 3.3, tal como Windows8 Pointer API, el uso de la reproducción de ANGLE Direct3D, el nuevo controlador de efectos G'Mic, las nuevas opciones en la linea de comando, el poder pintar de manera táctil, nuevos pinceles y modos de mezclado, entre otros trabajos que no se podrán mostrar en la versión 3.x, si no asta que se lance la 4.x.

 

La pasada version de prueba de Krita 4.0 fue en junio del 2017, [ésta versión](https://krita.org/en/item/first-development-builds-for-krita-4-0/) ya posee un gran numero de nuevas funciones:

- Las capas basadas en SVG con mejores herramientas.
- El nuevo motor de pincel tipo aerógrafo de Allan Marshall.
- El pincel de restauración de Eugene Ingerman.
- Un nuevo sistema que advierte al usuario si Krita no puede guardar el documento en el tipo de formato deseado, **ademas que ahora guardar documentos ocurre en el fondo**, esto es puedes guardar y seguir pintando mientras el proceso ocurre sin distracción.
- El nuevo panel de paletas de color de Wolthera.
- La programación con Python (solo disponible en Windows: se necesita de voluntarios para otros sistemas). Eliakin y Wolthera han añadido durante todo el verano pasado nuevos controladores de Python que poseen funciones especiales, esto a la ves que siguen desarrollando y mejorando éste sistema, tales como:
    - Diez pinceles - Te permite añadir hasta diez pinceles de tu gusto y se les asigna un atajo del teclado, lo cual hace su acceso fácil y rápido.
    - Panel de ajustes rápidos - Con botones de valor predefinido del tamaño, opacidad y flujo.
    - Herramientas para la organización de historietas "comics".

## Nuevas adiciones en Krita 4.0

### Se ha mejorado su desempeño de manera significante.

![](/images/posts/2017/gripes.png)

Tras la respuesta de la encuesta del uso de Krita, uno de los problemas principales resulto ser la lentitud, lo cual puede significar varias cosas, siempre habra sierto tipo de pinceles y o funciones que no pueden operar de manera instantanea, lo cual es normal. Aun así, se tuvo la oportunidad de trabajar en un proyecto específico al desempeño de Krita. Aun cuando esto significa que el lanzamiento de Krita se retardará un poco, se considera que este mejoramiento tendrá bastante significado y aceptación para los usuarios, esto incluye:

- Uso múltiple de los núcleos del CPU para el motor de pincel "pixel", alrededor del 80% de los pinceles pertenecen a éste motor.
- Mayor rapidez en el estampado de los trazos de cada pincel.
- Mayor capacidad de cacheo, lo que optimiza la reproducción de los pinceles.

Este video de Wolthera muestra el motor de pincel con uso múltiple de los núcleos del CPU.

https://www.youtube.com/watch?v=wnPUtYo2Y9Y

### Punto de referencia sobre el desempeño de Krita

Se ha añadido el sistema de punto de referencia lo cual nos permite ver el comportamiento de los pinceles, lo cual nos ayuda a crearlos de mejor manera:

![](/images/posts/2017/performance-benchmarking.gif)

 

 

### Cuadriculado de un Pixel

Andrey Kamakin a añadido la opcion de mostrar el cuadriculado de cada píxel cuando se hace un acercamiento del lienzo:

![](/images/posts/2017/pixel-grid-example.gif)

### Vista previa instantánea del pincel

Scott Petrovic ha estado trabajando junto a algunos artista en el diseño del editor de pinceles. Ya se han hecho bastantes cambios, la manera de nombrar y guardar es totalmente nueva. Ademas de la vista previa instantánea al cambiar cada parámetro del pincel.  Ahora también se puede disminuir los espacios de cada lado de la ventana para acomodarla en pantallas mas pequeñas.

![](/images/posts/2017/live-preview.gif)

### Cuadriculado Isométrico

Ésta nueva funcion puede ser controlada y modificada mediante el panel de cuadriculado:

[![](/images/posts/2017/isometric-1024x715.png)](/images/posts/2017/isometric.png)

## Filtros

- Nuevos
    - Filtro de detecto de borde.
    - Filtro de mapeo de altura hacia normal.
    - Filtro de balance de color ASC-CDL, con parámetros de inclinación, compensación y fuerza.
- Filtro de mapeo de gradientes mejorado.

### Capas

- Las capas archivo ahora pueden ser cambiadas de lugar.
- Una conversión de capas ha sido añadida, lo cual guarda las capas regulares reemplazándolas con capas archivo.

### Paneles

- Un nuevo panel para uso de pantallas tactiles, con botones mas grandes similares que asemejan los de una tableta Wacom.

### Y mucho mas

Por supuesto se han corregido un gran numero de errores de código, se ha mejorado la interfaz, etc. Hay [una lista mas detallada](https://krita.org/en/krita-4-0-release-notes/) que se está elaborando (en ingles por lo pronto) y mostrará todas las novedades del próximo lanzamiento de Krita.

### Nuevas funciones en desarrollo

Existen nuevas funciones que aun no están totalmente terminadas pero que se espera puedan ser incorporadas en Krita 4.0:

- La nueva herramienta de texto (apenas se ha comenzado, por lo que falta mucho trabajo por delante).
- Una capa mascara de coloreado mas rápida (ya existe, pero es muy lenta para ser usada).
- Pinceles encimados, donde se podrán poner mas de un tipo de punta de pincel y usarse al mismo tiempo.

Todo ésto bajo construcción, habrá muchos errores de código todavía ya que se está trabajando en ellos, ésta es una versión de prueba, se han hecho los paquetes listos para instalarse pero ten en consideración lo siguiente:

_**Esto es** **código** **pre-alfa. El programa se cerrará inesperadamente, se comportará de manera rara, puede inclusive destruir las** **imágenes** **en las que** **estés** **trabajando al tratar de guardarlas.**_

_**ADEMAS: ¡LOS DOCUMENTOS CON CAPAS DE VECTORES GUARDADOS EN KRITA 4.0 NO PODRAN SER EDITADOS EN KRITA3.x!**_

Puedes tener ambas versiones en el mismo sistema, pero las dos usarán la misma configuración, (por lo pronto, ya que ésto puede cambiar), lo que significa que cualquiera de las dos puede confundirse al tratar de usar los mismos archivos, pinceles y otros parámetros establecidos personalmente.

### Descargas

Por lo pronto, todos los paquetes, excepto por el Lime PPA, son creados y administrados por el director del proyecto Krita: Boudewijn Rempt, lo cual no es sustentable. Solo una persona extra ha ayudado a mantener los códigos para la creación del paquete de Windows. Se necesita realmente de voluntarios que puedan mantener los paquetes de Linux y MacOS/OSX vigentes. Lo que sugiere:

- El **Appimage** carece de **Python** y **sonido**, puede que también carezca del panel de pintura tactil basado en QML. No hemos logrado encontrar la forma de añadir éstas funciones en el Appimage, el cual para construirlo, requiere de un codigo que ya está anticuado, y Boudewijn no tiene tiempo nesesario para mejorarlo, con todo el resto del proyecto bajo su cuidado. **Por lo que necesitamos de  un mantenedor para los paquetes de Linux**.
- El **OSX/MacOS** carece de **DMG**, ademas de **Python**, el uso de **PDF** externos y el controlador **G'Mic**. Boudewijn simplemente no tiene el conocimiento detrás de estos sistemas para lograr integrar tales funciones. El desarrollo de Krita en OSX se ha mejorado gracias a Berhhard Liebl, pero aun con su ayuda **se necesita de un mantenedor para MacOS/OSX**.

 

### Descargas

#### Windows

En Windows, si se encuentran con cierres del programa inesperados, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por que suceden.

No hay paquetes de 32 bits en Windows, tampoco un instalador.

- Portable 64 bits Windows: [krita-4.0.0-prealpha.2c.zip](https://download.kde.org/unstable/krita/4.0.0-prealpha.2/krita-4.0.0-prealpha.2c.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.0.0-prealpha.2/krita-4.0.0-prealpha.2c-dbg.zip)

#### Linux

- 64 bits Linux: [krita-4.0.0-pre-alpha-x86\_64.appimage](https://download.kde.org/unstable/krita/4.0.0-prealpha.2/krita-4.0.0-pre-alpha-x86_64.appimage)

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.)

#### OSX

- OSX disk image: [krita-4.0.0-prealpha.2b.dmg](https://download.kde.org/unstable/krita/4.0.0-prealpha.2/krita-4.0.0-prealpha.2b.dmg)

Nota: El controlador de gmic-qt y de PDF no está disponible en OSX.

### Código fuente

- Código fuente: [krita-4.0.0-prealpha.2.tar.gz](https://download.kde.org/unstable/krita/4.0.0-prealpha.2/krita-4.0.0-prealpha.2.tar.gz)

#### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

#### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

#### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](https://krita.org/en/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22https://krita.org/en/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
