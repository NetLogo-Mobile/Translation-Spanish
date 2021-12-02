`turtles-here` informa un conjunto de **agentes** que contiene todas las tortugas en la misma parcela con la tortuga original, incluida la tortuga original en sí. Por ejemplo, si quisiéramos crear un modelo de enfermedad contagiosa donde las tortugas rojas transmitieran la enfermedad a todas las tortugas en la misma parcela, escribiríamos el siguiente código:



```
ask turtles with [color = red][
	ask turtles-here [
		set color red
	]
]
```


Cosas a tener en cuenta cuando usamos `turtles-here`:

* A menudo no es deseable tener la tortuga original en el conjunto de agentes que informa `turtles-here`. Incluso puedes causar errores en raras ocasiones. Por ejemplo, el siguiente código mostraría un error `ask turtles [ create-links-with turtles-here ]` porque la tortuga original intentaría crear un enlace consigo misma. En tales casos, podemos usar la `other` primitiva. Por ejemplo, el siguiente código no mostraría un error: `ask turtles [ create-links-with other turtles-here ]`.
* Siempre podemos usar el `with` para delimitar el conjunto de agentes informado por las `turtles-here`. Por ejemplo, el siguiente código solo reportaría las tortugas rojas que están en el mismo parche con la tortuga original: `turtles-here with [color = red]`.
- También puedes usar `turtles-here` con razas personalizadas cambiando el término *tortugas* con el nombre plural de la raza como `<breed>-here`. Por ejemplo: `ask goats [ if any? plants-here [ eat ] ]`.


En el ejemplo de modelo a continuación, tenemos tres parcelas blancas que representan hospitales y algunas tortugas que representan personas. Algunas de nuestras tortugas son verdes, lo que indica que están sanas, y algunas son violetas/moradas, lo que indica enfermedad. Usamos `turtles-here` para pedir manchas blancas para curar a las personas violetas.