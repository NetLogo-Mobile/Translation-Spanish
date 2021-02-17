*** Machine Translated
`create-turtles` es una primitiva que crea tortugas con colores y encabezados aleatorios en la forma predeterminada de un triángulo. `Crt` es la versión abreviada de create-turtles. La sintaxis es:

`create-turtles number-of-turtles [ optional-commands ]`

Al usar corchetes [], puede elegir pasar comandos a esas nuevas tortugas. Por ejemplo, puedes escribir

`create-turtles 100 [`

`set shape “person”`

`forward 10 ]`

que crea 100 tortugas en forma de persona y las mueve hacia adelante. ¡Solo el observador puede usar este comando! Para los parches que crean tortugas, vea [*brote*](http://ccl.northwestern.edu/netlogo/docs/dictionary.html#sprout) . Para crear tortugas a partir de tortugas existentes, vea [*hatch*](http://ccl.northwestern.edu/netlogo/docs/dictionary.html#hatch) .