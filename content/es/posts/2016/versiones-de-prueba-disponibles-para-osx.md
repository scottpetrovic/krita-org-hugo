---
title: "Versiones de prueba disponibles para OSX"
date: "2016-09-09"
categories: 
  - "uncategorized-es"
---

Desde el verano, [Julian Thijssen, conocido como Nimmy,](http://kritadev.blogspot.nl/) estudiante patrocinado por el Google Summer of Code, ha estado trabajando arduamente para lograr que Krita y Qt5 funcionen adecuadamente con el OpenGL 3.0 Core Profile. Esto dado a que el OpenGL 3.0 Compatibility Profile no se puede usar en algunos sistemas, tal como lo es OSX, mientras que Krita necesita de éstos para funcionar.

Esto significa que se tiene que eliminar todo el código OpenGL obsoleto de Qt OpenGL Painting, anteriormente ya se había intentado, sin embargo no se logro y quedaron muchas partes sin corregir en todo el código usado.

Ahora esta labor ha sido completada, se envió al proyecto Qt [https://codereview.qt-project.org/#/c/166202/.](https://codereview.qt-project.org/#/c/166202/) Ademas de ésto, también se realizaron mejoras por el lado de Krita, el código implementado ya esta listo y se a añadido al los repositorios principales, es decir que está listo para el siguiente lanzamiento.

_Pero_ se necesita que se ponga a prueba, y para esto se ha creado una "imagen de disco" (dmg) especial para los usuarios de OSX, la intencion es el obtener comentarios e información de los usuarios al probar dicha imagen, no para reportar errores de código (bugs), la información se puede dejar en el foro:[https://forum.kde.org/viewtopic.php?f=137&t=135853](https://forum.kde.org/viewtopic.php?f=137&t=135853) (en inglés)

**Ésta imagen contiene todos los ajustes de la versión 3.0.1 más el de la paleta emergente.**

Imagen de disco: [http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-nimmy2.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-nimmy2.dmg)
