`random-normal` es similar al primitivo `random`, en el sentido de que genera e informa un número aleatoriamente. Sin embargo, `random` y `random-normal` difieren en la distribución que generan.

`Random` producirá una **distribución uniforme**, lo que significa que cada número tiene la misma probabilidad de ser generado, y habrá aproximadamente la misma cantidad de cada número. Entonces, en `random 4`, 0, 1, 2 y 3 tienen la misma probabilidad de generarse, y después de muchas repeticiones de `random 4`, habrá un número igual de 0, 1, 2 y 3.

Pero `random-normal` tomará un *valor medio* y un *valor de desviación estándar* para producir una **distribución normal** , que parece una curva de campana con muchos valores en el medio y menos valores en las colas inferior y superior. Su sintaxis es la siguiente: `random-normal mean stdev`.

Las distribuciones normales se encuentran con más frecuencia en la naturaleza que las distribuciones uniformes y pueden agregar precisión a su modelo. Por ejemplo, si quisiéramos crear un modelo de evolución de errores en el que cada error tuviera una antena de diferente tamaño, pero con una distribución normal, escribiríamos el siguiente código:



```
create-bugs 100 [
	set shape "bug"
	set antenna-size random-normal 2.5 0.5
]
```


En el ejemplo de modelo a continuación, somos una población de coloridas mariposas. Cada 50 garrapatas, cada mariposa produce un nuevo bebé. Una mariposa bebé hereda el color de sus padres, pero puede tener un tamaño ligeramente diferente. Logramos esta diferencia de tamaño natural entre los adultos y los niños usando la primitiva `random-normal` Un histograma en la parte inferior muestra el cambio en la distribución de los tamaños de los errores a lo largo del tiempo. Observe cómo obtenemos errores mucho más grandes y mucho más pequeños después de ejecutar el modelo, pero el tamaño promedio de los errores (`mean [size] of turtles`) apenas cambia.