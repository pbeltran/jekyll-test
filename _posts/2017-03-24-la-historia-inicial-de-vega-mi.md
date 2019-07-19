--- 
layout: single 
title: La historia inicial de Vega, mi impresora 3D
author: Pablo Beltrán-Pellicer
categories:
 - impresión en 3D 
 - TIC en el aula 
---




No es la primera vez que mi hijo de 4 años me pregunta, intrigado a más
no poder, cómo construí la *máquina 3D*. Le debe parecer increíble el
proceso de ver una pieza en la pantalla del ordenador y, luego, observar
cómo se va imprimiendo. Cosa que, a su vez, me parece de lo más
encantador, sobre todo cuando el chaval no pregunta sobre cómo funcionan
los teléfonos, el ordenador, o cosas así. Esto de la impresión en 3D es
algo que todavía se sale de lo normal. Y, sin embargo, el funcionamiento
de una máquina de estas es simple como el de un botijo. Un chorro de
material fundido, plástico, que se va depositando capa a capa hasta
modelar una figura. Bueno, igual me he pasado, pero en fin. Antes de que
se me olvide la historia, prefiero dejarla aquí para la posteridad y, de
esta manera, puede que a alguien le resulte útil.  

![](/assets/img/2017-03-24-image-0000.jpg)

## Razón de ser y árbol (más bien línea) genealógico

