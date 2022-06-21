---
title: "Krita 3.1 - Versión candidata"
date: "2016-11-30"
categories: 
  - "uncategorized-es"
---

Dada la falta de salud, se alargó el lanzamiento a una semana después, sin embargo con gusto lanzamos hoy la versión candidata 3.1. Existen bastantes errores de código, muchos de los que se han corregido, otros están por corregir antes de la versión final. Entre los avances respecto a los errores tenemos:

- Se arregló el cierre del programa cuando se guarda el archivo en cualquier formato excepto el propio de Krita, con una capa de vectores (Regresión en la beta 3.x)
- Se arregló el exportar imágenes usando krita en la linea de comandos.
- Se actualizó el plug-in de QuickLook en OSX, que usará el tamaño adecuado en las vistas previas (thumbnails).
- Se mejoraron los tamaños de los iconos del menú.
- Se unificaron los colores en todos los iconos en formato svg.
- Se arreglaron las brochas con angulo que ahora funcionan adecuadamente al rotar o usar la función de reflejo del lienzo.
- Se mejoró el estabilizador de brocha.
- Se arregló el espacio isotrópico al pintar con la función de reflejo del lienzo.
- Se arregló un problema interno al guardar los archivos cuando Krita trata de ejecutar mas de una acción las cuales terminan bloqueándose.
- Se arregló el uso con ventanas múltiples, donde las opciones de herramientas están disponibles en todo lugar.
- Se arregló el uso incorrecto de la memoria.
- Se arregló el seleccionar donde se guardan las animaciones (Nota: todavía hay varios errores en éste funcionamiento, pero ya los estamos trabajando).
- Se mejoró la rapidez de presentación en el selector de la paleta emergente.

Puedes darle un vistaso a lo que viene en las notas de lanzamiento, no es concreto pero te puedes dar una idea de como será la version final 3.1: [Ver las notas (en inglés)](https://krita.org/en/release-notes-for-krita-3-1).

### Windows

Nota: para los usuarios de Windows, si has encontrado problemas con el programa por favor sigue [éstas instrucciones.](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para que podamos entender que fue lo que ocurrió. gracias.

- 32 bits Windows: [krita-3.0.94-x86-setup.exe](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x86-setup.exe) (MD5 Hash: 1fa424258d455f92aac071c47d820095)
- Portable 32 bits Windows: [krita\_3.0.94-x86.zip](http://download.kde.org/unstable/krita/3.0.94/krita_3.0.94-x86.zip) (MD5 Hash: fa00cc3575a56083916885626ff97d88)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x86-dbg.zip) (MD5 Hash: 538fefc19ca79cec36346a2b2564162e)

- 64 bits Windows: [krita-3.0.94-x64-setup.exe](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x64-setup.exe) (MD5 Hash: 908f52aee5deee6971783ce3c019e93e)
- Portable 64 bits Windows: [krita\_3.0.94-x64.zip](http://download.kde.org/unstable/krita/3.0.94/krita_3.0.94-x64.zip) (MD5 Hash: 4af2829289476d172032a68d26e55789)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x64-dbg.zip) (MD5 Hash: ee90e2c3e679a74d9fe77eec305f84f4)

### Linux

- 64 bits Linux: [krita-3.0.94-x86\_64.appimage](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x86_64.appimage) (MD5 Hash: e48aa1a805fbb631ab7d908d41c3ab84)

En el Ubuntu App Store, en el canal beta también puedes encontrar el appimage.

### OSX

- OSX disk image: [krita-3.0.94.dmg](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94.dmg) (MD5 Hash: c8fc18364587481d346009f3921a9142)

### Source code

- Código fuente: [krita-3.0.94.tar.gz](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94.tar.gz) (MD5 Hash: a8822566df7743405b37b72f22a1db53)
