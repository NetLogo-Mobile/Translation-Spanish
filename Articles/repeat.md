*** Machine Translated
`repeat` te permite ejecutar cualquier conjunto de comandos *n* cantidad de veces. Toma la forma de:

```repeat n [ commands ] ```

Por ejemplo, si le pides a una tortuga que `repeat 10 [ forward 1 ]`, ejecutará esos comandos 10 veces consecutivas, lo que dará como resultado que la tortuga avance 10 unidades hacia adelante. Puedes usar la `repeat` en cualquier contexto siempre que esté dentro de un comando de preguntar o fuera de un comando de preguntar. `repeat` puede ser especialmente útil al dibujar formas. Por ejemplo, el siguiente código haría que las tortugas dibujaran un cuadrado:

```
 ask turtles [
  pen-down
      repeat 4 [
      forward 10
      right 90
   ]
]
```