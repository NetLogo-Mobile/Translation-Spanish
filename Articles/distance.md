*** Machine Translated
`distance` es una primitiva de tortuga y parche que informa la distancia más corta entre el agente actual y otro agente proporcionado. Por ejemplo, el siguiente código haría que las tortugas que están lo suficientemente cerca del parche central (0,0) avancen un paso, pero si su distancia al parche central (0,0) es de 5 unidades o más, no lo harían. moverse.



```
ask turtles [
	if distance (patch 0 0) < 5 [ forward 1 ]
]
```


Cosas a tener en cuenta al usar la `distance` :

- Solo podemos proporcionar un agente específico a la `distance` primitiva. Por ejemplo, si tuviéramos una `breed` tortuga llamada *árboles* , el siguiente código mostraría un error incluso si solo hay un árbol en nuestro modelo: `distance trees` . Este error se muestra porque los `trees` siempre informarán sobre un conjunto de agentes. En una situación en la que sepa que solo habrá un agente en el modelo, puede usar el `one-of` primitivo: `distance one-of trees` .
- Si necesitamos conocer la distancia de un agente a una determinada ubicación, no a otro agente, podemos usar la `distancexy` x.


En el ejemplo de modelo a continuación, usamos la `distance` para implementar un comportamiento rudimentario de búsqueda de ruta para un leñador. El leñador tiene un árbol "objetivo" al que intentará acercarse y talar. Una vez que talen ese árbol, fijarán sus ojos en el árbol más cercano. Usamos la `distance` para obtener la distancia entre el leñador y todos los árboles para que podamos averiguar qué árbol está más cerca. En el caso de los empates, elegimos uno de los árboles más cercanos al azar.