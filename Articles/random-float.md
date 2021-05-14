*** Machine Translated
`random-float` es una primitiva que reporta un número flotante aleatorio entre 0 y el número dado, tanto números enteros como decimales. Por ejemplo, `random-float 10` podría reportar 6.9105, 7, 4.2, 0.451, 0.0000001, 9.99999, etc. (Consulta `random` para encontrar un número entero aleatorio).

En el caso común en el que deseas obtener un valor aleatorio que se encuentra en algún lugar entre las coordenadas x o y mínima y máxima, puedes usar los procedimientos `random-xcor` y `random-ycor`, que también informan valores no enteros.

**Nota:** debido a que `random-float` devolverá un número entre 0 y (n-1), `random-float 5.0` podría reportar `0.0` , pero nunca reportaría `5.0`.

En este modelo, `random-float` se usa para colocar aleatoriamente un dardo en algún lugar dentro (o fuera) de un tablero de dardos. Al usar `random-float`, nos aseguramos de que el dardo pueda caer en todos los puntos posibles del tablero de dardos, no solo en puntos enteros como `random` que produciría random.