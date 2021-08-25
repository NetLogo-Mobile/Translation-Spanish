*** Machine Translated
`turtles-own` nos permite definir características de tortuga personalizadas (variables) para todas las tortugas en un modelo (además de las características de tortuga predeterminadas como `color` , `size` y `heading` ). Aunque el nombre de la característica será el mismo para todas las tortugas, cada tortuga tendrá un valor diferente para estas características personalizadas. Una vez que creamos tales características personalizadas, podemos usar la primitiva de `set` para cambiar su valor. Por ejemplo, si quisiéramos crear un modelo de vehículos eléctricos en el que cada carro tuviera un nivel diferente de batería restante, escribiríamos el siguiente código:



```
turtles-own [remaining-battery passengers]
to setup
	clear-all
	create-turtles 100 [
		set shape "car"
		set remaining-battery random 100
		set passengers one-of [1 2 3]
	]
	reset-ticks
end
to go
	ask turtles [
		if remaining-battery > 0 [
			forward 1
			set remaining-battery remaining-battery - 1
		]
	]
	tick
end
```


Cosas a tener en cuenta al usar `turtles-own` :

- Siempre debes usar `turtles-own` al principio de tu código, en la parte superior de la pestaña de código.
- Podemos definir múltiples características dentro de una primitiva `turtles-own` las `turtles-own` separando cada característica con un espacio.
- Puede crear características específicas de la `<breed>-owns` formato de `<breed>-owns` . Por ejemplo, si tuviéramos un modelo con *bancos* y *clientes* , podríamos escribir `banks-own [balance customer-list] customers-own [income]` . Si tiene varias razas en su modelo, las características definidas con `turtles-own` se aplicarán a todas las tortugas independientemente de su raza.


En el ejemplo de modelo a continuación, tenemos tres carros en tres carreteras paralelas. Cada carro tiene una cantidad diferente de gasolina en su tanque, que se muestra con una etiqueta al lado de cada carro. Cuando se hace clic en el botón *Ir* , cada carro comienza a avanzar hasta que se queda sin gasolina.