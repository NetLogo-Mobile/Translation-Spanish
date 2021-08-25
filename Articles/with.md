*** Machine Translated
`with` es una primitiva informadora que nos permite extraer un sub-conjunto de agentes de un conjunto de agentes en función de un conjunto proporcionado de declaraciones condicionales. Una condición dentro de una instrucción `with` es similar a una instrucción `if` . Por ejemplo, si quisiéramos modelar un ecosistema de depredador-presa donde un halcón solo pudiera ver ratones de colores más brillantes, pero no los de colores más oscuros, escribiríamos el siguiente código:



```
ask hawks [
	if any? (mice-here with [color = gray and distance myself < 2]) [
		hunt
	]
]
```


Observe que primero escribimos el nombre del conjunto de agentes ( `mice-here` ), luego usamos el primitivo `with` y luego proporcionamos nuestras declaraciones condicionales entre corchetes ( `[ ]` ).

Cosas a tener en cuenta al usar `with` :

- Podemos usar `with` para todo tipo de tipos de agentes ( `turtles` , `patches` y `links` ).
- También puede hacer algunas operaciones sencillas dentro de un reportero que viene antes `with` como `customers with [(checking-account + savings-account) > 1000]` para obtener una agentset que contiene sólo los clientes cuyo saldo total de la cuenta es mayor que 1000 o `circles with [size / 2 > 1]` para obtener un conjunto de agentes que contenga solo los círculos con un radio mayor que 1.


En el ejemplo de modelo a continuación, tenemos tres carreteras paralelas y cada calle tiene un carro . En el procedimiento de ir, usamos `with` para diferenciar entre las velocidades de los carros azules y los carros rojos. Los carros azules van dos veces más rápido que los carros rojos cuando tienen suficiente gasolina. Cuando un carro no tiene suficiente gasolina, va mucho más lento. Por último, usamos `with` para detener el modelo cuando todos los carros quedan sin gasolina.