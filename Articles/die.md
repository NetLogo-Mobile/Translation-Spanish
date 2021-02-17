*** Machine Translated
`Die` tortugas usan troquel y enlaces para eliminarlo del modelo. Cuando se le pide a una tortuga o enlace que `die` , ya no existe en el modelo, no ejecutará más código y desaparecerá de cualquier conjunto de agentes en el que estaba. Por ejemplo, si `count turtles` devolvió 10, entonces `ask one-of turtles [die]` fue llamado, ahora `count turtles` devolvería 9.

En el siguiente modelo, un rebaño de ovejas se mueve y come pasto para ganar energía. Cuando una oveja se mueve, pierde energía; si una oveja alguna vez tiene 0 energía, morirá y se eliminará del modelo. Entonces incluimos el siguiente código para eliminar esas ovejas:

`if energy <= 0 [ die ]`