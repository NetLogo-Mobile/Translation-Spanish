`distance` es una primitiva de tortuga y parcelas que informa la distancia entre el agente actual y algún otro agente. Por ejemplo, si deseas imprimir la distancia de la tortuga 0 a la tortuga 1, puedes escribir

`ask turtle 0 [show distance turtle 1]`

o, desde la otra dirección,

`ask turtle 1 [show distance turtle 0]`

Tenga en cuenta que la `distance` respeta cualquier envoltura para la que el mundo está configurado. Entonces, si el mundo se envuelve horizontal o verticalmente, la `distance` informará la distancia más corta entre dos tortugas, que podría estar a lo largo de un camino que envuelve el mundo.

En este ejemplo, la `distance` se usa para implementar una búsqueda de ruta rudimentaria para un leñador. El leñador tiene un árbol "objetivo" al que intentará acercarse y talar. Una vez que tala ese árbol, establecerá su objetivo para que sea el árbol más cercano. (En el caso de las ataduras, se elegirá al azar uno de los más cercanos). Usamos la `distance` para obtener la distancia entre el leñador y todos los árboles para poder determinar cuál es el árbol más cercano.