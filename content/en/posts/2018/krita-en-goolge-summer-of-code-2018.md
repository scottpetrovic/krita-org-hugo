---
title: "Krita en Goolge Summer of Code 2018"
date: "2018-09-05"
categories: 
  - "uncategorized-es"
---

Éste año, hemos participado en el evento Google Summer of Code con tres estudiantes: [Ivan](https://colorathis.wordpress.com/), [Andrey](https://lieroz.github.io/) y [Michael](https://simeir.github.io/). Parte de el código que estos gran estudiantes han producido ya se encuentra en la versión 4.1.1 de Krita, y la mayoría del resto del código en la versión inestable, por lo que ya puedes ponerlo a prueba en las versiones "diarias" (Nightly Builds) disponibles para [Windows](https://binary-factory.kde.org/job/Krita_Nightly_Windows_Build/) y [Linux](https://binary-factory.kde.org/job/Krita_Nightly_Appimage_Build/). A continuación explicamos lo que se ha logrado éste año.

**El proyecto  de Ivan** se trata de hacer que las brochas actúen con mayor rapidez usando vectores.  Si ésto suena un tanto técnico, ¡Es por que lo es! Básicamente, el CPU es lo suficientemente fuerte para hacer bastantes cálculos al mismo tiempo, siempre y cuando sea el mismo tipo de operación, aun con números diferentes. Se le puede dar mas de 200 cifras al CPU, hacer que las multiplique, y lo hará tan rápido como el multiplicar una sola cifra. Y resulta que el producir el trazo de una brocha usa mas o menos el mismo calculo. Como todo proyecto, éste tiene también sus propias complicaciones y Ivan se ha dedicado a resolver estos problemas usando la misma lógica en brochas de Krita. Aquí mostramos una imagen con la comparación desde su [blog](https://colorathis.wordpress.com/):

[![](../images/avx_cgauss_60.gif)](https://krita.org/wp-content/uploads/2018/09/avx_cgauss_60.gif)

Arriba, trazo anterior; abajo, rapidez actual del trazo.

Si el proyecto de Ivan se trata de la rapidez, bueno, también lo es el de **Andrey**. Andrey ha estado trabajando en algo igual de técnico y complicado. Los CPU modernos tienen varios núcleos (Cores), algunos tienen cuatro pero virtualizan ocho, otros tienen diez y virtualizan veinte o mas. Y un silicio que no es usado, es prácticamente desperdiciado, por lo que Krita ha tenido la capacidad desde hace un tiempo de utilizar múltiples núcleos, desde que Dmitry Kazakov hizo su [proyecto del Google Summer of Code,](http://dimula73.blogspot.com/2009/08/gsoc-krita-tile-engine-wrap-up.html) en el 2009, el cual se baso en el motor del "tile". Nueve años después, Dmitry guía y supervisa el trabajo de Andrey de la misma índole. El motor de "tile" (pequeñas fracciones de una imagen, por lo que su nombre en ingles se basa en la semejanza de un "ladrillo" o "azulejo") fracciona las imágenes y el procesador trabaja independientemente en cada una de las piezas fraccionadas.

Por lo que cuando Dmitry, trabajo el año pasado en el uso de núcleos múltiples en Krita, descubrió que en ciertas circunstancias Krita hace que los núcleos trabajen de uno por uno y no de manera simultanea, por lo que recomendó el resolver este problema, al que se le llama "bloqueado" y cuya solución es el eliminarlo.

Así que el proyecto de Andrey es el hacer que la serie de de "tiles" funcionen sin bloqueo. Y tal trabajo ya se ha completado, todavía existen algunos problemas del código ya que esta parte es bastante complicada, por lo que se necesita bastante el poner a prueba estos cambios. Éste trabajo sera incluido en la versión 4.2 de Krita la cual estará lista al final de este año, parte del código ya se ha incluido en 4.1.1, ya que Andrey ha logrado bastantes mejoras con el mismo:

[![](../images/lockless-1024x506.png)](https://krita.org/wp-content/uploads/2018/09/lockless.png)

**Michael** ha estado trabajando en algo completamente diferente: La compatibilidad de paletas de color. Las paletas son una serie de colores, los cuales nosotros llamamos recursos. El manipular las paletas era hecho mediante el código proveniente de Calligra en las versiones previas y KOffice en las mas antiguas. El código es complicado y difícil de entender por lo que el primer objetivo de Michael fue el ponerlo en orden, y esta parte ya se ha terminado y es parte de la versión 4.1.1 de Krita.

El siguiente paso de su proyecto fue el trabajar en el panel de paletas, mismo cuyos detalles se encuentran en [ésta sección en Phabricator](https://phabricator.kde.org/D14815). Aun queda trabajo por realizar, sin embargo el trabajo planeado para el Google Summer of Code ya está completo.

[![](../images/listanddocker-1024x512.jpg)](https://krita.org/wp-content/uploads/2018/09/listanddocker.jpg)

Éste el el dialogo de preferencias:

[![](../images/DlgPaletteEditor-1024x517.png)](https://krita.org/wp-content/uploads/2018/09/DlgPaletteEditor.png)
