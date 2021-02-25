`all?` comprueba si todos los agentes de un conjunto de agentes satisfacen una o más condiciones de verdadero o falso. Si todos los agentes satisfacen la condición dada, `all?` en sí mismo informará un valor `true` Si incluso uno de los agentes en el conjunto de agentes dado no cumple la condición, `all?` informará un valor **falso**.

Por ejemplo, `all? turtles [ size > 1 ]` reportarían **verdadero** si y solo si cada tortuga en el modelo fuera más grande que una unidad.

¿Cosas a tener en cuenta al usar `all?`:

- No te olvides del signo de interrogación (`?`) Al final.
- Debe encapsular sus condicionales entre corchetes `[...]` .
- Puedes combinar varias declaraciones condicionales utilizando el primitivo `and`.
- `all?` en sí mismo no hace nada; debe usarlo dentro de una declaración condicional como `if` y `if-else` u otras primitivas que requieren valores verdadero-falso como `while` .