*** Machine Translated
`ifelse-value` es una primitiva que nos permite comprobar de forma rápida y concisa una serie de condiciones y elegir un valor en consecuencia. Esta primitiva no nos ayuda a escribir muchos consecutiva `if` o `ifelse` declaraciones.

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


Sin embargo, tantas `if` dificultan la lectura del código. En su lugar, podemos usar la `ifelse-value` la siguiente manera para hacer un código mucho más conciso:



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


Cosas a tener en cuenta al usar `ifelse-value` :

- Debe envolver todo `ifelse-value` entre paréntesis `()` .
- Puede proporcionar un último conjunto de comandos entre corchetes pero sin ninguna condición anterior. Este último conjunto de comandos se tratará como una `else` , especificando lo que sucederá si ninguna de las condiciones es verdadera. También puede omitir esta condición final.


En el ejemplo de modelo a continuación, tenemos seis formas de dados. Cada vez que hacemos clic en el botón de *rodar todo* , cada tortuga elige un número aleatorio entre 1 y 6. Luego, usamos la `ifelse-value` ifelse para elegir la forma de tortuga correcta para representar el valor del dado correspondiente.