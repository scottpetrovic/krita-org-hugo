---
title: "Krita 3.3.3"
date: "2018-01-12"
categories: 
  - "uncategorized-es"
---

Krita 3.3.3. es la versión estable mas reciente, es probable que sea la ultima versión en la serie 3.x. En este lanzamiento se han corregido bastantes errores de código, uno de los mas importantes para los usuarios de Windows es:

- Para los usuarios de tarjetas de video Intel, la reproducción gráfica usará automáticamente Direct3d/Angle. Las recientes actualizaciones del controlador (drivers) de Intel han producido una gran cantidad de problemas con el uso de Krita, esta no es la solución deseada si no una manera de circunvenir el problema. Si el programa se muestra muy lento, se puede intentar usar el OpenGL.

Otros cambios incluye:

- Corrección de la selección de los modos de mezclado cuando la capa es de escala de grises pero la imagen es de RGB.
- En Windows, selección automática del sistema operativo cuando se hace un reporte de error de código directamente desde Krita.
- Ahora se puede seleccionar el valor de un color en porcentaje en el selector de colores específicos.
- Nuevo botón de inversión en los filtros de niveles de color.
- Se ha implementado el abrir y guardar los estilos en los grupos de capas compatibles con PSD.
- Se ha corregido la manera en que se muestra el modo de borrado cuando se cambia entre éste y el modo de pincel.
- El guardado de la visibilidad de los asistentes gráficos en los documentos .kra.
- La posibilidad de usar las reglas con la segunda potencia.
- Se ha inhabilitado el auto desplazamiento en las herramientas de movimiento y transformación.
- Mejoras con los movimientos del "stylus" cuando se usa con el Windows Ink API.
- Se ha corregido el punto de enfoque al aumentar la imagen.
- Se ha corregido el abrir documentos netpbm con comentarios.

### Descargas

#### Windows

En Windows, si se encuentran el cerrado del programa inesperadamente, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por que suceden.

- 64 bits Windows: [krita-3.3.3-x64-setup.exe](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.3.3-x64.zip](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x64-dbg.zip)

- 32 bits Windows: [krita-3.3.3-x86-setup.exe](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.3.3-x86.zip](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x86-dbg.zip)

#### Linux

- 64 bits Linux: [krita-3.3.3-x86\_64.appimage](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x86_64.appimage)

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.)

Cuando se actualice, se podrá usar el repositorio de [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) para instalar Krita 3.3.3 en Ubuntu y sus derivados. Se está elaborando también un Snap.

#### OSX

- OSX disk image: [krita-3.3.3.dmg](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3.dmg)

Nota: El controlador de gmic-qt y de PDF no está disponible en OSX.

### Código fuente

- Código fuente: [krita-3.3.3.tar.gz](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3.tar.gz)

### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
