---
title: "Krita 3.0.1, versión de prueba."
date: "2016-07-22"
categories: 
  - "uncategorized-es"
---

Dadas las circunstancias inesperadas, nos hemos visto en la necesidad de reorganizar la fecha de lanzamiento de Krita, por lo que no hubo nueva versión la semana pasada, sin embargo, a pesar de los contratiempos, queremos mostrar los avances que se van a implementar al cien por ciento en la versión 3.0.1, la cual está planeada para el 5 de Septiembre del presente. Hay bastante que mostrar, por ejemplo las correcciones de código tales como "el doble punto en el nombre del archivo" (error que sucede al guardar/nombra el archivo), "Falla y cierre del programa con tabletas digitales de menor calidad", "Perdida de memoria interna en las tarjetas de video", entre otros. Nuevas funciones también están disponibles como lo es el ajuste del color de imprenta con el color del monitor llamado _Soft Proofing_. Es necesario tomar en cuenta que puede haber nuevos errores de código y que algunas de las nuevas funciones no trabajen correctamente; la creación del formato .gif o de videos con la función de animación aun esta bajo construcción y es muy posible que no funcione todavía.

Éste lanzamiento es solo una versión de prueba, aun bajo desarrollo para que experimentes y juegues con ella, de hecho la consideramos mucho mejor que la versión estable actual: 3.0.

También hemos progresado en Krita para el sistema OSX, ésta debe funcionar adecuadamente en las últimas versiones desde OSX 10.9 incluyendo 10.10. con todas sus _librerías dinámicas_ que han sido actualizadas.

#### Windows

En Windows, Krita es compatible con las tabletas digitales Wacom, Huion así como Yiynova, ademas de las Surface Pro. Los archivos zip contienen la versión portátil de Krita, la cual puede accederse extrayendo el contenido del archivo y haciendo un doble clic en el enlace correspondiente. Krita es compatible solo con las versiones de Windows 7, 8 y 10, y solo está disponible para la arquitectura de 64bits. Ademas tenemos disponible una versión que junto a _DrMingw_ ayuda a encontrar las fallas y errores de código (_debug_), para mas información puedes ver [FAQ entry](https://docs.krita.org/KritaFAQ#How_can_I_produce_a_backtrace_on_Windows.3F).

- [krita-3.0.1-Alpha-ef558bb-x64.zip](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0.1-Alpha-ef558bb-x64.zip) (MD5: b4e4bc6563fdf1fd62f2b90ba66b3b6e)
- [krita3-x64-dbg-latest.zip](http://files.kde.org/krita/3/windows/debugbuilds/krita3-x64-dbg-latest.zip) (MD5: c039820a78272f2502cc3270b1cc7307

 

#### Linux

Ofrecemos los _[AppImages](http://appimage.org/)_ que pueden usarse sin la necesidad de instalarse en cualquier sistema nuevo de Linux. Solo se requiere de descargar el archivo, hacerlo ejecutable para que funcione. Por ahora solo tenemos _AppImages_ para la arquitectura de 64bits.

- [krita-3.0.1-Alpha-4c91a18-x86_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0.1-Alpha-4c91a18-x86_64.appimage) (MD5: 772ca9e719cf00d4de49fe68c226c41f)

Krita está disponible en _[Ubuntu App Sotore](https://uappexplorer.com/app/krita.krita)_ en el formato _Snap_, gracias a la colaboración de Michael Hall. Nota: la versión de Krita en _Snap_ no funciona con las tarjetas de video de Nvidia dadas las limitaciones en Ubuntu ademas de no tener traducciones.

#### OSX y MacOS

La versión de Krita 3.1 será totalmente combatible con OSX, Krita 3.0 carece de la vista previa instantánea (_Instant Preview)_ así como de el ajuste del lienzo de alta calidad (_High Quality Canvas Sacaling_). Existe ademas el problema de reproducción de imágenes, ésto dada la decisión de Apple en la que se retiró la compatibilidad entre el _OpenGL_ 3.0 y los controladores de video, También existen problemas con los _Touch Pads_ y las Tabletas digitales. Por lo pronto, para que Krita funcione adecuadamente, recomendamos desactivar _OpenGL_. Krita debe funcionar en las versiones de OSX 10.9, 10,10 y 10.11, inclusive se ha reportado que funciona en MacOS.

- [krita-3.0.1-Alpha-4c91a18.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-Alpha-4c91a18.dmg) (MD5: 1d0faca3c92a36527c6fae048e442ce8)
