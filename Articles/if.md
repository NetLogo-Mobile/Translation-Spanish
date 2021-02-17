*** Machine Translated
`If` se usa cuando desea ejecutar un comando condicionalmente. Tiene la forma de:

`if condition [ command ], or `if this-is-true [ then run these commands ]`

Si la condición es **Verdadera** , el comando se ejecutará. Si la condición es **Falsa** , los comandos no se ejecutarán y si el valor se resuelve en algo distinto de verdadero o falso, se producirá un error. Por ejemplo,

`ask turtles [ if time = night [ sleep ]`

significaría “si es de noche, las tortugas se irán a dormir”. Se pueden ejecutar varios comandos, siempre que estén todos contenidos en el mismo `[ ]` .

En el siguiente modelo, la gente está jugando un juego de "el suelo es lava". Creamos condicionales usando `if` para determinar si una persona está a salvo (en un parche azul) o fuera (en un parche de lava).