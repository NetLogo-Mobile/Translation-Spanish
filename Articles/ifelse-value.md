*** Machine Translated
`ifelse-value` es una primitiva que permite al usuario verificar rápida y concisamente una serie de condiciones y ejecutar código diferente según los resultados. No hay nada que se puede hacer con `ifelse-value` que no se podía ya ver con una serie de `if` o `ifelse` declaraciones, pero la fuerza de `ifelse-value` está en su eficiencia sintáctica. Por ejemplo, supongamos que desea comprobar en cuál de los cuatro cuadrantes del mundo se encuentra una tortuga determinada. En comparación con la `if` , la `ifelse-value` es posiblemente mucho más limpia. 

```
to-report report-quadrant-if
  if xcor > 0 and ycor > 0 [
	report 1
  ]
  if xcor < 0 and ycor > 0 [
	report 2
  ]
  if xcor < 0 and ycor < 0 [
	report 3
  ]
  if xcor > 0 and ycor < 0 [
	report 4
  ]  
end

to-report report-quadrant-ifelse-value
  report (ifelse-value
	xcor > 0 and ycor > 0 [1]
	xcor < 0 and ycor > 0 [2]
	xcor < 0 and ycor < 0 [3]
                      	[4] ; else
  )
end
```
 Una cosa importante a tener en cuenta sobre el uso de `ifelse-value` es que debe envolver todo entre paréntesis si usa más de una condición. Además, sepa que puede omitir la condición final y el último conjunto de corchetes que escriba se tratará como una `else` , especificando lo que sucederá si ninguna de las condiciones es verdadera.

El siguiente ejemplo muestra un lugar donde `ifelse-value` se puede usar para hacer que el código sea más conciso y, uno que le resulte familiar, más legible: elegir uno de los seis iconos de dado para un seis