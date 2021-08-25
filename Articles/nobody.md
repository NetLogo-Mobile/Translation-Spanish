*** Machine Translated
`nobody` es una primitiva especial que usamos para verificar si un agente existe realmente. Además, cuando una tortuga muere, también se convierte en `nobody` . Por ejemplo, si quisiéramos crear un modelo en el que cada tortuga formara un vínculo con otra tortuga en un parche vecino, escribiríamos el siguiente código:


    ask turtles [
    let my-potential-friend one-of turtles-on neighbors
    if my-potential-friend != nobody [
    create-link-with my-potential-friend
    ]
    ]


Cosas a tener en cuenta al usar a `nobody`

- `nobody` se usa solo con un solo agente. Si necesitamos verificar si un conjunto de agentes está vacío, debemos usar `any?` primitivo como `if any? turtles with [color = green]` .
- Puede asignar el valor de una variable como `nobody` , como: `set my-friend nobody` . Esto funciona tanto para las variables globales que se crean con las `globals` primitivas y el agente de variables que se crean con `turtles-own` , `patches-own` , o `links-own` de variables.


En el ejemplo de modelo a continuación, tenemos una fogata en el medio, 10 carpas y 10 campistas. Cuando se hace clic en el botón Ir, cada campista se mueve al azar. Siempre que la `my-tent` un agente esté configurada como `nobody` , seguirán moviéndose. En otras palabras, los campistas reclaman las carpas al azar.