*** Machine Translated
`globals` es una primitiva que usamos para definir *variables globales* personalizadas en NetLogo. Una variable global es una variable que tiene el mismo valor para todos los agentes del modelo en todos los procedimientos. Puede definir sus variables globales personalizadas escribiendo `globals` seguidas de corchetes `[]` .



```
globals [
	temperature
	oil-price
	usd-eur-exchange-rate
]
```


Una vez que defina una variable global, puede usar la primitiva de `set` para cambiar su valor:



```
set usd-eur-exchange-rate 0.85
set temperature 36
```


Y use su nombre para acceder a su valor en su código como cualquier otra variable:



```
if oil-price < 1.5 and usd-eur-exchange-rate < 0.8 [
	buy-oil
]
```


Cosas a tener en cuenta al usar `globals` :

- Cuando se crea un elemento de interfaz, tales como un *control deslizante,* *conmutador* o *selector,* su nombre se convierte automáticamente en una variable global y no es necesario definirlo dentro de las `globals` primitivas.
- No puede tener dos variables globales con el mismo nombre.
- No puede comenzar un nombre de variable con un número. Por ejemplo, el siguiente código mostraría un error `globals [1st-offer]` .
- Siempre debe definir sus variables globales al comienzo de su código NetLogo.
- Si desea crear una variable que solo se necesita temporalmente y dentro de un solo procedimiento específico, debe usar la primitiva `let` lugar.
- Si necesita una variable que tenga un valor diferente para cada tortuga, cada parche o cada enlace, debe usar una de las siguientes primitivas: `turtles-own` , `patches-own` , `links-own` .


En el ejemplo de modelo a continuación, tenemos algunas manchas marrones que representan la tierra y algunas manchas verdes que representan bayas. También tenemos cinco tortugas que representan a las personas que recogen las bayas. Usamos una variable global para realizar un seguimiento del número total de bayas recolectadas por todas las personas en el modelo. En la `setup` procedimiento, lo ponemos a 0, y luego en el `go` procedimiento, cada vez que una persona agarra una baya (se vuelve un parche de verde a marrón), incrementamos el `berries-picked` variable global por uno. Verificamos el valor de esta variable global en cada tic. Si nuestros recolectores recogieron 60 o más bayas, detenemos el modelo. También mostramos el valor de esta variable a través de un monitor en la interfaz del modelo.