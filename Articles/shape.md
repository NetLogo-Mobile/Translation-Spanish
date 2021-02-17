*** Machine Translated
`shape` es una tortuga y una variable de enlace que representa la forma de un agente. Nuevos tortugas y se crean vínculos con el valor por defecto formas correspondientes, y se pueden cambiar usando `set shape “shape-name”` formato dentro de un `ask` contexto para cambiar las tortugas o Enlaces formas. También puede utilizar `shape` como reportero, como cualquier otra característica del agente, como 

```
ask turtles [ 
if shape = “rabbit” [ 
forward 1  
]
 ] 
```
 **Tenga en cuenta** que debe usar comillas ("") para las formas.

Para ver la lista de formas disponibles en NetLogo, haz clic en el menú Herramientas y elija las opciones "Editor de formas de tortuga" o "Editor de formas de enlace". Cada nuevo modelo de NetLogo viene precargado con un pequeño conjunto de formas (por ejemplo, oveja, tortuga, automóvil, cuadrado) que puede usar directamente en su código. Por ejemplo, el siguiente código funcionaría en cualquier modelo nuevo de NetLogo: `ask turtles [set shape "person"]` pero el siguiente código arrojaría un error: `ask turtles [ set shape “person lumberjack”]` . Puede utilizar la opción "Importar de biblioteca" en el editor para encontrar una lista extensa de formas que se utilizan en otros modelos. Además, puede crear sus propias formas en el editor.

En el modelo de abajo, hay ovejas y lobos deambulando. Solo las ovejas comen pasto y no los lobos, por lo que podemos distinguirlas usando `shape` para reducir el conjunto de agentes a solo `turtles with [ shape = "sheep" ]` .