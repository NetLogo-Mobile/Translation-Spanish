`Pen-down` (abreviado como `pd` ) se usa para rastrear los movimientos de las tortugas. El color de la pluma es el mismo que el color de la tortuga. Mientras que la `pen-down` comienza a rastrear, la `pen-up` (abreviado a `pu` ) deja de rastrear el movimiento de una tortuga. Piense en la `pen-up` y `pen-down` como una pluma en el vientre de una tortuga; `pen-down` baja el bolígrafo al suelo, dejando una marca en su camino, mientras que `pen-up` tira del bolígrafo hacia arriba, sin marcar más el suelo. `Pen-down` y `pen-up` son primitivas que se usan solo con tortugas. Por ejemplo, `ask turtles [ pen-down]` que comiencen a dibujar líneas a partir del movimiento de las tortugas, y `ask turtles [ pen-up]` que ya no sigan el movimiento. (El `Pen-down` , `pen-up` y `pen-erase` son equivalentes a configurar el `pen-mode` la tortuga en `down`, `up` o `erase`)

El siguiente código haría que las tortugas dibujen cuadrados y luego se muevan a una ubicación aleatoria sin dejar rastro:


    ask turtles [
    pen-down
    repeat 4 [ forward 10 right 90 ]
    pen-up
    setxy random-xcor random-ycor
    ]


`Pen-erase` (abreviado como `pe`) borra las líneas dibujadas previamente cuando la tortuga pasa sobre ellas. Piense en ello como un borrador en el vientre de la tortuga.

En el siguiente modelo, un avión está volando. Dependiendo del procedimiento seleccionado, el avión simplemente volará (usando el `pen-up`), volará dejando un rastro (usando el `pen-down`) o volará mientras borra las líneas pasadas (usando `pen-erase`).