La construcción inicial del clon \#541 Vega, tiene lugar durante
diciembre/enero de 2016. Se inscribe el día 1 de enero de 2016 en el
[Imperio de los
Clones](http://www.reprap.org/wiki/Clone_Wars:_El_imperio_de_los_clones/es) del
proyecto RepRap en español, como descendiente del clon \#409 Vulcano. La
culpa de que finalmente me decidiera a construir una impresora de estas
es del maker de Vulcano, [crjaso](https://twitter.com/crjaso), gran
amigo y mejor persona. Y es que Vega es, efectivamente, descendiente de
su clon. Literalmente, debido a que todas las piezas de plástico
iniciales (engranajes, poleas, extrusor, etc.) fueron imprimidas por
Vulcano. Si indagamos un poco en el Imperio de los Clones, la línea
genealógica de Vega es la siguiente:  
  
![](/assets/img/2017-03-24-image-0001.jpg)

  
Es decir, a modo de los nombres del Señor de los Anillos, podemos decir:
*\#541 Vega (Pablo Beltrán, Zaragoza, 01/01/2016), hija de \#409 Vulcano
 (C Rdguez. Zaragoza, 23 de septiembre de 2014), hijo de \#307 Golem
(Pedro Lahuerta, Cuenca, 10 de enero de 2014), hijo de \#228 Proteus
(Pedro Lahuerta. Cuenca, 30 de junio de 2013)*  

## Construcción inicial

Como la cosa tenía que tener su encanto, no valía con comprar un kit por
internet, que a esas alturas ya estaban disponibles. No, había que
participar de la comunidad, beber de la fuente primigenia, aprender cómo
funcionaba todo esto. Así que me dirijo al foro de [Clone Wars en
español](https://groups.google.com/forum/#!forum/asrob-uc3m-impresoras-3d),
y expreso que quiero participar en la [compra conjunta de marcos de
metal para la P3Steel
2.0](https://groups.google.com/forum/#!topic/asrob-uc3m-impresoras-3d/2yAV2iwXtDE%5B1-25%5D),
organizada por Álvaro Rey, joven fundador de
[MakerGal](http://www.makergal.es/). Esta impresora es una versión de la
[P3Steel](http://reprap.org/wiki/P3Steel/es) original.

  

Con el envío, se me pone en unos 180 euros el marco, varillas roscadas,
tornillería, fuente de alimentación, cama caliente de silicona,
hobbed-belt, rodamientos, flex coupling y correas GT2. A eso, habría que
añadir los motores, la electrónica (Arduino y RAMPS 1.4), los finales de
carrera y el fusor, que me fui agenciando de proveedores de China por
internet. Y las piezas de plástico ABS naranja que me regaló
[crjaso](https://twitter.com/crjaso).

<table>
<tbody>
<tr class="odd">
<td style="text-align: center;"><a href="https://3.bp.blogspot.com/-x0OS1JuRiIA/WM7--nsdqrI/AAAAAAAACgw/fnyfwKj12U4OIMVJm94PNqYhchsZgB9RACLcB/s1600/2015-10-12%2B23.15.03.jpg">![](/assets/img/2017-03-24-image-0002.jpg)

</tr>
<tr class="even">
<td style="text-align: center;">Embrión de Vega, a 12 de octubre de 2015.</td>
</tr>
</tbody>
</table>

El caso es que, una vez recibidos los marcos el 25 de septiembre de
2015, voy montando el engendro, con calma. No fue llegar y triunfar,
sino que hubo que hacer cierta labor de ajuste mecánico. Por ejemplo,
tuve que limar las abrazaderas de los rodamientos de la araña de la cama
caliente, porque pegaban con el marco al moverse en el eje Y.
Igualmente, creo recordar que algún flex coupling (las piezas sobre las
que se acoplan las varillas a los motores del eje Z) venía para otras
medidas y hubo que cambiarla. Más allá de esos contratiempos, mucho
atornillar y organizar cables, ajustar tensiones de las correas y poco
más.  

<table>
<tbody>
<tr class="odd">
<td style="text-align: center;"><a href="https://2.bp.blogspot.com/-GGkX6dylXcw/WNQ5lQ76QZI/AAAAAAAACjk/ROzPTopjQksyddXZ2SRxUk3aIt2ZNbkpwCLcB/s1600/2015-12-30%2B16.26.04.jpg">![](/assets/img/2017-03-24-image-0003.jpg)

</tr>
<tr class="even">
<td style="text-align: center;">El cerebro de Vega,<br />
a 30 de diciembre de 2015</td>
</tr>
</tbody>
</table>

La electrónica, casi me entran escalofríos. Creía que iba a ser lo más
fácil para mí. Sin embargo, no me percaté de que la fuente de
alimentación, al atornillarla al marco, hacía un ligero cortocircuito,
que solamente se manifestaba cuando conectaba el Arduino por USB al
ordenador y estaba siendo alimentado por la fuente. Y la manifestación
era en forma de humo negro. No me percataría de esto hasta unos meses
más tarde. Más allá de las placas quemadas, no fue mayor problema,
puesto que con el display LCD y su lector de tarjetas SD incorporado, se
podía hacer lo mismo.  
Hubo algún problemilla más, pero nada que una pensada, los buscadores o
los foros de internet no pudieran resolver. Por ejemplo, los cables
planos que van del display al Arduino no estaban aislados
electromagnéticamente (bendita EMI), con lo que los envolví en papel de
aluminio de forma independiente, con su obligatoria conexión a tierra (0
voltios).  

## El prisma de calibración

La prueba de fuego tuvo lugar durante las navidades de 2015/2016. Así,
el 1 de enero de 2016 pude imprimir la primera cosa. Un fantástico
prisma de calibración de 20x20x10 (en mm). Eso naranja que se observa en
la foto de la derecha es cinta térmica Kapton. Ahora imprimo
directamente sobre la cama de aluminio, y tan feliz.

  

 
![](/assets/img/2017-03-24-image-0004.jpg)


  

## Ajustes mecánicos a posteriori

<table>
<tbody>
<tr class="odd">
<td style="text-align: center;"><a href="https://2.bp.blogspot.com/-eUxPWoate5c/WM-bGF7qpZI/AAAAAAAAChA/PP6iUxfStzsSxy8wQIhLdTqXeTbbgKzaACLcB/s1600/vega_20160109.jpg">![](/assets/img/2017-03-24-image-0006.jpg)

</tr>
<tr class="even">
<td style="text-align: center;">Impresora Vega, a 9 de enero de 2016.</td>
</tr>
</tbody>
</table>

Después de las primeras pruebas me percato de que las barras que guían
el movimiento del eje Z presentan una curvatura más que evidente, y que
eso podría ser el causante de que el eje Z hiciera cosas raras
(separación entre capas a su libre albedrío). Un observador sagaz,
detectará en la imagen de la derecha este hecho. En su día tuve que
esforzarme, a base de martillo, en plan Thor, para meterlas en su sitio,
cosa que no fue buena idea. Por lo tanto, lo que me tocó hacer fue
utilizar la dremel para limar los agujeros de paso en el marco, y
avellanarlos ligeramente. De esta forma, conseguí que las barras de
acero pasasen rectas. Un problema menos, pues estaba claro que de esa
manera el avance en el eje Z no era lineal.  

En estas, que la fuente se me estropeó vete a saber por qué, y me compro
una nueva el 8 de febrero de 2016.

## To be continued...

Bueno, y  para los avispados que se hayan dado cuenta del cambio de look
en la foto inicial del artículo, esos colores amarillos que aparecen son
el resultado de una evolución, que será contada en otra ocasión. 
