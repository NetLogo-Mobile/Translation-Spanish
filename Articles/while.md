﻿*** Machine Translated
`While` comienza un ciclo que ejecuta un **bloque de comandos** , siempre que un **reportero** dado devuelva **Verdadero** . Si el reportero informa **Falso** , se sale del ciclo. Toma la forma:

`while [ reporter ] [ commands ]`

Por ejemplo, para hacer que la tortuga 0 siga avanzando hasta que llegue a un parche que no tenga otras tortugas, podríamos decir: 

```
ask turtle 0 [ 
    while [ any? Other turtles-here ] [ 
    	forward 1] ]
```


Nota: los bucles while y otros bucles no se utilizan con frecuencia en los modelos NetLogo. En el modelo a continuación, se utiliza un `while` de bucle para hacer una tortuga dibujar un cuadrado.