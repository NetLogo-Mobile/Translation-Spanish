`create-links-with` es un procedimiento de tortuga que crea un enlace entre la tortuga actual (mismo) y cada miembro de un conjunto de agentes proporcionado. 



```
ask turtles [
	create-links-with other turtles-here
]
```



Observe que usamos la primitiva `otro` en nuestro código porque si no usamos `otro`, nuestro código daría un error. NetLogo muestra este error porque la primitiva `turtles-here` reporta todas las tortugas en un modelo, incluida la tortuga que está tratando de crear los enlaces, pero una tortuga no puede crear un enlace consigo misma. Por lo tanto, no te olvidas utilizar el `otro primitivo` cuando utilice primitivos de reportero de conjunto de agentes similares, como` in-radius` y `turtles`.



También tenga en mente que esta primitiva se usa para crear varias enlaces en una vez, entonces necesitas proporcionar un conjunto de agentes. Si quieres usar un enlace con solo una tortuga específica, debes usar la primitiva `create-link-with`.



En el ejemplo de modelo a continuación, usamos la primitiva `create-links-with` para simular el rastreo de contactos. Cada vez que dos personas están en la misma parcela, se crea un nuevo vínculo entre ellas. Luego, el botón /procedimiento de rastreo usa los enlaces entre las personas para rastrear a las personas que pueden haber estado expuestas a una persona infecciosa.
