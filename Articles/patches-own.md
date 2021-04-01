`Patches-own` define variables que pertenecen exclusivamente a las parcelas de un modelo. (Vea su contraparte `turtles-own` de las tortugas para definir las variables de las tortugas.) Las variables son usualmente un rasgo o característica de las parcelas; por ejemplo, si sus parcelas representan suelo en su modelo, puedes usar `patches-own [ nutrients ]`. Tiene la forma:

```patches-own [ variable1 variable2 ... ] ```

y puede incluir varias variables, siempre que estén entre corchetes. Como las variables globales y otras variables del agente, debe definirse en la parte superior de su código, antes de cualquier definición de procedimiento. **Nota**: una tortuga que se encuentre en esa parcela también puede acceder a las variables de parcela.

En el siguiente modelo, estamos modelando un jardín con flores. Las flores crecerán dependiendo de la cantidad de nutrientes que tenga su parcela de suelo, por lo que creamos una variable de parcelas llamadas `nutrients` usando `patches-own`.