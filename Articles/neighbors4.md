*** Machine Translated
`neighbors4` informa de un agentset que contiene los cuatro parches que rodean el parche actual de un agente en el norte, este, oeste, sur y las instrucciones. Tanto las tortugas como los parches pueden usar este reportero. Por ejemplo, si quisiéramos crear un modelo en el que un incendio se propagara desde un parche a sus vecinos, escribiríamos el siguiente código:



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


Cosas a tener en cuenta al usar `neighbors4` :

- `neighbors4` siempre reportará parches incluso si lo usamos dentro de un contexto `ask turtles` Si desea que un agente vea las tortugas vecinas, puede usar las `turtles-on neighbors4` .
- También hay una `neighbors` que informa de los ocho parches vecinos.
- Tenga en cuenta *la envoltura* del mundo cuando use `neighbors4` como un parche en el borde del mundo informará el parche en el otro extremo del modelo como su vecino. Si desactiva el ajuste del *mundo* , un parche informará dos parches si está en la esquina o tres parches si está en el borde.


En el ejemplo de modelo a continuación, hay un incendio que se propaga en un bosque. Un parche en llamas se extenderá a los parches vecinos en direcciones cardinales que contienen árboles. Si un parche de fuego tiene parches marrones vecinos que indican suelo, se volverán grises para indicar el borde del incendio forestal.