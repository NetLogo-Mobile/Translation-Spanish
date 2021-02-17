*** Machine Translated
`Turtles-here` devuelve el **conjunto** de agentes de todas las tortugas en el parche de la persona que llama, incluido él mismo si la persona que llama es una tortuga. Por ejemplo, 

```
create-turtles 3 
ask turtles [ show count turtles-here ]
```
 informaría `3` . También puede especificar una raza usando `<breed>-here` ; si hubiera algunos gatos y ratones juntos en un modelo, `ask cats [ if any? mice-here [ chase ] ]` haría que un gato persiguiera a los ratones si están en el mismo parche.

En el modelo de abajo, hay algunas ranas moviéndose en un estanque. Si una rana salta sobre un nenúfar (parche verde), su peso empujará el nenúfar al agua, volviéndolo azul. Usamos `turtles-here` para comprobar si hay una rana encima de un nenúfar.