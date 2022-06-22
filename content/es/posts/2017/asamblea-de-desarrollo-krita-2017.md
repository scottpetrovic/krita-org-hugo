---
title: "Asamblea de desarrollo - Krita 2017"
date: "2017-11-27"
categories: 
  - "uncategorized-es"
---

Durante los primeros meses del 2017, una serie de problemas de impuestos y financieros nos dejaron sin la capacidad de planear una reunión entre los desarrolladores. Sin embargo con el plan de lanzar una versión nueva en unas cuantas semanas, nos es de suma importancia el poder colaborar y expresar el trabajo hecho y por realizar en persona, por lo que finalmente pudimos hacer una reunión, mucho mas pequeña que las anteriores, pero igualmente productiva, la cual tuvo lugar en Deventer, Holanda, del 23 al 26 de noviembre.

La ultima asamblea fue en agosto del año pasado [2016](https://krita.org/en/item/2016-krita-sprint-day-1/), lo que a dado lugar a la acumulación de una gran cantidad ideas, planes y proyectos, ademas que la cantidad de errores de código a los que se tiene que atender se ha incrementado de manera significante.

Enseguida se muestra un resumen de la asamblea Krita 2017.

En el rastreador de errores de código (bug tracker), se logro el eliminar alrededor de 120 reportes, es de entenderse que varios de estos reportes no corresponden a verdaderos problemas en el código, si no que son el resultado de algunos usuarios que han confundido el sistema para pedir ayuda del uso de Krita. También existen aquellos reportes que son duplicados de el mismo problema, por lo que se requiere que se enlacen. al final de la tarea se corrigieron mas de una docena de verdaderos errores de código, lo cual es bastante productivo:

[![](/images/posts/2017/bugs_november_sprint-874x1024.png)](https://krita.org/wp-content/uploads/2017/11/bugs_november_sprint.png)

### Krita 4.0

La lista de nuevas funciones y modificaciones para la versión 4.x se ha terminado, por lo que ademas se ha programado el tiempo y la fecha de desarrollo y lanzamiento, dado los problemas antes mencionados, el plan de finalizar esta versión durante este año ha sido imposible, por lo tanto se ha propuesto marzo del 2018.

entre las funciones que aun deseamos adoptar para ésta versión están:

- El pincel perezoso (Lazy brush) el cual facilita el colorear de manera mas rápida. (ya funciona, simplemente requiere de que se ponga a prueba)
- Pinceles apilados, la idea original ha sido descartada, se implementado una nueva versión, la cual funcionara de diferente forma.
- La nueva herramienta de texto, al igual que los pinceles apilados, se ha decidido el simplificar las ideas originales, Boudewijn aun esta trabajando en la orientación vertical del texto con Qt, pero no se espera el que este listo para el lanzamiento, por lo que se a decidido el hacer una herramienta simple pero que funcione correctamente para la mayoría de los usuarios.
- Algunas nuevas funciones como el controlador de Python y el nuevo editor de pinceles solo requieren de algunos ajustes por lo que se consideran casi listos.

Se han encontrando problemas al tratar de implementar ciertas funciones, tales como la falta de Python y GStreamer en las appimages para Linux, ademas que la forma en la que se añade G'Mic, no funciona correctamente; En OSX, G'Mic simplemente no funciona, ademas que no se pueden importar documentos PDF. Por el momento la solución a estos problemas esta mas allá de lo que el equipo de Krita puede hacer, por lo que se hace un llamado a conocedores en la materia, los cuales pueden ayudar corregir tal código.

El programa designado al lanzamiento sigue de la siguiente forma:

- El 31 de diciembre: Congelamiento, no se puede añadir nada extra, los componentes de Krita a este punto, son los que se lanzaran.
- El 3 de enero: Se lanza la primer versión de prueba beta.
- El 10 de enero: Se lanza la segunda versión de prueba beta, 4.0beta-1
- A partir del 10 de enero se proobeerá de versión de prueba diaria (siempre y cuando exista la facilidad de hacerlo)
- Tambien durante este tiempo mencionado, el equipo de dedicará casi exclusivamente a la correcion del codigo.
- El 7 de marzo: se lanza la primer prueba de los que sera la versión final de Krita 4.0
- El 14 de marzo: se lanza Krita 4.0

Dada la capacidad del equipo, es necesario el enfocarse en la versión 4.0, por lo que los errores reportados de la versión anterior tendrán menor prioridad.

#### Uso del HDR

Se han recibido varias veces, peticiones para que Krita se compatible con pantallas HDR, las cuales son diferentes a las de 10 bits por canal que son las que Krita puede funciona normalmente. La situación actual es que aun cuando los desarrolladores pueden que Krita detecte estos componentes, no hay mano de obra que se le pueda dedicar, ademas que el API parece ser algo que solo se usa en Windows.

#### "Get Hot New Stuff"

es el sistema en que los programas y el software de KDE comparten archivos, estos se pueden descargar directamente del programa tal como lo fuera Krita, desafortunadamente, cuando ya casi se tenía implementado, se cambio el método en el que funciona el servidor por lo que por lo pronto ésta función quedara en pausa hasta que se descubra que es lo que esta fallando, es muy posible que no será parte de la versión 4.0

#### Python API

Durante el verano pasado, se recopilo una gran cantidad de experiencia con el uso del controlador Python en Krita, uno de los estudiantes del "Google Summmer of Code" a colaborado de gran manera abriendo las posibilidades en las que puede ser implementado.

#### Summer of Code

Krita a participado en éste evento desde que se inició, y algunos de los desarrolladores de Krita comenzaron precisamente en este evento. Durante la asamblea se planeo como mejorar la participación del proyecto así como la forma de retener a los estudiantes aun cuando el evento se haya terminado. Uno de los problemas de éste evento es el limite impuesto en los estudiantes, los cuales solo pueden participar dos veces. sería mucho mejor y mas significante si se les permitiera participar durante todo el tiempo que cursan la universidad, lo cual ayuda que se mantengan activos con los proyectos como Krita.

Para que las futuras participaciones sean mas substanciales, se ha decidido cambiar el método de elección de estudiantes. Se han creado una serie de tareas con diferentes valores (del 1 al 3), y solo los candidatos que logren por lo menos 6 puntos tendrán la oportunidad de sus entradas sean puestas en revisión. Ademas se desea que los participantes puedan navegar la estructura del código por lo que se requiere que hagan un diagrama de cualquier subsistema.

#### Telemetría

Otra de las contribuciones del "Google Summer of Code" a sido el implementar una plataforma en la que se puede obtener información directamente del programa la cual muestra como es que se usa, se ha progresado en esta función pero no esta lista para ser implementada, su creador está haciendo su tesis en éste proyecto, lo cual lo mantiene en movimiento.

#### Guía de contribución

Actualmente, la información acerca de como contribuir al código de Krita se encuentra dispersa entre el sitio web, el manual y el wiki de KDE, Jouni ha creado una [serie de reglas](https://docs.google.com/document/d/1xIhmocYvbNf4FsW6k9LuerFi0ojDrTGiYR6UsXYVVFo/edit?ts=5a16ab20) la cual sera parte del manual. De hecho ya se ha comenzado con algunas partes: "[Como usar el rastreador de errores de código](https://phabricator.kde.org/T7492)"(en ingles).

Por lo pronto estos son los planes mas nuevos y vigentes del equipo de Krita. De antemano gracias a todos los usuarios por su apoyo, comprensión y esperamos sigan disfrutando de Krita.
