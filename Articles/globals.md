*** Machine Translated
`globals` mantiene la información que debería ser común a todo el modelo. Las variables globales siempre se declaran en la parte superior de su código, y su sintaxis es:

`globals [ variable-name ]`

De la misma manera que se puede acceder al valor de un control deslizante en cualquier parte del código NetLogo, cualquier parte de su código puede establecer (usando el comando `set`) y leer (escribiendo el nombre del global) el valor de un global. Este hecho hace que los globales sean útiles para definir constantes de todo el modelo que no desea que el usuario pueda cambiar desde un control deslizante. También los hace útiles para realizar un seguimiento de la información variable de todo el modelo que cualquier agente puede modificar, por ejemplo, el volumen total acumulado de transacciones en un modelo económico o la cantidad de veces que un depredador atrapó a su presa en un modelo ecológico.

En este ejemplo, se usa un valor global para realizar un seguimiento de una variable de todo el modelo, el total de parches de hierba que comieron las 20 ovejas del modelo. En el `setup`, lo configuramos en 0, y luego en el `go`, cada vez que una oveja come un parche de pasto, lo incrementamos en uno estableciendo su valor en el valor que solía ser más uno, es decir, `set total-food-eaten total-food-eaten + 1`.