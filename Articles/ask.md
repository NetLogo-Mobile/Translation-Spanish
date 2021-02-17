*** Machine Translated
`ask` es una de las primitivas fundamentales en NetLogo. Nos permite *pedirle a* uno o más agentes (es decir, tortugas, enlaces, parches) que sigan un conjunto de reglas proporcionado. Cuando `ask` con más de un agente, cada agente tomará su turno en un orden aleatorio.

Por ejemplo, el siguiente código haría que todas las tortugas en un modelo avanzaran una unidad y todos los parches en un modelo rosa. 

```
ask turtles [ fd 1 ] 
ask patches [ set pcolor pink ]
```


También puede proporcionar más de un comandos con un `ask` primitiva. Por ejemplo, el siguiente código haría que todas las tortugas `pen-down` su corral y luego giraran a la derecha diez grados y avanzaran una unidad 36 veces, lo que dibujaría un círculo. 

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
- Puede solicitar a los parches individuales que sigan un conjunto de reglas utilizando el formulario `patch xy` , como `patch 3 0 [...]` .
- Puede usar el `with` para preguntar a un subconjunto aún más pequeño de agentes dados, como `ask turtles with [color = red][ ... ]` o `ask patches with [pxcor = 5][ ... ]` .