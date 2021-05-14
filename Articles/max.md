*** Machine Translated
`max` informa el valor máximo en una lista determinada. Por ejemplo, `show max [14 -2 7]` reportaría 14. `max` se usa comúnmente para encontrar un agente específico dentro de un conjunto de agentes. Por ejemplo, si quisiéramos crear un modelo de división celular y tener la celda más grande para dividir por la mitad en cada tic, escribiríamos el siguiente código:



```
ask cells [
	if size = max [size] of cells [
		set size (size / 2)
		hatch 1
	]
]
```


En el ejemplo de modelo a continuación, tenemos algunas personas que representan una economía absurdamente simple. En cada tic, una tortuga elegida al azar ejecuta un intercambio al elegir otra tortuga al azar y darle a esa tortuga 5 de su dinero. Este intercambio se representa con un vínculo temporal entre las dos tortugas. Usamos `max` para cambiar el color de la tortuga más rica a azul. También usamos `min` para cambiar el color de la tortuga más pobre a rojo.