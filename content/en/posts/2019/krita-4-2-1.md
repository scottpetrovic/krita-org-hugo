---
title: "Krita 4.2.1"
date: "2019-06-05"
categories: 
  - "uncategorized-es"
---

## Krita 4.2.1

Apenas unos días después de lanzar la versión 4.2.0 ponemos a disposición la 4.2.1. En ésta se ha resuelto el problema donde después de usar Krita por un tiempo, el dibujar se hace bastante lento, esto por que las entradas de "deshacer" se hacían infinitas. También vienen otros ajustes como el guardar archivos .kra con capas de vectores, donde las imágenes usan letras que no son del "latin1". Tenemos ademas nuevos contribuyentes que han ayudado a solucionar algunos de estos errores: Carl Olsson y Dmitry Utkin, ¡Gracias!

Lista de problemas y errores de código resueltos:

- Lentitud después de uso prolongado ([BUG:408255](https://bugs.kde.org/show_bug.cgi?id=408255), [BUG:408133](https://bugs.kde.org/show_bug.cgi?id=408133))
- Cargar capas de vectores cuando la imagen tiene nombre que no es latin1 ([BUG:408280](https://bugs.kde.org/show_bug.cgi?id=408280))
- Cuadriculado incorrecto después de cambiar el tamaño del lienzo ([BUG:408166](https://bugs.kde.org/show_bug.cgi?id=408166))
- Ventana de propiedades de capas que permanece encima de otras ventanas ([BUG:408170](https://bugs.kde.org/show_bug.cgi?id=408170))
- Uso de filtro de posterizado con sRGB
- Permitir que la animación comience del fotograma 0 ([BUG:408198](https://bugs.kde.org/show_bug.cgi?id=408198))
- Seleccionado del opaco en grupos de capas ([BUG:408236](https://bugs.kde.org/show_bug.cgi?id=408236))
- Revisión de la fuente de almacén (drive) antes de producir la animación ([BUG:408246](https://bugs.kde.org/show_bug.cgi?id=408246))
- Prevención del borrado de capas que estan bloqueadas
- Copiado y duplicado de las capas ([BUG:408028](https://bugs.kde.org/show_bug.cgi?id=408028))
- Transparencia de la ventana de Krita con Qt en Linux ([BUG:408225](https://bugs.kde.org/show_bug.cgi?id=408225))
- Retraso del pincel al principio del trazo ([BUG:408133](https://bugs.kde.org/show_bug.cgi?id=408133))
- Doblaje/Desdoblaje de la imagen previa de las capas
- Hacer y deshacer en la guías de pintura (corregido por Tusooa Zhu)
- Mostrado de guías con Python API ([BUG:408113](https://bugs.kde.org/show_bug.cgi?id=408113))
- Consistencia con el tamaño mínimo de los pinceles
- Consistencia con el valor del espaciado del pincel ([BUG:359453](https://bugs.kde.org/show_bug.cgi?id=359453))
- Comportamiento del seleccionado en panel de las capas ([BUG:408002](https://bugs.kde.org/show_bug.cgi?id=408002))
- Rotación y amplificación del lienzo en macOS ([BUG:404321](https://bugs.kde.org/show_bug.cgi?id=404321))
- Trazos entre objetos de vectores [(BUG:407683](https://bugs.kde.org/show_bug.cgi?id=407683))
- Controlador de la herramienta de documentos ([BUG:408146](https://bugs.kde.org/show_bug.cgi?id=408146))
- Selección del nombre de la capa al editarse ([BUG:400357](https://bugs.kde.org/show_bug.cgi?id=400357))

Krita 4.2.1 ahora usa Qt 5.12.3 lo cual debe resolver los problemas con el arrastrar y relocar documentos, pero puede haber problemas con ls escala de la pantalla en Windows ya que el código experimental que resuelve los problemas con Qt trae nuevos conflictos.

## Descargas

### Windows

En Windows, si se encuentran el cerrado del programa inesperadamente, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por qué suceden.

- 64 bits Windows: [krita-x64-4.2.1-setup.exe](https://download.kde.org/stable/krita/4.2.1/krita-x64-4.2.1-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.1.zip](https://download.kde.org/stable/krita/4.2.1/krita-x64-4.2.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.1/krita-x64-4.2.1-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.1-setup.exe](https://download.kde.org/stable/krita/4.2.1/krita-x86-4.2.1-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.1.zip](https://download.kde.org/stable/krita/4.2.1/krita-x86-4.2.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.1/krita-x86-4.2.1-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.1-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.1/gmic_krita_qt-x86_64.appimage).

En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.

### OSX

- OSX disk image: [krita-4.2.1.dmg](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1.dmg)

Nota: El controlador de gmic-qt no está disponible en Mac OS X.

### Código fuente

- [krita-4.2.1.tar.gz](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1.tar.gz)
- [krita-4.2.1.tar.xz](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1.tar.xz)

### md5sum

Para todas las descargas:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.1/md5sum.txt)

### Key

[El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: 0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). Las firmas están [aquí](http://download.kde.org/unstable/krita/4.2.0-beta2/) (terminan en .sig).

### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
