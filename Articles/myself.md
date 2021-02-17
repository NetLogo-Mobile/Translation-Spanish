*** Machine Translated
Aunque `self` y `myself` parezcamos similares, se usan en situaciones diferentes y no deben confundirse. `Myself` se usa cuando un agente necesita referirse a sí mismo mientras intenta dirigirse a un agente o conjunto de agentes diferente dentro de un `ask` o un informador (por ejemplo, de, con). Por ejemplo, si desea que la puerta de una casa abra su puerta solo cuando una persona tenga el código de acceso correcto, puede escribir 

```
ask person 1 [ 
    ask houses [ 
        if keycode = [keycode] of myself [ open-front-door ] ] ]
```
 donde `myself` refiere a la **persona 1** . `Myself` se usa a menudo con `of` para informar o establecer variables del agente que `ask turtles with [pcolor = [pcolor] of myself]` o `ask turtles with [size < [size] of myself ]` ). Consulte el **ejemplo de mí mismo** en la biblioteca de modelos para obtener más ejemplos.

`Self` se usa cuando hay un solo `ask` y la tortuga, el enlace o el parche intentan referirse a sí mismos. Por ejemplo, 

```
let my-turtle nobody 
create-turtles 1 [ set shape “turtle” set my-turtle self] 
ask my-turtle [ forward 2]
```
 establecería la variable `my-turtle` como la tortuga recién creada. Rara vez se usa, porque `[color] of self` es equivalente a simplemente decir `color` .

En el siguiente modelo, nos utilizamos a `myself` para hacer que las personas solo entren a la casa que es de su mismo color, `if color = [ color ] of myself [ stay home ]`