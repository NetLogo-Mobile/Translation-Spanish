`Count` es una primitiva que devuelve el número de agentes en un conjunto de agentes específico. Por ejemplo, `count turtles` mostraría el número total de tortugas en un modelo, mientras que `count turtles with [color = green]` mostraría el número de tortugas verdes en el modelo. Puedes usar `count` con tortugas, parcelas, y enlaces.

También puedes usar `count` con razas de tortugas y razas de enlaces como `count dogs` o en combinación con otras primitivas agentes reporteros como `count turtles-here`.

En el ejemplo de modelo a continuación, tenemos un parque para perros en el centro y tenemos un grupo de tortugas que representan a los perros en un vecindario. Nuestros perros se mueven de forma completamente aleatoria. Cuando hay más de 5 perros en el patio de recreo en un momento dado, nuestro modelo muestra un mensaje *"El patio de recreo está demasiado lleno"*.
