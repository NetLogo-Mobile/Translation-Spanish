`sprout` es una primitiva de solo parcelas que nos permite pedir parcelas para crear nuevas tortugas. Se debe usar dentro de un contexto `ask patches [...]`. Por ejemplo, si quisiéramos crear un modelo en el que a cada parcela le brotara una flor una vez que se riega lo suficiente, escribiríamos el siguiente código:



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


Cosas a tener en cuenta cuando usas `sprout`:

* Una parcela puede brotar tantas tortugas como se proporcionen.
* `sprout` dará como resultado un resultado idéntico al de `create-turtles`, pero asignará automáticamente las coordenadas de las nuevas tortugas al centro de la parcela de brotación.
* Al igual que en `create-turtles`, puedes pasar reglas opcionales para que las sigan las nuevas tortugas simplemente agregando los corchetes (`[ ]`) al final de una `sprout` como se muestra arriba.
* `sprout` también se puede usar con razas. Por ejemplo, si tuviéramos una *variedad de plantas*, podríamos usar `sprout-plants 3`.
- A menos que se especifique en los comandos, las nuevas tortugas tendrán encabezados y colores aleatorios.
- Solo los `patches` pueden *brotar* nuevas tortugas. Si necesita que sus tortugas creen nuevas tortugas, debes usar `hatch`.


En el ejemplo de modelo a continuación, tenemos un jardín vacío y un agricultor. Nuestro agricultor se mueve al azar y fertiliza cada parcela. Cuando se fertiliza una parcela, su `pcolor` vuelve marrón más claro. Una vez que una parcela alcanza un cierto nivel de fertilización, brota una nueva planta. Si el agricultor fertiliza una parcela que ya tiene una planta allí, el fertilizante ayuda a que la planta crezca.