*** Machine Translated
`other` informa un conjunto de agentes que es el mismo que el conjunto de agentes de entrada pero omite el agente que solicita. Es muy útil cuando queremos que las tortugas se comuniquen entre sí. Por ejemplo, si quisiéramos crear un modelo de red en el que cada tortuga esté conectada a otra tortuga elegida al azar con un enlace, escribiríamos el siguiente enlace:



```
ask turtles [
	create-link-with one-of other turtles
]
```


Usamos `other` en este contexto porque si no lo hiciéramos, existe la posibilidad de que `one-of turtles` informe la misma tortuga. Si esto sucede, NetLogo mostraría un error porque una tortuga no puede crear un vínculo consigo misma.

En el ejemplo de modelo a continuación, tenemos grupos de tortugas estacionarias distribuidas aleatoriamente en el mundo que representan a las personas y tenemos una tortuga móvil que representa a un médico. El médico se mueve al azar y cuando se encuentra con `other turtles` , les pide a las otras tortugas en el mismo parche que se pongan verdes si están sanas y rojas si están infectadas.