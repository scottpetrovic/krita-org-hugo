---
title: "Krita 3.3.2"
date: "2017-11-03"
categories: 
  - "uncategorized-es"
---

Hoy lanzamos la subversión de Krita 3.3.2, la cual se enfoca en la compostura de dos problemas de la versión 3.3:

- Krita 3.3.1 entiende incorrectamente las texturas de los pinceles, lo cual hemos corregido.
- Windows 1709 corrompió de muchas formas el Wintab y el Windows Ink que manipulan las tabletas digitales, hemos trabajado en este problema y finalmente encontramos una solución temporal.

Ademas de los mencionados, las siguientes correcciones y mejoras se han incorporado:

- En la animación:
    - Hacer posible el exportar fotogramas vacíos al final del metraje.
    - Hacer posible el generar videos con hasta 10,000 fotogramas.
- Se ha añadido la opción en la ventana de comando para iniciar Krita con una nueva imagen en blanco: krita --new-image RGBA,8,5000,3000
- Mejoras:
    - Un mejor caché para los efectos y selecciones de mascaras.
    - Corrección de una fuga de memoria en el pincel de manchado (smudge).
    - Un mejor desempeño al usar la aceleración por _hardware_ en el lienzo.
    - En Windows, el uso de iconos es mas rápida.
    - En MacOS, ahora se genera la imagen en el monitor con la rapidez adecuada.
- Filtros:
    - Ahora es posible el editar las características de los filtros directamente en el documento xml que se usa para definir los mismos en los documentos .kra del programa.
    - Se ha añadido un filtro nuevo ASC CDL, para el balance de color con diversas opciones.
- Se ha corregido el cierre inesperado del programa cuando se cierra un documente al tener activa la función de lienzo infinito.
- Se ha hecho posible el copear/pegar grupos de capas.
- Interfaz:
    - Ahora se puede navegar con la rueda del ratón sobre los patrones de textura cuando la ventana es bastante estrecha.
    - Se ha mejorado la información en el panel de capas, cuando éstas se cambian de posición.
    - Ahora se oculta el icono de candado y se colapsa el titulo de los paneles cuando estos se dejan de manera flotante.
- Se ha actualizado el controlador para los efectos de imagenes: G'Mic.

### Descargas

#### Windows

En Windows, si se encuentran con cierres del programa inesperados, favor de seguir [las siguientes instrucciones](https://docs.krita.org/Dr._Mingw_debugger) (en ingles) para encontrar los errores y así poder entender por que suceden.

- 64 bits Windows: [krita-3.3.2-x64-setup.exe](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.3.2.1-x64.zip](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1-x64-dbg.zip)

- 32 bits Windows: [krita-3.3.2-x86-setup.exe](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.3.2.1-x86.zip](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1-x86-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- 64 bits Linux: [krita-3.3.2-x86\_64.appimage](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2-x86_64.appimage)

(En ocasiones Firefox trata el enlace como texto, para descargar el paquete simplemente has un clic a la derecha en el mismo enlace.)

En Ubuntu puedes instalar el “snap” de ésta versión. Ademas puedes usar el repositorio [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) en Ubuntu y sus derivados.

#### OSX

- OSX disk image: [krita-3.3.2.dmg](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.dmg)

Nota: El controlador de gmic-qt y de PDF no está disponible en OSX.

### Código fuente

- Código fuente: [krita-3.3.2.1.tar.xz](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1.tar.gz)

#### md5sums

Para todas las descargas:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

#### Llave

El appimage y la fuente tarbal han sido firmadas, la llave pública se encuentra en el siguiente enlace: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8).

Las firmas están [aquí](http://download.kde.org/unstable/krita/3.1.3-beta.1).

#### También puedes apoyarnos

Krita es un programa no solo de código libre si no ademas está a disposición de manera gratuita, éste proyecto solo es posible gracias a las donaciones hechas por nuestros usuarios, por favor considera la posibilidad de ayudarnos con una [donación](https://krita.org/en/support-us/donations/) o comprando [videos instructivos o nuestro libro de arte Made With Krita](https://krita.org/es/item/krita-3-2-0/%22https://krita.org/en/support-us/shop), solo con tu ayuda podremos mantener a nuestro pequeño grupo desarrollando Krita en tiempo completo, ¡Gracias!
