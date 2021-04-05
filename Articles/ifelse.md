`ifelse` se usa para definir dos conjuntos de reglas que deben seguir las tortugas condicionalmente: un conjunto si una condición proporcionada es *cierto* y otro conjunto si la condición es *falso*. Para hacerlo, usamos el siguiente formato: `ifelse condition (s) [...] [...]`.



```
ask cows [
	ifelse thirst > 10 [
		drink-water
	][
		eat-grass
	]
]
```



Cosas para tener en mente cuando usas `if-else`:

* Puedes combinar dos o más declaraciones condicionales usando las primitivas `and` o `or`.
* Puedes usar la primitiva `not` para hacer que las declaraciones ciertas sean falsas, y viceversa.
* Si necesitas que tus agentes sigan un conjunto de reglas solo si la condición proporcionada es cierta, pero no haga nada de otra manera, debes usar la primitiva `if`.



El ejemplo del modelo tiene algunos carros conduciendo por una carretera y una gasolinera en el medio. Los carros se detienen en la estación de servicio para llenar sus tanques antes de continuar. En cada tic, cada carro verifica si está en la estación de servicio y si su tanque no está lleno (menos de 1) (si la parcela en la que están tiene una coordenada x de 0). Si no está en la gasolinera, sigue moviéndose. Si está en la gasolinera, comienza a llenar su tanque hasta que esté lleno. De lo contrario, empezará a moverse de nuevo. Cada vez que un carro conduce, pierde un poco de gasolina, por lo que cuando regresa a la estación de servicio nuevamente, volverá a llenar su tanque.