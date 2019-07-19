--- 
layout: single 
title: Plantilla LaTeX para exámenes (clase exam) 
author: Pablo Beltrán-Pellicer 

categories:
 - latex 
---

![](/assets/img/2017-12-26-image-0000.png)

Vale. LaTeX es algo que se ama o se odia. Decidí incluirlo en los contenidos del curso [Matemáticas y las TIC](https://www.gitbook.com/book/catedu/matematicas-y-las-tic/details) porque creo que, por lo menos, hay que conocerlo. Por lo menos, para escribir expresiones matemáticas. Porque... algo tendrá cuando el mismo Word permita (de aquellas maneras) introducir las ecuaciones en sintaxis de LaTeX e, incluso, plataformas como Edmodo lo tienen habilitado para este fin. Personalmente, a mí lo que realmente me atrae de LaTeX, es su calidad tipográfica.  
  
El caso es que he preparado una plantilla LaTeX, a partir de la clase de documento *exam*, que puede ser una forma suave de introducirse en LaTeX. Además de suave, útil, porque en menos de 5 minutos te ves diseñando tus exámenes, con sus soluciones, puntuaciones, etc. Una plantilla «pro».      A la plantilla podemos acceder directamente desde ShareLaTeX, una plataforma online donde podemos compilar directamente los documentos LaTeX en un entorno, además, colaborativo: [enlace a la plantilla](https://es.sharelatex.com/project/59e28be7b1ea802c6058f481).  
  
Para los que gusten de usar un editor y compilador offline, se pueden descargar el archivo [aquí](https://drive.google.com/file/d/1dKM8oTkQJUATStNKC8X0Bfn1-G57vSe-/view?usp=sharing) o echar un vistazo al documento principal:  
 
``` 

    \documentclass[addpoints,spanish, 12pt,a4paper]{exam}
    % Hasta donde pone \begin{document} es lo que se conoce como preámbulo (preamble)

    %% Esto es de la clase exam. Si dejamos sin comentar \printanswers, se mostraran las soluciones. 
    %% Si la comentamos y dejamos sin comentar \noprintanswers, pues no se muestran las soluciones.
    \printanswers
    %\noprintanswers

    %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
    % Idioma y codificación de texto
    \PassOptionsToPackage{T1}{fontenc} 
    \usepackage{fontenc} 
    \usepackage[utf8]{inputenc}
    % Cargar babel y configurar para español
    \usepackage[spanish,es-lcroman, es-tabla, es-noshorthands]{babel}
    %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

    %%%%%%% Paquetes varios y alguna opción
    \usepackage{graphicx} % Paquete necesario para incluir imágenes, cambiarles el tamaño, etc.
    \usepackage{enumitem} % Para poder configurar las listas
    \everymath{\displaystyle} % Esto es para que las expresiones se vean... grandes, que resulta diferente de si las queremos entre líneas.

    %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
    %%%% Cosas a configurar de la clase EXAM %%%%

    \author{Pablo Beltrán-Pellicer}
    \pagestyle{headandfoot}
    \runningheadrule
    \extraheadheight{3cm}
    \firstpageheader{}
                    {\hspace*{-2cm}\includegraphics[height=1.6cm]{img/\string"logoDGA\string".jpg}\hspace*{10cm}\includegraphics[height=1.6cm]{img/\string"logocatedu\string".png}\\ 
                    IES CATEDU, Aragón\\
                    Examen de Matemáticas - Tema 2 - Polinomios\\15 de octubre, 2017
                    }
                    {}

    \runningheader{Matemáticas}
    {Examen del tema 2}
    {15 de octubre, 2017}
    \firstpagefooter{}{{ "{{" }}\tiny IES CATEDU, Aragón}}{}
    \runningfooter{}{{ "{{" }}\tiny  IES CATEDU, Aragón}}{Página \thepage\ de \numpages}
    \pointpoints{punto}{puntos}
    \bonuspointpoints{punto extra}{puntos extra}
    \hqword{Pregunta}
    \hpword{Puntos}
    \hsword{Calificación}
    \renewcommand{\solutiontitle}{\noindent\textbf{Solución:}\par\noindent}
    \pointformat{(\emph{\thepoints})}
    \bonuspointformat{(\emph{\thepoints})}
    \pointsinrightmargin % Para poner las puntuaciones a la derecha. Se puede cambiar. Si se comenta, sale a la izquierda.
    \extrawidth{-2.4cm} %Un poquito más de margen por si ponemos textos largos.
    \marginpointname{ \emph{\points}}
    %\bracketedpoints

    %%%%%%%%%%%%%%%%%%%%%% FIN DEL PREÁMBULO %%%%%%%%%%%%%%%%%%%%%

    \begin{document}
    \vspace{0.1in} %espacio vertical
    \makebox[\textwidth]{Nombre:\enspace\hrulefill}

    %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
    % Tabla para anotar la calificación
    %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

    \begin{center}
        %\resizebox{\textwidth}{!}{\gradetable[h][questions]} % Esto es por si la tabla sale muy grande, para ajustarla al ancho
        \gradetable[h][questions]
    \end{center}
    \vspace{0.1in} % Espacio vertical


    \begin{questions} % Comenzamos con las preguntas del examen
    % Entre corchetes se pone la puntuación de cada una

        %Pregunta con apartados
        \question Calcula:
            \begin{parts}
                \part[1] $2+2=$
                \part[2] $\frac{1}{2}+\frac{3}{4}=$ 
            \end{parts}
        \begin{solution} % Aquí ponemos la solución, es opcional.
            \begin{parts}
                \part $4$
                \part $\frac{5}{4}$ 
            \end{parts}
        \end{solution}
        
        \question[1 \half] Una pregunta sin apartados.
        \question[1] Otra pregunta.
        \question[1 \half] Otra pregunta más.
        \question[3] Una pregunta más complicada.

    \end{questions}

    \end{document}
```

   El siguiente paso es mantener una base de datos de preguntas de examen y tomarlas directamente de ahí. Ya escribí cómo hacerlo en su día con [probsoln](http://www.tierradenumeros.com/2014/10/mantener-una-base-de-datos-de-preguntas.html), y en breve dejaré por aquí un ejemplo de plantilla para combinar la potencia de la clase *exam* con *probsoln*.
