---
title: "Krita 4.0"
date: "2018-03-22"
categories: 
  - "uncategorized-es"
---

Hoy se lanza la version 4 de Krita, ésta contiene bastantes cambios importantes, por lo que se recomienda leer la información general del lanzamiento, la cual contiene todos los detalles. A continuación se puede apreciar parte de estos cambios en acción.

https://youtu.be/a-CY4hmkg\_I

La nueva imagen de presentación de Krita 4.0 creada por Tyson Tan, muestra a Kiki entre las flores del árbol de ciruela chino, esta versión estaba en planes de lanzamiento desde el año pasado, pero dado los conflictos fiscales se tubo que retrasar bastante, sin embargo Krita, al igual que el ciruelo chino, presenta las mejores flores solo después de un intenso invierno.

[![](../images/kiki_4.0_sm-1-1024x463.png)](https://krita.org/wp-content/uploads/2018/03/kiki_4.0_sm-1.png)

### Información general

Se recomienda leer todos los cambios que se han introducido en Krita 4.0, los cuales incluyen no solo nuevas funciones si no ademas nueva estructuras visuales en las que se muestra el programa.

[Leer la información general](https://krita.org/es/krita-4-0/)

Entre los cambios mas destacados se tiene las herramientas de SVG y texto, así como el controlador de Python, ademas de:

- Herramienta y capa tipo mascara de coloreado. [Mas información en el manual](https://docs.krita.org/Colorize_Mask), (en ingles)

[![](../images/colorize-mask.png)](https://krita.org/wp-content/uploads/2018/02/colorize-mask.png)

- Mascaras de Pincel: duplica las puntas y algunos de los parámetros de cada pincel para un resultado de efectos mas interesantes.

[![](../images/waterpaint.gif)](https://krita.org/wp-content/uploads/2018/02/waterpaint.gif)

- Nuevo juego de pinceles: Se ha creado un nuevo conjunto de los pinceles originales de Krita, este nuevo juego ahora viene como paquete "bundle", ademas que el juego anterior también esta disponible, solo se requiere que se active en el administrador de recursos.

[![](../images/bundles.png)](https://krita.org/wp-content/uploads/2018/03/bundles.png)

### Problemas presentes en esta version

Krita 4.0 presenta un cambio importante, bastante grande por lo que éste paso presenta algunos obstáculos:

- Krita 4.0 usa SVG para las imágenes de vector, lo cual significa que los documentos hechos en Krita 3.x cambiaran un poco al ser abiertos con ésta versión, se recomienda trabajar en copias y no en originales hasta cerciorarse de que no hay problemas.
- La nueva herramienta de texto no está completa en funciones tal como se había planeado. Su creación ha estado enfocada en un solo uso; el texto en historietas, por lo que el desarrollo de la misma aun esta en progreso.
-  Se tiene un nuevo systema para la creacion de las versiones de Linux y Windows, desafortunadamente no se han producido versiones de 32bits.
- Ya que MacOs tiene muy poca memoria compartida, el controlador GMIC no está disponible para esta plataforma.
- El panel de imágenes de referencias ya no está disponible, no solo presentaba una forma anticuada de trabajar si no ademas era responsable (dada su antigüedad) de muchos de los cierres inesperados de Krita. Una nueva herramienta de imágenes de referencia esta bajo construcción.

### Descargas

#### Windows

En Windows, si se encuentran el cerrado del programa inesperadamente, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por qué suceden.

- 64 bits Windows: [krita-x64-4.0.0-setup.exe](https://download.kde.org/stable/krita/4.0.0/krita-x64-4.0.0-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.0.0.zip](https://download.kde.org/stable/krita/4.0.0/krita-x64-4.0.0.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.0/krita-x64-4.0.0-dbg.zip)

Versiones en 32bits no están disponibles hasta nuevo aviso.

Nota: para Windows 7 y 8 se necesita instalar el "Universal C Runtime" de manera separada para que el controlador de Python pueda funcionar, ver el manual (en ingles): [Manual](https://docs.krita.org/Introduction_to_Python_Scripting#Technical_Details).

#### Linux

- - 64 bits Linux: [krita-4.0.0-x86\_64.appimage](https://download.kde.org/stable/krita/4.0.0/krita-4.0.0-x86_64.appimage)

Por el momento el Appimage no posee traducciones que funcionen.

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.)

Cuando se actualice, se podrá usar el repositorio de [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) para instalar Krita 3.3.3 en Ubuntu y sus derivados. Se está elaborando también un Snap.

#### OSX

- macOS disk image: [krita-4.0.0.dmg](https://download.kde.org/stable/krita/4.0.0/krita-4.0.0.dmg)

Nota: El controlador de gmic-qt y de PDF no está disponible en OSX.

### Código fuente

- Código fuente: [krita-4.0.0.tar.gz](https://download.kde.org/stable/krita/4.0.0/krita-4.0.0.tar.gz)

### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](https://krita.org/en/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22https://krita.org/en/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!

\[caption id="attachment\_6455" align="aligncenter" width="1024"\][![](../images/Krita4_Alegoric_final-1024x507.png)](https://krita.org/wp-content/uploads/2018/03/Krita4_Alegoric_final.png) Por Ramon Miranda\[/caption\]
