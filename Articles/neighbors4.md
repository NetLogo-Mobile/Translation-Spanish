*** Machine Translated
`neighbors` se utiliza para informar un conjunto de agentes que contiene los ocho parches circundantes del agente en las direcciones norte, noreste, este, sureste, este, suroeste, oeste y noroeste. Tanto las tortugas como los parches pueden usar este reportero. Por ejemplo, para poner en rojo los parches vecinos de la tortuga 1, diríamos:

`ask turtle 1 [`

`ask neighbors [ set pcolor red ] ]`

`neighbors4` se utiliza para informar de un agentset que contiene sólo las cuatro muestras cercanas en el norte, este, sur, oeste y direcciones (también llamados puntos cardinales). Tanto las tortugas como los parches pueden usar este reportero. Por ejemplo, para cambiar a amarillo solo los parches directamente arriba, abajo, a la derecha y a la izquierda de la tortuga 1, diríamos:

`ask turtle 1 [`

`ask neighbors4 [ set pcolor yellow ] ]`

En el siguiente modelo, hay un incendio que se propaga en un bosque. Un parche en llamas se extenderá a los parches vecinos que contienen árboles. Dependiendo de si el interruptor está en `neighbors` o `neighbors4` , el fuego se extenderá a todos los árboles vecinos o solo a los árboles en las direcciones cardinales, respectivamente.