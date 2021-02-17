*** Machine Translated
`To` se utiliza para comenzar un procedimiento de comando. Puede pensar en `to` como una forma de definir un conjunto de acciones / verbos para NetLogo, como `to go` , `to add-money` , etc. Puede usar estos procedimientos en cualquier parte del código. **Nota** : Debe poner `end` al final del procedimiento para que funcione. ¡Los procedimientos también se pueden llamar desde botones! Por ejemplo, el uso de un `go` (que se encuentra en la pestaña Interfaz) ejecuta el procedimiento creado como ir ... final. Veamos eso en acción. 

```
to setup
clear-all
create-turtles 100
end
```
 `Setup` es el nombre del procedimiento. `Clear-all` y `create-turtles 100` son los comandos de este procedimiento. Y `end` le dice a NetLogo que el procedimiento está completo. Cuando se usa como botón, todo sucede a la vez.

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
 Ver cómo en el primer trozo de código, que está llamando a las tortugas *de maniobra,* a continuación, *se mueve.* **Luego, menear** y **mover** se escriben como un procedimiento de comando. ¡Termina ahorrándote mucho espacio y repetición!