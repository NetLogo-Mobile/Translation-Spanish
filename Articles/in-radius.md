﻿*** Machine Translated
`in-radius` se utiliza cuando desea seleccionar todos los agentes dentro de un determinado radio del agente actual. Por ejemplo, a una tortuga le gustaría saber cuántas otras tortugas hay dentro de dos unidades de sí misma, o un parche podría querer saber cuántas tortugas hay dentro de tres unidades de sí misma. Puede pensar `in-radius` interno como un filtro que toma un gran conjunto de agentes y filtra a todos esos agentes demasiado lejos, dejando solo aquellos dentro de un radio determinado.

Por ejemplo, supongamos que desea modelar la contaminación del aire. En el siguiente modelo, todos los parches dentro de un cierto radio de una fábrica están contaminados, representados oscureciendo esos parches. Al variar el radio dado, podemos simular diferentes niveles de contaminación.