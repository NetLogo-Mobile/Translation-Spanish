`other` informa un conjunto de agentes que es el mismo que el conjunto de agentes de entrada pero omite el agente que solicita. En otras palabras, se excluye del conjunto de agentes resultante. Por ejemplo:



```
show count turtles-here
=> 10
show count other turtles-here
=> 9  
```


muestra cómo un agente, la tortuga original que llamó al comando, se excluye del conjunto de agentes, lo que da como resultado el recuento final de "9". `other` suele ser útil cuando queremos que nuestros agentes interactúen con otros agentes. Por ejemplo,

```ask turtles [ if any? turtles-here [ ```

```                             set color red ] ] ```

 haría que todas las tortugas sean rojas porque `turtles-here` informa la tortuga original también. Siempre hay al menos 1 tortuga cuando usamos `turtles-here` . Sin embargo, si escribimos

```ask turtles [if any? other turtles-here [ ```

```                             set color red ] ] ```

 sólo las tortugas que tienen otra tortuga en la misma parcela se pondrían rojas.