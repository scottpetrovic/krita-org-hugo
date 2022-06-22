---
title: "Krita 4.1.5"
date: "2018-10-11"
categories: 
  - "uncategorized-es"
---

Apenas al poco tiempo de la distribución de la versión 4.1.3, ponemos a disposición la versión de krita 4.1.5, esto en gran parte dado al desafortunado accidente con el controlador TIFF. Sin embargo esta versión viene con mucho mas que una pequeña compostura, ya que estamos celebrando la ultima semana de nuestro evento de recaudación de fondos con un encuentro bastante productivo aquí en Deventer, Holanda.

[![](/images/posts/2018/2018-fundraiser-hero2.png)](https://krita.org)

Entre lo que se puede encontrar en nuestro paquete tenemos mejoras en la escala de las pantallas de alta fidelidad tipo "Retina", ademas de la siguiente lista:

- Asociación de los documentos ICO en Krita.
- Actualización automática de la rotación de los pixeles cuando se cambia de pantalla.
- Desactivado del desplazamiento en la herramienta de vista panorámica.
- Desactivado de "arrastrar y dejar" en la lista de los documentos mas recientes. [BUG:399397](https://bugs.kde.org/show_bug.cgi?id=399397)
- Desactivado de las acciones de enfoque cuando se esta editando el texto en forma visual. [BUG:399157](https://bugs.kde.org/show_bug.cgi?id=399157)
- Ya no se añaden los documentos tipo plantilla a la lista de documentos recientes. [BUG:398877](https://bugs.kde.org/show_bug.cgi?id=398877)
- Ya no se permite el crear mascaras en capas bloqueadas. [BUG:399145](https://bugs.kde.org/show_bug.cgi?id=399145)
- Ya no se cierra automáticamente el dialogo de las opciones cuando se oprime la tecla de entrar cuando se busca por un atajo de teclado. [BUG:399116](https://bugs.kde.org/show_bug.cgi?id=399116)
- Llenado de figuras multilineares si un estilo del mismo ya había sido seleccionado. [BUG:399135](https://bugs.kde.org/show_bug.cgi?id=399135)
- Corrección de la tangente normal del "paintop" para su función con imágenes de 16 y 32 bit flotantes. [BUG:398826](https://bugs.kde.org/show_bug.cgi?id=398826)
- Corrección de el mezclado de color cuando se colecta un color por primera vez. [BUG:394399](http://394399)
- Corrección de los problemas con los espacios del nombre al cargar documentos SVG.
- Corrección con el clic a la derecha hecho sobre la linea de tiempo de la animación. [BUG:399435](https://bugs.kde.org/show_bug.cgi?id=399435)
- Corrección del selector de color emergente y su cerrado.
- Corrección de la escala del lienzo en modo "hidpi" [BUG:360541](https://bugs.kde.org/show_bug.cgi?id=360541)
- Corrección al eliminar los atajos de teclado pertenecientes a los dispositivos de entrada (tabletas, stylus, etc.) [BUG:385662](https://bugs.kde.org/show_bug.cgi?id=385662)
- Corrección al cargar texto con lineas múltiples y margen extra. [BUG:399227](https://bugs.kde.org/show_bug.cgi?id=399227)
- Corrección al cargar símbolos especiales de Unicode con espacios en blanco. [BUG:392710](https://bugs.kde.org/show_bug.cgi?id=392710)
- Corrección al cargar el canal alfa en un documento TIFF creado en Photoshop. [BUG:376950](https://bugs.kde.org/show_bug.cgi?id=376950)
- Corrección del atajo de teclado faltante para la herramienta de llenado. [BUG:399111](https://bugs.kde.org/show_bug.cgi?id=399111)
- Corrección al deshacer la acción de la creación de una capa. [BUG:399575](https://bugs.kde.org/show_bug.cgi?id=399575)
- Corrección en el guardado del bloqueo de las capas y bloqueo de alfa. [BUG:399513](https://bugs.kde.org/show_bug.cgi?id=399513)
- Corrección en el guardado de la locación de los archivos de audio en el documento KRA.
- Corrección  en las herramientas de selección y transformación cuando el modo de reflejo en el eje está activado. [BUG:395222](https://bugs.kde.org/show_bug.cgi?id=395222)
- Corrección al ajustar la sesión activa cuando se crea una sesión nueva.
- Corrección al mostrar el selector de color emergente en modo flotante.
- Corrección el atajo de teclado Ctrl-W para el cierre de la ventana en Windows. [BUG:399339](https://bugs.kde.org/show_bug.cgi?id=399339)
- Corrección del panel de la vista panorámica. [BUG:396922](https://bugs.kde.org/show_bug.cgi?id=396922), [BUG:384033](https://bugs.kde.org/show_bug.cgi?id=384033)
- Corrección el atajo de teclado Shift-I para la selección de color.
- Corrección al restaurar las sesiones lo cual bloqueaba Krita y prevenía el cierre del programa. [BUG:399203](https://bugs.kde.org/show_bug.cgi?id=399203)
- Ahora se importa los documentos SVG como tales y no como capas "raster". [BUG:399166](https://bugs.kde.org/show_bug.cgi?id=399166)
- Mejoras en los margenes de las categorías del menú de las funciones de entrada del lienzo.
- Ahora Krita une correctamente las capas aun si el orden no es de arriba hacia abajo. [BUG:399146](https://bugs.kde.org/show_bug.cgi?id=399146)
- Ahora es posible el seleccionar el texto SVG que se ha ocultado en un grupo determinado de objetos y vuelto a mostrar. [BUG:395412](https://bugs.kde.org/show_bug.cgi?id=395412)
- Ahora el selector de color interpreta el canal alfa correctamente. [BUG:399169](https://bugs.kde.org/show_bug.cgi?id=399169)
- Ahora se previene el abrir el dialogo de los filtros en capas bloqueadas. [BUG:398915](https://bugs.kde.org/show_bug.cgi?id=398915)
- Ahora se restaura el pincel aleccionado en el panel de los mismos al iniciar un nuevo documento. [BUG:399340](https://bugs.kde.org/show_bug.cgi?id=399340)
- Ahora se puede usar los factores de escala de las pantallas.
- Ahora se actualiza la historia de los colores al usar la herramienta de llenado. [BUG:379199](https://bugs.kde.org/show_bug.cgi?id=379199)

## Descargas

### Windows

En Windows, si se encuentran el cerrado del programa inesperadamente, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por qué suceden.

- 64 bits Windows: [krita-x64-4.1.5-setup.exe](https://download.kde.org/stable/krita/4.1.5/krita-x64-4.1.5-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.1.5.zip](https://download.kde.org/stable/krita/4.1.5/krita-x64-4.1.5.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.5/krita-x64-4.1.5-dbg.zip)

- 32 bits Windows: [krita-x86-4.1.5-setup.exe](https://download.kde.org/stable/krita/4.1.5/krita-x86-4.1.5-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.1.5.zip](https://download.kde.org/stable/krita/4.1.5/krita-x86-4.1.5.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.5/krita-x86-4.1.5-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.1.5-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.5/krita-4.1.5-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.5/gmic_krita_qt-x86_64.appimage).

En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.

Cuando se actualice, se podrá usar el repositorio de [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) para instalar Krita 4.1.5 en Ubuntu y sus derivados. Se está elaborando también un Snap

### OSX

- OSX disk image: [krita-4.1.5.dmg](https://download.kde.org/stable/krita/4.1.5/krita-4.1.5.1.dmg)

Nota: El panel de dibujo táctil, el controlador de gmic-qt y el de PDF no están disponibles en Mac OS X.

### Código original

- Código original : [krita-4.1.5.tar.gz](https://download.kde.org/stable/krita/4.1.5/krita-4.1.5.tar.gz)

### md5sum

Para todas las descargas.

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.5/md5sum.txt)

### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](https://krita.org/en/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22https://krita.org/en/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
