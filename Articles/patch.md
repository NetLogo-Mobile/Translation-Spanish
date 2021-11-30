Las parcelas son un tipo especial de agentes estacionarios en NetLogo que conforman el mundo de un modelo. Puedes pensar en las parcelas como los cuadrados que forman un tablero de ajedrez.

La `patch` informa de la parcela específica con las coordenadas dadas. Por ejemplo, si quisiéramos crear un modelo de una colonia de hormigas cuya entrada fuera la parcela en el centro, podríamos escribir el siguiente código:



```
ask patch 0 0 [
	set pcolor green
]
```


La `patches` informa sobre todos las parcelas del modelo. Esta primitiva es útil para pedir a todos las parcelas que hagan lo mismo (por ejemplo, cambiar pcolor) o reducir un subconjunto de parcelas. Por ejemplo, si quisiéramos crear un modelo de incendio forestal con algunos parcelas verdes que representan árboles, algunas parcelas verdes que representan el suelo y las parcelas más a la izquierda que representan el fuego (rojo), escribiríamos el siguiente código:



```
ask patches [
	set pcolor one-of [green brown]
]
ask patches with [pxcor = min-pxcor][
	set pcolor red
]
```


Cosas a tener en cuenta cuando usamos `patch` y `patches`:

* Los `patches` primitivos siempre informarán del mismo conjunto de agentes, pero el orden de las parcelas será aleatorio cada vez que lo usemos.
* Como las tortugas, las parcelas también tienen características. Algunas de las características vienen preconstruidas (por ejemplo, `pcolor`, `pxcor`, `pycor`, `plabel`), pero también podemos definir características personalizadas con la `patches-own` las parcelas, como `patches own [minerals water]`.
* No podemos crear razas de parcelas personalizadas.


En el ejemplo de modelo a continuación, tenemos una granja que está rodeada por una cerca. La cerca se representa con manchas marrones y el prado con manchas verdes o lima. También tenemos un cuadrado amarillo en el medio que representa un rancho y algunas vacas que se mueven al azar y comen el pasto en cada parcela hasta que no queda pasto.