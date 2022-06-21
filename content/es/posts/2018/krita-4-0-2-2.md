---
title: "Krita 4.0.2"
date: "2018-05-10"
categories: 
  - "uncategorized-es"
---

El equipo de Krita se complace en presentar la versión 4.0.2, ésta actualización es para corregir mas de cincuenta errores de código encontrados desde el lanzamiento de Krita 4.0.0. Durante éste desarrollo se obtuvieron contribuciones para correcciones de código de dos nuevos voluntarios: Emmet O'Neil y Seoras Macdonald, ¡Bienvenidos!

Por favor nótese lo siguiente:

- El panel de imágenes de referencia se ha eliminado completamente, la versión 4.1.0 tendrá una nueva herramienta que reemplazara ésta función. Ya se puede usar en las versiones de prueba de Windows y Linux. Ademas existe un controlador de Python creado por Antoine Roux [que añade un panel similar.](https://github.com/antoine-roux/krita-plugin-reference)
- Las traducciones no funcionan en varias circunstancias. En Linux todo debe funcionar normalmente. En Windows es posible que se tenga que seleccionar el lenguaje deseado como extra en el dialogo de preferencias, lo que también puede ser el caso para MacOS.
- Los paquetes para MacOS ya tienen firma, pero siguen sin tener los controladores G'Mic y Python.

 

Si tienes algún problema por favor consulta el [formulario para el reporte de errores de código](https://phabricator.kde.org/T7492) (en ingles) antes de reportar en Bugzilla, desde el lanzamiento de la versión 4.0.0 se han reportado mas de 150 "bugs" (errores de código), pero la mayoría eran reportes duplicados o simplemente preguntas y quejas las cuales deben ser dirigidas a el foro oficial o en el IRC. Estos pseudo-reportes toman bastante tiempo para ser revisados y hace que la corrección de verdaderos errores se tome mucho mas tiempo. Ademas solo reportes in ingles serán validados. ¡Gracias por comprendernos y ayudarnos!

[![](images/kiki_4.0_sm-1-1024x463.png)](https://krita.org/wp-content/uploads/2018/03/kiki_4.0_sm-1.png)

## Mejoras

### Windows

- Un QSaveFile corregido lo cual hace posible el trabajar en imágenes en servidores sincronizados (dropbox, google drive). [BUG:392408](https://bugs.kde.org/show_bug.cgi?id=392408)
- Se activa o se hace disponible el WinInk si el WinTab no se puede cargar.

### Animación

- Corrección al actualizar el lienzo cuando una animación se esta reproduciendo en el "cache". [BUG:392969](https://bugs.kde.org/show_bug.cgi?id=392069)
- Corrección al correr la animación en modo aislado. [BUG:392559](https://bugs.kde.org/show_bug.cgi?id=392559)
- Corrección al animar mascaras tipo filtro, de ajuste y transparencia. [BUG:393302](https://bugs.kde.org/show_bug.cgi?id=393302)
- Se ha cambiado el tamaño de algunos iconos los cuales se presentaban muy pequeños en Windows.
- Corrección en el copiado de la información de pixeles en capas de animación. [BUG:364162](https://bugs.kde.org/show_bug.cgi?id=364162)

### Pinceles

- Corrección en el cambio de modos "borrador/opacidad" al modificar un pincel. [BUG:393499](https://bugs.kde.org/show_bug.cgi?id=393499)
- Corrección en el dialogo editor de pinceles cuando se crea un pincel nuevo. [BUG:392869](https://bugs.kde.org/show_bug.cgi?id=392869)
- Ahora se muestra una escala de 0 a 100 por ciento en los controles de fuerza y opacidad del editor de pinceles.

### Compatibilidad con formato de documentos

- Corrección al guardar documentos con mascaras en formato KRA.
- Ahora se puede abrir correctamente documentos EXR con capas múltiples, por Nuke [BUG:393771](https://bugs.kde.org/show_bug.cgi?id=393771)
- PSD: ahora se transforma la imagen si el espacio de color no es compatible.
- Ahora se evita el parar ciertas acciones durante el auto guardado.

### Cuadriculado

- Se ha incrementado el rango para activar el cuadriculado al nivel de pixel.
- Ahora solo se permite el uso de cuadriculado isométrico si OpenGL esta activo [BUG:392526](https://bugs.kde.org/show_bug.cgi?id=392526)

### Cierre inesperado de Krita

- Corrección de una suspensión creada al cerrar una imagen [BUG:393916](https://bugs.kde.org/show_bug.cgi?id=393916)
- Corrección de un cerrado al duplicar una mascara de selección global. [BUG:382315](https://bugs.kde.org/show_bug.cgi?id=382315)
- Corrección de un cerrado al remover y recrear trayectorias de vecotores. [BUG:393209](https://bugs.kde.org/show_bug.cgi?id=393209), [BUG:393087](https://bugs.kde.org/show_bug.cgi?id=393087)
- Corrección de un cerrado al remover paletas de color. [BUG:393353](https://bugs.kde.org/show_bug.cgi?id=393353)
- Corrección de un cerrado cuando se cambia el tamaño del panel de opciones de herramientas mientras se usa la herramienta de selección de objetos. [BUG:393217](https://bugs.kde.org/show_bug.cgi?id=393217)

### Interfaz

- Ahora se muestran de manera exacta los limites de las capas en el dialogo de las propiedades de las mismas.
- Se ha añadido la habilidad de mostrar y configurar lineas radiales en los controles de la herramienta de asistencia de puntos de horizonte.
- Ahora se actualiza correctamente el control de saturado al elegir in color con un valor de 100. [BUG:391934](https://bugs.kde.org/show_bug.cgi?id=391934)
- Corrección al cortar segmentos en trayectorias cerradas.
- Se ha desestabilizado el clic a la derecha en la paleta emergente. [BUG:391696](https://bugs.kde.org/show_bug.cgi?id=391696), [BUG:378484](https://bugs.kde.org/show_bug.cgi?id=378484)
- Ahora no se permite que el "widget" de etiquetas corrompa las etiquetas mismas cuando se usa el clic a la derecha. [BUG:392815](https://bugs.kde.org/show_bug.cgi?id=392815)
- Corrección de la posición de el lienzo después que se ha reacomodado el control de rotación de lienzo. [BUG:391921](https://bugs.kde.org/show_bug.cgi?id=391921) ("parche" de codigo por Emmet O'Neil, ¡Gracias!)
- Se ha cambiado el comportamiento del botón de adición de capas. [BUG:385050](https://bugs.kde.org/show_bug.cgi?id=385050) ()
- Ahora al hacer un clic afuera del marco de la vista previa, mueve dicha vista a ese punto. [BUG:384687](https://bugs.kde.org/show_bug.cgi?id=384687) ("parche" por Seoras Macdonald, ¡Gracias!)
- Se ha implementado la acción de cancelar una transformación continua en dicha herramienta al presionar el boton de Esc dos veces. [BUG:361852](https://bugs.kde.org/show_bug.cgi?id=361852)
- Ahora se muestra el control de flujo y opacidad en porcentaje en vez de cero a uno en la barra de herramientas.

### Otros

- Corrección de la construcción del programa en ARM [BUG:393010](https://bugs.kde.org/show_bug.cgi?id=393010)
- Se han corregido un numero de alertas generadas por [PVS-Studio](https://www.viva64.com/en/pvs-studio/)

## Descargas

### Windows

En Windows, si se encuentran el cerrado del programa inesperadamente, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por qué suceden.

- 64 bits Windows: [krita-x64-4.0.2-setup.exe](https://download.kde.org/stable/krita/4.0.2/krita-x64-4.0.2-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.0.2.zip](https://download.kde.org/stable/krita/4.0.2/krita-x64-4.0.2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.2/krita-x64-4.0.2-dbg.zip)

- 32 bits Windows: [krita-4.0.2-x86-setup.exe](https://download.kde.org/stable/krita/4.0.2/krita-x86-4.0.2-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.0.2.zip](https://download.kde.org/stable/krita/4.0.2/krita-x86-4.0.2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.2/krita-x86-4.0.2-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.0.2-x86\_64.appimage](https://download.kde.org/stable/krita/4.0.2/krita-4.0.2-x86_64.appimage)

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.)

Cuando se actualice, se podrá usar el repositorio de [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) para instalar Krita 4.0.2 en Ubuntu y sus derivados. Se está elaborando también un Snap

### OSX

- OSX disk image: [krita-4.0.2.dmg](https://download.kde.org/stable/krita/4.0.2/krita-4.0.2.dmg)

Nota: El controlador de gmic-qt y de PDF no está disponible en OSX.

### Código fuente

- Código fuente: [krita-4.0.2.tar.gz](https://download.kde.org/stable/krita/4.0.2/krita-4.0.2.tar.gz)

### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](https://krita.org/en/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22https://krita.org/en/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
