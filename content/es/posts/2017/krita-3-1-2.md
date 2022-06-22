---
title: "Krita 3.1.2"
date: "2017-02-01"
categories: 
  - "uncategorized-es"
---

Esta es una versión intermedia con la corrección de errores de código "bugs" como objetivo principal, pero con algunas funciones extras como ya es acostumbrado en estos últimos lanzamientos.

### Las animaciones ahora pueden incluir audio.

<iframe src="https://www.youtube.com/embed/s08oHOjxo84" width="100%" height="450" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

Ahora se puede importar audio lo cual ayuda a sincronizar voces y música con la animación. En el video de demostracion, TImothée Giet nos muestra como se usa esta nueva función.

- Los formatos disponibles son WAV, MP3, OGG y FLAC
- Se ha agregado una nueva casilla en el dialogo de la reproducción de animaciones con la opción de incluir audio al exportar el documento.
- El manual de Krita ofrece una mejor explicación (en ingles) del como usar esta nueva función.

**Nota:** Las appimages de Krita aun no incluyen esta función de audio. está en estado experimental, y no se garantiza que funcione correctamente, por lo que esperamos que nos puedas ayudar reportando los problemas que pudieras encontrar.

### Cambios en general

- En la herramienta de selección de contorno, ahora se puede usar la tecla Ctrl (manteniendola presionada) para continuar dibujando la selección aun cuando se levanta la lapicera (o ratón) de la tableta digital, continuando dondequiera que se coloque nuevamente, anteriormente al levantar la lapicera digital terminaría la selección en esexportandolase punto.
- Se ha hecho posible el eliminar una selección al hacer un clik en el lienzo mientras cualquiera de las herramientas de selección de siluetas y entorno están activadas.
- Se ha incluido una opción para activar HiDPI en la ventana de configuraciones.
- Por lo pronto, dada la cantidad de problemas que ha presentado el exportar imágenes en PDF, ésta función se ha removido. ([BUG:372439](https://bugs.kde.org/show_bug.cgi?id=372439))

El siguiente enlace incluye la [lista de errrores de codigo](https://krita.org/es/krita-3-1-2/) que han sido corregidos.

### ¡Obten el libro de Krita y apoyanos al mismo tiempo!

Si quieres ver lo que otros usuarios han hecho con Krita, obtén el libro [**Made with Krita 2016**](https://krita.org/en/item/made-with-krita-2016-the-krita-artbook/) (Hecho con Krita), el primer libro de arte con nuestro software, ya lo puedes ordenar hoy mismo.

[![Made with Krita 2016](/images/posts/2017/cover_small-217x300.png)](https://krita.org/wp-content/uploads/2016/12/cover_small.png) Made with Krita 2016

### ¡Esperamos tus comentarios!

¡Casi 1000 personas ya han llenado la encuesta de Krita 2017! [Ayudanos a conocer mejor el como usas Krita y que tipo de computadoras y tabletas usas.](https://goo.gl/forms/cEeNopmGcMR4y3xD2) Tu información es confidencial. no es necesario el dar datos personales.

#### Windows

- 32 bits Windows: [krita-3.1.2.2-x86-setup.exe](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.2-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.1.2.2-x86.zip](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.2-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.2-x86-dbg.zip)

- 64 bits Windows: [krita-3.1.2.1-x64-setup.exe](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.1-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.1.2.1-x64.zip](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.1-x64-dbg.zip)

#### Linux

- 64 bits Linux: [krita-3.1.2-x86\_64.appimage](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2-x86_64.appimage)

Pronto estará disponible la version snap para Ubuntu. Ademas el existe el repositorio de [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) para Ubuntu y sus derivados.

#### OSX

- OSX disk image: [krita-3.1.2.0.dmg](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.0.dmg)

### Source code

- Código fuente: [krita-3.1.2.1.tar.gz](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.1.tar.gz)

#### md5sums

Para todas las descargas:

- [md5sums.txt](http://download.kde.org/stable/krita/3.1.2/md5sums.txt)

#### Key

Las appimage y el código fuente para Linux están firmados. La llave publica se encuentra en el siguiente enlace:  [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). Las firmas están [aquí.](http://download.kde.org/stable/krita/3.1.2).
