`patches-own` es una palabra clave especial de NetLogo que nos permite definir características que pertenecen exclusivamente a las parcelas en un modelo. Estas características son variables que tienen un valor único para cada parcela individual. `patches-own` es útil para modelar variables ambientales. Por ejemplo, si quisiéramos crear un modelo de contaminación donde una fábrica contaminaría los parches inmediatamente cercanos a ellos:



```
patches-own [pollution]
create-turtles 1 [
	set shape "factory"
	ask patches in-radius 3 [
		set pollution 100
	]
]
```


Cosas a tener en cuenta cuando usas `patches-own`:

* Podemos definir tantas variables como queramos dentro de los `patches-own`, como `patches-own [water nutrients heavy-metals altitude]` separando cada variable con un espacio.
* Una tortuga puede acceder directamente a una característica de su parcela actual. Por ejemplo, `ask turtles [set pollution 100]` hace lo mismo que `ask turtles [ ask patch-here [set pollution 100] ]`.


En el ejemplo de modelo a continuación, estamos modelando un jardín con flores. Definimos una *característica de nutrientes* para nuestras parcelas y asignamos a cada parcela un número aleatorio de nutrientes entre 0 y 10. También cambiamos el `pcolor` cada parcela de acuerdo con su nivel de nutrientes para que una parcela más oscura indique niveles de nutrientes más altos. Finalmente, hacemos brotar una flor en cada parcela. Inicialmente, cada flor tiene el mismo tamaño, pero cuando se hace clic en el botón Ir, cada flor crece de acuerdo con el nivel de nutrición de su parcela.