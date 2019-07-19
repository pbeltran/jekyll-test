--- layout: post title: Ajuste de la sonda inductiva con autolevel
(Marlin 1.1.8) date: '2018-01-05T00:46:00.001+01:00' author: Pablo
Beltrán-Pellicer tags: - impresión en 3D modified\_time:
'2018-01-05T00:46:16.479+01:00' thumbnail:
https://1.bp.blogspot.com/-eOwLdJlzMEg/WQWmtZJNs\_I/AAAAAAAADA4/SvKTe1H7SqUz5VOxG0XsYh\_eYGqY32jmACKgB/s72-c/IMG\_20170430\_103115.jpg
---
[<img src="https://1.bp.blogspot.com/-eOwLdJlzMEg/WQWmtZJNs_I/AAAAAAAADA4/SvKTe1H7SqUz5VOxG0XsYh_eYGqY32jmACKgB/s320/IMG_20170430_103115.jpg" width="320" height="240" />](https://1.bp.blogspot.com/-eOwLdJlzMEg/WQWmtZJNs_I/AAAAAAAADA4/SvKTe1H7SqUz5VOxG0XsYh_eYGqY32jmACKgB/s1600/IMG_20170430_103115.jpg)  
Marlin 1.1.8 software para Arduino, junto con una placa RAMPS 1.4.  
  
  
  
  

#### Para ajustar el eje Z.

Lo que pongo a continuación es para una sonda de tipo inductivo que se
dispara por cercanía al metal de la cama caliente (si es de aluminio, si
no lo es, hay que ponerle cinta metálica en los puntos de calibración).
Básicamente, con este calibrado tenemos que indicarle a la impresora a
qué distancia está la punta del nozzle del umbral de detección de la
sonda. Consiste en modificar la siguiente constante del Marlin, y parea
empezar pondremos un valor conservador, cercano a 0, lo que significaría
que está al mismo nivel que la sonda.  
  
*\#define Z\_PROBE\_OFFSET\_FROM\_EXTRUDER -0.75*  
  
M851 Z-0.36  
G28  
G1 Z0  
  
  
M500 para salvar  
  

#### Calibración fina del termistor del fusor (PID auto-tuning)

Antes del auto-tuning, observemos el rizado que presenta la señal de la
temperatura del fusor (en rojo). 

  

  

  

[<img src="https://3.bp.blogspot.com/-vN8PG_DwTwA/Wk67pELJeVI/AAAAAAAAEzo/kJPCCahf6JsrXF0adLQqr9cmpq0hCa9dwCLcBGAs/s320/antes_pid_autotune%2B2.png" width="320" height="289" />](https://3.bp.blogspot.com/-vN8PG_DwTwA/Wk67pELJeVI/AAAAAAAAEzo/kJPCCahf6JsrXF0adLQqr9cmpq0hCa9dwCLcBGAs/s1600/antes_pid_autotune%2B2.png)

  

Realizamos el procedimiento de auto-tuning. En la figura se ven los
ciclos en la parte de la derecha. 

  

[<img src="https://4.bp.blogspot.com/-axrpL1oM25o/Wk67qEbBZkI/AAAAAAAAEzs/B1ACP4LCjoQ0Olf5wYf9Awk30ZxO2_KagCLcBGAs/s320/autotune.png" width="320" height="293" />](https://4.bp.blogspot.com/-axrpL1oM25o/Wk67qEbBZkI/AAAAAAAAEzs/B1ACP4LCjoQ0Olf5wYf9Awk30ZxO2_KagCLcBGAs/s1600/autotune.png)

  

  

Y, finalmente, ya con el PID bien calculado, vemos cómo la gráfica
muestra una señal mucho más estable. 

  

[<img src="https://2.bp.blogspot.com/-f5o4wtUG2Ww/Wk67vHu8jqI/AAAAAAAAEz0/D3E75Wcm7kAdKOPtvPREt9NlIIuE-rkeQCLcBGAs/s320/con_autotune2.png" width="320" height="291" />](https://2.bp.blogspot.com/-f5o4wtUG2Ww/Wk67vHu8jqI/AAAAAAAAEz0/D3E75Wcm7kAdKOPtvPREt9NlIIuE-rkeQCLcBGAs/s1600/con_autotune2.png)

  
Thermistor aliexress <span
style="background-color: white; font-family: &quot;arial&quot; , &quot;helvetica&quot; , sans-serif; font-size: 12px;">100
K NTC B 3950</span>  
<span style="background-color: white; font-size: 12px;"><span
style="font-family: &quot;arial&quot; , &quot;helvetica&quot; , sans-serif;">https://es.aliexpress.com/item/ALL-matal-Jhead-J-head-Hotend-for-1-75mm-3-0mm-E3D-Bowden-Extruder-0-2mm/32222078934.html?spm=a2g0s.9042311.0.0.wJmomC</span></span>  
Si quieres calibrar el fusor  
 M303 C8 E0 S210 U1  

#### Calibrado de los ejes

  
M503 //devuelve los valores actuales  
M92 E880.5 // ajusta el extrusor  
M92 X79.87 //ajusta los pasos del X  
  
M500 para salvar //si queremos cancelar en lugar de salvar, M502 nos
devolvería a los que están guardados  
  
  
  
<span style="background-color: white; font-size: 12px;"><span
style="font-family: &quot;arial&quot; , &quot;helvetica&quot; , sans-serif;">  
</span></span><span
style="background-color: white; font-size: 12px;"><span
style="font-family: &quot;arial&quot; , &quot;helvetica&quot; , sans-serif;">  
</span></span>  

### Nivelado de la cama caliente

Necesitamos una hoja de papel. Se hace desde la cama.  
  
  
Incluir en el start gcode: M420 S1 para habilitar el bed level  
  
  
  
  
Para ajustarlo, podemos realizar los siguientes pasos hasta que esté a
la altura deseada:  
  
  
  
Paso 1: Acercar la sonda a la cama caliente hasta  que se ilumine su
led  
  
*G92 Z10 //con esto le decimos que está a 10mm de la cama, para poder
mover el eje Z hacia abajo con pronterface.*  
  
*M114*  
  

[![](https://2.bp.blogspot.com/-5mm_FRigFZI/WNFkocq3h5I/AAAAAAAACi4/0th1Iibin9EpBhdty0CjCVRdnjC-CuzjACLcB/s1600/m114a.png)](https://2.bp.blogspot.com/-5mm_FRigFZI/WNFkocq3h5I/AAAAAAAACi4/0th1Iibin9EpBhdty0CjCVRdnjC-CuzjACLcB/s1600/m114a.png)

  
Ahora vamos bajando el eje Z en pasos de 0,1mm desde pronterface, hasta
que una hoja de papel pase con un pelín de resistencia entre la punta
del nozzle y la cama.  
  

[![](https://2.bp.blogspot.com/-JJ90ZHzXGP4/WNFlKtrFFgI/AAAAAAAACjA/-UOho0Z0ALU3PeNOO7li4VuaV82r2qoQwCLcB/s1600/m114b.png)](https://2.bp.blogspot.com/-JJ90ZHzXGP4/WNFlKtrFFgI/AAAAAAAACjA/-UOho0Z0ALU3PeNOO7li4VuaV82r2qoQwCLcB/s1600/m114b.png)

  
La diferencia de los dos valores, en este caso 10,00-9,60=0,4, es lo que
tenemos que poner en el define del marlin, <span class="underline">en
negativo</span>.  
  

SI NO LO PONES EN NEGATIVO, EL NOZZLE PEGARÁ EN LA CAMA

  

[<img src="https://3.bp.blogspot.com/-xauAuO5g0lQ/WQWnaqV9tdI/AAAAAAAADBI/P7ue2V2tP_EpDwASxVDg-36BM8kvn4gLQCKgB/s200/IMG_20170430_103124-01.jpeg" width="200" height="171" />](https://3.bp.blogspot.com/-xauAuO5g0lQ/WQWnaqV9tdI/AAAAAAAADBI/P7ue2V2tP_EpDwASxVDg-36BM8kvn4gLQCKgB/s1600/IMG_20170430_103124-01.jpeg)

  
  

  

*<span class="underline">Créditos</span>*

En el fondo, y en la superficie también, es parte del procedimiento que
hacen aquí:

<http://www.print3dforum.com/showthread.php/488-HOW-TO-Set-up-your-Auto-Levelling-Bed>
