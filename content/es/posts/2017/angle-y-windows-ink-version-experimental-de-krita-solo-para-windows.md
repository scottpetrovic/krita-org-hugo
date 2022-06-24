---
title: "Angle y Windows Ink – versión experimental de Krita solo para Windows"
date: "2017-08-26"
categories: 
  - "uncategorized-es"
---

Hemos creado una versión especial de Krita 4.0 pre-alfa para que los usuarios de Windows la pongan a prueba. Ésta contiene dos nuevas funciones la cuales deberán resolver los problemas que mas afectan la versión de Windows:

- El uso de ANGLE: Ésto es puramente técnico, pero de manera general se puede decir que ANGLE es una tecnología que presenta un API de OpenGl pero que deja que Direct3D haga el trabajo. En Windows, muchos de los controladores con OpenGl han salido problemáticos, lo cual puede causar el cierre inesperado del programa, pantallas blancas o negras, la cual es problema mas "[odiado](https://bugs.kde.org/show_bug.cgi?id=360601)" que se nos ha presentado, ¡Y ni siquiera es nuestro código! Si al usar Krita en Windows has tenido que desactivar el OpenGl en las configuración del programa, ésta nueva función puede ser tu solución.
- El uso de Windows Ink/Windows8 Pointer Events. Lo cual es la tecnología local de Windows en los productos de la linea Surface de Microsoft, que se encuentra ademas en productos de Asus, Dell y HP, en los convertibles que usan plumas digitales.

**Nota**: ésta versión es puramente de prueba directamente de la rama de desarrollo principal, tiene, ademas de las mencionadas, otras nuevas funciones, muy atractivas pero **altamente inestables**, tal como programación con Python, nuevo sistema de guardado, gráficos SVG, etc. Si abres un documento hecho con Krita 3.x que contenga vectores en ésta versión, **NO** podrás abrir el mismo archivo nuevamente en Krita 3.x, recuerda, es experimental. **¡No se debe usar en trabajos importantes! Pero ayúdanos a ponerla a prueba.**

**La encuesta y otras partes de las instrucciones están disponibles solo en ingles.**

 

### Instrucciones para poner Angle a prueba:

- Abre la página de la encuesta en tu navegador: [https://goo.gl/forms/vYxPMbqGyVhPCc2q2](https://goo.gl/forms/vYxPMbqGyVhPCc2q2)
- Descarga el programa y los símbolos de depuración:
    - [https://files.kde.org/krita/4/windows/krita\_4.0-prealpha\_angle\_ink-1-x64.zip](https://files.kde.org/krita/4/windows/krita_4.0-prealpha_angle_ink-1-x64.zip)
    - [https://files.kde.org/krita/4/windows/krita\_4.0-prealpha\_angle\_ink-1-x64-dbg.zip](https://files.kde.org/krita/4/windows/krita_4.0-prealpha_angle_ink-1-x64-dbg.zip)
- Abre el primer archivo zip en Windows Explorer, y arrastra la carpeta de krita\_4.0-prealpha\_angle\_ink-1-x64 a tu pantalla de escritorio.
- Abre el segundo archivo zip en Windows Explorer y arrastra los archivos bin, lib y las carpetas compartidas adentro de la carpeta krita\_4.0-prealpha\_angle\_ink-1-x64 que ya habías movido a tu escritorio.
- Con Windows Explorer, entra a la carpeta de krita\_4.0-prealpha\_angle\_ink-1-x64 mencionada.
- Abre Krita dándole un doble clic en el enlace de Krita o directamente al archivo bin\\krita.exe.
- Se te presentará la siguiente opción:[![](/images/posts/2017/angle_question.png)](/images/posts/2017/angle_question.png)
- Te pedimos que uses primeramente la prueba de Test Desktop OpenGL. Produce una nueva imagen y trata de dibujar por un tiempo, completa la encuesta con los resultados, ya sea que el programa se haya cerrado inesperadamente o si funciona adecuadamente.
- Ahora puedes reiniciar Krita y elegir Test ANGLE. Produce una nueva imagen y trata de dibujar una ves mas por un tiempo. De igual manera te pedimos que completes la encuesta con los resultados.

**NOTA: En esta versión, no podrás desactivar el OpenGL/Angle, éstas funciones están activadas permanentemente por defecto dada la naturaleza de la prueba.**

### Instrucciones para probar Ink/Windows Pointer API

Ésta prueba solo es importante para los usuarios de Windows 8 y 10, ya que Windows 7 no posee ésta función (y Krita no está creada para funcionar con Windows 95, 98, XP ó Vista). Además del requerimiento del sistema, se supone que estarás usando una Surface Pro con la pluma digital y otra computadora convertible que use la tecnología n-trig de Mricrosoft.

- Abre la encuesta en tu navegador: [https://goo.gl/forms/N5Exyx8aKSOeAUmu2](https://goo.gl/forms/5TSCWNZvvjN5SVoq1)
- Si no lo has hecho aun con las instrucciones previas, descarga los siguientes paquetes.
    - [https://files.kde.org/krita/4/windows/krita\_4.0-prealpha\_angle\_ink-1-x64.zip](https://files.kde.org/krita/4/windows/krita_4.0-prealpha_angle_ink-1-x64.zip)
    - [https://files.kde.org/krita/4/windows/krita\_4.0-prealpha\_angle\_ink-1-x64-dbg.zip](https://files.kde.org/krita/4/windows/krita_4.0-prealpha_angle_ink-1-x64-dbg.zip)
- Abre el primer archivo zip en Windows Explorer, y arrastra la carpeta de krita\_4.0-prealpha\_angle\_ink-1-x64 a tu pantalla de escritorio.
- Abre el segundo archivo zip en Windows Explorer y arrastra los archivos bin, lib y las carpetas compartidas adentro de la carpeta krita\_4.0-prealpha\_angle\_ink-1-x64 que ya habías movido a tu escritorio.
- Con Windows Explorer, entra a la carpeta de krita\_4.0-prealpha\_angle\_ink-1-x64 mencionada.
- Abre Krita dándole un doble clic en el enlace de Krita o directamente al archivo bin\\krita.exe.
- Elige cualquiera de las dos opciones: Test Desktop OpenGL ó Test ANGLE, en éste caso no hay diferencia.
- Abre los diálogos de Preferencias>Configurar Krita>Tableta (Settings/Configure Krita/Tablet) y activa la opción experimental señalada en la imagen del _pointer api/windows ink_:[![](/images/posts/2017/tablet_support.png)](/images/posts/2017/tablet_support.png)
- Reinicia Krita.
- Produce un nuevo documento, dibuja con la herramienta principal de pincel, revisa si la variación de presión en la pluma digital cambia el tamaño y la opacidad de el trazo, por favor responde tus resultados en la siguiente encuesta (en inglés): [https://goo.gl/forms/5TSCWNZvvjN5SVoq1](https://goo.gl/forms/5TSCWNZvvjN5SVoq1)

### ¡De antemano Gracias!
