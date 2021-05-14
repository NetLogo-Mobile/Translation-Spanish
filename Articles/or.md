*** Machine Translated
`or` es una primitiva que se usa para verificar si *alguna* de las dos condiciones es cierto. Dadas dos verificaciones, o declaraciones de cierto o falso, `or` informará **Cierto** si 1) la primera es cierto, 2) la segunda es cierta o 3) ambas son ciertas. Solo informará **Falso** solo si *ambas* condiciones son falsas. Por ejemplo, digamos que tenía un cerdo y quería que comiera la comida en su parcela, sin importar si era comida para animales o para humanos. Podrías modelar eso con

````ask pigs [ ```

 ```if animal-food-here or people-food-here [ ```

 ```eat] ```

Además, si deseas verificar más de dos condiciones, puede simplemente encadenar una serie de `or` como: `if A or B or C or D [ do-something]`.

En este modelo, `or` se usa para comprobar si un balón de fútbol está dentro o fuera de la red. Usando el `check-if-miss` , si la pelota está fuera de los límites de la red, la coloreamos de rojo, y si está adentro, la coloreamos de verde. En el código, comprobamos si la pelota está demasiado lejos hacia la derecha *o* demasiado hacia la izquierda *o* demasiado alta. (En este modelo, el centro del mundo está configurado para ser el centro del borde inferior para facilitar las matemáticas).

También - Tenga en cuenta que bajo el capó, en la práctica, NetLogo a menudo solo tiene que verificar la primera de las dos condiciones para ver si el `or` se reportará como verdadero o no. Imagina que estamos comprobando dos condiciones, `condition1` y `condition2` . Si escribimos `if condition1 or condition2` y `condition1` es cierto, independientemente de si `condition2` es cierto o falsa, `or` siempre informará verdadero, entonces, ¿por qué molestarse en verificar `condition2`? Esto se llama "cortocircuito o" y lo verá en la mayoría de los lenguajes de programación modernos porque permite una ejecución más rápida del código, así como algunos otros beneficios para los programadores avanzados. Sin embargo, la conclusión para los programadores principiantes es más simple: si necesitas usar `or` para combinar dos comprobaciones, coloque primero la menos costosa desde el punto de vista computacional, porque si informa que es cierto, nunca tendrá que perder el tiempo de la computadora revisando la más costosa.