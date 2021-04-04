`facexy` hace que una tortuga cambie su dirección (`heading`) para apuntar hacia una coordenada dada (x, y). Por ejemplo, `ask turtles [facexy 0 0]` convierte a todas las tortugas en un modelo para que miren hacia el centro del modelo.

Cosas para tener en mente cuando usas `facexy`:

* `facexy` no cambia la posición de una tortuga, solo su rumbo.
* Si una tortuga ya está en el punto dado (x, y), no va a cambiar su rumbo.

En el ejemplo de modelo a continuación, hay algunos peces y una sola parcela de comida. Cuando haces clic en el botón ***agregar comida***, cambiamos el `pcolor` de la parcela en (3, -3) a blanco, lo que indica un alimento y le pedimos al pez que mire esta coordenada en orden para indicar que recurren a la comida.
