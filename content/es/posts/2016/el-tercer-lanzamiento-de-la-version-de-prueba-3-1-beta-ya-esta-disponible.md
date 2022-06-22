---
title: "El tercer lanzamiento de la versión de prueba 3.1-beta ya está disponible"
date: "2016-11-07"
categories: 
  - "uncategorized-es"
---

¡La tercer versión beta ya está lista! De Krita 3.1 en adelante la compatibilidad con OSX sera oficial. Se recomienda a todos los usuarios de OSX el usar ésta versión en lugar de la ultima lanzada hace dos semanas.

[![krita_animation_3_0_2](/images/posts/2016/krita_animation_3_0_2-1024x826.gif)](https://krita.org/wp-content/uploads/2016/09/krita_animation_3_0_2.gif)

Algo que is importante de notar es el hecho de que al guardar un documento, Krita no espera que la imagen se termine de producir, lo que significa que si Krita está produciendo una imagen, efecto o brochada, aparecerá un mensaje avisando que el documento puede quedar incompleto. Aun estamos trabajando en ésta situación, por lo que el mensaje no es la solución final. Para que los documentos se guarden correctamente sin perder información, es necesario cerciorarse que todas las acciones de Krita se han terminado de producir ademas de guardar el documento constantemente.

De entre las correcciones de código, las siguientes son de las mas importantes:

- Varios de los errores que cierran el programa se han solucionado.Ahora las "hojas de cebolla" (onion skins) no se combinan al juntar las capas.
- El eje centro en el modo de espejo ahora es independiente con cada imagen.
- Ya se puede abrir imágenes png con la etiqueta de resolución corrompida.
- En la herramienta de transformación se ha restaurado el cursor para la acción de "cortar".
- Se ha actualizado la imagen de presentación de Krita (splash image).
- Se ha corregido el cargar los nombres in los archivos ACO.
- Se ha corregido el problema de el "menú vacío" causado por el estilo de atajos de photoshop.

Nota, ésta versión beta contiene una nueva función llamada Lazy brush/mask. Es muy probable que **no** se incluya en la versión final 3.1 dado que requiere bastante trabajo para hacerla útil, por lo pronto solo es una demostración de lo que puede hacer, sin embargo es muy lenta pera ser utilizada en cualquier trabajo, por favor de tomar en cuenta que sabemos que “no funciona” correctamente por lo cual no es necesario reportarlo.

Esta versión es mucho mas estable y productiva que las anteriores betas, nos gustaría que la probaras tal como si fueras a producir un trabajo completo en ella y nos ayudes a reportar todos los problemas y errores que encuentres ¡Gracias!

### Windows

- 32 bits Windows: [krita-3.0.92-x86-setup.exe](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x86-setup.exe) (MD5 Hash: 092d30cbb158b7ebdc027ddba4ae768d)
- Portable 32 bits Windows: [krita-3.0.92-x86.zip](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x86.zip) (MD5 Hash: 78de5fb91b81b6b2c2f08711be5b9a57)
- [Debug symbols. (Unpack in the Krita installation folder) (MD5 Hash: 634630de985522f6b9f88b5f07d30c65)](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x86-dbg.zip)

- 64 bits Windows: [krita-3.0.92-x64-setup.exe](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x64-setup.exe) (MD5 Hash: 37ae1e819948abeefb2b50497bd01993)
- Portable 64 bits Windows: [krita-3.0.92-x64.zip](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x64.zip) (MD5 Hash: 74f15723011b8429c6431aba65d77e1a)
- [Debug symbols. (Unpack in the Krita installation folder) (MD5 Hash: 7d958532d84e73d1d3eaeb29a7ae17b8)](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x64-dbg.zip)

### Linux

- 64 bits Linux: [krita-3.0.92-x86\_64.appimage](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x86_64.appimage) (MD5 Hash: 2437a99ca375fcf79647147680714076)

En el Ubuntu App Store, en el canal beta también puedes encontrar el appimage.

### OSX

- OSX disk image: [krita-3.0.92.dmg](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92.dmg) (MD5 Hash: 4a938af31688f321d75285825a19d902)

### Source code

- Código fuente: [krita-3.0.92.tar.gz](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92.tar.gz) (MD5 Hash: 1a794cd2758e1bf1c63354ae829b0947)
