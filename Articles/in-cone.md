*** Machine Translated
`in-cone` es un elemento primitivo que nos ayuda a simular un "cono de visión" frente a una tortuga. Nos permite modelar a un agente que tiene alguna vista u otro sentido frente a ellos, pero no detrás o al lado de ellos.

El cono se construye con dos entradas: qué tan lejos puede ver el agente ( *radio* ) y qué tan ancho puede ver el agente ( *grados entre 0 y 360* ). Por ejemplo, si quisiéramos comer unos conejos si hubiera zanahorias delante de ellos, pero no detrás ni a los lados, podríamos escribir el siguiente código:



```
ask rabbits [
  if any? carrots in-cone 3 45 [ eat ]
]
```


Cosas a tener en cuenta al usar `in-cone` :

- También puede utilizar valores de punto flotante para los parámetros de radio y ángulo, como `in-cone 1.25 66.66` .
- Tanto las *tortugas* como los *parches* pueden usar `in-cone` .
- Tenga en cuenta que `in-cone` puede informar sobre la tortuga original, si está usando las mismas razas. Asegúrese de tener en cuenta eso en sus modelos utilizando la `other` primitiva. Por ejemplo, este código arrojaría un error `ask turtles [ create-links-with turtles in-cone 2 30 ]` , mientras que este funcionaría bien `ask turtles [ create-links-with other turtles in-cone 2 30 ]` .
- Puede combinar `in-cone` y `with` primitivas para reducir los agentes de destino, pero asegúrese de encapsular el primero `with` declaración entre paréntesis `( )` . Por ejemplo, ¿puede escribir un código como `if any? (carrots with [color = orange]) in-cone 3 45 [ eat ]` .


En el ejemplo de modelo a continuación, usamos `in-cone` para simular cuatro cámaras de vida silvestre activadas por movimiento. ¿Cuando una cámara detecta que las hay `any? animals in-cone 8 50` , se volverá amarillo para simular la toma de una fotografía. (Tenga en cuenta que los parches resaltados son solo para mostrar mejor visualmente el cono de visión. En realidad, ninguna de las `in-cone` tiene nada que ver con el parche en el que se encuentra la tortuga).