--- 
layout: single 
title: Mantener una base de datos de preguntas en LaTeX con probsoln 
author: Pablo Beltrán-Pellicer 
categories:
 - latex 
 
excerpt: ""
	header:
  overlay_image: /assets/img/2014-10-29-image-0000.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: ""
toc: true
toc_sticky: true

---

Tranquilos que no hace falta ser un experto en bases de datos, ya que el soporte que se utilizará para dicha recopilación de preguntas de examen, ejercicios o problemas, será un **simple fichero de texto**.  

![](/assets/img/2014-10-29-image-0000.jpg)
  
Hay varios paquetes LaTeX que pueden emplearse al respecto:
- [exercise](http://www.ctan.org/pkg/exercise),
- [answers](http://www.ctan.org/pkg/answers),
- [exsheets](http://www.ctan.org/pkg/exsheets) y
- [probsoln](http://www.ctan.org/pkg/probsoln). 

Cada uno tiene sus puntos fuertes y sus puntos débiles y, seguramente, cualquiera de ellos cubrirá las necesidades de un profesor. Sírvase el avezado lector de indagar en los enlaces anteriores. Pero había que decantarse por uno en particular, por lo que me he quedado con **probsoln**, en un compromiso de sencillez y funcionalidad. En este artículo voy a mostrar qué uso le doy, que no es el único.  
  

## ¿Qué puedo hacer con probsoln?

La idea es tener una base de datos independiente de preguntas de examen, ejercicios o problemas, en simples ficheros de texto .tex (sin preámbulo ni nada, sólo los problemas con sus soluciones). Posteriormente, esos ficheros se cargan en los proyectos LaTeX que desees, como apuntes, examenes, fichas de refuerzo, etc. Se puede elegir cargar aleatoriamente una serie de ejercicios, o indicar específicamente cuáles quieres incluir. Además, se puede mostrar la solución junto con cada problema o generar una hoja de soluciones aparte.

## ¿Qué pinta tienen los ficheros de ejercicios?

Pues básicamente son una ristra de entornos defproblem, cada uno con su etiqueta diferenciadora.  
  
```
    \begin{defproblem}{etiqueta}
    %Aquí se pone el enunciado, con los comandos de LaTeX que quieras.
      \begin{onlysolution}
       \begin{solution}
        %Aquí se pone la solución, con los comandos de LaTeX que quieras.
       \end{solution}
      \end{onlysolution}
    \end{defproblem}
```

## ¿Cómo se usa probsoln?

Basta con poner lo siguiente en el preámbulo:

  
```
    \usepackage[option]{probsoln} 
```
  
Option puede ser: *answers* y *noanswers*. Como su propio nombre indica, con answers se mostrarán las soluciones, y con noanswers, no. Hay otras opciones, pero son más para depurar o para usos más avanzados. En la [documentación](http://osl.ugr.es/CTAN/macros/latex/contrib/probsoln/probsoln.pdf) lo explican muy bien.  

## Trucos y consejos

### Cambiar el rótulo *Solution* por el que queramos

```
    \renewcommand{\solutionname}{Solución}
```

### Formatear la forma en que aparece la solución

Lo que viene a continuación es un ejemplo en el que se indica que se quiere que la solución se escriba con letra de tamaño footnotesize en un párrafo al margen (sí, empleo una plantilla con márgenes amplios). Como mi solución daba errores, lo pregunté en [tex.stackexchange](http://tex.stackexchange.com/questions/209461/probsoln-customization-of-solution-environment-set-as-marginpar). Un ejemplo mínimo sería este:  
  
```
    \documentclass{article}
    \usepackage{lipsum}
    \usepackage{environ} 
    \usepackage{probsoln}
    \showanswers
    %Definición del problema de ejemplo. Esto se hace normalmente desde un archivo aparte.
    \begin{defproblem}{problem1}
    \begin{onlysolution}
    \begin{solution}
    The answer is 42
    \end{solution}
    \end{onlysolution}
    We want to know the answer to The Ultimate Question of Life, the Universe, and     Everything 

    \lipsum[1]
    \end{defproblem}

    %%Esto es lo importante. Ponemos la solución al margen.
    \NewEnviron{solutionnew}{{ "{%" }}
      \leavevmode\marginpar{\raggedright\footnotesize My solution name:\\ \BODY}}{}
    \renewenvironment{solution}{\solutionnew}{\endsolutionnew}


    \begin{document}
    \useproblem{problem1}
    \end{document}
```
  
Y este es el resultado:  

![](/assets/img/2014-10-29-image-0001.jpg)

  

## Créditos

Imagen:

https://www.flickr.com/photos/reway2007/
  
  
