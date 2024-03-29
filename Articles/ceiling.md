﻿`ceiling` es una primitiva matemática que redondea *informa* el número entero más cercano por encima de un número dado. En otras palabras, se redondea el número *hacia arriba.* Por ejemplo, `ceiling 5.2` reportaría 6 y el `ceiling -4.8` reportaría -4.



En el ejemplo de modelo a continuación, cada tortuga tiene una variable `my-money` que aumenta o disminuye un poco en cada tic. Usamos la primitiva de `ceiling` para *redondear* la variable `my-money` una tortuga porque queremos presentar una etiqueta debajo de cada tortuga que muestre su dinero actual. Si no redondeamos esta variable hacia arriba o hacia abajo, su etiqueta mostraría muchos números de coma flotante como `1.822882372836`, lo que sería visualmente desagradable. También usamos la primitiva `ceiling` para establecer el parámetro `ycor` cada tortuga de modo que las tortugas se muevan solo cuando cambia la versión redondeada de su variable `my-money`. Si ganan o pierden solo una pequeña cantidad de dinero, permanecen estacionarios. Por último, usamos el `ceiling` y su `floor` opuesto para dos de nuestros tres monitores en la interfaz.

