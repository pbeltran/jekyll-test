--- layout: post title: Aplicaciones de las funciones date:
'2018-08-30T21:00:00.001+02:00' author: Pablo Beltrán-Pellicer tags:
modified\_time: '2018-08-30T21:00:35.755+02:00' --- Pero esto de las
funciones, ¿para qué sirve?  
  
Muchos de los fenómenos que se producen en la naturaleza pueden
describirse fielmente gracias a las funciones. Además, es posible
efectuar predicciones y cálculos muy exactos gracias al desarrollo del
análisis diferencial e integral. De esta manera, si tiramos un objeto
con una masa determinada desde cierta altura, podemos conocer el tiempo
que le costará llegar al suelo.  
  
Pero las funciones también resultan de utilidad en campos y disciplinas
de origen plenamente humano. Así, las fórmulas que se emplean en
economía para el cálculo de rendimientos o toda la estadística que se
emplea en cualquier disciplina, se basan en el estudio de las
funciones.  
  

### Electromagnetismo

Comencemos con el electromagnetismo. Sin la comprensión de este fenómeno
y las aplicaciones que han surgido a partir de dicho conocimiento, el
mundo actual sería muy diferente. Nada de radio, televisión ni
ordenadores y, por supuesto, nada de móviles e Internet.  
  
Los fenómenos eléctricos eran conocidos desde muy antiguo. De hecho, los
griegos ya habían observado que al frotar una varilla de ámbar
(élektron), ésta era capaz de atraer pequeños objetos. De igual forma,
se sabía que trozos del mineral denominado magnetita se atraían o
repelían, además de atraer al hierro. En el siglo IX, en China, se
inventa la brújula, mejorando notablemente la orientación en los viajes
marítimos de larga distancia.  
  
En el s. XVIII ya se sabía de la existencia de cargas positivas y
negativas, terminología que introdujo **Benjamin Franklin**, y que las
del mismo signo se repelían y las de distinto se atraían. Sin embargo,
hasta el s. XIX la electricidad y el magnetismo no pasaban de ser meras
curiosidades, si exceptuamos la ya mencionada brújula. En
1820, **Ampère **y **Oersted **mostraron que las corrientes eléctricas,
o cargas en movimiento, producían efectos magnéticos,  estableciendo la
ley de Ampère. Poco después, **Faraday **mostraría el fenómeno
contrario; es decir, que imanes en movimiento dan lugar a corrientes
eléctricas. Electricidad y magnetismo debían estar relacionados.  
  
Y en 1864 llegó uno de los momentos más apasionantes de la ciencia. Todo
ese conocimiento que, por decirlo de alguna manera, estaba flotando en
el ambiente, fue comprendido y condensado por **Maxwell**, formulando
toda una teoría matemática basada en sus famosas cuatro ecuaciones. Ello
constituye uno de los grandes triunfos del análisis, pues estas
ecuaciones además de describir los fenómenos que ya se conocían,
predecían la existencia de las ondas electromagnéticas, de las cuales
podía calcularse hasta su velocidad en función de las características
del medio de propagación. Casualmente, en el vacío, esta velocidad es
igual a la velocidad de la luz, que por entonces ya había sido medida
con bastante precisión por **James Bradley**.  
  
La descripción matemática que proporcionan las ecuaciones de Maxwell se
basa en campos vectoriales, por lo que se trata de una teoría de campos.
Los conceptos clave son los de vector desplazamiento eléctrico y campo
magnético:  
  

-   Desplazamiento eléctrico: $\\vec{D}=\\epsilon\_0\\vec{E}+\\vec{P}$,
    donde $\\vec{E}$ es el campo eléctrico, $\\vec{P}$ la polarización y
    $\\epsilon\_0$ la constante dieléctrica o permitividad del medio.
-   Campo magnético: $\\vec{H}=\\cfrac{\\vec{B}}{\\mu\_0}+\\vec{M}$,
    donde $\\vec{B}$ es el vector inducción magnética, $\\vec{M}$ la
    magnetización y $\\mu\_0$ la permeabilidad del medio.

Al tratarse de campos, la idea que transmiten es que una carga o un
dipolo magnético pasa a modificar las propiedades físicas de la región
del espacio en que se encuentra, de manera que si aparece otra carga o
dipolo, ésta se verá sometida a la acción de dicho campo.

  
En medios lineales e isótropos se simplifican mucho las ecuaciones, ya
que se tiene:  
  
