*** Machine Translated
 `Set` establece una variable en un cierto valor y toma la forma:

 `set variable value`

 Puede establecer variables globales que se han definido en la parte superior del código y variables locales que fueron definidas por `let`. También puede establecer variables pertenecientes al agente que llama al `set` (incluidas las variables de tortuga, raza o parcela definidas por las propias tortugas o parcelas); por ejemplo, 

```
turtles-own [age] 
ask one-of turtles [ 
	set age 10 ]
```
establecería la edad de una tortuga en 10. Las tortugas también pueden acceder y configurar la variable de la parcela en el que se encuentran.

En el siguiente modelo, `set` se usa para cambiar una variedad de variables, incluyendo una variable global, variables de parcelas y variables de tortuga.