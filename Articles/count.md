*** Machine Translated
`count` es una primitiva que informa el número de agentes en un conjunto de agentes dado. Por ejemplo, `count turtles` informa el número total de todas las tortugas en un modelo, mientras que `count turtles with [color = green]` informa el número de tortugas verdes en el modelo. Puede usar `count` con tortugas, parches y enlaces.

También podemos usar el `count` con razas de tortugas y razas de enlaces como `count dogs` o en combinación con otros agentes informadores primitivos como `count turtles-here` .

En el ejemplo de modelo a continuación, tenemos un parque para perros en el centro y tenemos un grupo de tortugas que representan a los perros en un vecindario. Nuestros perros se mueven de forma completamente aleatoria. Cuando hay más de 5 perros en el patio de recreo en un momento dado, nuestro modelo muestra un mensaje *"El patio de recreo está demasiado lleno".*