*** Machine Translated
`create-links-with` es un procedimiento de tortuga que crea un enlace entre la tortuga actual (self) y cada miembro de un conjunto de agentes proporcionado.



```
ask turtles [
	create-links-with other turtles-here
]
```


Observe que usamos la `other` primitiva en nuestro código porque si no usamos `other` , nuestro código daría un error. NetLogo muestra este error porque la `turtles-here` informa todas las tortugas en un modelo, incluida la tortuga que está tratando de crear los enlaces, pero una tortuga no puede crear un enlace consigo misma. Por lo tanto, no olvide utilizar la `other primitive` cuando utilice primitivas de reportero de conjunto de agentes similares, como `in-radius` y `turtles` .

También tenga en cuenta que esta primitiva se utiliza para crear varios enlaces a la vez, por lo que debe proporcionar un conjunto de agentes. Si desea crear un enlace con solo una tortuga específica, debe usar la primitiva `create-link-with`

En el ejemplo de modelo a continuación, usamos la `create-links-with` para simular el rastreo de contactos. Cada vez que dos personas están en el mismo parche, se crea un nuevo vínculo entre ellas. Luego, el botón / procedimiento de rastreo utiliza los vínculos entre las personas para rastrear a las personas que pueden haber estado expuestas a una persona infecciosa.