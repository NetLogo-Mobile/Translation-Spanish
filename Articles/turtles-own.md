`Turtles-own` define variables que pertenecen a todas las tortugas en un modelo. Las variables suelen ser un rasgo o aspecto específico de la tortuga, como *tiene hambre?* o *energía*. Su sintaxis es:

```turtles-own [ variable1 variable2 ... ]```

Como las variables globales y otras variables del agente, debe definirse en la parte superior de su código, antes de cualquier definición de procedimiento. Puedes definir una variable o varias, pero todas deben estar entre corchetes.

Si has definido varias razas de tortugas, `turtles-own` aplicará la variable a todas las razas. Sin embargo, puedes definir una variable para una raza específica usando `<breed>-own`, donde **<breed>** es el nombre de tu raza. Por ejemplo, si ya has definido una raza de tortugas por `breed [birds bird]`, puedes crear una variable solo para pájaros usando `birds-own [wing-size]`.

En el siguiente modelo, los carros circulan con una cierta cantidad de gasolina en sus tanques. Usamos `turtles-own` para definir la variable `gas`, lo que representa cuánta gasolina tiene un carro. Luego, usamos la variable `gas` para determinar si un automóvil puede seguir conduciendo o no.