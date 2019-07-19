--- 
layout: single 
title: Bibliografía APA en LaTeX date:
'2017-03-06T22:06:00.002+01:00
author: Pablo Beltrán-Pellicer 
categories:
 -
bibliografía - latex  

---

![](/assets/img/2017-03-06-image-0000.jpg)


Hay quien llega al mundo LaTeX porque ha oído acerca de lo que facilita
la gestión de bibliografías. Esto último es cierto. Pero también lo es
que si se quiere algo especial, la cosa puede convertirse en un *pain in
the ass*. Por especial me refiero principalmente a estilos de
bibliografía distintos de los que se usan en áreas
científico-tecnológicas y a diversas personalizaciones en función del
idioma.  
  
Pues bien, me he visto más de una vez en la tesitura de emplear el
estilo APA, uno de los más extendidos (el que más) para ciencias
sociales y humanas. Y lo quería usar en español. Tras diversas
probatinas y tener casi todo listo para que me funcionara con BibTex, en
algún foro se me insinuó que qué narices estaba haciendo empleando
BibTex para tamaño propósito. Que eso ya era cosa del pasado y que
BibLaTeX le daba mil vueltas. Aquí dejo mis conclusiones, que llevan
-todo hay que decirlo- cierto tiempo como borrador.  
  

Manos a la obra. En el preámbulo de nuestro documento pondremos:  
  
  

    \usepackage[babel]{csquotes}
    \usepackage[backend=biber,style=apa]{biblatex}
    \DeclareLanguageMapping{spanish}{spanish-apa}
    \addbibresource{Bibliography.bib}

  
En el documento en sí, incluiremos lo siguiente justo donde queramos que
aparezca la lista de referencias:  
  
  
  

    \printbibliography

  
O si quieres utilizar alguna de sus fabulosas opciones, como por ejemplo
añadir un título a la bibliografía, listar únicamente aquellas
referencias con la palabra clave "spanish" y hacer que aparezca en la
tabla de contenidos, quedaría de la siguiente manera:  
  
  
  

    \printbibliography[title={Referencias},keyword=spanish,heading=bibintoc]

  
Y para citar a lo largo del texto, hay varias opciones. Yo he ido
empleando  
  
  
  

    \textcite{autor2014}
    \textcite[p. 249]{autor2014}
    \parencite{autor2014}
    \citeauthor{autor2014}

Sólo un detalle. Es necesario tener instalado *biber* en el sistema,
cosa fácil tanto en Windows como en Linux, y hacer que nuestro editor lo
ejecute en lugar de BibTex.  
  
Bueno, y sobre todo dar gracias al autor del paquete
[biblatex-apa](https://github.com/plk/biblatex-apa) y a [Paco
Vila](http://tex.stackexchange.com/users/66007/paco-vila) que realizó
las modificaciones correspondientes en el código.  
  
<span style="font-size: x-small;">Créditos:</span>  
<span style="font-size: x-small;">Imagen de portada: By Lin Kristensen
from New Jersey, USA (Timeless Books) \[CC BY 2.0
(http://creativecommons.org/licenses/by/2.0)\], via Wikimedia
Commons</span>  
  
