`pen-up` (versión corta `pu`) se usa para dejar de rastrear los movimientos de las tortugas. El color del bolígrafo es el mismo que el color de la tortuga. Mientras que la `pen-up` deja de rastrear, la `pen-down` (versión corta de `pd`) comienza a rastrear el movimiento de una tortuga.

Piensa en la `pen-up` y `pen-down` como una pluma en el vientre de una tortuga; `pen-down` baja el bolígrafo al suelo, dejando una marca en su camino, mientras que `pen-up` tira del bolígrafo hacia arriba, sin marcar más el suelo. `Pen-down` y `pen-up` son primitivas que se usan solo con tortugas. Por ejemplo, si quisiéramos que nuestras tortugas dibujaran un cuadrado, escribiríamos el siguiente código:



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


En el siguiente modelo, un avión vuela entre dos destinos míticos: Atlantis y Valhalla. Mientras vuela, deja un rastro detrás de él si el interruptor `draw-path?` está encendido. Cada vez que un avión llega a un destino y gira, también cambia su color, lo que lleva a un nuevo color de ruta. Si el interruptor `draw-path?`  está apagado, nuestro avión toma su bolígrafo y deja de dibujar. También usamos la `clear-drawing` claro para borrar todos los trazados dibujados anteriormente cuando el `draw-path?` el interruptor está apagado. Tenga en cuenta que `clear-drawing` es una primitiva solo para el observador, por lo que lo usamos fuera de la declaración `ask turtles`.