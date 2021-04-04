`die` es una primitiva que usamos para eliminar tortugas y enlaces de un modelo. Cuando le preguntes a una tortuga o enlace a `die`, ya no existiría en el modelo, no ejecutará más código y se desaparecería de cualquier conjunto de agentes en cuales estaban. Por ejemplo, el siguiente modelo tendría 9 tortugas.



```
create-turtles 10
ask one-of turtles [ die ]
```



En el siguiente modelo, un rebaño de vacas se mueven en una pradera. Cada vez que están en una parcela verde, comen el pasto allí y aumentan energía. Cada vez que se mueven, pierden energía. Si un pasto tiene 0 energía, se muere y se elimina del modelo.