---
title: "Se han aceptado 3 estudiantes para el evento Google Summer of Code del 2018"
date: "2018-05-08"
categories: 
  - "uncategorized-es"
---

Desde el 2006, Google nos ha ofrecido la oportunidad de patrocinar estudiantes para que éstos desarrollen proyectos con Krita. Para el 2018 tenemos tres estudiantes muy talentosos los cuales participaran durante éste verano, ellos comenzaran a familiarizarse primero con el código base de Krita, luego nos mostraran mediante blogs sus experiencias y expectativas mientras trabajan en sus proyectos.

A continuación mostramos su presentación.

 

### Ivan Yossi - Optimizar la generación de mascaras de pinceles tipo Soft, Gaussian y Stamp para que se pueda usar el AVX con los archivos Vc

Krita requiere de una respuesta rápida en el uso de pinceles para ofrecer un rutina mas natural. Una linea dibujada consta de miles de imágenes acomodadas una tras otra, la creación de la mascara tiene que ser bastante rápida ya que se ejecuta miles de veces por segundo. Si el proceso que aplica éstas imágenes en el lienzo no es lo suficientemente rápido, la experiencia se arruina y el gusto de pintar con Krita puede disminuir drásticamente.

El optimizar la creación de las mascaras se puede hacer con el juego de instrucciones de AVX para poder aplicar las modificaciones en vectores en un solo paso. En este caso la información son las coordenadas que componen la imagen y a la vez la mascara. La programación de AVX se puede lograr con un archivo Vc, el cual maneja niveles bajos de manera optimizada y adaptada al uso de los procesadores. Sin embargo la información tiene que ser preparada para vida de poder optimizarse. De hecho ya se ha optimizado el motor de mascaras de pinceles principal, el cual es hasta cinco veces mas rápido que el actual motor de mascaras Gaussian.

Éste proyecto esta enfocado en proveer un mejor rendimiento al pintar implementando el código de AVX para las mascaras Gauss circular, Soft circular, Gaussian rectangular, Soft rectangular y Stamp.

### Michael Zhou - Un panel de muestras de color "Swatches" para Krita

Éste proyecto se enfoca en la creación de un panel de muestras de color para Krita, Parecido al panel de paletas de color que ya existe, pero con las siguientes ventajas:

- Los usuarios podrán fácilmente añadir, mover y remover colores, lo que ordenara visualmente de mejor manera los colores y la forma de usarlos.
- Los usuarios podrán guardar paletas de color con cada documento lo cual asegura que los colores usados estén siempre disponibles.
- Tendrá una interfaz mas intuitiva.

### Andrey Kamakin Optimizar el uso múltiple de procesos en el administrador de "tiles" de Krita

Éste proyecto se enfoca en mejorar de manera general el rendimiento de Krita introduciendo un "hash table" sin bloqueo que guarda "tiles" y mejora los bloqueos.

El problema: En la ejecución de procesos individuales de un programa, no se requiere de monitorear ningún recurso compartido ya que es garantizado que solo un proceso tendrá acceso a un recurso. En procesos múltiples entrelazados, es común el que los recursos se compartan entre ellos, por lo que en situaciones como "dirty read", etc. éstos tienen que ser excluidos del programa para un comportamiento normal. La forma mas simple de solucionar éste problema es el poner un bloqueo en las "hash tables" para que sus operaciones se limiten a un solo recurso por proceso.

\--

¡Les deseamos a todos los participantes mucha suerte y la mejor de las experiencias éste verano!
