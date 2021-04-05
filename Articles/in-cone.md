`in-cone` es una primitiva que nos ayuda a simular un "cono de visión" frente a una tortuga. Nos permite modelar a un agente que tiene alguna vista u otro sentido frente a ellos, pero no detrás o al lado de ellos.

El cono se construye con dos entradas: qué tan lejos puede ver el agente (*radio*) y qué tan ancho puede ver el agente (*grados entre 0 y 360*). Por ejemplo, si quisiéramos comer unos conejos si hubiera zanahorias delante de ellos, pero no detrás ni a los lados, podríamos escribir el siguiente código:



```
ask rabbits [
  if any? carrots in-cone 3 45 [ eat ]
]
```



Cosas para tener en mente cuando usas `in-cone`:

* También puedes usar valores de punto flotantes para los parámetros de radio y ángulo, como `in-cone 1.25 66.66`.
* Tanto *tortugas* como *parcelas* pueden usar `in-cone`.
* Tenga en cuenta que "in-cone" también puede informar sobre la tortuga original, si estás usando las mismas razas. Asegúrete de tener en cuenta eso en sus modelos mediante el uso de la primitiva `otro`. Por ejemplo, este código arrojaría un error `ask turtles [create-links-with turtles in-cone 2 30]`, mientras que este funcionaría bien `ask turtles [create-links-with other turtles in-cone 2 30]`.
* Puedes combinar `in-cone` y la primitiva `with` para delimitar los agentes objetivo, pero asegúrese de encapsular la primera declaración `with` dentro de las paréntesis `( )`. Por ejemplo, puedes escribir un código como `if any? (carrots with [color = orange]) in-cone 3 45 [ eat ]`.



En el ejemplo de modelo a continuación, usamos `in-cone` para simular cuatro cámaras de vida silvestre activadas por movimiento. Cuando una cámara detecta que hay `any? animals in-cone 8 50`, se volverá amarillo para simular la toma de una foto. (Tenga en cuenta que las parcelas resaltadas son solo para mostrar mejor visualmente el cono de visión. En realidad, ninguna de las detecciones de tortugas `in-cone` tiene nada que ver con la parcela en la que se encuentra una tortuga).