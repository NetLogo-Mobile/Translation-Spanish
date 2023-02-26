*** Machine Translated
`facexy` hace que una tortuga cambie su dirección ( `heading` ) para apuntar hacia una coordenada dada (x,y). Por ejemplo, `ask turtles [ facexy 0 0 ]` que todas las tortugas de un modelo queden orientadas hacia el centro del modelo.
 
Cosas a tener en cuenta al usar `facexy` :
 
- `facexy` no cambia la posición de una tortuga, solo su rumbo.
- Si una tortuga ya está en el punto dado (x, y), no cambiará su rumbo.

En el ejemplo del modelo a continuación, hay algunos peces y una sola porción de comida. Cuando se hace clic en el botón ***Agregar comida*** , cambiamos el `pcolor` del parche en (3, -3) a blanco, lo que indica una comida y le pedimos a los peces que miren esta coordenada para indicar que recurren a la comida.