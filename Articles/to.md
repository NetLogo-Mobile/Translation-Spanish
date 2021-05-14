*** Machine Translated
`To` se usa para comenzar un procedimiento de comando. Puedes pensar en `to` como una forma de definir un conjunto de acciones/verbos para NetLogo, como `to go`, `to add-money`, etc. Puedes usar estos procedimientos en cualquier parte del código. **Nota**: Necesitas poner `end` al final del procedimiento para que funcione. ¡Los procedimientos también se pueden llamar desde botones! Por ejemplo, el uso de botón de `go` (el que se encuentra en la pestaña Interfaz) ejecuta el procedimiento creado como ir ... terminar. Ahora vamos a ver eso en acción. 

```
to setup
clear-all
create-turtles 100
end
```

`Setup` es el nombre del procedimiento. `Clear-all` y `create-turtles 100` son los comandos de este procedimiento. Y `end` le dice a NetLogo que el procedimiento está completo. Cuando se usa como un botón, todo sucede a la vez.

Otro propósito de esta primitiva es dividir el código en partes más pequeñas. Por ejemplo: 

```
ask turtles [
  wiggle  ;; first turn a little bit
  move    ;; then step forward
]

to wiggle
  rt random 90
  lt random 90
end

to move
fd 1
end
```
Ve cómo en el primer pedazo del código, le estás pidiendoa las tortugas a *menear*, y luego a *mover*. **Menear** y **mover** luego se usan como un procedimiento de comandos. ¡Así, te ahorra mucho espació y repetición!