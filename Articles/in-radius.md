*** Machine Translated
"in-radius" es una primitiva que informa sobre todos los agentes dentro de un cierto radio del agente actual. Por ejemplo, a una tortuga le gustaría saber cuántas otras tortugas hay dentro de un radio de dos unidades de sí misma o a una parcela le gustaría saber cuántas tortugas hay dentro de tres unidades de sí misma.



```
ask turtles [
	if any? other turtles in-radius 2 [
		create-link-with one-of other turtles in-radius 2
	]
]
```



Cosas a tener en mente cuando usas `in-radius`:

* También puedes usar valores de punto flotantes para el parámetro de radio, como `in-radius 3.65`.
* Tanto *tortugas* como *parches* pueden usar `in-radius`.
* Tenga en cuenta que `in-radius` también puede informar sobre la tortuga original, si está usando las mismas razas. Asegúrese de tener en cuenta eso en sus modelos mediante el uso de la primitiva `otro` como se muestra en el ejemplo anterior.
* Puedes usar `in-radius` y la primitiva `with` para reducir los agentes de destino, pero asegúrete de encapsular la primera declaración `with` dentro de las paréntesis `( )`. Por ejemplo, puedes escribir un código como `if any? (carrots with [color = orange]) in-radius 2 [ eat ]`.



En el ejemplo de modelo a continuación, tenemos un entorno representado con parcelas verdes y una fábrica en el centro. Cuando se hace clic en el botón ir, la fábrica contamina todas las parcelas dentro de un radio de 5, representados por parcelas de color verde más oscuro.