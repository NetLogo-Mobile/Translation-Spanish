*** Machine Translated
`patch-ahead` informa el parche único que es la distancia dada *por delante* de esta tortuga. Puedes pensar en ella como la tortuga mirando un parche frente a ella. La sintaxis de `patch-ahead` es

`patch-ahead distance`

La distancia puede ser un número entero o decimal, y es qué tan lejos estará el parche que informa el `patch-ahead` Por ejemplo, para convertir el parche 3 unidades frente a una tortuga verde, diríamos:



```
ask patch-ahead 4 [ set pcolor green ] 
```


**Nota** : Este reportero no informará a `nobody` si el parche no existe (es decir, si el parche está fuera de las coordenadas dadas de NetLogo). En el modelo a continuación, queremos que el automóvil conduzca solo en parches grises y no rojos. Por lo tanto, usamos el `patch-ahead` para hacer que el automóvil se detenga, si el parche de adelante es rojo.