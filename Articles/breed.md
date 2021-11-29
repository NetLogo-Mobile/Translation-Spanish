`breed` es una primitiva especial que solo se puede colocar en la parte superior de una pestaña de código de NetLogo. Usando `breed`, puede definir tipos personalizados o *razas* de tortugas. Es más útil cuando tenemos diferentes grupos de tortugas y cada una necesita tener su propio comportamiento y queremos tener una manera fácil de hacer referencia a cada grupo dentro de su código.



Para crear un nuevo tipo de tortuga, usamos `breed` seguida por un corchete de apertura `[` , la versión plural de la raza, un espacio, la versión singular de la raza y un corchete de cierre `]`. Por ejemplo, `breed [dogs dog]`, `breed [buildings building]` y `breed [cars car]`.



NetLogo requiere las versiones plural y singular de una raza porque:

* Los diferentes idiomas hablados pueden tener diferentes convenciones para las palabras en plural y en singular.
* Algunas cosas pueden tener formas no convencionales para plural y singular, como `breed [cacti cactus]` , `breed [mice mouse]` o `breed [leaves leaf]` .



`breed` también es especial porque crea otros comandos relacionados que se pueden usar más adelante en su código. Por ejemplo, si creamos una **raza de perros**, podemos usar primitivos como `create-dogs`, `dogs-here`, `hatch-dogs`, `sprout-dogs` etc.



Podemos crear tantas razas como desee en su modelo. También podemos usar la `link-breed` de enlaces para crear diferentes grupos de enlaces.



En el ejemplo de modelo de ejemplo a continuación, usamos la primitiva `breed` para crear dos tipos de tortugas con un comportamiento muy diferente: árboles y leñadores. Los árboles simplemente se quedan allí, mientras que los leñadores deambulan y talan los árboles si se encuentran con una parcela con un árbol. Si bien no sería demasiado difícil crear una versión de este modelo sin `breed` usando propiedades de tortuga personalizadas definidas con la `turtles-own` las tortugas, la primitiva `breed` nos permite diferenciar fácilmente entre diferentes tipos de tortugas. El uso de razas también facilita la lectura del código.