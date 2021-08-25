*** Machine Translated
`link-neighbors` Neighbor es una primitiva de tortuga que reporta un conjunto de agentes que contiene todas las tortugas que están conectadas a la tortuga original a través de enlaces. Por ejemplo, si estuviéramos usando enlaces para representar relaciones de amistad, una tortuga podría enviar a sus amigos nuevos mensajes usando la primitiva `link-neighbors` Por ejemplo, el siguiente código aseguraría que las tortugas con menos de 2 amigos hagan nuevos amigos.



```
ask turtles [
	if count link-neighbors < 2 [
		make-new-friends
	]
]
```


En el ejemplo de modelo a continuación, usamos `link-neighbors` para simular el rastreo de contactos. Cada vez que dos tortugas se acercan, se forma un vínculo entre ellas. Cada enlace representa un "contacto" entre dos tortugas, por lo que llamar a `link-neighbors` en un individuo informa a todas las demás personas con las que este individuo tuvo contacto. Cuando implementamos el `trace-back` en nuestro código (en la línea 26), les pedimos a todos los `link-neighbors` de cualquier individuo expuesto (rojo) que se pongan rojos ellos mismos para indicar que ellos también han estado expuestos.