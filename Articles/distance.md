`distance` es una primitiva de tortuga y parcela que informa la distancia más corta entre el agente actual y otro agente proporcionado. Por ejemplo, el siguiente código haría que las tortugas que están lo suficientemente cerca de la parcela central (0,0) avancen un paso, pero si su distancia al centro es de 5 o más, no se moverán.

```
ask turtles [
	if distance patch 0 0 < 5 [ forward 1 ]
]
```

En el ejemplo de modelo a continuación, usamos `distance` para implementar un comportamiento rudimentario de búsqueda de ruta para un leñador. El leñador tiene un árbol "objetivo" al que intentará acercarse y talar. Una vez que talan ese árbol, fijarán sus ojos en el árbol más cercano. Usamos `distance` para obtener la distancia entre el leñador y todos los árboles para que podamos averiguar qué árbol está más cerca. En el caso de los empates, elegimos uno de los árboles más cercanos al azar.
