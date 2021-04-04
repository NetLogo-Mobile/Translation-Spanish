`if` es una primitiva que nos permite definir comportamientos de agentes condicionales. Tiene la siguiente estructura: ```si condición [comando (s)]```. Si la condición dada es cierta, NetLogo ejecutará el código proporcionado entre corchetes. Si la condición dada es falsa, NetLogo no hará nada.



```
ask cars [
	if my-speed < 60 [
		accelerate
	]
]
```



Cosas a tener en mente cuando usas `if`:

* Puedes combinar una o más declaraciones condicionales al usar primitivas `and` y `or`.
* Puedes usar la primitiva `not` para hacer declaraciones ciertas falsas y viceversa.
* Si necesitas que tus agentes sigan un conjunto de reglas por separado si la condición proporcionada es falsa, debes usar la primitiva `ifelse`.



En el ejemplo de modelo a continuación, tenemos algunos parches que representan trampas para ratones y algunos ratones que se mueven aleatoriamente. Si un ratón pisa una trampa para ratones, establece su variable `trapped?` En `true`. Los ratones que están `not trapped` continúan moviéndose, mientras que los que están atrapados permanecen estacionarios.
