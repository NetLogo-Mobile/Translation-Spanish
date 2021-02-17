*** Machine Translated
`one-of` se utiliza para seleccionar aleatoriamente solo un agente de un conjunto de agentes o una lista. Toma la forma de:

`one-of <agentset/list>`

Por ejemplo, `ask one-of patches [ set pcolor red ]` hará que un parche aleatorio se vuelva rojo. `One-of` también puede seleccionar aleatoriamente un elemento de una lista proporcionada. Por ejemplo, para cambiar el color de cada tortuga al azar a rojo, amarillo o azul, podríamos decir:

`ask turtles [set color one-of [ red yellow blue ] ]`

**Nota** : Si `one-of` en un conjunto de agentes que no tiene agentes (por ejemplo, `ask turtles with [color = red]` pero no hay tortugas rojas), se producirá un error. No vea a `nobody` para saber cómo evitar el error.

En el siguiente modelo, se está propagando una enfermedad. Comienza con una persona infectada, que se elige al azar. Para elegir a una persona para que comience la propagación de la enfermedad, usamos `one-of` para elegir una tortuga al azar.