`layout-circle` es un elemento primitivo que mueve un conjunto de tortugas a un círculo espaciado uniformemente de un radio determinado. Por ejemplo:



```
create-turtles 100 [
	set shape "person"
]
layout-circle turtles 10
```



Cosas para tener en cuenta cuando usas `layout-circle`:

* `layout-circle` es una primitiva de *solo observadores*, entonces no lo puedes usar con una declaración de `ask`.
* La ubicación real de las tortugas en un diseño circular será aleatoria cada vez que use esta primitiva con un *conjunto de agentes*.
* Puedes usar layout-circle con razas de tortugas personalizadas como `layout-circle tables 3`.



El siguiente ejemplo de modelo demuestra cómo funciona `layout-circle`. Tiene dos botones de *preparar*: uno para crear un modelo vacío y otro para crear un modelo con 10 casas en lugares aleatorios. Cuando haces clic en el botón ir, creamos una nueva casa en cada marca si hay menos de 10 casas (es decir, si usamos el botón de configuración vacía). Luego, usamos `layout-turtle` para organizar nuestro vecindario. Este modelo también incluye un radio variable y lo incrementa en cada tic para mostrar cómo funciona `layout-turtle` para diferentes valores de radio.