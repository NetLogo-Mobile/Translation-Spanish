*** Machine Translated
`Random-normal` es similar a la primitiva `random`, ya que genera e informa un número aleatoriamente. Sin embargo, `random` y `random-normal` difieren en la distribución que generan. `Random` producirá una **distribución uniforme**, lo que significa que cada número tiene la misma probabilidad de ser generado, y habrá aproximadamente la misma cantidad de cada número. Entonces, en `random 4`, 0, 1, 2 y 3 tienen la misma probabilidad de generarse, y después de muchas repeticiones de `random 4`, habrá un número igual de 0, 1, 2 y 3.

Pero `random-normal` producirá una **distribución normal**, que parece una curva de campana con muchos valores en el medio y menos valores en las colas superior e inferior. Su sintaxis es:

```random-normal mean standard-deviation ```

Las distribuciones normales se encuentran con más frecuencia en la naturaleza que las distribuciones uniformes y pueden agregar precisión a su modelo. Así que `random-normal 5 1` representaría una distribución normal con una media de 5 y una desviación estándar de 1; es mucho más probable que se generen números cercanos a 5 que 3 o 7, que son dos desviaciones estándar de la media.

En el modelo siguiente, modelamos las alturas de 100 personas al azar. Debido a que en la vida real la altura se distribuye normalmente, queremos que más personas tengan la estatura media que muy altas o muy bajas. Al observar el histograma, puede ver la diferencia entre una distribución uniforme de altura y una distribución normal.