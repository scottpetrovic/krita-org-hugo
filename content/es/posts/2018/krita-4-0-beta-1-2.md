---
title: "Krita 4.0 beta-1"
date: "2018-01-11"
categories: 
  - "uncategorized-es"
---

Hemos entrado, oficialmente en la etapa de "congelamiento", lo cual en lenguaje de desarrolladores significa "¡Es suficiente!".  Todas las nuevas funciones planeadas para la version 4.0 ya están listas, nada más será añadido desde éste punto hasta el lanzamiento final, tiempo que se usará para corregir cuantos errores de código sean posibles.

El cambio de las versiones 3.x y 4.x es tan extensa e importante que nos es necesario hacer notar la siguiente advertencia:

_**EL FORMATO DE LAS CAPAS DE VECTORES HA CAMBIADO. SI GUARDAS UN DOCUMENTO EN KRITA 4.0 CON CAPAS DE VECTORES, KRITA 3.X NO PODRÁ ABRIRLOS. DE IGUAL MANERA SI HAS CREADO UN DOCUMENTO EN KRITA 3.X CON VECTORES Y LUEGO LO ABRES CON KRITA 4.0, ES POSIBLE QUE LAS CAPAS DE VECTORES SE CORROMPAN. ANTES DE ABRIR CUALQUIER DOCUMENTO EN KRITA 4.0, CERSIORATE DE HACER UN DUPLICADO DEL MISMO.**_

Lo mismo va para documentos con texto, ya que en Krita 3.x ésta funcion está basada en ODT, mientra que en Krita 4.x se usará SVG. Esta version beta es la primera que contiene la nueva herramienta de texto, por lo que es necesario notar lo siguiente:

- No es la herramienta que habíamos planeado, si no una alternativa, dado los problemas de impuestos que tuvimos durante el año, no tuvimos el tiempo de elaborar la herramienta con las funciones y capacidades planeadas.
- Dado que el texto en Krita 3.x no es lo suficientemente bueno, fue necesario actualizar de cualquier manera la herramienta misma, por lo que se improviso con pocas funciones, pero suficientes para realizar texto simple, tal como en los diálogos de las historietas.
- Esta simplicidad ha dejado fuera la capacidad de usar texto vertical, para los formatos Chinos y Japoneses. Tampoco se puede manipular las fuentes Open Type, y carece de controles tipográficos.
- La ventana de la herramienta aun está en proceso de construcción, algunas partes serán modificadas y mejoradas, sin embargo, ésta herramienta es mas o menos lo que vendrá durante la versión 4.0

### Otras funciones

Esta versión beta contiene todo lo que vendrá en la versión final, algunas funciones que se han venido elaborando desde el 2016.

- Nuevo sistema de SVG, herramientas y métodos.
- Exportar e importar SVG.
- Nueva herramienta de texto.
- Controlador de Python.
- Panel de la paleta de colores mejorada.
- Tamaños del pincel mas grandes disponibles.
- Modificador de pinceles mejorado.
- Reconstrucción de los métodos de guardado y exportado. Ahora el guardado automático se hace en el fondo sin interrumpir al usuario, exportar ahora presenta advertencias cuando el documento contiene elementos que no se pueden guardar/exportar en el formato elegido.
- La herramienta de colorear se ha optimizado.
- Los pinceles con el motor de "pixel" son mucho mas rápidos en computadoras con procesadores múltiples.
- Muchas mejoras en la vista del programa en general.

Te invitamos a descargar y poner a prueba ésta versión, veras todo lo nuevo y si te encuentras con problemas tales como los errores de código, ¡Repórtalos!

Algo que aún esta en progreso y solo disponible en las "versiones diarias" ó "Nightly build" es el nuevo set de pinceles.

 

### Notas para cada sistema operativo

#### Windows

- Solo hay paquetes de 64bits disponibles. No se ha decidido si habrá de 32bits.
- Se puede descargar la ["versión diaria"](https://binary-factory.kde.org/job/Krita_Nightly_Build/).

#### Linux

- El AppImage no contiene la habilidad de sonido en las animaciones.
- El AppImage no contiene la habilidad de usar el controlador Python.
- El AppImage si contiene la version mas reciente del controlador G'MIC.

#### OSX

- La aplicación no contiene el controlador de G'MIC
- La aplicación no contiene el controlador de Python
- La aplicación no contiene la habilidad de importar documentos PDF.

### Descargas

#### Windows

En Windows, si se encuentran con cierres del programa inesperados, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por que suceden.

- 64 bits Windows: [krita-x64-4.0.0.51-setup.exe](https://download.kde.org/unstable/krita/4.0.0.51/krita-x64-4.0.0.51-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.0.0.51.zip](https://download.kde.org/unstable/krita/4.0.0.51/krita-x64-4.0.0.51.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.0.0.51/krita-x64-4.0.0.51-dbg.zip)

#### Linux

- 64 bits Linux: [krita-4.0.0-beta.1-x86\_64.appimage](https://download.kde.org/unstable/krita/4.0.0.51/krita-4.0.0-beta1.1-x86_64.appimage)

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.)

Cuando se actualice, se podrá usar el repositorio de [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) para instalar Krita 4.0 beta-1 en Ubuntu y sus derivados.

#### OSX

- OSX disk image: [krita-4.0.0-beta.1.dmg](https://download.kde.org/unstable/krita/4.0.0.51/krita-4.0.0-beta.1.dmg)

Nota: El controlador de gmic-qt y de PDF no está disponible en OSX.

### Código fuente

- Código fuente: [krita-4.0.0.51.1.tar.gz](https://download.kde.org/unstable/krita/4.0.0.51/krita-4.0.0.51.tar.gz)

#### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

#### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

#### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](https://krita.org/en/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22https://krita.org/en/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
