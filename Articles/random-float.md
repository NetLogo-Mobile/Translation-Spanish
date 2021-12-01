`random-float` es una primitiva matemática que informa un número de coma flotante aleatorio en cualquier lugar entre 0 y el número dado. Por ejemplo, `random-float 10` podría reportar 6.9105, 7, 4.2, 0.451, 0.0000001, 9.99999, etc. `random-float` es muy útil para modelar fenómenos que requieren números continuos. Por ejemplo, si quisiéramos crear un modelo en el que quisiéramos tener personas con varias alturas, podríamos escribir el siguiente código, que haría que cada persona tuviera una altura aleatoria entre 5 pies y 7 pies:



```
create-people 100 [
	set size 5 + random-float 2
]
```


Cosas a tener en cuenta cuando usas `random-float`:

* Si deseas generar un número aleatorio entre un rango personalizado, puedes usar el siguiente formato: `minnumber + (random-float (maxnumber - minnumber))`. Por ejemplo, si quisiéramos generar un número de punto flotante aleatorio entre 4 y 7, escribiríamos el siguiente código: `4 + random-float 3`.
* En el caso común en el que deseas obtener un valor aleatorio que se encuentra en algún lugar entre las coordenadas `random-xcor` y `random-ycor`, que también informan valores no enteros.
* Debido a que `random-float` devolverá un número entre 0 y (n-1), `random-float 5.0` podría reportar `0.0`, pero nunca reportar `5.0` . El número más alto que puede reportar un `random-float` `4.999999....`.


En el ejemplo de modelo a continuación, usamos `random-float` para colocar aleatoriamente un dardo en algún lugar dentro (o fuera) de un tablero de dardos. Cuando usamos `random-float`, nos aseguramos de que el dardo pueda aterrizar en todos los puntos posibles del tablero de dardos, no solo en puntos enteros.