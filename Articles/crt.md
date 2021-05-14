*** Machine Translated
`create-turtles` es una primitiva que crea un número determinado de tortugas nuevas en el modelo. Estas nuevas tortugas se colocan en el centro del modelo con la misma forma predeterminada pero con colores y encabezados aleatorios. La versión abreviada de esta primitiva es `crt` .



```
create-turtles 1015
crt 30
```


Además, podemos usar los corchetes () `[ ]` ) para dar inmediatamente algunas reglas a nuestras nuevas tortugas. Por ejemplo, el siguiente código no solo crearía 100 nuevas tortugas, sino que también haría que todas estas tortugas fueran verdes y que cada una vaya a un parche aleatorio. De esta manera, no necesitaríamos usar un comando `ask`



```
create-turtles 100 [
	set color green
	move-to one-of patches
]
```


Cosas a tener en cuenta al usar `create-turtles` :

- Puede utilizar el `create-<breed>` para crear nuevas tortugas de una raza personalizada específica, como `create-dogs 100` o `create-buildings 5 [ set color gray ]` .
- Solo el `observer` puede crear nuevas tortugas. No puede usar esta primitiva dentro de una primitiva de `ask` Por ejemplo, tanto `ask chickens [create-eggs 1]` como `ask patches [ create-plants 1 ]` mostrarían un mensaje de error. Si necesita tortugas ya existentes para crear nuevas tortugas, debe usar la primitiva `hatch` Si necesita los parches para crear nuevas tortugas, debe usar la primitiva `sprout`


En el ejemplo de modelo a continuación, usamos el `create-turtles` para crear un paisaje con una casa, algunas plantas, personas, perros y nubes.