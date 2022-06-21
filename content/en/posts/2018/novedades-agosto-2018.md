---
title: "Novedades del mes de Agosto 2018"
date: "2018-09-05"
categories: 
  - "uncategorized-es"
---

Anteriormente teníamos novedades semanales referentes al desarrollo de Krita, sin embargo el enfocarnos directamente en el desarrollo mismo no nos permite el crear una publicación semanal lo cual es una lastima. Aun así nos gusta el compartir lo que hacemos con todos ustedes y no solo de manera técnica tal como la bitácora de [git](https://github.com/KDE/krita), por lo que veamos si podemos revivir la tradición...

En agosto, comenzamos la preparación para el siguiente evento de recaudación de fondos. Desde mediados de septiembre y hasta mediados de Octubre estaremos promoviendo Krita para financiar su desarrollo. Los últimos eventos estuvieron enfocados en nuevas funciones, éste por otro lado, estará basado solo en la estabilidad y desempeño. Lo llamamos **Zero** **Bugs** (cero errores de código) que aun que no es literal dado el aspecto técnico, es nuestro emblema para esta ocasión. Nos hemos cambiado a un nuevo sistema de pagos, lo cual ahora hace posible el hacer donaciones a Krita no solo por medio de Paypal, si no ademas con transferencias de banco, tarjetas de crédito, varios sistemas de pago electrónico e inclusive bitcoin. Éstos métodos ya están disponibles en [nuestra pagina de donaciones](/support-us/donations/).

De hecho ya tuvimos un buen comienzo referente a la estabilidad, con el "unittests", pequeños programas que ponen a prueba las funciones de Krita los cuales usamos para ver si el código falla en alguna parte. Ademas hemos solucionado casi cien errores de código, y por ultimo pero de igual importancia, el evento de [Google Summer of Code](/item/kritas-2018-google-summer-of-code/) ha llegado a su fin.

Veamos algunos detalles de lo mas sobresaliente:

### Pulir, pulir y pulir

Después de haber actualizado Krita a Qt5, varias partes del código fallaron el los "unittests" y simplemente no se podía construir el programa con ellos, o producían "congelamientos", cerrado inesperados, etc. Durante agosto la calor fue bastante fuerte como para trabajar arduamente en cualquier cosa que fuera muy complicada, por lo que nos dedicamos a solucionar las partes que no funcionaban adecuadamente, claro, aparte de otros trabajos que se han realizado durante este tiempo.

### Mejoras del seleccionado

Dmitry, uno de los desarrolladores principales, y cuyo trabajo se costea con tus donaciones, ha estado trabajando desde hace un par de semanas en el mejoramiento de [las selecciones](https://phabricator.kde.org/T3920) en Krita. El seleccionar en Krita es un tanto diferente a otros programas, ya que tenemos dos tipos, locales y globales, las cuales se pueden visualizar con el "desfile de hormigas" (linea de guiones) o con una mascara, ademas esta pueden ser basadas en pixeles o vectores. Por lo que Dmitry se ha enfocado en:

- Pintar en la mascara de selección de manera instantánea.
- Hacer posible mas de una selección local.
- Habilidad de añadir opacidad, cruzar opacidad y remover opacidad de las selecciones globales.
- Una selección es automáticamente creada cuando se usa la función "mostrar la selección global".
- Convertir selecciones de pixeles a vectores y viceversa.
- Hacer posible el modificar las selecciones.

https://www.youtube.com/watch?v=gWv--Do9L0E

### Reconstruccion de el manejo de los recursos

Los recursos son cosas que el usuario quiere usar en Krita, tales como Pinceles, punta de pinceles, gradientes, trazos y espacios de trabajo. Algunos recursos ya vienen incluidos con Krita, otros son creados con Krita por el usuario y otros pueden ser descargados del internet. El sistema de recursos de Krita existe desde el ultimo siglo, o si se prefiere desde el ultimo milenio. Fue diseñado en los días cuando un pincel de 50 pixeles era considerado **enorme** y los trazos se median en no mas de 128 pixeles por lado. En la actualidad el usuario quiere usar pinceles de 1000 pixeles y trazos de 5000, y muchos a la ves.

El diseño original ya no logra abastecer los nuevos recursos, ademas, después de mas de veinte años de modificaciones, el código es todo un enredo. Comenzar desde cero es casi siempre un gran error, sin embargo, ya estamos trabajando en rehacer esa parte de Krita de cualquier modo. Boudewijn ha progresado bastante, pero ello es algo que aun no esta listo para ser usado por el publico, pero se puede apreciar parte del desarrollo en la "tarea" de [Phabricator](https://phabricator.kde.org/T379). Es algo que ya hemos estado discutiendo y planeando por mucho tiempo. Todos los errores relacionados con el etiquetado, añadir y remover recursos serán solucionados al implementar este nuevo código.

Al menos ése es el plan...  Pero aun hay bastante por hacer.

[![](../images/resource_db_explorer-300x145.png)](https://krita.org/wp-content/uploads/2018/09/resource_db_explorer.png)

También tuvimos una sorpresa y otras cosas extras:

### Nuevo e inesperado

Una nueva y fantástica función el la mascara de la gama, creada por Anna Medonosova. Lo cual incluye el editar y aplicar la mascara al selector artístico de colores. Ver el articulo de [James Gurney](https://gurneyjourney.blogspot.com/2008/01/color-wheel-masking-part-1.html) (en ingles) para mayor información.

[![](../images/gamut-300x300.png)](https://krita.org/wp-content/uploads/2018/09/gamut.png)

Ahora tambien tenemos un panel para la observación de errores. por lo que los usuarios de Windows ya no tienen que lidiar con la ventana de la misma función:

[![](../images/log-docker-300x300.png)](https://krita.org/wp-content/uploads/2018/09/log-docker.png)(Art de [Iza Ka](http://LifeFinalEdited.pl))

Y por supuesto, han habido mas actividades, Reptorian a creado un conjunto de modos de mezclado y ahora está trabajando en una nueva selección de mezclado. Jouni ha estado mejorando y solucionando problemas con la nueva herramienta de imágenes de referencia y ha implementado el [clonado de fotogramas para la animación](https://phabricator.kde.org/T8764).
