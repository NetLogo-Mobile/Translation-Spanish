`repeat` nos permite ejecutar cualquier conjunto de comandos *n* cantidad de veces consecutivas. `repeat` es especialmente útil cuando se dibujan formas geométricas junto con las primitivas de `pen-down` y `pen-up`. Por ejemplo, si quisiéramos que nuestras tortugas dibujaran un cuadrado, escribiríamos el siguiente código:



```
ask turtles [
	pen-down
	repeat 4 [
		right 90
		forward 5
	]
	pen-up
]
```


En el ejemplo de modelo a continuación, tenemos 36 tortugas que se colocan inicialmente en un diseño de círculo cuando se hace clic *en el botón de configuración.*. Cuando hacemos clic en el botón ir, cada tortuga gira a la derecha 1 grado y avanza 0.03 unidades 360 veces. Este simple comportamiento de repetición da como resultado una forma muy interesante.