*** Machine Translated
`create-turtles` es una primitiva que crea un número dado de tortugas nuevas en el modelo. Estas nuevas tortugas se colocan en el centro del modelo con la misma forma predeterminada pero con colores y encabezados aleatorios. La versión abreviada de este primitivo es `crt`. por ejemplo, `create-turtles 100`.



También, puedes usar los corchetes `[]` para dar inmediatamente algunas reglas a sus nuevas tortugas. Por ejemplo, el siguiente código no solo crearía 100 tortugas nuevas, sino que también haría que todas estas tortugas fueran verdes y que cada una vaya a una parcela aleatoria. De esta manera, no necesitarías usar un comando `ask` separado.



```
create-turtles [
	set color green
	move-to one-of patches
]
```



Cosas para tener en cuenta cuando usando `create-turtles`:

* Puedes usar el formato `create-<breed>` para crear nuevas tortugas de una raza específica como `create-dogs 100` o `create-buildings 5 [ set color gray ]`.
* Solo el `observador` puede crear nuevas tortugas. No puedes usar esta primitiva dentro de una primitiva `ask`. Por ejemplo, ambas `ask gallkens [create-eggs 1]` y `ask patches [create-plants 1]` mostrarían un mensaje de error. Si necesitas tortugas ya existentes para crear nuevas tortugas, debes usar la primitiva `hatch`. Si necesitas las parcelas para crear nuevas tortugas, debes usar la primitiva `sprout`.

En el ejemplo de modelo a continuación, usamos la primitiva `crear-tortugas` para crear un paisaje con una casa, algunas plantas, personas, perros y nubes.