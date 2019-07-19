--- 
layout: single 
title: Introduciendo el modelado y la impresión 3D en el aprendizaje de matemáticas
author: Pablo Beltrán-Pellicer 

categories:
 
- didáctica 
- infantil 
- secundaria
- impresión en 3D 
- TIC en el aula 
- primaria

excerpt: "A pesar de que las impresoras en 3D utilizan una tecnología conocida ya desde hace tiempo, es en los últimos años cuando se han comenzado a extender entre el gran público, mostrando un amplio rango de aplicaciones."
header:
  overlay_image: /assets/img/2018-08-11-image-0000.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: ""
toc: true
toc_sticky: true

---



A pesar de que las impresoras en 3D utilizan una tecnología conocida ya desde hace tiempo, es en los últimos años cuando se han comenzado a extender entre el gran público, mostrando un amplio rango de aplicaciones. Las causas de este auge hay que buscarlas, en primer lugar, en lo asequible que resulta adquirir uno de estos aparatos. Para ello, ni siquiera hemos de ir a comercios especializados, basta con acudir a un centro comercial o comprarla en Internet.  

![](/assets/img/2018-08-11-image-0000.jpg)

## Comunidades y clones

Por otro lado, de forma previa y anticipando esta popularización de la tecnología, surgieron comunidades formadas por personas interesadas en la impresión en 3D, tanto a nivel profesional como amateur. En el seno de estas comunidades han ido surgiendo modelos de impresoras cuyo diseño se compartía libremente. De esta forma, alguien que desee construirse una de estas máquinas, puede hacerlo teniendo en cuenta esos diseños, encontrar a alguien que le imprima -normalmente, de manera altruista- las piezas de plástico necesarias, y comprar el resto.     

