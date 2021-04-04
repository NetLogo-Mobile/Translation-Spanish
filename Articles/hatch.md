`hatch` es un elemento primitivo que crea un número proporcionado de copias idénticas de una tortuga. Similar a la primitiva `create-turtles`, toma un número y también permite definir reglas opcionales para las nuevas tortugas siguiéndolas con corchetes` [] `.



```
ask turtles [
	if season = "spring" [
		hatch 3 [
			set size 0.1
			set shape "penguin egg"
			set color white
		]
	]
]
```



Cosas para tener en cuenta cuando usas `hatch`:

* `hatch` solo puede ser usado por tortugas dentro de una declaración `ask`. si necesitas tus parcelas para crear nuevas tortugas, debes usar la primitiva `sprout`.
* También puedes usar `hatch` para razas de tortugas personalizadas, al usar la convención `hatch-pluralbreedname`. Por ejemplo, si tu modelo tiene una raza de *pingüinos*, puedes usar `hatch-penguins` y si tienes una raza de `eggs`, puedes usar `hatch-eggs`.



En el ejemplo de modelo a continuación, tenemos una tortuga que representa un insecto y algunas manchas marrones que representan comida. Cuando un insecto choca con un parche de comida mientras camina al azar, se come la comida y luego *incuban* un nuevo insecto. Tenga en cuenta que cada vez que creamos un nuevo error con la primitiva `hatch`, agregamos el siguiente comando entre corchetes `[right random 360]` porque si no agregamos este código, nuestra nueva tortuga tendría exactamente la misma ubicación, tamaño, y la dirección con su tortuga madre, lo que nos hace prácticamente imposible diferenciar los dos.

