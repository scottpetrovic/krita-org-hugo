---
title: "Maratón de desarrollo - Reunión de Krita 2018"
date: "2018-05-22"
categories: 
  - "uncategorized-es"
---

El pasado fin de semana, Los desarrolladores de Krita así como artistas de diferentes partes del mundo se reunieron en el apacible pueblo de Deventer, con la finalidad de comprar queso..., corrección, con la finalidad de discutir todo lo relacionado con Krita así como el hacer un maratón de programación intensivo. Por cierto, [la mejor tienda de queso](http://www.kaashandel-debrink.nl/) de Holanda se encuentra en Deventer, así como la fundación de Krita. Comenzamos el pasado jueves (mayo 17) y hoy (mayo 22) se despiden los últimos en partir.

\[caption id="attachment\_6665" align="aligncenter" width="1024"\][![](../images/2018-05_Krita-sprint_Deventer-1024x345.jpg)](https://krita.org/wp-content/uploads/2018/05/2018-05_Krita-sprint_Deventer.jpg) Imagen de David Revoy\[/caption\]

Eventos como estos son muy importantes, ya que reúnen a las personas no solo para el desarrollo y un dialogo serio en cuanto a nuestro proyecto, sino ademas para convivir a un nivel mas personal, mediante comidas y caminadas, lo que facilita nuestra comunicación a través del Internet. Éste evento anual, no fue efectuado en el 2017 dadas las condiciones de la fundación, la ultima reunión fue en el [2016](https://krita.org/es/item/la-reunion-krita-2016-dia-primero/).

Por lo que, cual fue el resultado de nuestra reunión? Primero se realizo una [discusión](https://files.kde.org/krita/krita_meeting_docs/Other%20Meetings/2018%20Krita%20Sprint%20Meeting.odt) con los siguientes temas:

- **Recaudacion de fondos del 2018.** Actualmente se reciben alrededor de €2000 al mes en donaciones, ademas de tener ocho _subscriptores de desarrollo_, lo cual es fantástico, ya que se puede pagar el salario de Dmitry. Sin embargo nos es necesario el hacer un evento de recaudación de fondos anual, planeado para septiembre, éstos eventos siempre traen buena vibra y fuerza de la comunidad. Hemos decidido no hacerlo con Kickstarter, es algo repetitivo a este punto, éste año queremos hacer algo similar a un festival, y por supuesto no habrá nuevas funciones in Krita como premios, la razón es la siguiente.
- **El tema de éste año es:** _zarro bugs_. Éste termino era lo que bugzilla solía mostrar si al buscar un bug (error de código) el resultado era cero. Durante los últimos dos años hemos implementado una gran cantidad de funciones y cambios, tales como el traslado del código a Qt5 lo que produjo una gran cantidad del mismo. Pero no todo lo implementado está terminado, tenemos demasiados reportes de errores, y otros tantos mas de pruebas y de la [aplicación PVS](https://www.viva64.com/en/b/0569/). Por lo tanto, la meta de éste año es el corregir estos problemas.
- **This year's focus**: _zarro bugs._ That's what bugzilla used to tell you if your search didn't find a single bug. Over the past couple of years we've implemented a lot of features, ported Krita to Qt5 and in general produced astonishing amounts of code. But not everything is done, and we've got way too many open bug reports, way too many failing unittests, way too many  way too many features that aren't completely done yet -- so our goal for this year is to work on that.
- [**Trabajos por terminar:**](https://phabricator.kde.org/T8758) Hemos identificado los puntos mas importantes en los que necesitamos trabajar, se consultó con los artistas presentes sobre la situacion de Krita y se formuló lo siguiente:
    - Boudewijn trabajará en:
        - [Componer los recursos que usa Krita](https://phabricator.kde.org/T379)
        - Unificar los atajos de teclado y el control del lienzo, así como de sus errores en el código.
        - Mejorar la comunicación entre Krita y G'Mic.
    - Dmitry trabajará en:
        - Mascaras y selecciones.
        - Mejorar el motor y uso de texto, compatibilidad con OpenType, escritura vertical, e implementar mas funciones de SVG2.
        - Mejoras en SVG: compatibilidad con filtros y patrones, devanado y agrupación.
        - Mejoras en los estilos de capas.
    - Jouni trabajará en mejoras con la función de animacion:
        - Ciclos y clonado de fotogramas.
        - Mascaras de transformacion y curvas interpolares.
    - Wolthera trabajará en:
        - La coleccion de informacion sobre los aspectos faltantes de el API de Krita.
        - Filtros de la gradiente de colores.
- **Lanzamientos.** Planeamos lanzar la versión de Krita 4.1.0 en junio 20. Esperamos ademas el continuar lanzando una subversión de corrección de errores. Hemos hablado con los administradores de KDE sobre la posibilidad de poner a disposición estas versiones antes de su lanzamiento final, para que los usuarios las pongan a prueba. Krita 4.1 tendrá muchas mas funciones relacionadas con la animación, intercambio del _cache,_ implemento de recursos y la nueva herramienta de imágenes de referencia.

También dialogamos sobre la mejora de el manejo de los recursos que usa Krita. trabajamos arduamente en hacer que el uso del OpenGL en el lienzo funcione mejor, especialmente en MacOS, donde no funciona de manera fluida, añadimos ffmpeg en el instalador de Windows, se corrigieron problemas con las traducciones, se mejoro la función de auto guardado, se resolvieron algunos errores de código relacionados a la animación, se implemento un filtro de gradientes de color. Durante estos días y al mismo tiempo, los programadores que no estuvieron presentes, trabajaron a distancia en la mejora del uso del formato OpenEXR (lo que ahora usa procesos múltiples), se corrigieron algunos errores con el selector de muestra de color al mismo tiempo que se simplificó su código y mejoras en el panel de animación.

Y ésto no es todo, Wolthera, Timothee y Raghukamath terminaron de trasladar el manual a Sphinx, lo que hará posible el generar documentos para leerlo locamente (en PDF) así como el traducirlo. El manual consiste de mas de 1000 paginas.

En ésta ocasión tuvimos la parecencia de tres personas nuevas en esta reunión, el artista Raghukamath, el As del desarrollo en Windows Alwin Wong y el desarrollador de la aplicación de opciones de tabletas digitales de Plasma Valeriy Malov, quien mejoró la compatibilidad con dispositivos parecidos al cintiq.

Y por supuesto no podría faltar, durante las caminatas, ir a comer a nuestro lugar favorito [De Rode Kater](http://www.derodekater.nu/), comprar queso, y éste pasado domingo, hasta el sol salio relumbrante, y nosotros por lo pronto, ¡de regreso al código!

\[caption id="attachment\_6669" align="aligncenter" width="1024"\][![](../images/rode_kater-1024x529.jpg)](https://krita.org/wp-content/uploads/2018/05/rode_kater.jpg) Imagen de David Revoy.\[/caption\]

Éste evento fue patrocinado por KDE e.V. (viajes) y por la Fundación Krita (hospedaje y comida).
