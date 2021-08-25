*** Machine Translated
Los parches son un tipo especial de agentes estacionarios en NetLogo que conforman el mundo de un modelo. Puede pensar en los parches como los cuadrados que forman un tablero de ajedrez.

La `patch` informa del parche específico con las coordenadas dadas. Por ejemplo, si quisiéramos crear un modelo de una colonia de hormigas cuya entrada fuera el parche en el centro, podríamos escribir el siguiente código:



```
ask patch 0 0 [
	set pcolor green
]
```


La `patches` informa sobre todos los parches del modelo. Esta primitiva es útil para pedir a todos los parches que hagan lo mismo (por ejemplo, cambiar pcolor) o reducir un subconjunto de parches. Por ejemplo, si quisiéramos crear un modelo de incendio forestal con algunos parches verdes que representan árboles, algunos parches verdes que representan el suelo y los parches más a la izquierda que representan el fuego (rojo), escribiríamos el siguiente código:



```
ask patches [
	set pcolor one-of [green brown]
]
ask patches with [pxcor = min-pxcor][
	set pcolor red
]
```


Cosas a tener en cuenta al usar `patch` y `patches` :

- Los `patches` primitivos siempre informarán del mismo conjunto de agentes, pero el orden de los parches será aleatorio cada vez que lo usemos.
- Como las tortugas, los parches también tienen características. Algunas de las características vienen preconstruidas (por ejemplo, `pcolor` , `pxcor` , `pycor` , `plabel` ), pero también podemos definir características personalizadas con la `patches-own` los parches, como `patches own [minerals water]` .
- No podemos crear razas de parches personalizados.


En el ejemplo de modelo a continuación, tenemos una granja que está rodeada por una cerca. La cerca se representa con manchas marrones y el prado con manchas verdes o lima. También tenemos un cuadrado amarillo en el medio que representa un rancho y algunas vacas que se mueven al azar y comen la hierba en cada parcela hasta que no queda hierba.