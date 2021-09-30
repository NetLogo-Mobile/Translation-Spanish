`and` es un primitivo que nos permite combinar dos declaraciones verdadero-falso en una sola declaración que es verdadera *si y solo si* ambas declaraciones son verdaderas.



Por ejemplo, si quisiéramos que una tortuga comiera **solo** si (A) tienen hambre *y* (B) si había comida en el mismo parche, podríamos decir:



```
if my-hunger-level > 100 and food-here > 0 [
  eat-food
  set my-hunger-level 0
]
```

  

Cosas a tener en cuenta cuando usas `and`:

* Puedes usar más de uno primitivo `and` en el mismo primitivo condicional como `if color = red and size > 3 and xcor < 0 [ ... ]` o `ask turtles with [hunger > 1 and food < 1 and money > 10 ]`.
* `and` mismo no hace nada; debes usarlo dentro de una declaración condicional como `if` y `if-else` u otras primitivas que requieren valores verdadero-falso como `while`.



En el modelo ejemplo abajo, usamos `and` para generar un río por el medio de nuestro mundo. Una parcela se convierte en azul *si y solo si* las coordenada x es *both* a la izquierda de `(width / 2)` *and* a la derecha de `- (width / 2)`, si no, sigue siendo una parcela verde.