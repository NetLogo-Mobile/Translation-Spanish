*** Machine Translated
`n-of` se utiliza cuando desea seleccionar aleatoriamente exactamente n elementos de un conjunto de agentes. Su sintaxis es:

`n-of desired-number agentset`

Por ejemplo, imagina que estás intentando elegir equipos de cierto tamaño para un partido de fútbol. Desea que las personas de estos equipos se seleccionen al azar, pero desea asegurarse de que el tamaño de cada equipo sea fijo. En el siguiente modelo, `n-of` para elegir miembros para el equipo rojo de entre los 20 miembros posibles. Luego, `n-of` se usa nuevamente para elegir miembros para el equipo azul entre todos los individuos que aún no se han elegido.