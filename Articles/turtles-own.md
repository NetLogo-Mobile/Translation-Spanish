*** Machine Translated
`Turtles-own` define variables que pertenecen a todas las tortugas en un modelo. Las variables suelen ser un rasgo o aspecto específico de la tortuga, como ¿ *tiene hambre?* o *energía* . Su sintaxis es:

`turtles-own [ variable1 variable2 ... ]`

Como las variables globales y otras variables del agente, debe definirse en la parte superior de su código, antes de cualquier definición de procedimiento. Puede definir una variable o varias, pero todas deben estar entre corchetes.

Si ha definido varias razas de tortugas, `turtles-own` aplicará la variable a todas las razas. Sin embargo, puede definir una variable para una raza específica usando `<breed>-own` , donde<breed> es el nombre de tu raza. Por ejemplo, si ya ha definido una raza de tortugas por <code>breed [birds bird]</code> , puede crear una variable solo para pájaros utilizando <code>birds-own [wing-size]</code> .</breed>

En el siguiente modelo, los carros circulan con una cierta cantidad de gasolina en sus tanques. Usamos `turtles-own` para definir la variable `gas` , que representa cuánta gasolina tiene un coche. Luego, usamos la variable `gas` para determinar si un automóvil puede seguir conduciendo o no.