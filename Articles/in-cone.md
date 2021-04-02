*** Machine Translated
`in-cone` es una primitiva que permite simular un "cono de visión" frente a una tortuga. Esto nos permite modelar a un agente que tiene alguna vista u otro sentido frente a ellos, pero no detrás o al lado de ellos.

El cono se construye con dos entradas: qué tan lejos puede ver el agente (el radio) y qué tan ancho puede ver el agente (el número de grados, entre 0 y 360). Por ejemplo, si quisiéramos que algunos conejos comieran si hubiera zanahorias delante de ellos, pero no detrás ni a los lados, podríamos decir 

```
ask rabbits [
  if any? carrots in-cone 3 45 [ eat ]
]
```
 Tenga en cuenta que, al igual que `in-radius` , `in-cone` puede terminar reportándose a sí mismo. Asegúrese de tenerlo en cuenta en sus modelos si es necesario con el `other` primitivo.

En este modelo de ejemplo, `in-cone` se usa para simular 4 cámaras de vida silvestre activadas por movimiento. ¿Cuando una cámara detecta que las hay `any? animals in-cone 8 50` , se volverá amarillo para simular la toma de una fotografía. (Tenga en cuenta que los parches resaltados son solo para mostrar mejor visualmente el cono de visión. En realidad, ninguna de las `in-cone` tiene nada que ver con el parche en el que se encuentra la tortuga).