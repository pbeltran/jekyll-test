--- 
layout: single 
title: Insertando ecuaciones LaTeX en MS Word 
author: Pablo Beltrán-Pellicer 

categories:
 
- latex 
- TIC en el aula 
- recursos 
---

![](/assets/img/2017-09-17-image-0000.jpg)

De lo que se entera uno. Ya se pueden escribir [ecuaciones en la sintaxis de LaTeX en documentos de MS Word](https://blogs.msdn.microsoft.com/murrays/2017/07/30/latex-math-in-office/). Para Powerpoint hay una triquiñuela, pero no he conseguido hacerla funcionar con el paquete de idioma español, ya le dedicaremos una entrada diferente.   Vamos a centrarnos ahora en lo que funciona desde la versión 1707 (Build 8326.2058) y posteriores, o sea desde verano de 2017 aproximadamente. Y esto es una novedad, a la que tampoco se le ha dado mucha publicidad, pero para la que existía una potencial comunidad de usuarios que la esperaban como agua de mayo. Facilita enormemente, por ejemplo, el copy-paste de fórmulas de otros sitios. Además, la sintaxis de LaTeX puede parecer extraña al principio, pero es bastante más eficaz para escribir ecuaciones y fórmulas que el seleccionado manual con el ratón a través de múltiples menús.    

### Cómo funciona 

1- Insertar ecuación y seleccionar modo {}LaTeX  
  

![](assets/img/2017-09-17-image-0001.jpg)

  
2- En el cuadro de la ecuación, escribir (o pegar) en sintaxis LaTeX la expresión que deseemos. Por ejemplo: 

```
\frac{a+b}{c+d}  
```

![](assets/img/2017-09-17-image-0002.jpg)

3- Para ir alternando habrá que darle a "Convertir". Si convertimos a "Profesional", veremos el resultado:  

![](assets/img/2017-09-17-image-0003.jpg)

4- Mientras que si convertimos a "Lineal", volveremos a ver la expresión LaTeX que hay detrás de ese renderizado, pudiendo modificarla de nuevo.  

### Cosas interesantes

Si copiamos una fórmula de estas y pegamos en otra aplicación (editor de LaTeX o un simple notepad), lo que aparecerá será la expresión LaTeX. Maravilloso. Aunque sería todavía mejor si Word permitiese entrar en el modo ecuación tecleando \$\$ o \\\[. Todo llegará, supongo. Y otra cosa que tampoco está habilitada en el editor de ecuaciones en modo LaTeX es el empleo de tags como \\begin o \\end. Dejo aquí una pequeña demo disponible en la web oficial:  
     

### Para saber más 

Aquí se explica lo de Powerpoint, por ejemplo, pero ya he mencionado que no parece funcionar de momento con el paquete de idioma español):

[https://blogs.msdn.microsoft.com/murrays/2017/07/30/latex-math-in-office/](https://blogs.msdn.microsoft.com/murrays/2017/07/30/latex-math-in-office/)

  
  
  
