---
title: "Krita en el 2018 y hacia el 2019"
date: "2018-12-24"
categories: 
  - "uncategorized-es"
---

Al final del [2017](https://krita.org/en/item/looking-back-looking-forward/) le dimos una mirada retrospectiva al año nuevo y pasado, es tiempo de darle un nuevo vistazo, después de todo el 2018 fue mucho mejor que el 2017 y logramos mas metas que el año previo.

**Lanzamos [Krita 4.0](https://krita.org/en/item/krita-4-0-0-released/)**, la cual incluyó programación con Python, la nueva herramienta de texto (aun que no la que habíamos planeado), el cambio de ODG a SVG y mucho más.

{{< youtube a-CY4hmkg_I >}}

Y justo después hemos mantenido la serie con nuevos lanzamientos [4.0.1](https://krita.org/en/item/krita-4-0-1-released/), [4.0.2](https://krita.org/en/item/krita-4-0-2-released/), [4.0.3](https://krita.org/en/item/krita-4-0-3-released/), [4.0.4](https://krita.org/en/item/krita-4-0-4-released/), [4.1.0](https://krita.org/en/item/krita-4-1-0-released/) (que trajo la [nueva herramienta de imágenes de referencia, manejo de sesiones y mucho mas.](https://krita.org/en/krita-4-1-release-notes/)) [4.1.1](https://krita.org/en/item/krita-4-1-1-released/), [4.1.3](https://krita.org/en/item/krita-4-1.3-released/), [4.1.5](https://krita.org/en/item/krita-4-1.5-released/) y [4.1.7](https://krita.org/en/item/krita-4-1.7-released/). Ésto es diez lanzamientos en un año, lo cual estuvo cerca de nuestra previa meta de un lanzamiento por mes, pero esto no fue suficiente para sentirnos realizados... Tuvimos en plan el lanzar la serie 4.2. con todo el trabajo creado por los estudiantes del evento Google Summer of Code. Desafortunadamente, una de las partes esenciales no se ha terminado lo cual produce inestabilidad al trabajar con imágenes de grandes proporciones. Por lo pronto todo este nuevo código se ha estado acumulando en la versión de prueba, de hecho, con tantas cosas nuevas, corremos el peligro de olvidar parte de lo que será incluido por lo que ya empezamos [a documentar las nuevas notas de lanzamiento](https://krita.org/en/krita-4-2-release-notes/).

Y hablando del evento de [**Google Summer of Code**](https://summerofcode.withgoogle.com/archive/), en el cual participamos como parte del grupo de [KDE](https://www.kde.org), tuvimos en el 2018 a tres estudiantes los cuales terminaron sus proyectos completamente, todo el código creado se ha integrado en la versión de prueba, y a pesar de que se requiere de ajustar varios detalles, fue un buen año de trabajo.

El el 2019 habrá otro evento, no estamos seguros si tendremos participantes, pero independientemente de lo que suceda, hemos creado algunas [ideas](https://community.kde.org/GSoC/2019/Ideas) en la cuales los estudiantes que deseen participar pueden tomar nota. Si eres uno de los interesados, ya es tiempo de que te pongas en contacto con el equipo de Krita. (Inglés es requerido)

[![](/images/posts/2018/2018-fundraiser-hero2.png)](/images/posts/2018/2018-fundraiser-hero2.png)

Ademas tuvimos nuestro evento de **recaudación** [de fondos](https://krita.org/en/fundraising-2018-campaign/), el cual fue todo un éxito. Esta vez no utilizamos Kickstarter, por lo que fue bastante difícil [el promoverlo](https://mail.kde.org/pipermail/kde-community/2018q4/004976.html). Por otro lado, sin tener que pagar por el servicio de Kickstarter, la ganancia neta que tuvimos igualó a la del evento del 2016, lo cual nos ha otorgado alrededor de 7 u 8 meses de trabajo completo.

[![](/images/posts/2018/busy.png)](/images/posts/2018/busy.png)Nuestra comunidad ha crecido, Krita se ha descargado cercas de **dos millones** de veces durante el año, y eso es solo contando nuestra pagina, mas las descargas de la tienda de Windows, la tienda de Steam, y los Flatpacks de la comunidad. Ademas, las descargas de Windows y de las distribuciones de Linux se han puesto mas al día con las ultimas versiones disponibles.

En el equipo de Krita, nos gusta el interactuar mas con los usuarios de nuestro programa, desafortunadamente, la gran cantidad de usuarios es demasiado grande para los pocos miembros que somos (alrededor de seis regulares) y nuestro tiempo lo deseamos poner en el código de Krita. Por lo que hemos decidido el crear un sitio con [preguntas y respuestas](https://ask.krita.org), y aun que todavía no sucede, esperamos que eventualmente se convierta en otra de las comunidades de los usuarios de Krita.

Así pues el 2018 fue bastante productivo, ¿Qué nos espera en el 2019?

Primeramente el mantener nuestros lanzamientos, estamos trabajando duro en la serie 4.2 y ésta ya se puede poner a prueba con todo lo nuevo, pero hay dos proyectos especiales en los que nos estamos enfocando.

Trabajando en par con Intel, estamos preparando la **habilidad de pintar en** [**HDR**](https://phabricator.kde.org/T9256). Lo cual nos pone en la delantera en en ésta área, esta tecnología es tan nueva que muy pocos productos lo tienen, y el único sistema operativo con ésta habilidad es Windows 10. (Existe el trabajo preliminar respecto a los controladores para Linux/X11)

Hemos logrado el introducir esta tecnología, mas como una prueba de nuestras habilidades, la experiencia de pintar con un gamut amplio bajo 1000 nits es casi mágica. Nos queremos asegurar de que ésta habilidad con HDR se convierta en parte del código de Qt mismo, para que otros programas que lo usan se beneficien, lo cual, en turno hace que mas proyectos y compañías adopten esta tecnología.

El otro gran proyecto, el cual a tomado muchas horas de trabajo y el cual esta lejos de ser terminado el el **sistema de recursos**. Los recursos son cosas como las puntas de los pinceles y los pinceles mismos, las texturas y gradientes. Cuando KImageShop comenzó, viente años atrás, los discos duras eran pequeños, la memoria muy limitada y imágenes de 1k pixeles por lado se consideraba enormes. Por lo tanto, los recursos eran pequeños en tamaño y los usuarios hacían poco uso de los mismos.

Hoy en día, los recursos son bastante grandes y los usuarios usan bastantes. El código que se encarga de ésta parte del programa a crecido sin una dirección bien definida, y se ha parchado constantemente para mantenerlo activo y funcionando. En el 2017 comenzamos a diseñar un nuevo sistema, y en el 2018 hemos empleado bastante tiempo tratando de implementarlo, trabajo que aun estamos haciendo arduamente. El nuevo sistema tendrá un mejor uso de memoria, lo cual reduce el tiempo que el programa toma al abrirse, ademas de que el manejar los recursos sera mucho mas correcto, al menos esa es la meta.

Y por supuesto, hemos y seguiremos corrigiendo errores de código, mejorando todo el programa y poniéndolo todo ésto a dispocicion de nuestros usuarios.

¡Y el 2019 [es el veinteavo aniversario de Krita](https://phabricator.kde.org/R511:3e91e954652b9db5c715b71c717b2a58cfe49bcd)!
