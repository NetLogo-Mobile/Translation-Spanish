*** Machine Translated
`Clear-patches` es una primitiva que restablece todos los parches a la vez. Hace que los valores de las variables de parche personalizadas (definidas con `patches-own` ) tengan sus valores iniciales predeterminados y hace que todos los parches sean negros. La versión abreviada de esta primitiva es `cp` .

`clear-patches` solo se usa cuando no queremos usar *clear-all* . Por ejemplo, si quisiera borrar los parches pero mantener los valores de algunas variables globales y mantener iguales las tortugas existentes, usaría `clear-patches` .

En el ejemplo de modelo a continuación, tenemos dos botones. El primero hace que el color de los parches sea verde y crea algunas vacas en posiciones aleatorias. El segundo botón simplemente ejecuta la `clear-patches` para borrar los parches pero dejar las vacas igual.