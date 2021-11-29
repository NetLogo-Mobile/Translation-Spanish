`forward` es un primitivo de tortuga que hace que la tortuga solicitada se mueva hacia adelante en una parcela recto para una cantidad determinada de unidades. La versión abreviada de esta primitiva es `fd` .



```
ask turtles [
	forward 2
]
ask turtle 0 [
	fd 3.35
]
```





Cosas a tener en cuenta cuando usar `forward`:

* Puedes proporcionar tanto números enteros (p. Ej., 48, -4) como números de punto flotante (p. Ej., 0.05, -6.23, 3.14159).
* Si proporcionas números negativos, la tortuga se moverá hacia atrás en un camino recto.
* Puedes proporcionar una variable en lugar de un número específico, como `ask turtles [ forward speed]`.
- Una tortuga siempre mantendrá su camino recto con la primitiva `forward`.
- Si le pides a una tortuga que avance de una manera que requiera que se mueva más allá del borde del mundo NetLogo, hay dos resultados posibles:
    - Si la envoltura del mundo está activada, que es la configuración predeterminada en los nuevos modelos de NetLogo, su tortuga dejará el mundo en un borde y volverá a ingresar desde el borde opuesto.
    - Si la envoltura del mundo está desactivada (a través del menú Configuración), su tortuga se moverá hasta el borde del mundo y luego se quedará *atascada* allí a menos que cambie su dirección con las primitivas `right` o `left` o usando la primitiva de `set` para cambiar su parámetro de `heading`.



En el ejemplo de modelo a continuación, tenemos una calle representada con parcelas grises y un carro en la calle. Usamos el código de `set heading 90` en nuestro procedimiento de *configuración* para asegurarnos de que nuestro carro se dirija hacia el este. Nuestro modelo tiene 3 botones de avance diferentes: `go-slow`, `go-fast` y `go-back`, cada uno haciendo exactamente lo que sugiere el nombre.

