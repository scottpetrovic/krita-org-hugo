---
title: "Krita 4.0.3"
date: "2018-05-12"
categories: 
  - "uncategorized-es"
---

Se ha detectado una regresión importante en Krita 4.0.2 por lo que hoy se lanza la version 4.0.3: Se ha corregido el que en ciertos casos el copiado entre imágenes que se abren con Krita causan un cierre inesperado del programa ([BUG:394068](https://bugs.kde.org/show_bug.cgi?id=394068)).

[![](images/kiki_4.0_sm-1-1024x463.png)](https://krita.org/wp-content/uploads/2018/03/kiki_4.0_sm-1.png)

## Otras mejoras

- Krita  ahora trata de cargar el sistema del perfil de color en Windows
- Krita ahora puede abrir documentos .rw2 RAW.
- La imagen de inicio del programa "splash image" ahora funciona mejor en HiDPI con pantallas Retina ([BUG:392282](https://bugs.kde.org/show_bug.cgi?id=392282))
- El filtro de exporte de OpenEXR ahora convertirá imágenes con un canal de profundidad antes de ser guardados en vez de mostrar el dialogo de error.
- El filtro de exporte de OpenEXR ya no muestra las advertencias donde se auto nombra filtro TIFF.
- Se a corregido el dialogo de error mostrado incorrectamente al exportar ciertos tipos de filtros. ([BUG:393850](https://bugs.kde.org/show_bug.cgi?id=393850)).
- El metodo "setBackGroundColor" en el Python API se ha renombrado a "setBackgroundColor" para una mejor consistencia.
- Se ha corregido el cerrado del programa al usar KisColorizeMask ([BUG:393753](https://bugs.kde.org/show_bug.cgi?id=393753))

## Descargas

### Windows

En Windows, si se encuentran el cerrado del programa inesperadamente, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por qué suceden.

- 64 bits Windows: [krita-x64-4.0.3-setup.exe](https://download.kde.org/stable/krita/4.0.3/krita-x64-4.0.3-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.0.3.zip](https://download.kde.org/stable/krita/4.0.3/krita-x64-4.0.3.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.3/krita-x64-4.0.3-dbg.zip)

- 32 bits Windows: [krita-4.0.3-x86-setup.exe](https://download.kde.org/stable/krita/4.0.3/krita-x86-4.0.3-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.0.3.zip](https://download.kde.org/stable/krita/4.0.3/krita-x86-4.0.3.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.3/krita-x86-4.0.3-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.0.3-x86\_64.appimage](https://download.kde.org/stable/krita/4.0.3/krita-4.0.3-x86_64.appimage)

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.)

Cuando se actualice, se podrá usar el repositorio de [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) para instalar Krita 4.0.3 en Ubuntu y sus derivados. Se está elaborando también un Snap

### OSX

- OSX disk image: [krita-4.0.3.1.dmg](https://download.kde.org/stable/krita/4.0.3/krita-4.0.3.1.dmg)

Nota: El controlador de gmic-qt y de PDF no está disponible en OSX.

### Código fuente

- Código fuente: [krita-4.0.3.tar.gz](https://download.kde.org/stable/krita/4.0.3/krita-4.0.3.tar.gz)

### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](https://krita.org/en/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22https://krita.org/en/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
