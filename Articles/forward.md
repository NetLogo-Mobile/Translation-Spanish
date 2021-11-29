`forward` es un primitivo de tortuga que hace que la tortuga solicitada se mueva hacia adelante en una parcela recta para un número determinado de unidades. La versión abreviada de esta primitiva es `fd`.



```
ask turtles [
	forward 2
]
ask turtle 0 [
	fd 3.35
]
```





Cosas para tener en cuenta cuando usas `forward`:

* Puedes proporcionar dos números enteros (como 48, -4) y números de punto flotante (0.05, -6.23, 3.14159).
* Si proporcionas un número negativo, la tortuga se moverá hacia atrás en un camino recto.
* Puedes proporcionar un variable en vez de un número específico como `ask turtles [ forward speed]`.
* Una tortuga siempre va a mantener su camino recto con la primitiva `forward`.
* Si le pides a una tortuga que avance de una manera que requiera que se mueva más allá del borde del mundo NetLogo, hay dos posibles resultados:
 * Si la envoltura del mundo está activada, lo que es la configuración predeterminada en los nuevos modelos de NetLogo, tu tortuga dejará el mundo en un borde y lo entraría desde el borde opuesto.
 * Si la envoltura del mundo está desactivada (a través del menú Configuración), tu tortuga se moverá hasta el borde del mundo y luego se *atascará* allí a menos que cambie su dirección con las primitivas `right` o `left` o usando la primitiva `set` para cambiar su parámetro `header`.



En el ejemplo de modelos siguiente, tenemos una calle representado con parcelas grises y un carro en la calle. Usamos el código `set heading 90` un nuestro procedimiento *preparar* para asegurar que nuestro carro está moviendo hacia el este. Nuestro modelo itene 3 diferente botones para ejecutar: `go-slow`, `go-fast`, y `go-back`, cada uno haciendo exactamento lo que el nombre sugiere.

