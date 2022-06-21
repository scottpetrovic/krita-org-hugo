---
title: "Krita 3.3.1"
date: "2017-10-11"
categories: 
  - "uncategorized-es"
---

Krita 3.3.1 ya está disponible, ésta versión mínima está dedicada a la correccion de algunos errorres y problemas del código presentes en la version 3.3.0. Dos de los ajustes mas importantes son:

- Evitar que Krita se cierre inesperadamente al reiniciar el programa después de haberse cerrado con el panel de imágenes de referencia en estado flotante.
- Cuando los documentos .kra y backup.kra se descomprimían manualmente, Krita no podía abrirlos, lo cual se a corregido.

Ademas, los siguientes cambios y correcciones han sido incluidos:

- Se ha corregido el cierre inesperado del programa cuando se crea un documento "swap" en OSX (Bernhard Liebl).
- Cuando se unen las capas, éstas no incluyen las que se han bloqueado manualmente (Nikita Smirnov).
- Se ha mejorado el funcionamiento y desempeño en general, especialmente en MacOs (Bernhard Liebl).
- Se ha mejorado la presentación para las acciones de arrastrar y mover las capas (Bernhard Liebl).
- Se han mejorado la información emergente (tooltip) en el selector de pinceles (Bernhard Liebl).
- Se ha corregido la fuga de memoria al usar el selector de color (Boudewijn Rempt).
- Se ha corregido el rotar el lienzo al usar el Windows Ink api (Alvin Wong).
- Se ha desactivado el uso de la herramienta de relleno en capas de grupo (Boudewijn Rempt).
- Se ha añadido la capacidad de cambiar el brillo y el contraste en los pinceles con textura (Rad).
- Se ha añadido la capacidad de copiar bajo el cursor (Dmitry Kazakov).
- Se ha mejorado el desempeño de el lienzo con el CPU (Alvin Wong).
- Se ha corregido el cierre inesperado de Krita cuando la memoria de copiado (clipboard) contiene información (Dmitry Kazakov)
- Se ha añadido un botón para abrir los archivos de capas de una imagen (Wolthera van Hövell tot Westerflier).

 

### Descargas

#### Windows

En Windows, si se encuentran con cierres del programa inesperados, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por que suceden.

64 bits Windows: [krita-3.3.1-x64-setup.exe](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x64-setup.exe)

- Portable 64 bits Windows: [krita-3.3.1-x64.zip](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x64-dbg.zip)

 

- 32 bits Windows: [krita-3.3.1-x86-setup.exe](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.3.1-x86.zip](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x86-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- 64 bits Linux: [krita-3.3.1-x86\_64.appimage](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x86_64.appimage)

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.)

En Ubuntu puedes instalar el "snap" de ésta versión. Ademas puedes usar el repositorio [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) en Ubuntu y sus derivados.

#### OSX

- OSX disk image: [krita-3.3.1.dmg](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1.dmg)

Nota: El controlador de gmic-qt y de PDF no está disponible en OSX.

### Código fuente

- Código fuente: [krita-3.3.1.tar.gz](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1.tar.gz)

#### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

#### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

#### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](https://krita.org/en/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22https://krita.org/en/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
