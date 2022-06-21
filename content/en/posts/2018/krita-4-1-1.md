---
title: "Krita 4.1.1"
date: "2018-07-18"
categories: 
  - "uncategorized-es"
---

Ésta es la primera versión de correcciones de la serie 4.1.x, lo cual incluye:

- Corrección en el cargado de PyKrita cuando se usa PyQt 5.11 (colaboracion de Antonio Rojas, ¡Gracias!) ([BUG:396381](https://bugs.kde.org/show_bug.cgi?id=396381))
- Corrección de cerrado del programa inesperadamente al usar objetos de vectores.  ([BUG:396145](https://bugs.kde.org/show_bug.cgi?id=396145))
- Corrección al cambiar el tamaño de un pincel del motor de pixel en el editor de pinceles. ([BUG:396136](https://bugs.kde.org/show_bug.cgi?id=396136))
- Corrección al usar el lenguaje del sistema en MacOS cuando mas de un lenguaje esta activado.
- Ya no se muestra el botón inhabilitado para seleccionar un color en el panel de las opciones de herramientas de vector. ([BUG:389525](https://bugs.kde.org/show_bug.cgi?id=389525))
- Corrección en el sistema de auto-guardado. ([BUG:393266](https://bugs.kde.org/show_bug.cgi?id=393266))
- Corrección en la curva del filtro de los canales de color. ([BUG:396244](https://bugs.kde.org/show_bug.cgi?id=396244))
- Corrección en la capa que usa la herramienta de imágenes de referencia.
- Corrección al juntar capas en modo aislado. ([BUG:395981](https://bugs.kde.org/show_bug.cgi?id=395981))
- Corrección al abrir documentos con mascaras tipo transformación que usan el filtro tipo caja. ([BUG:395979](https://bugs.kde.org/show_bug.cgi?id=395979))
- Ahora se alerta al usuario cuando se quiere usar Krita en una versión de Windows que ya no es compatible.
- Corrección del cerrado inesperado cuando se oculta el ultimo canal de color disponible. ([BUG:395301](https://bugs.kde.org/show_bug.cgi?id=395301))
- Ahora es posible el cargar paletas que no son compatibles con la licencia GPL tal como https://lospec.com/palette-list/endesga-16
- Reincorporar en el menú la opción "Selección invertida". ([BUG:395764](https://bugs.kde.org/show_bug.cgi?id=395764))
- Ahora se usa KFormat para mostrar números con formatos (contribución de Pino Toscano, ¡Gracias!
- Se ha ocultado la pagina de configuración de los controles deslizantes de color.
- Ahora ya no se puede seleccionar ningún color de una imagen de referencia si ésta es cien por ciento transparente. ([BUG:396358](https://bugs.kde.org/show_bug.cgi?id=396358))
- Se ha corregido el cierre inesperado cuando se enclava una imagen de referencia en un documento.
- Se han corregido algunos problemas al guardar y abrir imágenes de referencia. ([BUG:396143](https://bugs.kde.org/show_bug.cgi?id=396143))
- La herramienta de selección de color ahora funciona con las imágenes de referencia. ([BUG:396144](https://bugs.kde.org/show_bug.cgi?id=396144))
- Se ha extendido el rango del panorama para poder incluir cualquier tipo de imágenes de referencia.

## Descargas

### Windows

En Windows, si se encuentran el cerrado del programa inesperadamente, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por qué suceden.

- 64 bits Windows: [krita-x64-4.1.1-setup.exe](https://download.kde.org/stable/krita/4.1.1/krita-x64-4.1.1-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.1.1.zip](https://download.kde.org/stable/krita/4.1.1/krita-x64-4.1.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.1/krita-x64-4.1.1-dbg.zip)

- 32 bits Windows: [krita-x86-4.1.1-setup.exe](https://download.kde.org/stable/krita/4.1.1/krita-x86-4.1.1-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.1.1.zip](https://download.kde.org/stable/krita/4.1.1/krita-x86-4.1.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.1/krita-x86-4.1.1-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.1.1-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.1/krita-4.1.1-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.1/gmic_krita_qt-x86_64.appimage).

En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.

Cuando se actualice, se podrá usar el repositorio de [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) para instalar Krita 4.1.1 en Ubuntu y sus derivados. Se está elaborando también un Snap.

### OSX

- OSX disk image: [krita-4.1.1.dmg](https://download.kde.org/stable/krita/4.1.1/krita-4.1.1.dmg)

Nota: El panel de dibujo táctil, el controlador de gmic-qt y el de PDF no están disponibles en Mac OS X.

### Código fuente

- Código fuente: [krita-4.1.1.tar.gz](https://download.kde.org/stable/krita/4.1.1/krita-4.1.1.tar.gz)

### md5sum

Para todas las descargas:

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.1/md5sum.txt)

### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
