---
title: "Krita 4.1.7"
date: "2018-12-13"
categories: 
  - "uncategorized-es"
---

Ya tenemos la nueva versión de Krita disponible la cual se enfoca en la corrección de ciertos problemas presentes en la versión previa dentro de la misma serie 4.1.x.

Una de las correcciones mas importantes es ademas una de las mas extrañas, introducimos un elemento que presenta las novedades de nuestra pagina en el programa mismo cuando no hay ningún documento abierto, este código no es activo y no hace ninguna conexión con por si mismo, pero la parte del codigo de Qt que se requiere para la creación del nuestro interactúa con las opciones de WiFi de la computadora a todo momento. Para referencia véase estos dos reportes: [https://bugreports.qt.io/browse/QTBUG-46015](https://bugreports.qt.io/browse/QTBUG-46015) y [https://bugreports.qt.io/browse/QTBUG-40332](https://bugreports.qt.io/browse/QTBUG-40332).

En otro caso, estuvimos trabajando en otro error de código perteneciente a Qt 5.12 que causa el cierre del programa de manera inesperada en cuanto se usa el stylus de una tableta de dibujo digital. Nuestros paquetes todavía no usan esa versión de Qt por lo que en Windows, MacOs y nuestras Appimages no presentan el problema, éste solo está presente en sistemas mas actualizados tales como Arch Linux.

Aparte de resolver estos dos problemas tenemos estas correcciones y mejoras:

- Se ha corregido el mostrar correctamente si el audio esta disponible, en el menú de animación.
- Se ha deshabilitado el usar cache con el disco duro en Windows, lo cual produce problemas con animaciones que poseen mas de 150 fotogramas.  ([BUG 401326](https://bugs.kde.org/show_bug.cgi?id=401326))
- Se ha corregido el congelamiento del programa al buscar imágenes de muestra cuando estas han cambiado de directorio. ([BUG:401939](https://bugs.kde.org/show_bug.cgi?id=401939))
- Se ha hecho posible el usar  el panel LUT cuando Angle esta activado en Windows, ademas se el código OpenColorIO se ha actualizado.
- Ahora se mantiene el estado de anti-alias en las herramientas de selección.  ([BUG:401730](https://bugs.kde.org/show_bug.cgi?id=401730))
- Se ha añadido un atajo de teclado para la herramienta de texto. ([BUG:401655](https://bugs.kde.org/show_bug.cgi?id=401655))
- Se ha regresado la habilidad de mover la barra de herramientas.
- Se ha hecho posible que al seleccionar con un rango de color se pueda incluir toda la imagen. ([BUG:346138](https://bugs.kde.org/show_bug.cgi?id=346138))
- Se ha habilitado el HiDPI por defecto, los problemas con la visualización del lienzo se han corregido.
- Se ha hecho posible que Krita pueda importar mas de un archivo a la vez cuando se hace mediante el navegador de archivos.  ([BUG:401476](https://bugs.kde.org/show_bug.cgi?id=401476))
- Se ha corregido el uso de la rueda del ratón cuando se usa en un cuadro combinado en Linux. ([BUG:399379](https://bugs.kde.org/show_bug.cgi?id=399379)) Corregido por Mykola Krachkovsky.
- Se ha corregido el calculo de la ausencia de saturación promedio. ([BUG:400493](https://bugs.kde.org/show_bug.cgi?id=))
- Se ha eliminado el cierre inesperado del programa cuando se exporta un composición. ([BUG:400627](https://bugs.kde.org/show_bug.cgi?id=400627))
- Se ha corregido el mostrar correctamente el cursor de la la herramienta de traslado en todos los modos.
- Ahora se puede mover capas invisibles con la herramienta de traslado.
- Se ha corregido un error en el selector artistico de color. ([BUG:399860](https://bugs.kde.org/show_bug.cgi?id=399860))

## Descargas

### Windows

En Windows, si se encuentran el cerrado del programa inesperadamente, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por qué suceden.

- 64 bits Windows: [krita-x64-4.1.7-setup.exe](https://download.kde.org/stable/krita/4.1.7/krita-x64-4.1.7-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.1.7.zip](https://download.kde.org/stable/krita/4.1.7/krita-x64-4.1.7.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.7/krita-x64-4.1.7-dbg.zip)

- 32 bits Windows: [krita-x86-4.1.7-setup.exe](https://download.kde.org/stable/krita/4.1.7/krita-x86-4.1.7-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.1.7.zip](https://download.kde.org/stable/krita/4.1.7/krita-x86-4.1.7.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.7/krita-x86-4.1.7-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.1.7-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.7/krita-4.1.7-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.7/gmic_krita_qt-x86_64.appimage).

En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.

Cuando se actualice, se podrá usar el repositorio de [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) para instalar Krita 4.1.7 en Ubuntu y sus derivados. Se está elaborando también un Snap

### OSX

- OSX disk image: [krita-4.1.7.1.dmg](https://download.kde.org/stable/krita/4.1.7/krita-4.1.7.1.dmg)

Nota: El panel de dibujo táctil, el controlador de gmic-qt y el de PDF no están disponibles en Mac OS X.

### Código original

- Código original: [krita-4.1.7.101.tar.gz](https://download.kde.org/stable/krita/4.1.7/krita-4.1.7.101.tar.gz)

### md5sum

Para todas las descargas:

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.7/md5sum.txt)

### Llaves

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
