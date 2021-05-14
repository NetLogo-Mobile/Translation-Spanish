*** Machine Translated
`ifelse-value` es una primitiva que nos permite verificar rápidamente y concisamente una serie de condiciones y elegir un valor en consecuencia. Esta primitiva nos ayuda a no escribir muchas declaraciones "if" o "ifelse" consecutivas.



Por ejemplo, si quisiéramos comprobar en cuál de los cuatro cuadrantes del mundo se encuentra una determinada tortuga, nuestra primera opción es escribir un código de la siguiente manera:

```
to-report where-am-i
  if xcor > 0 and ycor > 0 [
    	report "upper-right"
  ]
  if xcor < 0 and ycor > 0 [
    	report "upper-left"
  ]
  if xcor < 0 and ycor < 0 [
    	report "lower-left"
  ]
  if xcor > 0 and ycor < 0 [
    	report "lower-right"
  ]  
end
```



Sin embargo, esta cantidad de declaraciones `if` dificulta la lectura del código. En su lugar, podemos usar la primitiva `ifelse-value` de la siguiente manera para hacer un código mucho más conciso:



```
to-report where-am-i
  report (ifelse-value
    	xcor > 0 and ycor > 0 ["upper-right"]
    	xcor < 0 and ycor > 0 ["upper-left"]
    	xcor < 0 and ycor < 0 ["lower-left"]
    	["lower-right"] ; if none of the conditions are true
  )
end
```



Cosas a tener en mente cuando usas `ifelse-value`:

* Debes envolver el `ifelse-value` en complete entre paréntesis `()`.
* Puedes proporcionar un último conjunto de comando entre corchetes pero sin ninguna condición anterior. Este último conjunto de comandos se tratará como una declaracíon de `else`, especificando lo que sucederá si ninguna de las condiciones son ciertas. También puedes omitir esta condición.



En el modelo a continuación, tenemos seis dados. Cada vez que hacemos clic en el botón *roll-all*, cada tortuga elige un número aleatorio entre 1 y 6. Luego, usamos la primitiva `ifelse-value` para elegir la forma correcta de la tortuga para representar el calor del dado correspondiente.