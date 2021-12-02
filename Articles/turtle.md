Las tortugas son agentes móviles en NetLogo que se pueden colocar en cualquier parte del mundo, pueden verse como cualquier cosa (por ejemplo, forma, color, tamaño) y pueden moverse. Son el tipo principal de agentes en los modelos NetLogo.

La primitiva `turtle` reporta una tortuga específica con el número dado. Por ejemplo, si quisiéramos crear un modelo con solo dos tortugas, una un gato y la otra un ratón, podríamos escribir el siguiente código. Observe que cuando creamos tortugas, la numeración comienza con cero.



```
create-turtles 2
ask turtle 0 [
	set shape "cat"
]
ask turtle 1 [
	set shape "mouse"
]
```


El primitivo `turtles` informa todos las parcelas en el modelo. Este primitivo es útil para pedir a todas las tortugas que hagan las mismas cosas (por ejemplo, moverse, cambiar de forma) o reducir un subconjunto de tortugas usándolo junto con el primitivo `with`. Por ejemplo, si quisiéramos crear un modelo de incendio forestal con algunas tortugas verdes que representan árboles sanos y algunas tortugas amarillas que representan árboles muertos/secos, y quisiéramos iniciar un incendio desde un árbol seco, escribiríamos el siguiente código:



```
create turtles 100 [
	set shape "tree"
	setxy random-xcor random-ycor
	set color one-of [green yellow]
]
ask one-of turtles with [color = yellow][
	set color red
]
```


Cosas a tener en cuenta cuando usamos `turtle` y `turtles`:

* Las `turtles` primitivas siempre reportarán el mismo conjunto de agentes (a menos que una tortuga muera), pero el orden de las tortugas será aleatorio cada vez que lo usemos.
* Las tortugas tienen algunas características predeterminadas que pueden tener un valor diferente para cada tortuga. Algunas de las características vienen preconstruidas (por ejemplo, `color`, `xcor`, `ycor`, `label`, `size`, `heading`), pero también podemos definir características personalizadas con el primitivo `turtles-own` las `turtles-own`, como `turtles-own [minerals water]`.
* También podemos crear razas de tortugas personalizadas usando el primitivo de la `breed`, como la `breed [trees tree]`.


En el ejemplo de modelo a continuación, tenemos varias tortugas y cada tortuga representa un agente diferente. Tenemos una tortuga grande que representa una casa, algunas tortugas verdes que representan plantas, algunas tortugas coloridas que representan perros, algunas tortugas que representan personas y algunas tortugas en la parte superior que representan nubes. La casa y las plantas permanecen inmóviles, mientras las personas, los perros y las nubes se mueven. Por otro lado, las plantas crecen poco a poco con cada tic.