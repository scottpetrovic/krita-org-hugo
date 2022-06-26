---
title: "Krita 3.0.1, la versión alfa."
date: "2016-08-16"
categories: 
  - "news-es"
---

La semana pasada se comenzó la etapa de estabilidad de Krita. Varios aportes de los desarrolladores conjugaron sus proyectos con nuevas e interesantes funciones, incluyendo una nueva visualización "head-up" para ajustar las brochas, un filtro "wavelet", otro de "threshold", se agregó el funcionamiento para realizar ecuaciones matemáticas en los espacios para escribir valores, solo falto hacer posible el guardar videos de las animaciones hechas en Krita, todavía se encuentra bajo construcción.

Por cuestiones de mal funcionamiento electrónico, no se logró crear nuevas versiones de desarrollo la semana anterior, ademas que solo hay una persona que hace todas las versiones para los diferentes sistemas, Krita necesita mas voluntarios que ayuden a ejercer esta tarea. Afortunadamente con los nuevos discos duros, las versiones mas nuevas ya están disponibles, estas se encuentran una semana atrasadas, por lo ya se a avanzado con algunos de los errores de codigo presentes en estos paquetes. Sin embargo si encuentras problemas por favor repórtalos, cerciórate primero si alguien mas ya lo ha hecho, puedes agregar a la información o si no hay casos similares, puedes crear el reporte tu mismo en bugs.kde.org.

La semana entrante se espera el lanzar la primera versión beta de lo que sera la versión final planeada para el cinco de septiembre.

#### Windows

En windows Krita puede usar las tabletas digitales Wacom, Huion y Yiynova, también las Surface Pro. Se ha probado en Windows7, 8 y 10, solo existen lanzamientos en el formato de 64 bits. Ademas existe la versión que ayuda a rastrear los problemas cuando ocurren, ésta funciona con el programa llamado DrMingw, para mas información [visita ésta página](https://docs.krita.org/KritaFAQ/es#.C2.BFComo_puedo_crear_un_.22backtrace.22_en_Windows.3F). En esta ocasión, Krita puede responder mas lentamente dado a que se ha desactivado la vectorización.

- [krita-3.0.1-alpha2-x64.zip](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0.1-alpha2-x64.zip) (a0ee7187035d890445c468a381d3fc2c)
- [krita3-x64-dbg-latest.zip](http://files.kde.org/krita/3/windows/debugbuilds/krita3-x64-dbg-latest.zip) (a0c100335a7d55cfc2710fe1cb2b39a2)

#### Linux

Al igual que en las ultimas versiones, y para que mas personas puedan probar el programa en desarrollo sin la necesidad de compilarlo o de repositorios no oficiales, se a puesto a disposición la versión mas nueva en un AppImage, solo en el formato de 64 bits. Una ves descargado el paquete, lo haces ejecutable y lo usas directamente en el mismo archivo, recuerda que aun que funciona muy bien, tanto Krita como AppImage son experimentales.

- [krita-3.0.1-Alpha2-d33dbe0-x86_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0.1-Alpha2-d33dbe0-x86_64.appimage) (f61f8991a517a7835ceebf7159288d8e)

#### OSX and MacOS

Krita será totalmente funcional para este sistema en la versión 3.1, por lo pronto en Krita 3.0 todavía faltan algunas funciones tales como la vista previa inmediata y la vista de alta calidad de el lienzo, ademas de problemas tales como el de reproducir imágenes. Esto es dado a que Apple a decidido dejar afuera la compatibilidad con OpenGL 3.0 en algunos dispositivos, por lo pronto se recomienda el desactivar OpenGL en Krita. Esta versión de Krita funciona con OSX 10.9, 10.10 y 10.11, se ha reportado ademas que puede funcionar en MacOS.

- [krita-3.0.1-Alpha2.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-Alpha2.dmg) (26a2ee299e63aed6a0a77b6c5a78ab0b)

#### Source

El paquete con el código para compilar ahora contiene también las traducciones de Krita.

- [krita-3.0.99.89.tar.xz](http://files.kde.org/krita/3/source/krita-3.0.99.89.tar.xz) (af9424c06ce6b1504859a5abd703955a)
