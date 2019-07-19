--- layout: post title: Temas (archivos de preferencias) descargables
para Geogebra date: '2017-09-27T23:20:00.002+02:00' author: Pablo
Beltrán-Pellicer tags: - geogebra - TIC en el aula modified\_time:
'2017-09-27T23:20:27.814+02:00' thumbnail:
https://2.bp.blogspot.com/-SGeY45COi-k/WNWSmfjZY6I/AAAAAAAACk0/LGLaY-FngDoAdxwQTliYztViQnG60MibACLcB/s72-c/estandar.png
--- [Geogebra](https://www.geogebra.org/) no dispone, por el momento, de
una opción que nos permita ir cambiando fácilmente de *tema*,
entendiendo por tema los patrones por defecto (los colores de puntos,
rectas y demás objetos) . Únicamente se puede crear una configuración
alternativa a la que viene de fábrica. Y no es lo mismo hacer una
construcción para verla en el ordenador o en la tablet, que para usarla
en las clases, que para imprimirla. Así que voy a dejar aquí los
archivos de configuración que me he ido preparando. Llamémosles temas,
skins, patrones por defecto o como queramos.  

### ¿Cómo instalo estos temas?

El caso es que, cuando modificamos esos patrones por defecto se guarda
en el archivo *defaults.xml*; y cuando cambiamos las preferencias (como
el color de los ejes y cosas así), se modifica el archivo *prefs.xml*.  
  
En Linux los encontraremos en la ruta:  
  
  
  
Y en Windows, estos archivos los podemos encontrar en el directorio:  
*C:\\Users\\&lt;Mi nombre de usuario&gt;\\AppData\\Roaming\\GeoGebra
5.0\\prefs\\*  
  
Para instalar los temas en Geogebra 5.0 basta con sobreescribir
*defaults.xml* y *prefs.xml* con unos nuevos. Cuidado, antes de lanzarte
a la piscina, es buena idea hacer una copia de seguridad de estos
archivos. Estos cambios únicamente se aplicarán a construcciones nuevas.
Si abrimos una que ya teníamos hecha o descargada, se abrirá con sus
colores originales.  
Un aviso. Si modificamos las preferencias y luego le damos a guardar,
nos machacará los que ya teníamos. Eso significa que alguna de las
configuraciones se pierdan. Por ejemplo, en todos los temas que he
preparado se ve por defecto el rótulo (*caption*) de cada objeto con la
tipografía de LaTeX. Eso se perderá, ya que, para ello, he tenido que
incluir el tag *caption*, que no está contemplado en los patrones por
defecto:  
  
*&lt;caption val="$ \\scalebox{1.5} {{ "{%" }}n} $"/&gt;*  
*&lt;labelMode val="8"/&gt;*  
  

### Para descargar

Por defecto, vienen con los ejes y la cuadrícula activados. Además de
los colorines y los tamaños de los objetos, en todos los temas he
elegido grados (entre 0 y 180) para los ángulos. Recuerdo que, en
principio, los ficheros sirven para Geogebra 5.0 (no he probado en otras
versiones):  
  
  

[<img src="https://2.bp.blogspot.com/-SGeY45COi-k/WNWSmfjZY6I/AAAAAAAACk0/LGLaY-FngDoAdxwQTliYztViQnG60MibACLcB/s200/estandar.png" width="200" height="175" />](https://2.bp.blogspot.com/-SGeY45COi-k/WNWSmfjZY6I/AAAAAAAACk0/LGLaY-FngDoAdxwQTliYztViQnG60MibACLcB/s1600/estandar.png)

**Tema estándar de Geogebra**. Todo muy blanco y con las letras y
objetos muy pequeños. Aunque en el ordenador se ve bien, no me gusta
para la pizarra de clase porque no se ven apenas los rótulos de los
objetos. Tampoco me gusta que los ángulos aparezcan por defecto entre 0º
y 360º, prefiero entre 0º y 180º.  
  
  
  
  
  
  
  
  

### Si quiero cambiar de tema una construcción ya hecha

Si abrimos una construcción que se hizo con un tema diferente, la
solución que he encontrado (y que no es perfecta) consiste en:  
1- Seleccionar todos los objetos de la construcción (Ctrl-A)  
2- Entrar en Opciones-&gt;Avanzado-&gt;Patrones -por defecto.  
3- Seleccionamos todos los patrones. Es decir, pinchamos el de más
arriba, luego mantenemos presionada la tecla MAYUS y pinchamos en el de
más abajo.  
4- Aplicar a los objetos elegidos.  
  
Lo que no cambia es:  
- Color de fondo.  
- Color y grosor de los ejes y cuadrícula.  
- El tipo de rótulo (caption). Se pone el de por defecto.  

### Comparte tus temas

Si alguien ha creado una combinación especialmente atractiva de colores
para Geogebra y quiere compartirla, puede dejar un comentario en este
post :)
