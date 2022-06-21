---
title: "Krita 4.0.4"
date: "2018-06-13"
categories: 
  - "uncategorized-es"
---

El equipo de Krita se complace en anunciar el lanzamiento de la versión 4.0.4 de nuestro programa, la ultima de ésta serie, esta versión contiene solo correcciones de código.

Ésta es la lista de las correcciones y o cambios:

- El OpenColorIO ahora funciona en Mac OS X
- Se han corregido las fallas visuales al pintar con un pincel del motor de brocha tipo pixel en una mascara de transparencia. ([BUG:394438](https://bugs.kde.org/show_bug.cgi?id=394438))
- Se ha corregido el problema interno al usar el generador de capas.
- Se ha corregido el cierre inesperado del programa al editar capas tipo mascaras de transformación. ([BUG:395224](https://bugs.kde.org/show_bug.cgi?id=395224))
- Se ha añadido la historia del pincel al Script de los Diez pinceles, para mejorar el cambiar continuamente los pinceles.
- Se ha mejorado el desempeño de las capas tipo trazos. ([BUG:361130](https://bugs.kde.org/show_bug.cgi?id=361130), [BUG:390985](https://bugs.kde.org/show_bug.cgi?id=390985))
- Ya no se permite el usar un documento KRA como capa de otro documento KRA, ésto producía errores al abrir estos documentos.
- Ahora se mantiene el canal alfa cuando se usa el filtro de umbral. ([BUG:394235](https://bugs.kde.org/show_bug.cgi?id=394235))
- Ya no se usa automáticamente el nombre de un paquete de pinceles como etiqueta de los mismos. ([BUG:394345](https://bugs.kde.org/show_bug.cgi?id=394345))
- Se ha corregido el poder seleccionar colores usando el Python Script del panel de paletas de color. ([BUG:394705](https://bugs.kde.org/show_bug.cgi?id=394705))
- Ahora se restablecen los últimos colores usados cuando se comienza Krita, mas no cuando se crea una nueva vista. ([BUG:394816](https://bugs.kde.org/show_bug.cgi?id=394816))
- Ahora se permite el crear un grupo de capas aun si el nodo seleccionado es una mascara. ([BUG:394832](https://bugs.kde.org/show_bug.cgi?id=394832))
- Ahora se muestra la opacidad correctamente en el editor de gradientes. ([BUG:394887](https://bugs.kde.org/show_bug.cgi?id=394887))
- Se han eliminado los atajos del teclado que ya no funcionan tales como los de la pasada herramienta de texto. ([BUG:393508](https://bugs.kde.org/show_bug.cgi?id=393508))
- Ahora se puede usar fracciones para designar el angulo de la herramienta de multipincel.
- Se ha mejorado el desempeño del OpenGL, especialmente en Mac OS.
- Se ha corregido el pintado en los grupos de capas aisladas con el funcionamiento de _atravesado_. ([BUG:394437](https://bugs.kde.org/show_bug.cgi?id=394437))
- Se ha mejorado el abrir documentos OpenEXR (aportación de Jeroen Hoolmans)
- El auto guardado funcionará aun cuando Krita esta completamente trabajando en algo mas.
- Se ha mejorado el uso de el lenguaje que se debe usar por de facto.
- Se ha corregido el elegir un color al hacer un doble clic. ([BUG:394396](https://bugs.kde.org/show_bug.cgi?id=394396))
- Se ha corregido el enumerado errático cuando se usa FFMpeg. ([BUG:389045](https://bugs.kde.org/show_bug.cgi?id=389045))
- Se ha corregido el intercambio de canales en Mac OS, donde en 16 y 32 bits flotantes, los canales rojo y azul se intercambian.
- Se ha corregido el uso del modo táctil en versiones recientes con Qt.
- Se ha corregido el uso del estilo de la interfaz Breeze, ya que Krita no trata de producir un _widget_ en una acción separada. ([BUG:392190](https://bugs.kde.org/show_bug.cgi?id=392190))
- Se ha corregido el uso de importe en grupo en Python.
- Ahora se cargan los perfiles de color del sistema en Windows y Mac OS.
- Se ha corregido un cierre inesperado en Mac OS reportado aquí: ([BUG:394068](https://bugs.kde.org/show_bug.cgi?id=394068))

## Descargas

### Windows

En Windows, si se encuentran el cerrado del programa inesperadamente, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por qué suceden.

- 64 bits Windows: [krita-x64-4.0.4-setup.exe](https://download.kde.org/stable/krita/4.0.4/krita-x64-4.0.4-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.0.4.zip](https://download.kde.org/stable/krita/4.0.4/krita-x64-4.0.4.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.4/krita-x64-4.0.4-dbg.zip)

- 32 bits Windows: [krita-4.0.4-x86-setup.exe](https://download.kde.org/stable/krita/4.0.4/krita-x86-4.0.4-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.0.4.zip](https://download.kde.org/stable/krita/4.0.4/krita-x86-4.0.4.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.4/krita-x86-4.0.4-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.0.4-x86\_64.appimage](https://download.kde.org/stable/krita/4.0.4/krita-4.0.4-x86_64.appimage)

En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.

Cuando se actualice, se podrá usar el repositorio de [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) para instalar Krita 4.0.4 en Ubuntu y sus derivados. Se está elaborando también un Snap.

### OSX

- OSX disk image: [krita-4.0.4.dmg](https://download.kde.org/stable/krita/4.0.4/krita-4.0.4.dmg)

Nota: El controlador de gmic-qt y de PDF no están disponibles en Mac OS X.

### Código fuente

- Código fuente: [krita-4.0.4.tar.gz](https://download.kde.org/stable/krita/4.0.4/krita-4.0.4.tar.gz)

### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
