`sort-on` nos permite clasificar los agentes en un conjunto de agentes en función de un informador, como una característica del agente (p. ej., `size`, `xcor`) o una variable de agente personalizada (p. ej., `age`, `speed`). Su sintaxis es: `sort-on [ variable-or-reporter ] agentset`. Por ejemplo, si quisiéramos crear un modelo de búsqueda y rescate de terremotos en el que los rescatistas revisaran primero los edificios más grandes, escribiríamos el siguiente código:



```
let buildings-sorted sort-on [size] buildings
ask rescuers [
	move-to last buildings-sorted
]
```


Cosas a tener en cuenta cuando usas `sort-on`:

* `sort-on` siempre clasificará en orden ascendente, por lo que si deseas obtener los resultados en orden descendente, puedes pasar la salida al `reverse`, como `reverse sort-on [size] turtles`.
* Aunque usamos una característica de agente simple en el ejemplo anterior, el reportero puede incluir reporteros más avanzados. Por ejemplo, si quisiéramos clasificar las tortugas en función de lo cerca que estaba su coordenada x de 0, podríamos usar `sort on [abs xcor] turtles` que obtendrían el valor absoluto de xcor antes de pasar al algoritmo de clasificación.
* La salida de `sort-on` siempre será una lista recién creada; no modificará en absoluto el conjunto de agentes original.