---
title: "Se termina la reunión Krita 2016 - Nuevas versiones de prueba."
date: "2016-08-29"
categories: 
  - "uncategorized-es"
---

Los artistas, desarrolladores, mantenedores de la pagina web y los escritores de los documentos que estuvieron en La reunión Krita 2016 desde el pasado jueves van poco a poco de regreso a casa, Algunos se quedaran un poco mas, otros se regresan el Domingo.

[![DSCF5848](/images/posts/2016/DSCF5848-1024x768.jpg)](https://krita.org/wp-content/uploads/2016/08/DSCF5848.jpg)

Siempre es algo extremadamente agotador y a la vez un regocijo el tener una reunión en persona, se tocaron bastantes temas:

- Se planteó, y se sigue planteando como el usuario va a interactuar con las herramientas de vectores y [texto](https://phabricator.kde.org/T1004#5 0665), las cuales fueron costeadas en la ultima campaña de "Kickstarter.
- Se realizó una gran cantidad de trabajo para la compatibilidad con [OSX](https://codereview.qt-project.org/#/c/166202) -- ¡El ajuste en el OpenGL parece estar listo para usarse en Qt! Además se implementaron algunas correcciones con el uso de las tabletas digitales.
- ¡Tuvimos tres estudiantes del Google Summer of Code presentes! Wolthera terminó la segunda parte de su proyecto (la primera fue [Soft Proofing](http://wolthera.info/?p=802) la cual ya está en la version 3.0.1): Un nuevo selector de color interno en Krita. Jouni presento su trabajo con la animación y Julian mostró lo que ha hecho con el OpenGL QPainter de Qt.

[![index](/images/posts/2016/index-1024x584.png)](https://krita.org/wp-content/uploads/2016/08/index.png)

 

- Se habló acerca de la publicación por la Fundacion Krita de el libro de Pepper&Carrot de David Revoy.

[![Pepper loves Kiki!](/images/posts/2016/PepperLovesKiki_001-1024x724.png)](https://krita.org/wp-content/uploads/2016/08/PepperLovesKiki_001.png) ¡A Pepper le encanta Kiki!

- Hemos mejorado el proceso para lanzar nuevas versiones así como para recibir pedidos de nuevas funciones, como son implementadas y añadidas a la versión final.
- Jouni junto con Steven, autor de los dibujos de éste articulo y quién está ademas bien establecido en cuestiones de animacion, revisaron la rutina de trabajo que se hace en Krita.
- Se habló de como se necesita bastante de una nueva arquitectura y diseño de el manejador de recursos.
- Se planeo el mejorar la pagina web y la tienda de la misma.
- Dmitry mostró una nuevo controlador de brocha: "marcadores de alcohol" el cual puede usar diámetros enormes -- 2500 pixeles no serán imposibles.
- Corregimos bastantes errores de codigo...

[![Kiki_Angel &Demon](/images/posts/2016/Kiki_Angel-Demon-1-1024x724.png)](https://krita.org/wp-content/uploads/2016/08/Kiki_Angel-Demon-1.png)

- Y finalmente nos divertimos bastante, varios de los miembros de el grupo no se conocían en persona, pero ahora ya tenemos bien localizadas las caras y voces en relación con los apodos en el chat y en los mensajes de los desarrolladores.

La reunion Krita 2016 fue patrocinada por [KDE e.V.](https://www.kde.org/community/donations/) (pasajes) y por la [Fundación Krita](https://krita.org/en/support-us/donations/) (accomodation and food). (lugar y comida). ¡Muchas Gracias! Ademas resulta que la semana que decidimos reunirnos el verano Danes nos recibio con un fuerte calor, afortunadamente pudimos pasarla bien usando una [bodega que nos mantuvo frescos](http://petrusenpaulus.eu/), con Internet y enchufes eléctricos se convirtió en un buen comedor y sala de "hackeo".

[![DSCF5836](/images/posts/2016/DSCF5836-1024x768.jpg)](https://krita.org/wp-content/uploads/2016/08/DSCF5836.jpg)

#### Nuevas versiones disponibles

Y por supuesto ya tenemos nuevas versiones, con una nueva imagen de presentación y correcciones de código.

[![electrichearts_20160517_20160820_kiki_02](/images/posts/2016/electrichearts_20160517_20160820_kiki_02-1024x594.png)](/images/posts/2016/electrichearts_20160517_20160820_kiki_02.png)

- Se arreglo al 100% la opacidad al comienzo de las lineas en OSX
- Ya no se permite que los usuarios eliminen las gradientes auto generadas.
- Se corrigió que el programa se cierre cuando el selector de recursos trata de mostrar un recurso que ha sido eliminado.
- Se actualizo el conjunto original de los modos visuales de Krita.
- Se corrigió el exportar animaciones al formato CSV.
- Se corrigieron las traducciones en Windows.

#### Windows

En Windows Krita puede usar las tabletas digitales Wacom, Huion y Yiynova, también las Surface Pro. Los archivos "zip" portátiles se pueden extraer y abrir haciendo un doble clic en el enlace de Krita.

En windows Krita puede usar las tabletas digitales Wacom, Huion y Yiynova, también las Surface Pro. Se ha probado en Windows7, 8 y 10, solo existen lanzamientos en el formato de 64 bits. Ademas existe la versión que ayuda a rastrear los problemas cuando ocurren, ésta funciona con el programa llamado DrMingw, para mas información [visita ésta página](https://docs.krita.org/KritaFAQ/es#.C2.BFComo_puedo_crear_un_.22backtrace.22_en_Windows.3F). En esta ocasión, Krita puede responder mas lentamente dado a que se ha desactivado la vectorización.

- [krita\_3.0.99.91-x64.zip](http://files.kde.org/krita/3/windows/devbuilds/krita_3.0.99.91-x64.zip)
- [krita3-x64-dbg-latest.zip](http://files.kde.org/krita/3/windows/debugbuilds/krita3-x64-dbg-latest.zip)

#### Linux

Al igual que en las ultimas versiones, y para que mas personas puedan probar el programa en desarrollo sin la necesidad de compilarlo o de repositorios no oficiales, se a puesto a disposición la versión mas nueva en un AppImage, solo en el formato de 64 bits. Una ves descargado el paquete, lo haces ejecutable y lo usas directamente en el mismo archivo, recuerda que aun que funciona muy bien, tanto Krita como AppImage son experimentales.

- [krita-3.0.99.91-Beta-x86\_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0.99.91-Beta-x86_64.appimage)

También puedes obtener Krita en [Ubuntu’s App Store en formato "snap"](https://uappexplorer.com/app/krita.krita). Esta versión incluye las traducciones de Krita. Se puede instalar con el siguiente comando:

snap install --beta krita

#### OSX and MacOS

Krita será totalmente funcional para este sistema en la versión 3.1, por lo pronto en Krita 3.0 todavía faltan algunas funciones tales como la vista previa inmediata y la vista de alta calidad de el lienzo, ademas de problemas tales como el de reproducir imágenes. Esto es dado a que Apple a decidido dejar afuera la compatibilidad con OpenGL 3.0 en algunos dispositivos, por lo pronto se recomienda el desactivar OpenGL en Krita. Esta versión de Krita funciona con OSX 10.9, 10.10 y 10.11, se ha reportado ademas que puede funcionar en MacOS.

- [krita-3.0.99.91.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.99.91.dmg)

#### Source

El paquete con el código para compilar ahora contiene también las traducciones de Krita.

- [krita-3.0.99.91.tar.gz](http://files.kde.org/krita/3/source/krita-3.0.99.91.tar.gz)
