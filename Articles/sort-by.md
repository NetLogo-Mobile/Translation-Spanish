*** Machine Translated
`sort-by` nos permite ordenar listas o conjuntos de agentes mediante una comparación definida por el usuario. `sort-by` se utiliza mejor en la circunstancia específica de que está ordenando una lista y necesita un control muy específico de cómo se ordenan los elementos de esa lista. Como ejemplo de cómo utilizar la `sort-by` , considere el ejemplo de clasificación de una lista de cadenas de acuerdo con su longitud:



```
to-report smaller-length [a b]
  report (length a) < (length b)
end

show sort-by smaller-length ["xyz", "abcd" "12345"]
=> ["xyz" "abcd" "1234"]
```


La sintaxis exacta es `sort-by <reporter> <list>` , por lo que en el ejemplo anterior, de `smaller-length` es el reportero. Para que un reportero sea utilizado por `sort-by` , debe (1) tomar dos entradas y (2) informar verdadero o falso. Dadas dos entradas `A` y `B` , si el informador informa verdadero, entonces `A` se coloca antes de `B` , y si informa falso, `B` se coloca antes de `A` O, dicho de manera más intuitiva, trabajando de izquierda a derecha en la lista de salida ordenada, el reportero será verdadero para cada par de números. Es decir, en la lista `["xyz" "abcd" "1234"]` , longitud "xyz" &lt;longitud "abcd", longitud "abcd" &lt;"1234".

Cosas a tener en cuenta al usar la `sort-by` :

- `sort-by` siempre se clasificará en orden ascendente, por lo que si desea obtener los resultados en orden descendente, puede pasar la salida a la `reverse` , como `reverse sort-by [size] smaller-length ["xyz", "abcd" "12345"]` .
- La salida para `sort-by` es siempre una lista, incluso si la entrada es un conjunto de agentes. Al clasificar conjuntos de agentes, los vínculos se rompen al azar. Sin embargo, al ordenar listas, la ordenación es "estable", lo que significa que si dos elementos "iguales" están en un cierto orden en la lista de entrada, permanecerán en ese orden en la lista ordenada.
- Aunque la `sort-by` funciona tanto en conjuntos de agentes como en listas, casi siempre querrá utilizar la `sort-on` porque es mucho más fácil de usar para ordenar conjuntos de agentes.