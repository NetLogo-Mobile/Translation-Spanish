*** Machine Translated
`any?` se utiliza para determinar si hay al menos un agente dentro de un conjunto de agentes determinado. Si los hay, devolverá **verdadero** ; de lo contrario, devolverá **falso** .

Por ejemplo, el siguiente código repetiría la ejecución del `go` de forma repetida siempre que haya al menos 1 tortuga en el modelo. Si, digamos, hubiera muchas tortugas pero pudieran `die` , el modelo se detendría cuando todas las tortugas murieran. 

```
while any? turtles [ go ]
```


¿Puedes combinar `any?` con un reportero condicional que usa la `with` como el siguiente ejemplo que detiene el modelo si alguna de las tortugas en el modelo es menor que 1 unidad: 

```
if any? turtles with [size < 1] [stop]
```


¿Cosas a tener en cuenta al usar `any?` :

- No olvide el signo de interrogación ( `?` ) Al final.
- ¿Puede usar el `not` primitivo, como en el ejemplo anterior, para revertir el resultado de `any?` . Esto te vendría bien si
- `any?` en sí mismo no hace nada; debe usarlo dentro de una declaración condicional como `if` y `if-else` u otras primitivas que requieren valores verdadero-falso como `while` .