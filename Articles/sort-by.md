*** Machine Translated
`sort-by` te permite ordenar listas o conjuntos de agentes mediante una comparación definida por el usuario. Aunque la `sort-by` funciona tanto en conjuntos de agentes como en listas, para clasificar conjuntos de agentes casi siempre querrás usar la `sort-on` porque es mucho más fácil de usar. `sort-by` se usa mejor en la circunstancia específica de que está ordenando una lista y necesita un control muy específico de cómo se ordenan los elementos de esa lista.

Como ejemplo de cómo usar la `sort-by`, considera el ejemplo de clasificación de una lista de cadenas de acuerdo con su longitud: 

```
to-report smaller-length [a b]
  report length a < length b
end

show sort-by smaller-length ["xyz", "abcd" "12345"]
=> ["xyz" "abcd" "1234"]
```
La sintaxis exacta es `sort-by <reporter> <list>`, por lo que en el ejemplo anterior, más `smaller-length` es el reportero. Para que un reportero sea usado por `sort-by`, debe (1) tomar dos entradas y (2) informar cierto o falso. Dadas dos entradas `A` y `B`, si el informador informa cierto, entonces `A` se coloca antes de `B` , y si informa falso, `B` se coloca antes de `A` O, dicho de manera más intuitiva, trabajando de izquierda a derecha en la lista de salida ordenada, el reportero será cierto para cada par de números. Es decir, en la lista `["xyz" "abcd" "1234"]`, longitud "xyz" < longitud "abcd", longitud "abcd" < "1234".

Tenga en cuenta que la salida para `sort-by` es siempre una lista, incluso si la entrada es un conjunto de agentes. Al clasificar conjuntos de agentes, los vínculos se rompen al azar. Sin embargo, al ordenar listas, la ordenación es "estable", lo que significa que si dos elementos "iguales" están en un cierto orden en la lista de entrada, permanecerán en ese orden en la lista ordenada.