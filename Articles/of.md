﻿`of` es una primitiva que te permite acceder a un agente y extraer el valor de alguna variable que posee. Normalmente, se accede a las variables del agente (como `color`, `size`, `shape`, así como las variables definidas con los `<agent>-own`) dentro de un contexto de agente, es decir, dentro de un `ask turtles [...]` o `ask patches [...]` bloque. `of` le permitirá llegar a esas variables fuera de dicho bloque, o obtener todos los valores para cada agente en un conjunto de agentes de una sola vez.

`of` se usa con un reportero dentro de un `[]` bloque, como:

```[reporter] of agent` or `[reporter] of agentset ```

 Por ejemplo, si quisiéramos obtener el `pcolor` de la parcela en el centro del mundo, diríamos `[pcolor] of patch 0 0` , porque `pcolor` es el nombre de la variable que queremos obtener y el `patch 0 0` es el agente del que queremos obtener la variable. Si quisiéramos obtener los `size` de cada tortuga, escribiríamos `[size] of turtles` y obtendríamos una lista del tamaño de cada tortuga.

Nota: sus reporteros pueden ser más elaborados que simplemente obtener el valor de una variable. Puedes tratar el código dentro del bloque reporter como lo haría con cualquier otro código en Netlogo y escribir expresiones completas dentro de él. Por ejemplo, di que cada tortuga tiene un diámetro almacenado en una `diameter` y deseas obtener una lista del radio de cada tortuga. Una forma sencilla de hacerlo sería escribir `[diameter / 2] of turtles`.