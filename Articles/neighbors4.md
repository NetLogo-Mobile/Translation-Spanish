`neighbors4` informa un agentset que contiene los cuatro parches que rodean el parche actual de un agente en el norte, este, oeste, sur y las instrucciones. Tanto las tortugas como los parches pueden usar este reportero. Por ejemplo, si quisiéramos crear un modelo en el que un incendio se propagara desde una parcela a sus vecinos, escribiríamos el siguiente código:



```
ask patches [
	if pcolor = red [
		ask neighbors4 [
			if pcolor = green [
				set pcolor red
			]
		]
	]
]
```


Cosas a tener en cuenta cuando usas `neighbors4`:

* `neighbors4` siempre reportará parcelas incluso si lo usamos dentro de un contexto `ask turtles` Si deseas que un agente vea las tortugas vecinas, puedes usar las `turtles-on neighbors4`.
* También hay una `neighbors` que informa de las ocho parcelas vecinas.
* Tenga en cuenta *la envoltura* del mundo cuando usas `neighbors4` como una parcela en el borde del mundo informará la parcela en el otro extremo del modelo como su vecino. Si desactiva el ajuste del *mundo*, una parcela informará dos parcelas si está en la esquina o tres parcelas si está en el borde.


En el ejemplo de modelo a continuación, hay un incendio que se propaga en un bosque. Una parcela en llamas se extenderá a las parcelas vecinas en direcciones cardinales que contienen árboles. Si una parcela de fuego tiene parcelas marrones vecinos que indican suelo, se volverán grises para indicar el borde del incendio forestal.