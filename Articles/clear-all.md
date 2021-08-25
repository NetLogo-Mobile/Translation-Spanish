*** Machine Translated
`clear-all` esencialmente borra todo en un modelo: *todos los* dibujos, tortugas, parcelas, enlaces, etc. También establece los valores de todas las `globals` y del agente en cero y hace que todos los parches sean negros. Básicamente, vuelve el modelo a una pizarra en blanco. También puede utilizar `ca` como una versión abreviada.

`clear-all` generalmente se encuentra al comienzo del procedimiento de configuración de un modelo para asegurarse de que el modelo comience sin nada allí.

En el ejemplo de modelo a continuación, tenemos dos botones. El primero hace que el color de los parches sea amarillo y pide a las tortugas que dibujen algunas líneas al azar. El segundo botón, simplemente corre el `clear-all` primitiva a todo claro.