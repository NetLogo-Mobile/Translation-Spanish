*** Machine Translated
`pcolor` es una variable de parche incorporada que informa el color de un parche. Debido a que `pcolor` es una variable, además de un reportero, puede usar `set` para cambiarlo. `pcolor` se puede establecer simplemente indicando el color (por ejemplo, marrón, amarillo, rojo; tenga en cuenta que no hay comillas alrededor de los nombres de los colores) o el color NetLogo (un solo número). Por ejemplo, si quisiéramos que nuestros parches fueran azules para representar un océano y luego crear una isla en el medio, escribiríamos el siguiente código:



```
ask patches [
	set pcolor blue
	if distancexy 0 0 < 5 [
		set pcolor brown
	]
]
```


Si quisiéramos poner algunos árboles en nuestra isla, `pcolor` sería útil de la siguiente manera:



```
create-trees 10 [
	move-to one-of patches with [pcolor = green]
]
```


Cosas a tener en cuenta al usar `pcolor` :

- Una tortuga puede acceder directamente al `pcolor` de su parche. Por ejemplo, `ask turtles [set pcolor green]` da como resultado el mismo resultado que `ask turtles [ ask patch-here [ set pcolor green ] ]` .
- NetLogo utiliza un esquema de numeración personalizado para representar colores. Puede acceder a este esquema de numeración de colores haciendo clic en el *menú Herramientas* y eligiendo la opción *Muestras de color.*
- Como notó en los ejemplos anteriores, puede usar los nombres de los colores comunes directamente en su código. Estos nombres son: `red` , `green` , `blue` , `brown` , `black` , `pink` , `white` , `violet` , `magenta` , `cyan` y `gray` .
- Debe escribir el nombre de un color directamente, sin comillas alrededor del nombre del color ( `""` ).
- Como NetLogo utiliza un esquema de numeración simple para los colores, puede tratar los nombres de los colores como valores numéricos. Esto nos permite manipular la claridad de los colores con matemáticas simples. Por ejemplo, `green + 2` resultará en un color verde más claro, mientras que `green - 2` resultará en un verde más oscuro. También puede utilizar números que no sean enteros para lograr un color aún más preciso, como `red + 0.25` o `blue - 1.85` .


En el ejemplo de modelo a continuación, tenemos algunas ovejas que deambulan al azar. Usamos `pcolor` para hacer que algunos de nuestros parches sean `brown` para representar el suelo y algunos de nuestros parches `green` para representar la hierba. Las ovejas solo pueden comer cuando están en un parche con pasto, por lo que solo pueden comer `if pcolor = green` . Este modelo no solo cambia el `pcolor` de un parche usando `set` , sino que muestra cómo `pcolor` en declaraciones condicionales.