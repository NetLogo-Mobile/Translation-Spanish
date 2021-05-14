*** Machine Translated
`Clear-patches` es una primitiva que restablece todos las parcelas a la vez. Hace que los valores de las variables de parcela personalizadas (definidas con `patches-own`) tengan sus valores iniciales predeterminados y hace que todos las parcelas sean negros. La versión abreviada de esta primitiva es `cp` .

`clear-patches` solo se usa cuando no queremos usar *clear-all* . Por ejemplo, si quisieras borrar las parcelas pero mantener los valores de algunas variables globales y mantener iguales las tortugas existentes, usarías `clear-patches`.

En el ejemplo de modelo a continuación, tenemos tres botones. El primero hace que el color de las parcelas sea verde y crea algunas vacas en posiciones aleatorias. El segundo botón simplemente ejecuta la `clear-patches` para borrar las parcelas pero dejar las vacas igual. El tercero ejecuta la `clear-turtles` priimitiva para eliminar las vacas del modelo pero deja parcelas/pasto como es.