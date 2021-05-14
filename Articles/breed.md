*** Machine Translated
`breed` es una primitiva especial que solo se puede colocar en la parte superior de una pestaña de código de netlogo. Usando la `breed`, puedes definir tipos personalizados o *razas* de tortugas. Es más útil cuando tienes diferentes grupos de tortugas que necesitan tener su propio comportamiento y quieres tener una manera fácil de hacer referencia a cada grupo dentro de tu código.

Para crear un nuevo tipo de tortugas, usa la primitiva `breed` seguida de un corchete de apertura `[` , la versión plural de la raza, un espacio, la versión singular de la raza y un corchete de cierre `]` . Por ejemplo, `breed [dogs dog]`, `breed [buildings building]` y `breed [cars car]`.

NetLogo requiere las versiones plural y singular de una raza porque:

- Los diferentes idiomas hablados pueden tener diferentes convenciones para las palabras en plural y en singular
- Algunas cosas pueden tener formas no convencionales de plural y singular, como `breed [cacti cactus]` , `breed [mice mouse]` o `breed [leaves leaf]` .


`breed` también es especial porque crea otros comandos relacionados que se pueden usar más adelante en su código. Por ejemplo, si crea una **raza de perros** , puede usar primitivas como `create-dogs` , `dogs-here` , `hatch-dogs` , `sprout-dogs` etc.

Puedes crear tantas razas como desee en su modelo. También puedes usar la `link-breed` de enlaces para crear diferentes grupos de enlaces.