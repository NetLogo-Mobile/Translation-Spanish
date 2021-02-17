*** Machine Translated
`sort-on` permite clasificar los agentes en un conjunto de agentes. Los agentes se ordenan en función de alguna variable de agente elegida por el usuario o un informador arbitrario. Su sintaxis es:

`sort-on [ variable-or-reporter ] agentset`

Por ejemplo, si desea obtener una lista de tortugas ordenadas por su `xcor` , puede usar `sort-on [xcor] turtles` , o si desea obtener una lista de parches ordenados por el valor de su variable de parche `"pollution"` , podría utilizar `sort-on [pollution] patches` .

Tenga en cuenta que, si bien en los ejemplos anteriores el reportero era solo una variable simple entre llaves, puede incluir reporteros más avanzados. Por ejemplo, digamos que queremos ordenar las tortugas en función de lo cerca que `sort on [abs xcor] turtles` que obtendría el valor absoluto de xcor antes de pasar al algoritmo de clasificación.

Tenga en cuenta que la salida de `sort-on` es siempre una lista recién creada; no modifica en absoluto la lista original. También, al igual que `sort` ordena en orden ascendente, por lo que si desea los resultados en orden descendente, puede pasar la salida a la `reverse` .