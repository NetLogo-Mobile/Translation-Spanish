`right` es un primitivo que le dice a una tortuga que gire cierto número de grados (entre 0 y 360) hacia la derecha.



```
ask turtles [
	right 90
]
```


Cosas a tener en cuenta cuando usas `right`:

- La(s) tortuga(s) girará a la izquierda si proporciona un número negativo.
- También puedes proporcionar un número de punto flotante como `right 30.5` `right -185.3` o `right -185.3`.


El siguiente ejemplo de modelo demuestra cómo funcionan las primitivas `right` y su hermana `left`. Tenemos 12 puntos que representan las 12 horas en el reloj y una flecha que representa la hora. Cuando hacemos clic en `spin-right`, nuestra flecha gira a la derecha 1 grado en cada tic hasta que completa el número especificado de grados en el control deslizante.