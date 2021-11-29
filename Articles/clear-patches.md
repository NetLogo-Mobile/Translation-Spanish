`clear-patches` es una primitiva que restablece todas las parcelas a la vez. Hace que los valores de las variables de parcelas personalizadas (definidas con la primitiva `patches-own`) tengan sus valores iniciales predeterminados y hace que todos las parcelas sean negras. También puedes usar su versión abreviada `cp` en tu código.



`clear-patches` solo se usa cuando no queremos usar *clear-all* . Por ejemplo, si quisiéramos borrar las parcelas pero mantener los valores de algunas variables globales y las tortugas existentes iguales, usaríamos `clear-patches`.



En el ejemplo de modelo a continuación, tenemos tres botones. El primero hace que el color de las parcelas sea verde y crea algunas vacas en ubicaciones aleatorias. El segundo botón ejecuta la `clear-patches` para limpiar las parcelas, como un sustituto del césped, pero deja las vacas igual. El tercer botón ejecuta la `clear-turtles` para eliminar las vacas del modelo pero dejar las parcelas/pasto como están.