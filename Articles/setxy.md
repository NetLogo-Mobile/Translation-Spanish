*** Machine Translated
`setxy` mueve una tortuga a una determinada coordenada del mundo. Toma la forma de:

```setxy xy ```

donde **x** es la coordenada x deseada (izquierda/derecha) e **y** es la coordenada y deseada (arriba/abajo).

Por defecto, las coordenadas X e Y en el centro del mundo son ambas 0, por lo que `setxy 0 0` establecerá la posición de la tortuga en el centro del mundo. Las coordenadas xey dadas a `setxy` pueden ser valores decimales, no solo números enteros, por lo que `setxy 0.5 -0.5` colocará a la tortuga 0.5 unidades a la derecha y 0.5 unidades hacia abajo desde el centro.

Tenga en cuenta que `setxy` sigue las reglas de envoltura del mundo actual de NetLogo, por lo que en un mundo de 10 unidades por 10 unidades con envoltura vertical y horizontal, `setxy 26 42` se ajustaría hasta (6,2).

En este modelo de ejemplo, `setxy` se usa con dos valores ingresados por el usuario para colocar una pieza de ajedrez en un lugar elegido en el tablero de ajedrez. Puedes imaginar lo esencial que `setxy` para crear un juego de ajedrez real en NetLogo.

**Nota:** El "tablero de ajedrez" en este modelo es de 7 cuadrados por 7 cuadrados en lugar del tradicional 8 por 8. Esto se hizo a modo de ejemplo porque, de forma predeterminada, NetLogo fomenta mundos con longitudes de borde impares para asegurarse de que el centro sea siempre en (0,0) y el mundo general es simétrico. Para que este "tablero de ajedrez" tenga el tamaño adecuado, vaya al panel de configuración que se encuentra en la pestaña de la interfaz y cambie la ubicación del origen (otra palabra para el centro del mundo) a "Personalizado". Allí puedes cambiar `max-pxcor` y `min-pycor` a 4. Voila, un tablero de ajedrez real.