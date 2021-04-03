`color` es una característica de tortugas que representa el color de la tortuga. Cada vez que creamos nuevas tortugas, cada una se asigna un colo aleatoria. Podemos usar la primitiva `set` y la primitiva `color` juntas para crear el color de una tortuga como sigue: `set color red`.

```
ask turtles [
	ifelse size > 2 [
		set color red
	][
		set color green
	]
]
```

`color` también es un reportero; lo podemos usar para acceder el color de una tortuga como sigue: 

```
ask turtles with [color = red][
	set size 5
]
```

Cosas para tener en cuenta cuando usas `color`:

* NetLogo usa una esquema de numeración personalizada para representar colores. Puedes acceder a este esquema de numeración de color al hacer clic en el menú de *Herramientas* y escoger el opción de *Muestras de Color*.
* Como notaste en los ejemplos anteriores, puedes usar los nombres de los colores comunes directamente en su código. Estos nombres son: `red`,`green`,`blue`,`brown`,`black`,`pink`,`white`,`violet`,`magenta`,`cyan`, y `gray`.
* Necesitas escribir el nombre de un color directamente, sin cotizaciones alrededor del nombre del color (`""`).
* Como NetLogo usa un esquema de numeración simple para los colores, puedes tratar los nombres de colores como valores númericos. Esto nos permite manipular la claridad de los colores con matemáticas simples. Por ejemplo, `green + 2` resultará en un color verde más claro, mientras que `green - 2` resultará en un verde más oscuro. También puedes usar números que no sean enteros para lograr un color aún más preciso, como `red + 0.25` o `blue - 1.85`.

En el ejemplo de modleo a continuación, tenemos una oveja blanca y algunas plantas. Usamos la primitiva `color` para hacer que algunas plantas sean verdes y otras amarillas. Usamos `ask turtles with [color = white]` para pedirle a la oveja que se mueva, mientras que las plantas permanecen estacionarias. Nuestras obejas se mueven al azar. Cuando hay una planta amarilla en la misma parcela, nuestras ovejas simplemente la ignora. Sin embargo, si hay una planta verde en la misma parcela, nuestra oveja se come la planta verde.