*** Machine Translated
`create-links-with` es un procedimiento de tortuga que crea un enlace entre la tortuga actual (mismo) y cada miembro de un conjunto de agentes proporcionado. (compáralo con `create-link-with`, que crea un vínculo desde la tortuga actual a una *sola* otra tortuga).

Una cosa importante a tener en cuenta al usar `create-links-with` es que una tortuga que crea un vínculo a sí misma provocará un error. Por ejemplo, si escribieras: 

```
ask turtles [
  create-links-with turtles in-radius 5
]
```
 obtendría un error, porque la tortuga "propia" actual se incluiría en `turtles in-radius 5` , lo que provocaría que una tortuga intentara crear un vínculo consigo misma, que no es permitido. Para evitar este problema, a menudo verás el comando `other` usado con `create-turtles-with` para asegurarse de que no se creen autovínculos accidentalmente. Por ejemplo, para corregir el error anterior, puede escribir: 

```
ask turtles [
  create-links-with other turtles in-radius 5
]
```
 En este ejemplo, `create-links-with` se usa para simular el rastreo de contactos, en el que rastreamos a cada par de personas que interactúan (en nuestro caso con un enlace) y luego usamos esa información para rastrear a las personas que pueden haber estado expuestas a una enfermedad infecciosa. En nuestro modelo, en cada tic, cada individuo crea un vínculo con todos los demás individuos dentro de un pequeño radio de sí mismo, lo que representa un "contacto". Luego, podemos usar el botón de rastreo para resaltar a cada individuo que se ha puesto en contacto con un individuo potencialmente infectado mediante el rastreo a lo largo de esos enlaces.