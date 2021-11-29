`diffuse` es un primitivo observador que actúa en cada parcela del modelo. Hace que cada parcela difunda (o distribuya) el valor de una variable de parche dada a sus 8 parcelas vecinas. Esta primitiva es muy útil cuando queremos simular procesos donde ocurre la difusión como la difusión de un olor o la contaminación en el aire.



Por ejemplo, si cada parcela tuviera una variable de *contaminación* que mantuviera un registro de cuán contaminado estaba esa parcela, podrías usar (como observador, no dentro de un bloque de `ask patches` solicitud) `diffuse heat 0.5` y cada parcela distribuiría por igual la mitad de su calor a sus 8 vecinos circundantes. Cada vecino obtendría 1/8 de la 1/2 del calor original, lo que haría que el calor de cada vecino aumentara pero el calor del parche original se redujera a la mitad.



Cosas a tener en cuenta cuando usas `diffuse`:

* No se puede usar `diffuse` dentro del `ask` bloque. Es una primitiva solo para observadores.
* También puedes usar la primitiva `diffuse4` si deseas lograr el mismo resultado exacto pero con los 4 vecinos de dirección cardinal.



En el ejemplo de modelo a continuación, usamos `diffuse` para modelar la contaminación del aire de una fábrica. Con cada tic, la fábrica libera algo de contaminante al aire aumentando la variable de contaminación de la parcela allí en 1. Luego, la contaminación se difunde desde esta parcela original a sus vecinos, y luego de sus vecinos a los vecinos de sus vecinos, y así en. Como resultado, el contaminante se esparce por el aire, creando zonas y focos de contaminación.