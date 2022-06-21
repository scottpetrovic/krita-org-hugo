---
title: "Krita 3.2.1"
date: "2017-08-25"
categories: 
  - "uncategorized-es"
---

Ésta es una versión mínima de correcciones de código, a continuación se presenta la lista de los cambios:

- Se ha corregido el cierre inesperado del programa si solo encuentra OpenGl version 2.1. Los usuarios de Krita 3.2 que necesitaban desactivar OpenGl, ahora pueden reactivarlo.
- Se ha corregido el cierre inesperado de Krita al cambiar el tipo de capas en el controlador de efectos gráficos Gmic-Qt.
- Se ha corregido el problema de cierre del programa al usar Gmic-Qt en imágenes con tamaños poco común.
- Se ha eliminado el problema que al usar la herramienta de texto afectaba el funcionamiento de la herramienta de pinceles.
- La opción de usar diálogos de archivos correspondientes al sistema en uso se ha restaurado.
- Se ha corregido el error de código donde al usar la herramienta de lineas, el control de flujo del pincel era desactivado.
- Los problemas con el panel LUT han sido corregidos.

### Descargas

#### Windows

En Windows, si se encuentran con cierres del programa inesperados, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por que suceden.

- 32 bits Windows: [krita-3.2.1-x86-setup.exe](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.2.1-x86.zip](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x86-dbg.zip)

- 64 bits Windows: [krita-3.2.1-x64-setup.exe](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.2.1-x64.zip](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x64-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- 64 bits Linux: [krita-3.2.1-x86\_64.appimage](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x86_64.appimage)

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un click a la derecha en el mismo enlace.)

En Ubuntu puedes instalar el "snap" de ésta versión. Ademas puedes usar el repositorio [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) en Ubuntu y sus derivados.

#### OSX

- OSX disk image: [krita-3.2.1.dmg](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1.dmg)

Nota: El controlador de gmic-qt y de PDF no está disponible en OSX.

 

### Código fuente

- Código fuente: [krita-3.2.1.tar.gz](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1.tar.gz)

#### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

#### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

#### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](https://krita.org/en/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22https://krita.org/en/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
