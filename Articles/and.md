`and` es un primitivo que nos permite combinar dos declaraciones verdadero-falso en una sola declaración que es verdadera *si y solo si* ambas declaraciones son verdaderas.



Por ejemplo, si quisiéramos que una tortuga comiera **solo** si (A) tienen hambre *y* (B) si había comida en el mismo parche, podríamos decir:



```
if my-hunger-level > 100 and food-here > 0 [
  eat-food
  set my-hunger-level 0
]
```

  

<br />

Cosas a tener en cuenta al usar `and`:

- Puede usar más de uno primitivo `and` en el mismo primitivo condicional como `if color = red and size > 3 and xcor < 0 [ ... ]` o `ask turtles with [hunger > 1 and food < 1 and money > 10 ]` .
- `and` mismo no hace nada; debes usarlo dentro de una declaración condicional como `if` y `if-else` u otras primitivas que requieren valores verdadero-falso como `while` .