`all?` comprueba si todos los agentes de un conjunto de agentes satisfacen una o más condiciones de verdadero o falso. Si todos los agentes satisfacen la condición dada, `all?` en sí mismo informará un valor **`true`**. Si incluso uno de los agentes en el conjunto de agentes dado no cumple la condición, `all?` informará un valor **`falso`**.



Por ejemplo, `all? turtles [ size > 1 ]` reportará **`verdadero`** si y solo si cada tortuga en el modelo fuera más grande que una unidad.




Cosas a tener en cuenta cuando usas `all?`:

* No te olvides del signo de interrogación (`?`) Al final.
* Debes encapsular sus condicionales entre corchetes `[...]`.
* Puedes combinar varias declaraciones condicionales utilizando el primitivo `and`.
* `all?` en sí mismo no hace nada; debes usarlo dentro de una declaración condicional como `if` y `if-else` u otras primitivas que requieren valores verdadero-falso como `while`.


En el modelo ejemplo abajo, hay un rebaño de ovejas. Las ovejas se mueven aleatoriamente y cuando llegan a una parcela verde, comen el pasto en la parcela. Queremos que el modelo deja de trabajar después de que las ovejas ya han comido a lo menos una  vez para que podemos incluir la línea siguiente:



```
if all? turtles [ food-eaten > 0 ][
    stop
]
```
