`Max` informa el valor máximo en una lista determinada. Por ejemplo, `show max [1 2 3]` devolverá 3. `Max` se usa comúnmente en una variable específica de un conjunto de agentes, que se vería así:

`max [variable] of agentset`

Entonces, para colocar la tortuga o tortugas más grandes en un modelo blanco, diríamos:

`ask turtles with max [size] of turtles [ set color white ]`

En el modelo siguiente, hay un grupo de personas que están envejeciendo. Queremos realizar un seguimiento de quién es el mayor, por lo que usamos `max` para cambiar el color de la persona mayor.