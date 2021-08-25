*** Machine Translated
Un **informador** es un procedimiento predefinido que devuelve un valor y, a diferencia de un comando, no puede ser un elemento de código independiente. NetLogo tiene algunos reporteros incorporados útiles que no se pueden cambiar directamente, como `ticks` , `pi` , `e` , `world-width` y `world-height` . Por ejemplo, no podemos simplemente escribir `ticks` en el código. Necesitamos usar ticks en algún otro algoritmo como:



```
if ticks > 9 [ 
	wake-up 
]
```


Otras primitivas que usamos para filtrar conjuntos de agentes o manipular listas como `of` , `with` , `sort-on` y `word` son también reporteros.

Muchas propiedades de tortuga, parche y enlace, como el `color` o la `label` se pueden considerar como variables que podemos cambiar con el `set` , así como como reporteros que nos proporcionan los valores de estas variables. Observe en el siguiente ejemplo que los corchetes `[ ]` vienen antes `of` :



```
if xcor < 0 [ 
	if [pycor] of patch-here > 0 [ 
		set label “Quadrant II” 
	] 
]
```


Finalmente, puede crear reporteros personalizados usando la `to-report` para comenzar un procedimiento de reportero y el `report` al final de su procedimiento, justo antes de la palabra clave `end` Los reporteros pueden ser útiles para ordenar su código y evitar que repita líneas de código; Si usa la misma ecuación o una línea larga de código varias veces, se puede usar un procedimiento de `to-report`

Por ejemplo, en lugar de escribir `ask turtles with [ shape = “person” and color = green and size > 5 ]` muchas veces, podríamos definir un procedimiento de reportero de la siguiente manera:



```
to-report big-green-people 
	report turtles with [ shape = “person” and color = green and size > 5 ]
end
```


Una vez que definamos esta variable, podemos reemplazar cada `turtles with [ shape = “person” and color = green and size > 5 ]` en nuestro código con `big-green-people` , como `ask big-green-people [ do-things ]` .

`to-report` se utiliza a menudo para cálculos complejos. Por ejemplo, si quisiéramos calcular el área de los círculos muchas veces en nuestro código, podríamos definir el siguiente reportero:



```
to-report circle-area [ r ]
	report ( pi * ( r  ^ 2 ) )
end
```


Ahora, siempre que queramos calcular el área de un círculo, simplemente podríamos escribir el `circle-area radius` .

En el ejemplo de modelo a continuación, tenemos muchos círculos grandes y pequeños. Estos círculos representan partículas dentro de un recipiente de gas. Cada partícula tiene la misma energía. Sin embargo, cada uno de ellos tiene una velocidad diferente porque la energía cinética de una partícula es igual a su masa multiplicada por el cuadrado de su velocidad dividida por dos ($ E = \ frac 

```
if xcor < 0 [ 
	if [pycor] of patch-here > 0 [ 
		set label “Quadrant II” 
	] 
]
```
 

```
to-report big-green-people 
	report turtles with [ shape = “person” and color = green and size > 5 ]
end
```
 mv ^ 2 $). En lugar de escribir este complicado código para calcular la velocidad de una partícula dentro del `go` , definimos un reportero de *velocidad.* Aunque mantuvimos el código de este ejemplo de modelo deliberadamente simple, definir este reportero haría una gran diferencia si tuviéramos un modelo más complejo en el que necesitáramos calcular la velocidad de una partícula en muchas partes diferentes de nuestro código.