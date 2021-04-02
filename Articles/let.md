*** Machine Translated
`Let` se usa para crear una nueva **variable local** y establecer su valor. Una **variable local** es una variable que solo existe dentro de los corchetes o `[...]` procedimiento en el que fue creada, a diferencia de una variable global. Solo se puede usar en el código que viene *después de* su declaración y toma la forma de:

```let variable-name initial-value```

Por ejemplo, para crear una nueva variable local llamada `my-blue-friends` y establecer su valor para todas las tortugas azules con forma de persona, diríamos:

```
let my-blue-friends turtles with [ color = blue and shape = “person” ]
ask my-blue-friends [ forward 1 ]
```

Luego, pedirles a `my-blue-friends` que avancen hace que todas las tortugas azules con forma de persona avancen. Para cambiar el valor de la variable después de crearla, usa `set` .