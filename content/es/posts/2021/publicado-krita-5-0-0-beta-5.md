---
title: "Publicado Krita 5.0.0 beta 5"
date: "2021-12-07"
categories: 
  - "noticias"
---

Tras lanzar una beta para macOS dañada, estamos lanzando Krita 5.0.0 beta 5. Beta 4 no ocurrió pues, mientras se compilaba, Dmitry Kazakov reparó un problema que realmente queríamos fuera verificado tan pronto fuera posible.

![](/images/posts/2021/2021-11-16_kiki-piggy-bank_krita5.png) Krita es un programa libre y de código abierto. Por favor considere ayudar al desarrollo del proyecto con una [donación](https://fund.krita.org) o [comprando videos de entrenamiento](https://krita.org/en/shop/). Con tu ayuda podemos mantener al equipo de desarrollo de Krita trabajando a tiempo completo.

Esta versión contiene las siguientes mejoras desde la beta 3:

- El DMG de macOS funciona una vez más...
- Se corrigió un problema en el selector de recursos donde el recurso erróneo es seleccionado.
- Las paletas de color sólo se guardaban si fueron modificadas.
- Se corrigió el interlineado muy grande en las figuras de texto.
- Se corrigió el tamaño de las figuras de texto que difieren con respecto a Krita 4
- Se removió el atajo de teclado obsoleto para brillo y contraste
- Se crean paquetes MSIX para Krita en la fábrica de binarios.
- Se corrigió la animación errónea el el diálogo de guardado de valores predefinidos de pinceles
- Corregido el cargado de recursos desde paquetes si existen versiones más recientes que fueron borradas de la carpeta de recursos
- Corregido el modelo de color de capas agrupadas
- Corregidos varios problemas con las pruebas de pantalla (Soft Proofing)
- Se corrigieron los pinceles predefinidos que usan el modo de mapa de gradiente.

## Descargar

### Windows

Si está usando los archivos ZIP portables, abra el archivo ZIP en el Explorador y arrastre la carpeta a algún lugar conveniente, luego haga doble click en el ícono de Krita. Esto no impactará la versión instalada de Krita, aunque sí se compartirán sus preferencias y recursos personalizados con la versión instalada. Para reportar fallos, también descargue la carpeta de símbolos de depurado.

Recuerde que ya no estamos construyendo la versión de Windows de 32 bits.

- Instalador para Windows 64 bits: [krita-x64-5.0.0-beta5-setup.exe](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x64-5.0.0-beta5-setup.exe)
- Versión portable Windows 64 bits: [krita-x64-5.0.0-beta5.zip](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x64-5.0.0-beta5.zip)
- [Símbolos de depuración (Descomprima en la carpeta donde instaló la versión beta).](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x64-5.0.0-beta5-dbg.zip)

### Linux

- Linux 64 bits: [krita-5.0.0-beta5-x86\_64.appimage](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5-x86_64.appimage)

Nota: La AppImage de G'MIC-Qt ya no es necesaria.

(Si por alguna razón Firefox intenta cargar el archivo como texto: para descargar, haga click derecho sobre el vínculo).

### macOS

Nota: Si usa macOS Sierra o High Sierra, por favor [revise este video](https://www.youtube.com/watch?v=3py0kgq95Hk) para aprender cómo permitir que el sistema ejecute binarios firmados por desarrolladores, en lugar de sólo binarios firmados por Apple.

- Imagen de disco macOS: [krita-5.0.0-beta5.dmg](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5.dmg)

### Android

Los lanzamientos en Android se hacen desde el "tarball" de lanzamiento, por lo que tienen traducciones. Consideramos a Krita en ChromeOS y Android aún como **_beta_**. Algunas características no funcionan y otras son imposibles de realizar sin un teclado físico.

- [64 bits Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x86_64-5.0.0-beta5-release-signed.apk)
- [32 bits Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x86-5.0.0-beta5-release-signed.apk)
- [64 bits Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-arm64-v8a-5.0.0-beta5-release-signed.apk)
- [32 bits Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-armeabi-v7a-5.0.0-beta5-release-signed.apk)

### Código fuente

- [krita-5.0.0-beta5.tar.gz](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5.tar.gz)
- [krita-5.0.0-beta5.tar.xz](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5.tar.xz)

### md5sum

Para todas las descargas:

- [md5sum.txt](https://download.kde.org/unstable/krita/5.0.0-beta5/md5sum.txt)

### Key

La AppImage de Linux y el código fuente .tar.gz y .tar.xz están firmados. Puede obtener la llave pública [aquí](https://files.kde.org/krita/4DA79EDA231C852B). Las firmas se encuentran [aquí](https://download.kde.org/unstable/krita/5.0.0-beta5/) (nombres de archivo que terminan en .sig).
