*** Machine Translated
`scale-color` es una primitiva que informa un tono de un color proporcional al valor de un número dado. Por ejemplo, si quisiéramos crear un modelo de tráfico en el que los carros con tanques más llenos fueran más brillantes que aquellos con tanques más vacíos, escribiríamos el siguiente código:



```
ask cars [
	set color scale-color white tank-level 0 100
]
```


O si quisiéramos modelar un rebaño de ovejas donde más parches de hierba exuberante fueran más brillantes que los que ya se han comido, escribiríamos el siguiente código:



```
ask patches [
	set pcolor scale-color green lushness 0 100
]
```


Cosas a tener en cuenta al usar `scale-color` :

- La sintaxis de `scale-color` puede ser difícil de recordar. Es como sigue `scale-color base_color exact_point lowest_value highest_value` .
- Puede pensar en el valor *base\_color* como el punto medio en el rango proporcionado. Por ejemplo, si `scale-color green 50 0 100` , obtendríamos exactamente verde.
- No olvide que el color base deseado viene primero, luego viene el valor exacto, el `number` es el valor por el que desea escalar (generalmente una tortuga o una variable de parche), y `range1` y `range2` son parámetros para describir los valores mínimo y máximo de `number` . Si `range1` es menor que `range2` , los números más grandes dan como resultado colores más brillantes, pero si `range2` es menor que `range` , los números más grandes dan como resultado colores más oscuros. Si el `number` está fuera del rango, se elige el tono más claro o el más oscuro.
- De forma predeterminada, `scale-color` produce tonos más oscuros para valores más pequeños y tonos más claros para valores más grandes. Sin embargo, es posible revertir esto escribiendo el valor máximo como `range1` y el valor mínimo como `range2` , como `scale-color lushness 50 100 0` `range2` `scale-color lushness 50 100 0` . Estamos haciendo exactamente esto en el ejemplo de modelo a continuación para el nivel de nutrición de cada parche.


En el ejemplo de modelo a continuación, usamos `scale-color` para ajustar el color de cada parche para reflejar su nivel de nutrición (1 es el más bajo, 5 es el más alto). Cada vez que nuestro agricultor se muda a un parche, verifica el nivel de nutrición allí. Si el nivel de nutrición es superior a 3, el agricultor planta una verdura. También damos color a las verduras usando `scale-color` según el nivel de nutrición de su parche. Las verduras que reciben más nutrición tienen un color verde más brillante.