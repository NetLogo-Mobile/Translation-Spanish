*** Machine Translated
`While` comienza un bucle que ejecuta un **bloque de comandos**, siempre que un **reportero** dado devuelva **Cierto** . Si el reportero informa **Falso**, se sale del ciclo. Toma la forma:

`while [ reporter ] [ commands ]`

Por ejemplo, para hacer que la tortuga 0 siga avanzando hasta que llegue a una parcela que no tenga otras tortugas, podríamos decir: 

```
ask turtle 0 [ 
    while [ any? Other turtles-here ] [ 
    	forward 1] ]
```


Nota: los bucles while y otros bucles no se usan con frecuencia en los modelos NetLogo. En el modelo a continuación, se usa un `while` de bucle para hacer una tortuga dibujar un cuadrado.