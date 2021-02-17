*** Machine Translated
`With` se utiliza para delimitar un conjunto de agentes, generalmente **parches** o **tortugas** , al dirigirse a un grupo específico de agentes que tienen una determinada característica. El uso de `with` se dirigirá solo a los agentes del conjunto que coincidan con la característica determinada. Su sintaxis es:

`agentset with [ desired-characteristic ]`

Por ejemplo, `ask turtles with [color = blue] [forward 1]` hará que solo las tortugas azules avancen. Puede tener varias características requeridas dentro de la `[ ]` separados por `and` o `or` para reducir aún más la agentset. Por ejemplo

`ask turtles with [color = red and size > 5] [`

`forward 1 ]`

haría que solo las tortugas rojas mayores de 5 avanzaran.