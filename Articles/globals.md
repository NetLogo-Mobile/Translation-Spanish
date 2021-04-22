*** Machine Translated
`globals` es una primitiva que usamos para definir *variables globales* personalizadas en NetLogo. Una variable global es una variable que tiene el mismo valor para todos los agentes del modelo en todos los procedimientos. Puedes definir tus variables globales personalizadas al escribir `globals` seguido de corchetes `[]`.



```
globals [
	temperature
	oil-price
	usd-eur-exchange-rate
]
```



Una vez que definas un variable flobal, luego puedes usar la primitiva `set` para cambiar su valor:



```
set usd-eur-exchange-rate 0.85
set temperature 36
```



Y usar su nombre para acceder su valor en el código exactamente como cualquier otro variable:




```
if oil-price < 1.5 and usd-eur-exchange-rate < 0.8 [
	buy-oil
]
```


Cosas para tener en mente cuando usas `globals`:

* No puedes comenzar el nombre de una variable con un número. Por ejemplo, el siguiente código mostraría un error `globals [1st-offer]`.
* Siempre debes definir sus variables globales al comienzo de su código NetLogo.
* Siempre debes definir tus variables globales al comienzo de tu código de NetLogo.
* Si deseas crear una variable que solo sea necesaria temporalmente y dentro de un solo procedimiento específico, debes usar la primitiva `let` en su lugar.
* Si necesitas un variable que tiene un diferente valor para cada tortuga, cada parcela, o cada enlace debes usar una de las siguientes primitivas: `turtles-own`, `patches-own`,`links-own`.



En el ejemplo de modelo a continuación, tenemos algunas manchas marrones que representan la tierra y algunas manchas verdes que representan bayas. También tenemos cinco tortugas que representan a las personas que recogen las bayas. Usamos una variable global para realizar un seguimiento del número total de bayas recolectadas por todas las personas en el modelo. En el procedimiento `setup`, lo configuramos en 0, y luego en el procedimiento `go`, cada vez que una persona toma una baya (cambia una parcela de verde a marrón), incrementamos la variable global `berries-pick` por una. Verificamos el valor de esta variable global en cada tic. Si nuestros recolectores recogieron 60 o más bayas, detenemos el modelo. También mostramos el valor de esta variable a través de un monitor en la interfaz del modelo.