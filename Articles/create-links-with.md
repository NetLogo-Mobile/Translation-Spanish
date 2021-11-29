`create-links-with` es un procedimiento de tortuga que crea un enlace entre la tortuga actual (self) y cada miembro de un conjunto de agentes proporcionado.



```
ask turtles [
	create-links-with other turtles-here
]
```



Observa que usamos la primitiva `other` en nuestro código porque si no usamos `other`, nuestro código daría un error. NetLogo muestra este error porque la `turtles-here` informa todas las tortugas en un modelo, incluida la tortuga que está tratando de crear los enlaces, pero una tortuga no puedes crear un enlace consigo misma. Por lo tanto, no te olvides usar la `other primitive` cuando uses primitivas de reportero de conjunto de agentes similares, como `in-radius` y `turtles`.



También tenga en cuenta que esta primitiva se usa para crear varios enlaces a la vez, por lo que debes proporcionar un conjunto de agentes. Si deseas crear un enlace con solo una tortuga específica, debes usar la primitiva `create-link-with`.



En el ejemplo de modelo a continuación, usamos la `create-links-with` para simular el rastreo de contactos. Cada vez que dos personas están en la misma parcela, se crea un nuevo vínculo entre ellas. Luego, el botón/procedimiento de rastreo usa los vínculos entre las personas para rastrear a las personas que pueden haber estado expuestas a una persona infecciosa.