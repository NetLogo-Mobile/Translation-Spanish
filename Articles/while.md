*** Machine Translated
`while` comienza a repetir un conjunto de reglas provisto (como `ask` ) indefinidamente siempre que un reportero dado informe verdadero. Si el reportero informes **falsos,** `while` se detiene la repetición de las reglas previstas. Por ejemplo, si quisiéramos crear un modelo de mercado inmobiliario donde cada comprador continuara buscando una casa hasta encontrar una lo suficientemente barata, escribiríamos el siguiente código:



```
ask turtles [
	let found-home? false
	while [not found-home?] [
		move-to one-of patches with [residents = 0]
		if [price] of patch-here < my-budget [
			set found-home? true
		]
	]
]
```


En el ejemplo de modelo a continuación, tenemos muchas tortugas colocadas en un diseño de cuadrícula. Cada tortuga es morada o verde y cada una está feliz o triste dependiendo de la cantidad de tortugas a su alrededor. Si una tortuga tiene más de 2 vecinas con un color diferente, usamos el `while` primitivo para hacer que cada tortuga se mueva alrededor de la cuadrícula hasta que encuentren un lugar que las haga felices.