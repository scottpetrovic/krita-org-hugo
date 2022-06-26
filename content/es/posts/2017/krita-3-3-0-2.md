---
title: "Krita 3.3.0"
date: "2017-09-28"
categories: 
  - "uncategorized-es"
---

Justo a una semana de la versión de prueba, anunciamos el lanzamiento final de Krita 3.3.0, como ya se ha mencionado, ésta versión posee cambios importantes para los usuarios de Windows, por lo que se recomienda que se actualicen.

Alvin Wong ha implementado la compatibilidad con los eventos del API de Windows 8, lo que significa que Krita ahora puede usar el stylus n-trig en la linea de laptops Surface (así como otras similares tales como Dell, HP y Acer). Dado que está función es muy nueva, tiene que ser activada en la ventana de opciones::

[![](/images/posts/2017/wintab-1024x840.png)](/images/posts/2017/wintab.png)

Además Alvin W. también reconstruyó la funcionalidad de Krita que depende de la aceleración por hardware, lo que permite de manera opcional usar Angle en Windows en vez de OpenGL. Ésto significa que que los problemas con las tarjetas de gráficos Intel y sus controladores se podrán hacer de lado ya que Krita usará indirectamente Direct3D.

[![](/images/posts/2017/display-1024x840.png)](/images/posts/2017/display.png)

Por supuesto ésto no es la única novedad, además tenemos:

- Algunos problemas visuales cuando se usa pantallas de alta resolucion "hi-dpi" se han corregido (nota: En Windows y LInux, se requiere que ésta función se active en la ventana de opciones).
- Si se crea una nueva imagen directamente de la memoria del copiador "clipboard", la imagen mantendrá su nombre como título.
- Los modos de mezclado y los pinceles favoritos ahora se cargan correctamente al abrir el programa.
- GMIC
    - El controlador se ha actualizado a la última versión disponible tanto en Windows como en Linux.
    - La configuración para seleccionar la localización del controlador se ha eliminado. Krita lo busca primeramente donde se encuentra su archivo ejecutable, de ahí lo buscará dentro de una carpeta con el nombre de "gmic" en el mismo lugar.
    - Se han corregido varias fallas con la comunicación entre GMIC y Krita
- Algunos sitios en el Internet descargan imágenes con la extensión incorrecta, lo cual confundía Krita, ahora el programa busca dentro del archivo para verificar que tipo de imagen es y así la puede abrir correctamente.
- PNG
    - Las imágenes con los espacios de color 16 y 32 bit flotante ahora son convertidas al espacio 16 bit completo cuando la imagen se guarda/exporta como una PNG.
    - Ahora es posible el guardar el canal alfa en una imagen PNG aun cuando no existan pixeles semi ó transparentes en la imagen
- Cuando se desactivaba la aceleración gráfica del hardware, la imagen del cursor cuando se activa la herramienta de selección de color se mostraba incorrectamente, lo cual se ha corregido.
- El panel de imágenes de referencia ahora solo muestra las imágenes cuando el panel esta visible, y no automáticamente al comenzar Krita. Nota: éste panel usa el controlador de Qt _imageio_, Si usas Linux, cercíorate de remover todos los componentes del escritorio Deepin, ya que éste utiliza una versión del controlador con problemas, el cual produce el cierre inesperado de cualquier programa que requiere el usarlo para mostrar imanes.
- Nuevas funciones para la linea de comandos:
    - \--nosplash para comenzar Krita sin la imagen de presentacion.
    - \--canvasonly para comenzar Krita en el modo de lienzo.
    - \--fullscreen para comenzar Krita en el modo de pantalla completa.
    - \--workspace Nombredelworkspace para comenzar Krita en determinada configuración de trabajo.
- Selecciones
    - La acción de _seleccionar todo_ ahora remueve previas selecciones antes de ejecutarse.
    - Ahora es posible el extender las selecciones mas allá del lienzo.
- Se ha mejorado el funcionamiento en general, se han eliminado las revisiones innecesarias de algunas opciones, lo que hace que el generar la imagen de muestra de una capa sea mas rápido, o se puede pintar mucho mejor aun si la aceleración gráfica del hardware ha sido desactivada.
- Los espacios inteligentes de entradas de cifras _input boxes_, ahora usan la configuración del teclado del sistema, lo que facilita el su uso.
- La ventana con el dialogo para reportar los errores de código se ha mejorado.
- MacOS/OSX específicamente
    - Bernhard Liebl ha mejorado la precisión de las tabletas/stylus. Se ha avanzado con el problema en el que los círculos poseen lineas rectas, aun que todavía no se ha eliminado completamente.
    - Para los que tienen una tarjeta de video AMD en éstos sistemas, se ha desactivado completamente la aceleración gráfica del hardware ya que ésto congela Krita al tratar de guardar/exportar imágenes en los formatos PNG y JPG.

### Descargas

#### Windows

En Windows, si se encuentran con cierres del programa inesperados, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por que suceden.

- 64 bits Windows: [krita-3.3.0-x64-setup.exe](https://download.kde.org/stable/krita/3.3.0/krita-3.3.0-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.3.0-x64.zip](https://download.kde.org/stable/krita/3.3.0/krita-3.3.0-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.0/krita-3.3.0-x64-dbg.zip)

- 32 bits Windows: [krita-3.3.0-x86-setup.exe](https://download.kde.org/stable/krita/3.3.0/krita-3.3.0-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.3.0-x86.zip](https://download.kde.org/stable/krita/3.3.0/krita-3.3.0-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.0/krita-3.3.0-x86-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- 64 bits Linux: [krita-3.3.0-x86_64.appimage](https://download.kde.org/stable/krita/3.3.0/krita-3.3.0-x86_64.appimage)

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.)

En Ubuntu puedes instalar el “snap” de ésta versión. Ademas puedes usar el repositorio [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) en Ubuntu y sus derivados.

#### OSX

- OSX disk image: [krita-3.3.0.dmg](https://download.kde.org/stable/krita/3.3.0/krita-3.3.0.dmg)

Nota: El controlador de gmic-qt y de PDF no está disponible en OSX.

### Código fuente

- Código fuente: [krita-3.3.0.tar.gz](https://download.kde.org/stable/krita/3.3.0/krita-3.3.0.tar.gz)

#### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

#### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

#### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](https://krita.org/en/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22https://krita.org/en/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
