`Hatch` se usa para crear nuevas tortugas por una tortuga existente. Toma la forma de:

`hatch number-of-new-turtles [ optional-commands ]`

Las nuevas tortugas heredan las mismas características que la tortuga madre (por ejemplo, tamaño, color, ubicación, etc.). Después de ser creadas, las nuevas tortugas ejecutarán los comandos de forma independiente. (Nota: debido a que agregar comandos es opcional, se usan si deseas cambiar una variable del padre o hacer que la nueva tortuga haga algo específico). `Hatch` es una primitiva que solo pueden usar las tortugas, es decir, dentro de una `ask turtles [ … ]`; solo las tortugas pueden incubar tortugas. Para crear tortugas a partir de parcelas, vea `sprout`.