`min-pycor` informa el `pycor` de las parcelas más bajos en un modelo. Este primitivo y sus hermanos (`max-pxcor`, `max-pycor`, `min-pycor`) son muy útiles para modelar el comportamiento del agente que involucra los límites de un entorno. Por ejemplo, si quisiéramos construir un modelo donde tuviéramos una pared en los bordes, escribiríamos el siguiente código:



```
ask patches [
	if pxcor = max-pxcor or
	   pxcor = min-pxcor or
	   pycor = max-pycor or
	   pycor = min-pycor [
	   		set pcolor gray
	   ]
]
```


O si quisiéramos que las tortugas no caminaran más allá de las fronteras del mundo, escribiríamos el siguiente código:


    ask turtles [
    if [pxcor] of patch-ahead 1 < min-pycor [
    forward 1
    ]
    ]


Cosas a tener en cuenta cuando usamos `min-pycor`:

* `max-pxcor`, `min-pxcor`, `max-pycor` y `min-pycor` no son variables; son reporteros constantes. Es decir, un código como `set min-pxcor 30` mostraría un mensaje de error.
* Puedes cambiar el tamaño de su modelo a través del **botón Configuración** en la pestaña Interfaz o usando la primitiva `resize-world`.


En el ejemplo de modelo a continuación, usamos `min-pycor` y sus hermanos para crear paredes que representan un contenedor. Las bolas dentro del contenedor rebotan en la pared verde pero se *adhieren* a la pared roja.