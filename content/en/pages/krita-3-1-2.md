---
title: "Krita 3.1.2"
date: "2017-02-01"
---

Esta es una versión intermedia con la corrección de errores de código "bugs" como objetivo principal, pero con algunas funciones extras como ya es acostumbrado en estos últimos lanzamientos.

### Las animaciones ahora pueden incluir audio.

<iframe src="https://www.youtube.com/embed/s08oHOjxo84" width="100%" height="450" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

Ahora se puede importar audio lo cual ayuda a sincronizar voces y música con la animación. En el video de demostracion, TImothée Giet nos muestra como se usa esta nueva función.

- Los formatos disponibles son WAV, MP3, OGG y FLAC
- Se ha agregado una nueva casilla en el dialogo de la reproducción de animaciones con la opción de incluir audio al exportar el documento.
- El manual de Krita ofrece una mejor explicación (en ingles) del como usar esta nueva función.

**Nota:** Las appimages de Krita aun no incluyen esta función de audio. está en estado experimental, y no se garantiza que funcione correctamente, por lo que esperamos que nos puedas ayudar reportando los problemas que pudieras encontrar.

 

### Cambios en general

- En la herramienta de selección de contorno, ahora se puede usar la tecla Ctrl (manteniendola presionada) para continuar dibujando la selección aun cuando se levanta la lapicera (o ratón) de la tableta digital, continuando dondequiera que se coloque nuevamente, anteriormente al levantar la lapicera digital terminaría la selección en esexportandolase punto.
- Se ha hecho posible el eliminar una selección al hacer un clik en el lienzo mientras cualquiera de las herramientas de selección de siluetas y entorno están activadas.
- Se ha incluido una opción para activar HiDPI en la ventana de configuraciones.
- Por lo pronto, dada la cantidad de problemas que ha presentado el exportar imágenes en PDF, ésta función se ha removido. ([BUG:372439](https://bugs.kde.org/show_bug.cgi?id=372439))

### Correciones de códidgo

- Se han corregido una serie de problemas al crear y editar paquetes de pinceles. ([BUG:352151](https://bugs.kde.org/show_bug.cgi?id=352151))
- Se ha compuesto y reestablecido el adaptador para exportar de Spriter.
- Se ha corregido el cargar los pinceles con patrones internos. ([BUG:374745](https://bugs.kde.org/show_bug.cgi?id=374745))
- Se ha corregido el modo de borrador del pincel, ahora mantiene correctamente el los modos de fusión. ([BUG:348290](https://bugs.kde.org/show_bug.cgi?id=348290))
- Se ha compuesto la creación de pinceles a partir de un estampado. ([BUG:373846](https://bugs.kde.org/show_bug.cgi?id=373846))
- Ahora se puede cargar archivos RGBA TIFF que no tienen un perfil ICC incluido, como sRGB con corrección de gama. ([BUG:375479](https://bugs.kde.org/show_bug.cgi?id=375479))
- Se ha hecho posible el usar el mismo lenguaje que el resto del sistema está usando. ([BUG:374928](https://bugs.kde.org/show_bug.cgi?id=374928))
- Se ha corregido el cierre del programa inesperado al usar tabletas Wacom de modelos pasados con Windows 10, así como la incapacidad de rotar el lienzo con esas lapiceras. ([BUG:375253](https://bugs.kde.org/show_bug.cgi?id=375253))
- Se ha añadido un mayor grado de precisión al usar los niveles de en los filtros de ajuste. ([BUG:375201](https://bugs.kde.org/show_bug.cgi?id=375201))
- Se ha arreglado la función acumulativa al deshacer una acción.
- Se han ocultado los textos en la barra de herramientas cuando existe un icono que los substituye.
- Se han restaurado la sección de "favoritos" en los modos de fusión.
- Se ha hecho posible el eliminar etiquetas de pinceles que existen por defecto.  ([BUG:347607](https://bugs.kde.org/show_bug.cgi?id=347607))
- Se ha restaurado las escalas de 0.1 el radio, para la herramienta de recorte. ([BUG:374021](https://bugs.kde.org/show_bug.cgi?id=374021))
- Se ha corregido el guardar el nombre de una mascara de selección. ([BUG:374383](https://bugs.kde.org/show_bug.cgi?id=374383))
- Se ha corregido el cierre del programa inesperado  al crear y cerrar un documento que tiene fotogramas de opacidad. ([BUG:374381](https://bugs.kde.org/show_bug.cgi?id=374381))
- Nuevos iconos para la barra de herramientas.
- Se ha corregido el cierre del programa inesperado al abrir o usar un documento que contiene un espacio de color de 16-bit flotante XYZ.
- Se ha corregido el hacer de la acción de pantalla completa seleccionable un vez mas. ([BUG:373906](https://bugs.kde.org/show_bug.cgi?id=373906))
- Se ha corregido el que no se pierdan los cambios de OCIO al mover la ventana. ([BUG:373481](https://bugs.kde.org/show_bug.cgi?id=373481))
- Se ha corregido el modo de atravesar las capas cuando estas están en grupo.
- Se ha hecho que el nombre de los espacio de colores ante el usuario, tengan consistencia .
- Se ha corregido el cierre del programa inesperado al usar dos ventanas. ([BUG:371124](https://bugs.kde.org/show_bug.cgi?id=371124))
- Se ha resuelto la confusión al guardar las opciones de mas de una lapicera digital entre sesiones. ([BUG:374957](https://bugs.kde.org/show_bug.cgi?id=374957))
- Se ha corregido el cierre del programa inesperado al usar la función de deshacer. ([BUG:374524](https://bugs.kde.org/show_bug.cgi?id=374524))
- No se crearan vistas previas sin valores de lo alto y ancho. ([BUG:373835](https://bugs.kde.org/show_bug.cgi?id=373835))
- Se ha corregido el cierre del programa inesperado cuando se selecciona el botón de las opciones de herramientas en la barra misma. ([BUG:374497](https://bugs.kde.org/show_bug.cgi?id=374497))
- Se ha corregido el reproducir una animación que no empieza en el primer fotograma.
- Ya no se pierde la configuración del rango de reproducción de una animación, al estar continuamente exportándolas.

Esperamos que este lanzamiento ayude a mejorar mucho mas aun la rutina de dibujo y arte de nuestros usuarios, los reportes las correcciones de errores ayudan ha reforzar el programa y esto nos da la oportunidad de hacerlo mas estable. ¡Gracias y a disfrutar de la pintura digital!
