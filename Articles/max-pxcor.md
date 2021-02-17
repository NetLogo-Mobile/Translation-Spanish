*** Machine Translated
`Max-pxcor` y `max-pycor` devuelven la coordenada x máxima y la coordenada y máxima de los parches, respectivamente. Las coordenadas xey máximas de los parches también determinan el tamaño del modelo y siempre deben ser mayores o iguales a cero. `Max-pxcor` y `max-pycor` no se pueden cambiar dentro del código; el tamaño del mundo solo se puede cambiar editando la vista.

De manera similar, `min-pxcor` y `min-pycor` devuelven la coordenada x mínima y la coordenada y mínima de los parches, respectivamente. Las coordenadas mínimas xey deben ser menores o iguales a cero. Por ejemplo, `ask patches with [pxcor = min-pxcor or pycor = min-pycor] [ set pcolor blue ]` establecería los parches a lo largo de la parte inferior e izquierda del modelo en azul.

Nota: al igual que las tortugas usan el `color` y los parches usan `pcolor` , es importante distinguir entre `xcor` e `ycor` , que solo usan las tortugas, y `pxcor` y `pycor` , que solo usan los parches.