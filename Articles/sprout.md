*** Machine Translated
`sprout` es una primitiva de solo parche que nos permite pedir parches para crear nuevas tortugas. Debe usarse dentro de un contexto `ask patches [...]` Por ejemplo, si quisiéramos crear un modelo en el que a cada parche le brotara una flor una vez que se riega lo suficiente, escribiríamos el siguiente código:



```
ask patches [
	if water-level > 10 [
		sprout 1 [
			set shape "flower"
			set color yellow
			set size 0.1
		]
	]
]
```


Cosas a tener en cuenta al usar `sprout` :

- Un parche puede brotar tantas tortugas como se proporcionen.
- `sprout` dará como resultado un resultado idéntico al de `create-turtles` , pero asignará automáticamente las coordenadas de las nuevas tortugas al centro del parche de brotación.
- Al igual que en `create-turtles` , puede pasar reglas opcionales para que las sigan las nuevas tortugas simplemente agregando los corchetes ( `[ ]` ) al final de una `sprout` como se muestra arriba.
- `sprout` también se puede utilizar con razas. Por ejemplo, si tuviéramos una *variedad de plantas* , podríamos usar `sprout-plants 3` .
- A menos que se especifique en los comandos, las nuevas tortugas tendrán encabezados y colores aleatorios.
- Solo los `patches` pueden *brotar* nuevas tortugas. Si necesita que sus tortugas creen nuevas tortugas, debe usar `hatch` .


En el ejemplo de modelo a continuación, tenemos un jardín vacío y un agricultor. Nuestro agricultor se mueve al azar y fertiliza cada parche. Cuando se fertiliza un parche, su `pcolor` vuelve marrón más claro. Una vez que un parche alcanza un cierto nivel de fertilización, brota una nueva planta. Si el agricultor fertiliza un parche que ya tiene una planta allí, el fertilizante ayuda a que la planta crezca.