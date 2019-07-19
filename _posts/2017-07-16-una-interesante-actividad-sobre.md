--- 
layout: single 
author: Pablo Beltrán-Pellicer 
title: "Una interesante actividad sobre probabilidad (y geometría) con la impresora 3D" 

categories:
 - probabilidad-estadística 
- secundaria 
- impresión en 3D 
- TIC en el aula 
- recursos 

excerpt: "Eso que aparece imprimiéndose en la foto de portada, es un dado. Diseñado por un alumno de 2º de ESO. "
header:
  overlay_image: /assets/img/2017-07-16-image-0000.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: ""
toc: true
toc_sticky: true

---

Eso que aparece imprimiéndose en la foto de portada, es un dado. Diseñado por un alumno de 2º de ESO. Se trata de una experiencia piloto en primer ciclo de secundaria sobre la enseñanza-aprendizaje de nociones probabilísticas, en la que los alumnos diseñan dados, los imprimen en 3D y posteriormente analizan si son sesgados. La experiencia se enmarca dentro del significado frecuentista de la probabilidad, facilitando su puesta en relación con el significado clásico o a priori.  


![](/assets/img/2017-07-16-image-0000.jpg)
  
Para esta experiencia se optó por utilizar [Tinkercad](https://www.tinkercad.com/), que simplifica la tarea de   diseño. Se planteó como actividad voluntaria en 2º de ESO, prácticamente a final de curso y la consigna inicial fue la siguiente:  
  
*La tarea consiste en diseñar un dado con ordenador. Es voluntario y añade 0,5 puntos al examen de geometría. Después, imprimiré en 3D vuestros dados, que*   *os podréis quedar, y os pediré que los probéis para ver si están o no sesgados. A continuación,*   *os explico cómo hacerlo.*  
  

![Aspecto del entorno de Tinkercad](/assets/img/2017-07-16-image-0001.jpg)

## Consideraciones en el diseño de dados 
  
El diseño de dados no es algo trivial, habiendo propiciado interesantes discusiones en los repositorios de modelos online, como [Thingiverse](http://www.thingiverse.com/thing:147883/#comments).  Los usuarios han realizado, incluso, pruebas chi-cuadrado de significancia estadística para comprobar el correcto balanceo de los dados. Las conclusiones más relevantes son:  
  
- Los dados con esquinas más redondeadas, evidentemente, ruedan más. Esto es algo que amplifica cualquier sesgo de diseño, lo que constituye una ventaja de cara a nuestros objetivos.  
- Si colocamos el dado para que se imprima girado 45º, obtenemos mejores resultados.  
- El porcentaje de relleno de los dados influye. El software traductor permite ahorrar plástico, rellenando el interior de la pieza con un mallado rectangular o hexagonal. Se comprueba que es mejor imprimir dados sólidos al 100%.  
  

## Errores de los alumnos
Los errores de diseño que se identifican en los diseños de los alumnos, y que se prueban experimentando, son los siguientes:
 

1.  Cuando se indican los puntos con cavidades, no se ha retirado la misma cantidad de material en todas las caras, por lo que unas caras pesan más que otras
2.  Un error similar se produce cuando en lugar de retirar material, se añade, con lo que se propicia que se mantenga sobre ciertas caras mayor masa que en otras.
3.  No se tiene en cuenta que la suma de las puntuaciones de las caras debería sumar 7 para facilitar el equilibrado del dado (esto está relacionado con el error de tipo 2), como ocurre en los dados estándar.
4.  No se centran o alinean los puntos de cada cara, lo cual influye también en la distribución de masa del dado.
5.  El dado no presenta las mismas dimensiones en todas sus caras. 

![](/assets/img/2017-07-16-image-0002.jpg)
![](/assets/img/2017-07-16-image-0003.jpg)
![](/assets/img/2017-07-16-image-0004.jpg)

  
## Para saber más

Todo esto se explica con detalle en: Beltrán-Pellicer, P. (2017). [Modelado e impresión 3D como recurso didáctico en el aprendizaje de la probabilidad](http://thales.cica.es/epsilon/sites/thales.cica.es.epsilon/files/epsilon95_6.pdf).*Épsilon: Revista de Educación Matemática, 34*(95), 99-106.