Las máquinas RepRap (*Replicating Rapid-prototyper*) fueron inventadas por Adrian Bowyer, apareciendo esta idea por primera vez en Internet en 2004 y, no en vano, es en torno a la web [RepRap.org](https://www.reprap.org/) que se ha creado la que posiblemente sea la comunidad más importante. El árbol genealógico de la rama española, iniciado por Juan «Obijuan» González Gómez y Andrés Prieto en 2009, puede verse en el [Imperio de los Clones](https://www.reprap.org/wiki/Clone_Wars:_El_imperio_de_los_clones/es).  

## Y en matemáticas, qué

Aunque esto de las impresoras 3D dé mucho juego -obviamente- en asignaturas como Tecnología, el proceso de fabricación de un objeto está lleno de matemáticas. A continuación, introducimos brevemente algunas tareas que hemos propuesto [@crjaso](https://twitter.com/crjaso) y un servidor (que están descritas en más detalle [aquí](http://hdl.handle.net/10481/44193) y [aquí](http://thales.cica.es/epsilon/sites/thales.cica.es.epsilon/files/epsilon95_6.pdf)):  

## Montaje de una impresora

[@crjaso](https://twitter.com/crjaso) realizó este proyecto con un grupo de alumnos de 3º de ESO (programa de diversificación) durante todo un curso, persiguiendo objetivos de aprendizaje transversales. Por un lado, para los alumnos participantes:   
- Que aplicaran sus conocimientos científico-tecnológicos en el proceso
de montaje y calibración de la impresora   
- Que desarrollaran su capacidad de expresión en público.  

![](/assets/img/2018-08-11-image-0001.jpg)

Por otro lado, el taller trata de acercar la tecnología de modelado e impresión en 3D al resto del alumnado del centro, transmitiendo los valores de aprender por aprender y la cultura del software libre. Todos los viernes, durante el recreo, el taller de tecnología se convirtió en un lugar de entrada libre donde se explicaban los progresos.  
La apertura del proyecto al resto de alumnado, permitió flexibilizar las actividades para adaptarlas a otros niveles, como programar la impresora para que dibujara. Para ello, se acopló en el cabezal de la impresora un rotulador de forma que esta se podía programar para que dibujara sobre un papel colocado en la base. Puesto que este tipo de impresora es de tipo “cartesiana”, se aprovechó el momento para en el aula dar el tema de funciones y el plano, haciendo hincapié en las coordenadas de los puntos del plano.  

## Conceptos geométricos

Otra actividad implementada por [@crjaso](https://twitter.com/crjaso), esta vez con un alumnos de 2º de ESO, fue la realización de un taller sobre los sólidos platónicos. Los objetivos eran conocer estos cuerpos y deducir cuáles son sus propiedades fundamentales, evitando la enseñanza de tipo memorística y ausente de significado. Las tareas que se plantearon utilizaron como recurso una impresora 3D y palos de brochetas. Los alumnos se organizaron en grupos de 3 o 4 integrantes, teniendo lugar la experiencia durante dos sesiones de clase de 50 minutos, incluyendo las siguientes tareas: 

- *Tarea 1: fórmula de Euler para el cubo*

A partir de la imagen mental, dibujos u objetos cotidianos.

- *Tarea 2: fórmula de Euler para el resto de sólidos platónicos*

En este caso, a los alumnos con dificultades se les dejó un poliedro
físico para facilitarles la comprobación. 

- *Tarea 3: impresión de los vértices necesarios*

Ahora los alumnos proceden a construir los poliedros correspondientes. Los vértices los tenía impresos el profesor de antemano, ya que es algo que puede consumir bastante tiempo. Lo interesante del modelo de vértice escogido (de W. Adams, disponibles en [http://www.thingiverse.com/thing:9359](http://www.thingiverse.com/thing:9359) es que es un diseño paramétrico y, por tanto, permite adaptar el modelo al grosor del objeto que seleccionemos como arista (los palos de brocheta, en nuestro caso) posibilitando el hacer poliedros de gran tamaño. 

![](/assets/img/2018-08-11-image-0002.png)

- *Tarea 4: montaje de los poliedros*

El uso de palos de brochetas como aristas conlleva una manipulación. Hay que cortarlas para que sean todas iguales y, pese a que al alumnado se le pidió que fuera riguroso, siempre hay alumnos que cuando pasan a la fase de montaje se dan cuenta que necesitan nuevas aristas de la longitud correcta.

![](/assets/img/2018-08-11-image-0003.png)

## Relacionando geometría, fabricación y probabilidad

Y de paso, articular significado frecuencial y clásico de la probabilidad. En este caso, la tarea la propuse yo con otro grupo de 2º de ESO, de forma voluntaria en la asignatura de matemáticas, durante la unidad didáctica de cuerpos geométricos, aunque el objetivo final era detectar intuiciones primarias erróneas y sesgos en el razonamiento probabilístico de los alumnos. La consigna fue:  
  

*La tarea consiste en diseñar un dado con ordenador. Es voluntario y añade 0,5 puntos al examen de geometría. Después, imprimiré en 3D vuestros dados, que os podréis quedar, y os pediré que los probéis para ver si están o no sesgados. A continuación, os explico cómo hacerlo. *


El mismo día de presentación de la actividad, se introdujo a los alumnos brevemente en el manejo de la aplicación online TinkerCad, y durante esa misma semana fueron entregando sus diseños.

![](/assets/img/2018-08-11-image-0004.png)

Posteriormente, se les citó individualmente para hacerles una breve entrevista basada en las siguientes preguntas: ¿es este el dado que diseñaste? ¿te gusta cómo ha quedado? ¿lo usarías para jugar a algún juego de mesa? ¿cómo sabrías si es un buen dado? ¿hacemos la prueba? En la experiencia que realizamos se observó cómo, casi ninguno de ellos, intenta ni siquiera que las caras de los dados pesen lo mismo.

## Y en educación infantil también

La cuarta y última de las situaciones se realizó con un niño de 5 años de edad (segundo curso de Educación Infantil). La tarea consistió en construir un juego sobre los animales de los polos, para el que se utilizó el software de modelado [Tinkercad](https://www.tinkercad.com/) y la impresora 3D para hacer realidad esos diseños, los cuales se subieron a [Thingiverse](http://www.thingiverse.com/thing:1321560). Los objetivos didácticos, desde el punto de vista lógico-matemático, consistieron en trabajar formas de figuras planas y de cuerpos en el espacio, así como vocabulario propio de medida y de geometría (altura, grosor, espesor, círculo, cilindro, etc.), así como lógico (unión de figuras, diferencia).  

![](/assets/img/2018-08-11-image-0005.png)

## Para terminar

Hemos esbozado diferentes opciones de introducir el modelado y la impresión en 3D en la enseñanza de las matemáticas. Los diferentes paquetes de software mencionados poseen características que complementan otros entornos de geometría dinámica, como Geogebra, que ya son habituales en las aulas, permitiendo articular álgebra y geometría y facilitando la manipulación y visualización de las piezas. 

Por otro lado, el disponer de una impresora en el centro educativo abre las puertas a la introducción de la robótica. Si bien existen modelos de robots orientados al ámbito educativo, el abanico de posibilidades se extiende al poder diseñar piezas nuevas, modificar diseños existentes e imprimirlos directamente. 
  
## Referencias

**Para saber más**, os invitamos a leer el artículo en extenso en la revista ReiDoCrea:   

Beltrán-Pellicer, P. y Rodríguez-Jaso, C. (2017). [Modelado e impresión en 3D en la enseñanza de las matemáticas: un estudioexploratorio](http://digibug.ugr.es/bitstream/10481/44193/1/6-2.pdf).
*ReiDoCrea, 6*, 16-28.  
  
La experiencia del dado está descrita en detalle en este otro artículo: Beltrán-Pellicer, P. (2017). [Modelado e impresión 3D como recurso didáctico en el aprendizaje de la probabilidad](http://thales.cica.es/epsilon/sites/thales.cica.es.epsilon/files/epsilon95_6.pdf). *Épsilon: Revista de Educación Matemática, 34*(95), 99-106.  
  
Curiosidad: en el [Imperio de los Clones](https://www.reprap.org/wiki/Clone_Wars:_El_imperio_de_los_clones/es) puede verse que la máquina de Carlos es el clon \#409, *Vulcano*, mientras quela mía es el clon  \#541, *Vega*, descendiente de la de Carlos.  
  
![](/assets/img/2018-08-11-image-0006.png)
![](/assets/img/2018-08-11-image-0007.png)

 