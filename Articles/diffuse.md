*** Machine Translated
`diffuse` es un comando de observador que actúa en cada parche del modelo. Hace que cada uno de ellos difunda (o distribuya) el valor de una variable de parche dada a sus 8 parches [vecinos](/primitives/neighbors) . Por ejemplo, si cada parche tuviera una variable de "calor" que mantuviera un registro de qué tan caliente estaba ese parche, podría llamar (como el observador, es decir, no dentro de un bloque `ask patches` ) `diffuse heat .5` y cada parche se distribuiría por igual la mitad de su calor a los 8 vecinos circundantes (cada vecino obtendría 1/8 del 1/2 del calor original, lo que da como resultado que el calor de cada vecino aumente en 1/16 del calor original). El parche original mantendría al otro 50% del calor original.

Esta primitiva se utiliza cuando desea simular procesos en los que ocurre la difusión, como la transferencia de calor o la difusión en líquidos y en el aire.

Vea el comando relacionado `diffuse4` que hace exactamente lo mismo con los 4 vecinos de dirección cardinal.

En el siguiente ejemplo, `diffuse` se utiliza para modelar la contaminación del aire de las fábricas. Cada tic, cada fábrica tiene un 20% de probabilidad de liberar algún contaminante al aire. `diffuse` se usa luego para modelar cómo ese contaminante se propagaría por el aire, creando zonas y puntos calientes de contaminación.