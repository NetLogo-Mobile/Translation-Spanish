`left` es primitivo que le dice a una tortuga que gire cierto número de grados (entre 0 y 360) hacia la izquierda.



```
ask turtles [
	left 90
]
```


Cosas a tener en cuenta cuando usas `left`:

* La(s) tortuga(s) girará a la derecha si proporciona un número negativo.
* También puedes proporcionar un número de punto flotante como `left 30.5` `left -185.3` o `left -185.3`.


El siguiente ejemplo de modelo demuestra cómo funcionan las primitivas `left` y su hermana `right`. Tenemos 12 puntos que representan las 12 horas en el reloj y una flecha que representa la hora. Cuando hacemos clic en `spin-left`, nuestra flecha gira a la izquierda 1 grado en cada tic hasta que completa el número especificado de grados en el control deslizante.