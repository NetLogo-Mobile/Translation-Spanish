*** Machine Translated
`random` es una primitiva que nos permite agregar aleatoriedad a nuestros modelos. Cuando proporcionamos un número `random` , informará un número aleatorio de 0 a N-1. Imagina que cada vez que ejecutas el primitivo `random N` , estás lanzando un dado con N número de lados. Por ejemplo, si quisiéramos crear un incendio forestal en el que asignamos a cada parche un árbol ( `pcolor = green` ) o un suelo ( `pcolor = brown` ) pero con una densidad de árboles del 70 por ciento, escribiríamos el siguiente código:



```
ask patches [
	ifelse random 100 < 70 [
		set pcolor green
	][
		set pcolor brown
	]
]
```


Cosas a tener en cuenta al usar `random` :

- Recuerde siempre que `random` nos dará números dentro del rango de 0 a N - 1, en lugar de 1 a N. Por ejemplo, si ejecutamos `random 3` , podemos obtener 0, 1 o 2, *pero no 3* .
- Si desea generar un número aleatorio entre un rango personalizado, puede utilizar el siguiente formato: número `minnumber + (random (maxnumber - minnumber))` . Por ejemplo, si quisiéramos generar un número de punto flotante aleatorio entre 4 y 7, podríamos escribir el siguiente código: `4 + random 3` .
- `random` solo genera números enteros positivos. Si necesita generar números de punto flotante, debe usar `random-float` .
- El algoritmo de `random` genera una *distribución uniforme* . Por ejemplo, cada vez que ejecutamos al `random 5` , existe la misma probabilidad de obtener 0, 1, 2, 3 o 4. Si desea generar números aleatorios sobre una *distribución normal* , debe usar `random-normal` .


En el ejemplo de modelo a continuación, tenemos 6 tortugas que representan las 6 caras de un dado. Cada vez que hacemos clic en el botón de **lanzar dados** , cada tortuga elige un número aleatorio entre 1 y 6 (incluido 6) y actualiza su forma en consecuencia.