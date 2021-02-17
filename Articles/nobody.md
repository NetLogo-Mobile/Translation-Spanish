*** Machine Translated
`Nobody` es un valor especial que se utiliza para indicar que el agente que buscaba no existe. Cuando una tortuga muere, se vuelve igual a `nobody` . `Nobody` se suele utilizar a nadie para comprobar que hay un agente en un conjunto de agentes para evitar un error. Por ejemplo, puede incluir 

```
if one-of turtles with [color = red] != nobody [ 
   ask turtles with [color = red ] forward 1 ]
```
 para que, en el caso de que no haya tortugas rojas, evitaría un error.

Es importante señalar que un conjunto de agentes vacío no es igual a `nobody` ; `nobody` solo se usa cuando se busca un solo agente, generalmente en el contexto de `turtle` , `one-of` o `max-one-of` .