$$\\vec{D}=\\epsilon \\vec{E}$$  
$$\\vec{H}=\\cfrac{\\vec{B}}{\\mu}$$  
Y las famosas ecuaciones de Maxwell son:  

1.  Divergencia de $\\vec{E}$: $\\nabla\\cdot
    \\vec{E}=\\cfrac{\\rho}{\\epsilon}$, con $\\rho$ la densidad de
    carga.
2.  Divergencia de $\\vec{B}$: $\\nabla\\cdot \\vec{B}=0$
3.  Rotacional de $\\vec{E}$: $\\nabla\\times
    \\vec{E}=\\cfrac{-\\partial \\vec{B}}{\\partial t}$
4.  Rotacional de $\\vec{B}$: $\\nabla\\times \\vec{B}=\\mu
    \\vec{J}+\\mu\\epsilon\\cfrac{\\partial \\vec{E}}{\\partial t}$, con
    $\\vec{J}$ la densidad de corriente.

Al aplicar el operador divergencia a un campo vectorial se obtiene un
campo escalar, que se define como el flujo del campo vectorial por
unidad de volumen. En coordenadas cartesianas viene a ser:  
$$\\nabla \\cdot \\vec{F}=\\cfrac{\\partial F\_x}{\\partial
x}+\\cfrac{\\partial F\_y}{\\partial y} +\\cfrac{\\partial
F\_z}{\\partial z}$$.  
Por otro lado, el rotacional de un campo vectorial es un operador
vectorial que va a mostrar la tendencia de cierto campo a inducir una
rotación en un punto. Se calcula:  
  
$$\\nabla \\times \\vec{F} =  \\begin{vmatrix}  
\\hat{x} & \\hat{x} & \\hat{x} \\\\  
\\cfrac{\\partial }{\\partial x} &  \\cfrac{\\partial }{\\partial y} &
\\cfrac{\\partial }{\\partial z \\\\  
F\_x &  F\_y & F\_z  
\\end{vmatrix} $$  
  
Hasta aquí 622 palabras y 3614 caracteres sin espacios  

### Teoría de la relatividad

dddddd  
  
  

### Método de los elementos finitos

Los métodos numéricos de cálculo aproximado han permitido el desarrollo
de importantes aplicaciones en disciplinas como la ingeniería o la
física. Lo que comenzó con  predicciones de órbitas planetarias y la
formulación de la teoría de los errores, ha desembocado en un
auténtico *mare magnum* de herramientas científico-tecnológicas. El
método que describimos a continuación, el de los elementos finitos
(MEF), es tan popular que empresas de diseño industrial hacen uso de él
en su trabajo diario mediante los paquetes de software apropiados.  Esta
técnica permite resolver casos que hasta hace poco eran considerados
como inabarcables con los métodos del análisis tradicional. Así, cuando
se diseñaba una pieza y se quería comprobar su resistencia y
propiedades, se construía un prototipo, al que se le sometía a una
batería de pruebas reales. Si algo iba mal, se reajustaba el diseño y se
volvía a fabricar un prototipo, con el coste que ello implicaba. Y así
sucesivamente, lo que además del coste, aumentaba el tiempo de
desarrollo.  
  
El MEF, en cambio, va a construir  un modelo matemático de cálculo del
sistema real, mucho más sencillo y económico de modificar. Ahora bien,
siempre será un método aproximado y los prototipos seguirán siendo
necesarios o, cuando menos, deseables, al menos de las últimas fases. La
idea general del método es la división de un continuo en un conjunto de
pequeños elementos interconectados por una serie de puntos llamados
nodos. Las ecuaciones que rigen el comportamiento del continuo regirán
también el de cada uno de los elementos. Lo que se ha conseguido, en
términos matemáticos, es pasar de un sistema continuo, con infinitos
grados de libertad, a un sistema con un número finito de grados de
libertad, cuyo comportamiento se modela con un sistema de ecuaciones,
lineales o no,  
  
Economía  
  
El estudio de funciones juega un papel muy importante en economía.
Además, esta importancia ha ido en aumento en las últimas décadas. Así,
además de ser las matemáticas el vehículo mediante el cual se expresan y
comunican ideas económicas, permiten el desarrollo de la economía como
disciplina científica. La creciente actividad de los mercados
financieros, tan tristemente de actualidad hoy en día y, especialmente,
las transacciones de productos derivados, responden a modelos
matemáticos más o menos complejos.  
  
  
  
  
  
  
  
  
  
  
  
  
