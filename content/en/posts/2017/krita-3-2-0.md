---
title: "Krita 3.2.0"
date: "2017-08-17"
categories: 
  - "uncategorized-es"
---

Un poco después de lo planeado, presentamos la version de Krita 3.2.0. La cual incluye el nuevo controlador de filtros G'Mic-qt, la herramienta de "parche inteligente", dibujo con el dedo en pantallas táctiles, nuevos pinceles y muchas correcciones de errores de código.

Éste es un video introductorio de [GDQuest's](http://gdquest.com/):

https://youtu.be/f9K48jXml4s

Ahora Krita incluye el controlador gmic-qt tanto en Windows como en las AppImage para Linux, ésto es, no se necesita descargarlo e instalarlo de manera separada. Nota: El controlador [gmic-qt](https://github.com/c-koi/gmic-qt) no está disponible para el sistema de OSX. Además es posible que necesites [reiniciar las configuraciones previas](https://docs.krita.org/KritaFAQ/es#Restablecer_la_configuraci.C3.B3n_de_Krita.).

### Cambios desde la ultima versión de prueba:

- Se ha corregido el que el panel LUT se mantenga en la posición predefinida al cambiar la ventana de Krita entre mas de un monitor.
- Inicio correcto de el filtro de exposición en el panel LUT.
- Añadir la función faltante en la herramienta de desplazo.
- Se ha mejorado la velocidad del pincel en el modo "normal" en un 30% (primera contribución al código de Daria Scherbatyuk).
- Se ha corregido el cierre inesperado del programa al crear una segunda vista de la misma imagen.
- Se ha mejorado la interacción con el controlador gmic-qt, ahora Krita busca primeramente en su propio archivo.
- Si Krita ha sido creado con Qt 5.7.1 ó mas nuevo, el problema de desplazamiento con el ratón estará solucionado.
- Se ha corregido el poder pintar con gmic-qt en una imagen que no posee el espacio de color RGBA.
- De igual manera en una imagen sin RGBA, ahora se usan los valores de los canales de color correctamente al usar gmic-qt.
- Se ha corregido el poder abrir mas de una ventana de Krita.

 

#### Descargas

#### Windows

En Windows, si se encuentran con cierres del programa inesperados, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por que suceden.

- 32 bits Windows: [krita-3.2.0-x86-setup.exe](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.2.0-x86.zip](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x86-dbg.zip)

- 64 bits Windows: [krita-3.2.0-x64-setup.exe](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.2.0-x64.zip](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x64-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- 64 bits Linux: [krita-3.2.0-x86\_64.appimage](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x86_64.appimage)

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un click a la derecha en el mismo enlace.)

En Ubuntu puedes instalar el "snap" de ésta versión. Ademas puedes usar el repositorio [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) en Ubuntu y sus derivados.

#### OSX

- OSX disk image: [krita-3.2.0.dmg](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0.dmg)

Nota: El controlador de gmic-qt y de PDF no está disponible en OSX.

### Código fuente

- Código fuente: [krita-3.2.0.tar.gz](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0.tar.gz)

#### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

#### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

#### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita]("/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
