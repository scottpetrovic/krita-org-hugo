---
title: "Invitado de la reunion de Krita 2018"
date: "2018-06-02"
categories: 
  - "uncategorized-es"
---

En la pasada reunion, tubimos un invitado especial: Valeriy Malov, quien desarrolla el modulo de configuracion de Wacom en Plasma. Le pedimos que nos escribiera su experiencia durante la reunion, ésto es lo que nos dice:

Hola,

Éste es mi reporte general acerca de la reunion Krita 2018 / y un avance de la nueva version del modulo [wacomtablet](https://userbase.kde.org/Wacomtablet).

### Reunion de Krita 2018

Dos semanas atrás, atendí la reunión de Krita, fue un evento tanto divertido como productivo. Boudewijn, Timothee and Raghukamath pusieron a prueba la versión "git" del modulo Wacomtablet en sus computadoras. También yo puse a prueba varias tabletas Wacom con KCM, obtuvimos la información de su uso y se implementaron algunas correcciones:

- Calibrar dispositivos como Cintiq se ha mejorado bastante. Anteriormente el KCM no tomaba en cuenta el sensor de coordenadas del sistema, el cual no comienza con oxo, ya que los sensores son generalmente mas grandes que los que poseen las pantallas.
- Se ha añadido compatibilidad con dispositivos que reportan un USB ID separado para los sensores táctiles. Ne es perfecto (todavía), ya que aun requiere intervención manual. Si tienes una tableta que se muestra doble en KCM, por favor activa el buscador Wacom Tablet Finder y marca la tableta/lapicera de manera correspondiente.
- Algunas otras mejoras en el calibrado y coordenadas: desactivar el botón de proporciones, la ventana de calibrado ahora se abre en la pantalla la que se está sincronizada, ademas ahora existe una opción para calibrar manualmente los valores sin la necesidad de usar los documentos de configuración. (esto fue propuesto durante la reunión, sin embargo ha sido añadido después de la misma).
- Un par de correcciones del código: el modo táctil ahora se coordina con la rotación de la tableta, las teclas de acceso rápido ya no se repetirán.
- La idea general fue que el la interfaz del KCM posee algunos problemas visuales o de uso. Le estaré preguntando al equipo de Krita para que me ayuden con ello, pero esto sera pospondrá hasta la versión del modulo 3.1.0. También existe la cuestión sobre cual es la mejor configuración por defecto.
- Puse a prueba la compatibilidad con LED. Funciona siempre y cuando el sistema ha sido configurado para dejar que el usuario tenga acceso al Wacom LED API (probablemente mediante las reglas de udev). No hay compatibilidad con OLED todavía, pero usa el mismo API. Basicamente, es algo que se puede trabajar, debe ser algo facil el hacerlo, desafortunadamente no es una prioridad ya que muchos dispositivos no poseen LEDs/OLEDs.

Quiero agradecer a Boudewijn and Irina por la hospitalidad, a la Fundación Krita y KDE e.V por patrocinar el evento. Sin éste apoyo, pasaria mucho tiempo antes de poder resolver todos estos problemas.

### La nueva version y su prueba

También hay un cambio mayor desde la version 3.0.0: compatibilidad con libwacom. Ésto debe incrementar la cantidad de dispositivos que se pueden usar. Sinembargo, solo es parcial por lo pronto (no LED, no USB ID múltiples, los esquemas de los botones que proporciona libwacom no encajan correctamente en la interfaz actual). Ademas se requiere libwacom 0.29 para dispositivos con botones peculiares (todavía se puede construir el modulo con versiones anteriores, pero resulta con menor funcionalidad). Así que no debes descartar el buscador "Wacom Tablet Finder" todavía.

Otro cambio pequeño es que el "reporte" se a cambiado a QLoggingCategory, lo que significa que para activar reporte de errores se necesita iniciar **kdebugsettings** y buscar "wacom".

Con todos estos cambios, pronto construiré la rama de la versión 3.1.0, lo que significa que el lanzamiento puede ocurrir éste mes. Las correcciones mas importantes desde la versión 3.0.0 son muy difíciles de retroalimentar por lo que muy posiblemente no habrá la versión 3.0.1, mis disculpas por ello. Tampoco habrá la versión beta (Neon Dev Unstable, Arch y Gentoo ya proveen de paquetes git para probar el modulo).

Problemas conocidos:

- No hay compatibilidad con Wayland. Esto es, ni siquiera un poco, no ETA. Estoy listo para cooperar con quienquiera implementar la compatibilidad con tabletas en Kwin-Wayland, pero no puedo trabajar en ello de tiempo completo.
- El rastreo de rotación automática es casi seguro que no funcionara en casos de pantallas múltiples. Éste es un error de Qt.
- La pantalla para calibrar puede accidentalmente cambiar a "arrastrar" cuando se toca/usa la lapicera. Esto es frustrante pero no debe alterar los resultados del calibrado. Esto es una función de KDE (que puedes desactivar en las configuraciones de los estylos de widget), lo que no se como evitar por lo pronto.

Ademas existen algunos problemas que aun están por atender, pero después de la versión 3.1.0 los iré revisando y cerrando conforme se consideren resueltos, a no ser que alguien mas los pueda reproducir.

- [**Bug 334520**](https://bugs.kde.org/show_bug.cgi?id=334520) - El calibrado falla en una PC tipo tableta si una pantalla externa está conectada aun cuando las coordenadas apuntan a la interna. (funciona en git/3.1.0)
- [**Bug 336748**](https://bugs.kde.org/show_bug.cgi?id=336748) - El calibrado no funciona adecuadamente en Cintiq13 (funciona en git/3.1.0).
- [**Bug 322918**](https://bugs.kde.org/show_bug.cgi?id=322918) - Problemas con calibrado en Cintiq 13HD (funciona en git/3.1.0).
- [**Bug 327952**](https://bugs.kde.org/show_bug.cgi?id=327952) - El modulo Wacom no calibra el modelo Cintiq 21ux (funciona en git/3.1.0).
- [**Bug 364043**](https://bugs.kde.org/show_bug.cgi?id=364043) - El Intuos Pro no puede generar perfiles, tampoco configurar botones.
- [**Bug 343666**](https://bugs.kde.org/show_bug.cgi?id=343666) - El dispositivo 'Wacom Bamboo One M Pen' no está en la lista, no se puede configurar con la tableta(funciona en git/3.1.0).
- [**Bug 339138**](https://bugs.kde.org/show_bug.cgi?id=339138) - Las coordenadas de la ta tableta se pierden al reiniciar KDE.
- [**Bug 325520**](https://bugs.kde.org/show_bug.cgi?id=325520) - En Dell latitude xt2: la función táctil está invertida cuando se rota al marco (funciona en git/3.1.0).

Lista completa de los errores o funciones deseadas [aquí](https://bugs.kde.org/buglist.cgi?component=general&list_id=1520931&product=wacomtablet&resolution=---).

No dudes en reportar si encuentras algun problema. Si no hay problemas despues de la versión 3.1.0, la prioridad del proyecto será el mejorar su uso.

### Empaquetado del modulo

Esto es algo muy importante pero a lo que no puede hacerle mucho directamente. Actualmente, la compatibilidad de Wacom en KDE es un componente opcional, así que si la seccion de **Tabletas** no aparece en los **Dispositivos de entrada**, se requiere que los instales manualmente. El paquete generalmente posee el nombre **wacomtablet ó kcm-wacomtablet**. Pedes verificar la existencia del paquete [aquí](https://repology.org/metapackage/kcm-wacomtablet/versions) y también [aquí](https://repology.org/metapackage/wacomtablet/versions). Asta donde yo se, solo KDE Neon, Arch (+ derivados) y Gentoo proveen un paquete actualizado. Kubunut tambien lo tiene, pero esta oculto entre el repositorio [experimental PPA](https://launchpad.net/~kubuntu-ppa/+archive/ubuntu/experimental/+packages). Si tu usas otras distribuciones las opciones son:

- Construir el modulo e instalarlo manualmente tal como se describe en el documento README.md, algo que no me gusta que los usuarios hagan por muchas razones.
- Pedirle a alguien (de preferencia quien sea que empaquete KDE en tu distribución) que lo compile. Ésto se hace generalmente mediante los "bugtracker" o en los foros.

Desafortunadamente dada la estructura del proyecto (lo cual solo es un conjunto de controladores), no creo que pueda crear un AppImage para que todos puedan usar el modulo. Así que la mejor alternativa es pedirle a los administradores de tu distribución que éste modulo existe y que tu lo necesitas.
