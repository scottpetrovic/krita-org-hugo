---
title: "Krita 3.1.3 versión beta"
date: "2017-04-07"
categories: 
  - "uncategorized-es"
---

Después de una semana de haber lanzado la versión alfa, se pone a disposición la beta, indicio de buena estabilidad, recordemos que ésta versión está orientada a la corrección de errores de código en la serie 3.x.x, esto es, no hay nuevas funciones todavía, las cuales se esperan en la serie 4.x.

Por lo pronto se está puliendo la versión estable y es de bastante importancia la cooperación de los usuarios de Krita, descarga esta versión beta y ponla a prueba, si encuentras problemas, te pedimos que busques en la [lista de errores de código](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1431433&product=krita&query_format=advanced) para verificar si alguien mas ya ha reportado lo mismo, si no encuentras nada referente al problema te agradecemos que lo reportes.

Desde la versión alfa, esto es lo que en lo que se ha trabajado y que se espera funcione adecuadamente:

- Se ha añadido la lista de los contribuyentes durante el Kickstarter 2016 en la ventana "acerca de" de Krita.
- Se usa por defecto el nombre de la mascara con filtro para nombrar la capa misma, anteriormente solo era llamada "efecto" dificultando su identificacion.
- Ya no se cubren las ventanas de dialogo al comenzar el programa tal como sucede con la imagen del "splash screen".
- Se ha rectificado el problema con la mascara de transformacion de tipo liquido, la cual no funcionaba correctamente.
- Se ha correjido el efecto donde el canvas se cubre en negro al usar la herramienta de transformacion liquida al tiempo de estar aumentado en alta escala.
- Se ha corrijido el cargar el "cache" de las reproducciones de video.
- Ahora se usa el selector original de OSX ya que el selector de Krita no puede seleccionar colores mas allá de su propia ventana, tal como en otro programa o imagen.
- Ahora por defecto el guardar o exportar las imagenes en PNG usa una compresion al nivel 3 en ves del nivel 9, ésto agiliza el proceso y la imagen termina con la misma medida.
- Se ha eliminado el problema con el cierre inesperado del programa al usar el atajo del teclado V para crear lineas rectas.
- Se ha corrigido la advertencia durante la instalacion que menciona Calligra.
- Ahora se puede arrastrar las guias con tabletas digitales correctamente.

### Nota para los usuarios de Windows.

**Todavía no se ha podido solucionar o encontrar que es lo produce el problema que algunos sistemas de Windows en tarjetas de video de Intel presentan. Parece estar relacionado con algunas actualizaciones en los controladores de de las tarjetas de video, pero dado a que los desarrolladores no han encontrado este problema en sus sistemas disponibles, no ha sido posible verificar cual es la causa.** Por lo pronto, si tienes problemas puedes desactivar el OpenGL en Krita.

#### Windows

En Windows, si se encuentran con cierres del programa inesperados, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por que suceden.

- 32 bits Windows: [krita-3.1.3-beta.1-x86-setup.exe](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.1.3-beta.1-x86.zip](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x86-dbg.zip)

- 64 bits Windows: [krita-3.1.3-beta.1-x64-setup.exe](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.1.3-beta.1-x64.zip](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x64-dbg.zip)

#### Linux

- 64 bits Linux: [krita-3.1.3-beta.1-x86_64.appimage](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x86_64.appimage)

En Ubuntu puedes instalar el "snap" de ésta versión. Ademas puedes usar el repositorio [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) en Ubuntu y sus derivados.

#### OSX

- OSX disk image: [krita-3.1.3-beta.1.dmg](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1.dmg)

### Source code

- Código fuente: [krita-3.1.3-beta.1.tar.gz](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1.tar.gz)

#### md5sums

Para todas las descargas:

- [md5sums.txt](http://download.kde.org/unstable/krita/3.1.3-beta.1/md5sums.txt)

#### Key

El appimage y la fuente tarbal han sido firmadas, la llave publica se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).
