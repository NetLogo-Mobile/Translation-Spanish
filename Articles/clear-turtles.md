`Clear-turtles` es una primitiva que elimina todas las tortugas del modelo a la vez. La versión abreviada de esta primitiva es `ct`.

`clear-turtles` solo se usa cuando no queremos usar *clear-all*. Por ejemplo, si quisieras eliminar las tortugas pero mantener las parcelas iguales y preservar los valores de las variables globales, usaría `clear-turtles`.


En el ejemplo de modelo a continuación, tenemos tres botones. El primero hace que el color de las parcelas sea verde y crea algunas vacas en posiciones aleatorias. El segundo botón simplemente ejecuta la `clear-patches` para borrar las parcelas pero dejar las vacas igual. El tercero botón ejecuta elimina las vacas del modelo pero deja parcelas/pasto como es.