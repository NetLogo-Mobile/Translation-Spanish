`patch-ahead` informa la parcela única que es la distancia dada *por delante* de esta tortuga. Puedes pensar en ella como la tortuga mirando una parcela frente a ella. La sintaxis de `patch-ahead` es

``patch-ahead distance ``

La distancia puede ser un número entero o decimal, y es qué tan lejos estará la parcela que informa el `patch-ahead`. Por ejemplo, para convertir la parcela 3 unidades frente a una tortuga verde, diríamos:



```
ask patch-ahead 4 [ set pcolor green ] 
```


**Nota**: Este reportero no informará a `nobody` si la parcela no existe (es decir, si la parcela está fuera de las coordenadas dadas de NetLogo). En el modelo a continuación, queremos que el automóvil conduzca solo en parcelas grises y no rojas. Por lo tanto, usamos el `patch-ahead` para hacer que el automóvil se detenga, si la parcela de adelante es roja.