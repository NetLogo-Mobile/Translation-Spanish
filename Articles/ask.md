*** Machine Translated
`ask` es una de las primitivas fundamentales en NetLogo. Nos permite *pedirle a* uno o más agentes (es decir, tortugas, enlaces, parches) que sigan un conjunto de reglas proporcionado. Cuando `ask` con más de un agente, cada agente tomará su turno en un orden aleatorio.

Por ejemplo, el siguiente código haría que todas las tortugas en un modelo avanzaran una unidad y todos los parches en un modelo rosa. 

```
ask turtles [ fd 1 ] 
ask patches [ set pcolor pink ]
```


También podemos proporcionar más de un comando con una `ask` primitiva. Por ejemplo, el siguiente código haría que todas las tortugas `pen-down` su corral y luego giraran a la derecha diez grados y avanzaran una unidad 36 veces, lo que dibujaría un círculo. 

```
ask turtles [
	pen-down
	repeat 36 [
	   right 10
	   forward 1
	]
]
```


Cosas a tener en cuenta al usar `ask` :

- Puede usar la `ask` con los tipos de tortuga personalizados que defina con la primitiva `breed`
- Puede pedir a las tortugas individuales que sigan un conjunto de reglas usando la forma `turtle n` , como `ask turtle 1 [...]` `ask turtle 2 [...]`
- Puede pedir a los parches individuales que sigan un conjunto de reglas utilizando el formulario `patch xy` , como `patch 3 0 [...]` .
- Puede usar el `with` para preguntar a un subconjunto aún más pequeño de agentes dados, como `ask turtles with [color = red][ ... ]` o `ask patches with [pxcor = 5][ ... ]` .
- Puede usar `ask` con `turtles` , `links` y `patches` .
- Si escribe un código fuera de una instrucción ask, NetLogo intentará pedirle al `observer` que ejecute el código, pero no puede escribir un código como `ask observer [...]` .
- Tenga en cuenta que cada primitiva de NetLogo tiene un *alcance* . Si usa una primitiva dentro de una instrucción ask incompatible, NetLogo mostrará un error. Una primitiva puede ser solo para el observador (p. Ej., `create-turtles` , `diffuse` ), solo turtle (p. Ej., `forward` , `hatch` ), solo parche (p. Ej., `sprout` , `max-pxcolor` ) o solo enlace (p. Ej., `tie` , `thickness` ). Por otro lado, algunas primitivas pueden usarse dentro de múltiples alcances (por ejemplo, `pcolor` , `neighbors` ) y las primitivas de utilidad son independientes del alcance (por ejemplo, `mean` , `with` ).


En el modelo a continuación, queremos que los peces naden aleatoriamente y las estrellas simplemente roten, y queremos que todas las tortugas (peces + estrellas) crezcan poco a poco. Para hacer que sigan estas acciones, ¡simplemente usamos la primitiva `ask`