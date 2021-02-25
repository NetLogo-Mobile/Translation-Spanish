`Floor` es una primitiva de redondeo que informa el número entero más cercano debajo del número, redondeando hacia abajo. Por ejemplo, el `show floor 4.8` devolvería 4 y el `show floor -7.5` devolvería -8.

`Ceiling` es otra primitiva de redondeo que informa el entero más cercano por encima del número, redondeando hacia arriba. Por ejemplo, `show ceiling 5.3` devolvería 6 y `show ceiling -4.4` devolvería -4.

En el siguiente modelo, usamos el `ceiling` y el `floor` para redondear hacia arriba o hacia abajo los puntajes de las pruebas de una clase. Si el maestro está siendo amigable, usaremos el `ceiling` para redondear los puntajes hacia arriba, y si el maestro está siendo antipático, usaremos el `floor` para redondear los puntajes hacia abajo.