---
title: "Krita 3.2.0 final - primera versión de prueba"
date: "2017-08-07"
categories: 
  - "uncategorized-es"
---

La semana pasada tuvimos las malas noticias referente a la auditoria de estado financiero hecha por el gobierno Holandés a la Fundación de Krita, en la que debido al manejo de impuestos y la manera en la que la Fundación se remunera, el gobierno decidió multar con mas de veinte mil euros, lo cual dejó a la Fundación sin dinero suficiente para mantener a los únicos dos desarrolladores con sueldo. Justo horas de que Boudewijn Rempt, quien esta a la cabeza de la organización y el desarrollo de Krita, nos comunicó de la difícil situación, la comunidad de los usuarios del programa Krita respondieron de con gran entusiasmo, ayudando con donaciones y propagando las noticias, en un par de días y con la ayuda de todos los usuarios así como del patrocinio de la compañía [Private Internet Access](https://www.privateinternetaccess.com/). se logro recaudar lo perdido en la multa e impuestos, lo cual a logrado que Krita continué en movimiento.

Aun que los problemas ocurrieron desde Febrero, Boudewijn logró mantener el equipo de Krita en continuo desarrollo, por lo cual para los usuarios, no ha existido ninguna interrupción, el programa a seguido y se mantiene en activo. Por lo que hoy se ha logrado lanzar la primera prueba de la versión final.

 

Aun que ésta es prácticamente la versión final 3.2.0, es posible que aparezcan algunos inconvenientes y ó problemas, por lo que es necesario poner a prueba ésta versión antes de su lanzamiento definitivo. De antemano gracias por la toda la ayuda en cualquiera de sus formas, el equipo de Krita les está bastante agradecido, y por supuesto, con los problemas de impuestos ya resueltos, las donaciones y contribuciones se siguen aceptando y seguirán ayudando a hacer de Krita un mejor programa.

La siguiente es una lista de las correcciones de código y problemas que se han resuelto desde la segunda versión beta.

- Mejoras en la manera en que trabaja OpenGL.
- Se muestra de mejor manera cuando el error con wintab32.dll falla al cargarse en Windows.
- Se ha corregido los problemas con la herramientas de lazo para crear figuras y o selecciones, las cuales no cerraban la linea final y no podían usarse después del primer intento.
- Se ha corregido el trabajar con varias archivos abiertos al tiempo que uno de ellos se ha designado para sobreponerse encima de los demás.
- Se ha corregido la memoria de el "nivel de detalle", esto compone el que al cambiar la visibilidad de una capa, el color que se recoge no sea de otra capa ya expirada.
- En el panel de imágenes de referencia, se mantiene o "recuerda" la ultima carpeta abierta.
- Se ha corregido el crear documentos con la función de auto guardar para que estos no se acumulen.
- Se ha añadido la compatibilidad con tabletas digitales de la de tipo uc-logic.
- Se ha mejorado el estabilizador.
- Se ha mejorado la interacción entre Krita y el controlador de filtros gmic-qt.
- Se ha corregido la manera en que se muestra el progreso del controlador gmic-qt.
- Se ha corregido el modificar adecuadamente un pincel que usa como texto "punta".
- Se ha actualizado el juego de pinceles de Krita.

### Descargas

#### Windows

En Windows, si se encuentran con cierres del programa inesperados, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por que suceden.

- 32 bits Windows: [krita-3.2.0-rc.1-x86-setup.exe](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.2.0-rc.1-x86.zip](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x86-dbg.zip)

- 64 bits Windows: [krita-3.2.0-rc.1-x64-setup.exe](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.2.0-rc.1-x64.zip](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x64-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/kritashellex-1.2.4.0-setup.exe)

#### Linux

- - 64 bits Linux: [krita-3.2.0-rc.1-x86_64.appimage](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x86_64.appimage)

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un click a la derecha en el mismo enlace.)

En Ubuntu puedes instalar el “snap” de ésta versión. Ademas puedes usar el repositorio [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) en Ubuntu y sus derivados.

#### OSX

- OSX disk image: [krita-3.2.0-rc.1.dmg](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1.dmg)

### Código fuente

- Código fuente: [krita-3.2.0-rc.1.tar.gz](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1.tar.gz)

#### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-rc.1/md5sums.txt)

#### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

#### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](https://krita.org/en/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-version-beta/%22https://krita.org/en/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
