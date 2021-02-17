*** Machine Translated
`facexy` es un comando para tortugas que establece el rumbo de la tortuga hacia el punto (x, y). Su sintaxis es:

`facexy [x-cor y-cor]`

`facexy` no cambia la posición de una tortuga, solo su rumbo. Por ejemplo, para hacer que la tortuga 1 mire hacia el punto (2,3), diríamos:

`ask turtle 1 [ facexy 2 3 ]`

**Nota:** si la tortuga ya está en el punto (x, y), el rumbo de la tortuga no cambiará. En el modelo a continuación, hay algunos peces y un solo parche de comida. Los peces tienen hambre y todos enfrentan el parche de comida usando `facexy` .