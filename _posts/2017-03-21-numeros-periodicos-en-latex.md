--- 
layout: single 
title: Números periódicos en LaTeX 
author: Pablo Beltrán-Pellicer 
categories:
 - latex 
---




Mira que es una cosa tonta, y mira que LaTeX tiene comandos en los
paquetes estándar para dar rienda suelta a nuestra creatividad
tipográfica. Pues resulta que escribir números periódicos no es algo tan
directo en LaTeX. Más que nada, porque la [notación
anglosajona](https://en.wikipedia.org/wiki/Repeating_decimal) utiliza
normalmente una barra recta o puntitos sobre los números del período. Y
claro, los que utilizamos el arco de toda la vida (de toda la vida, para
nosotros, claro), nos las tenemos que apañar de alguna manera.  

  ![](/assets/img/2017-03-21-image-0000.png)
  
Lo más fácil y directo es utilizar el paquete *yhmath*, así que, en el
preámbulo, lo cargamos:  
  
  

    \usepackage{yhmath}

  
Y luego, ya en el documento, lo usamos a discreción:  
  
  

    4,\wideparen{9}

De esta forma, obtenemos algo del siguiente estilo:  
  

![](/assets/img/2017-03-21-image-0001.png)


  
El problema está en que en algunos editores de fórmulas online, no se
permite cargar paquetes adicionales. Por ejemplo, en
[CodeCogs](https://www.codecogs.com/latex/eqneditor.php) podemos
utilizar *\\overarc* (del paquete *arcs*), en sustitución de
*\\wideparen*, pero queda un poco menos bonito. De hecho, les he escrito
a ver si lo incorporan:  
  

![](/assets/img/2017-03-21-image-0002.png)


  
  

Por cierto, para representar el 4,99... no hace falta ningún símbolo
raro. Podemos escribir, sencillamente, 5 ;)  
  
Bueno, y si alguien sabe de alguna otra forma para escribir los números
periódicos en LaTeX, ¡para eso están los comentarios!  
-----  
Parece que la gente se anima a escribir comentarios y han dejado esta
forma de escribir el período:  

    4,\widehat{89}

La ventaja es que está admitida, por ejemplo, en el editor online de
[CodeCogs](https://www.codecogs.com/latex/eqneditor.php). Ahora bien,
proporciona un arco un pelín puntiagudo:  

[![](/assets/img/2017-03-21-image-0003.png)](/assets/img/2017-03-21-image-0003.png)

  
*<span class="underline">Créditos</span>*  
Esto ha sido un poco de investigación profunda en internet, pero la
mayor parte se puede encontrar en
[tex.stackexchange](http://tex.stackexchange.com/questions/15468/frown-and-mathop-stackrel-overset).
