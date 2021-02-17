*** Machine Translated
Un **informador** es algo que devuelve un valor y, a diferencia de un comando, no puede ser un elemento de código independiente. NetLogo tiene algunos reporteros integrados útiles que no se pueden cambiar directamente, como `ticks` , `pi` , `e` , `world-width` y `world-height` . Por ejemplo, no podemos simplemente escribir `ticks` en el código. Necesitamos usar ticks en algún otro algoritmo como: `if ticks > 9 [ wake-up ]` o `let world-area (world-width * world-height)` .

Otras primitivas que usamos para filtrar conjuntos de agentes o manipular listas como `of` , `with` , `sort-on` y `word` son reporteros.

Muchas propiedades de tortuga, parche y enlace, como el `color` o la `label` se pueden considerar como variables que podemos cambiar con el `set` , así como como reporteros que nos proporcionan los valores de estas variables. Observe en el siguiente ejemplo que los corchetes `[ ]` que vienen antes 

```
if xcor < 0 [ 
If [pycor] of patch-here > 0 [ 
set label “Quadrant II” ] 
]
```
 Finalmente, puede crear reporteros personalizados usando la `to-report` para comenzar un procedimiento de reportero y el `report` al final de su procedimiento, justo antes de la palabra clave `end` Los reporteros pueden ser útiles para ordenar su código y evitar que repita líneas de código; si usa la misma ecuación o una línea larga de código varias veces, se puede usar un procedimiento de `to-report`

Por ejemplo, si escribe `ask turtles with [ shape = “person” and color = green and size > 5 ]` muchas veces, podría agregar un procedimiento de reportero como 

```
to-report big-green-people 
report turtles with [ shape = “person” and color = green and size > 5 ]
end
```
 y luego reemplace cada `turtles with [ shape = “person” and color = green and size > 5 ]` para personas `big-green-people` en su código, como `ask big-green-people [ do-things ]` . Una vez que haya calculado el valor que le gustaría devolver del procedimiento, agregue el `report` primitivo delante del valor.

`to-report` se utiliza a menudo para los cálculos. Por ejemplo, si desea calcular el área de los círculos muchas veces en su código, puede escribir 

```
To-report circle-area [ r ]
Report ( pi * ( r  ^ 2 ) )
end
```
 Ahora, siempre que desee calcular el área de un círculo, simplemente escriba `circle-area [ radius ]` .