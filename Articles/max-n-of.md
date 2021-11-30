`max-n-of` informa un conjunto de agentes que contiene un número específico de agentes con el valor más alto de un informador determinado. Por ejemplo, si quisiéramos crear un modelo en el que las 5 tortugas más grandes se dividan por la mitad, escribiríamos el siguiente código: 

```
ask max-n-of 5 turtles [size] [
	set size (size / 2)
	hatch 1
]
```


Cosas a tener en cuenta cuando usas `max-n-of`:

* También hay una primitiva `min-n-of` que informa de un conjunto de agentes que contiene un número específico de agentes con el valor más bajo de un informador determinado.
* Si hay menos del número especificado de tortugas en un conjunto de agentes dado, `max-n-of` informará el conjunto de agentes completo. Por ejemplo, si solo tenemos 2 tortugas en un modelo, un `max-n-of 5 turtles [ size ]` reportaría las 2 tortugas.
* Cuando las tortugas se clasifican según sus características, los lazos se rompen al azar.


En el ejemplo de modelo a continuación, tenemos algunas personas que representan una economía absurdamente simple. En cada tic, una tortuga elegida al azar ejecuta un intercambio eligiendo otra tortuga al azar y dándole a esa tortuga 5 de su dinero. Este intercambio se representa con un vínculo temporal entre las dos tortugas. Usamos `max-n-of` para cambiar el color de las tres tortugas más ricas a azul. También usamos `min-n-of` para cambiar el color de las 3 tortugas más pobres a rojo.