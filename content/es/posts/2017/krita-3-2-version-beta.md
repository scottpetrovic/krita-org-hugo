---
title: "Krita 3.2 versión beta"
date: "2017-07-18"
categories: 
  - "uncategorized-es"
---

## Krita 3.2 versión beta

Se pone a disposición la por primera vez la versión beta de la serie 3.2, la cual en comparación con 3.1.4 lanzada en mayo, ésta posee un gran numero de correcciones de código así como algunas nuevas funciones. Ayúdanos a encontrar los errores de código, lo cual nos permitirá ofrecerte una versión final mas estable y solida.

### Error reportado

Como toda versión beta, ésta no está lista al cien por ciento, existen errores de código que están presentes, entre estos encontramos uno que deshabilita los controles de tamaño y flujo en la barra de herramientas. Esto ya lo tenemos por conocido y estamos trabajando en ello, problema que estará resuelto en la versión 3.2 final.

### Novedades

- Krita 3.2 usara ahora el nuevo controlador o “plugin” de efectos “gmic-qt” creado por los desarrolladores del proyecto [G'Mic](http://gmic.eu/) con los que continuamos colaborando en la creación de versiones que puedan funcionar correctamente en Windows, OSX y en la mayoría de Linux. Este controlador reemplazará completamente el antiguo “gimic”.
- Se ha añadido una nueva serie de pinceles creados por Radian.

[![](/images/posts/2017/new_brushes-478x1024.jpg)](/images/posts/2017/new_brushes.jpg)

Los cuales están orientados a la creación de pinturas de estilo tradicional:

[![](/images/posts/2017/kiki_with_new_brushes_by_rad.jpg)](/images/posts/2017/kiki_with_new_brushes_by_rad.jpg)

- Ahora se puede controlar la visibilidad y bloqueo de las capas mediante atajos de teclado.
- e ha mejorado el pincel de “clon”.
- Se a agregado una nueva ventana de dialogo la que te permite copiar información de tu sistema para reportar errores de código.
- Hemos agregado la herramienta de “parche inteligente” o “Smart Patch Tool” en ingles, la cual solo estaba planeada para la versión 4.x.

https://youtu.be/jI87VzDtkPY

- l filtro de difuminado Gaussian, ahora puede usar centros de 1000 pixeles en diámetro.

## Correcciones de código

Las correcciones mas destacadas son:

- Habilidad de pintar con el dedo en pantalla táctil, ésta función se puede activar en la ventana de ajustes.
- Aun que no se garantiza ésta corrección en todos y cada uno de los sistemas que usan OpenCL, se ha removido la “linea verde” que delinea el tamaño del pincel en la pantalla.
- Se ha mejorado la estabilidad del programa en general.
- La ventana para abrir y guardar documentos se ha mejorado, ahora debe de seleccionar mejor que carpeta abrir, que nombre predispone y que tipo de archivo se está usando.

Junto al resto de otras correcciones menores.

#### Descargas

La pagina de KDE se ha actualizado, la cual ahora ofrece https.

#### Windows

En Windows, si se encuentran con cierres del programa inesperados, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por que suceden.

- 32 bits Windows: [krita-3.2.0-beta.1-x86-setup.exe](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.2.0-beta.1-x86.zip](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x86-dbg.zip)

- 64 bits Windows: [krita-3.2.0-beta.1-x64-setup.exe](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.2.0-beta.1-x64.zip](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x64-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.3.0-setup.exe](https://download.kde.org/unstable/krita/kritashellex-1.2.3.0-setup.exe)

#### Linux

- - 64 bits Linux: [krita-3.2.0-beta.1-x86\_64.appimage](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x86_64.appimage)

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un click a la derecha en el mismo enlace.)

En Ubuntu puedes instalar el “snap” de ésta versión. Ademas puedes usar el repositorio [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) en Ubuntu y sus derivados.

#### OSX

- OSX disk image: [krita-3.2.0-beta.1.dmg](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1.dmg)

### Código fuente

- Código fuente: [krita-3.2.0-beta.1.tar.gz](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1.tar.gz)

#### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

#### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

#### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](https://krita.org/en/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita]("https://krita.org/en/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
