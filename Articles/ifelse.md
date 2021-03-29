`ifelse` , al igual que `if` , se utiliza para ejecutar ciertos comandos de forma condicional, es decir, en función de alguna condición de verdadero o falso. `ifelse` se utiliza cuando deseas ejecutar un conjunto de comandos *si* una condición es verdadera y otro conjunto en caso contrario.

Por ejemplo, al comienzo de muchos partidos deportivos, se lanza una moneda para determinar quién recibe la pelota primero. *si* el equipo A gana, recibe el balón; *de lo contrario* (en caso contrario), el equipo B recibe el balón. para poner esto en el código NetLogo, diríamos: 

```
ifelse team-A-wins-flip [
	give-team-A-ball
] [
	give-team-B-ball
]
```
 Este ejemplo simula carros que conducen por una calle y se detienen en una estación de servicio para llenar sus tanques antes de continuar. Cada tic, cada automóvil verifica si están en la estación de servicio (si la parcela en la que están tiene una coordenada x de 0) y si tienen menos de un tanque lleno de gasolina. Si es así, comienzan a llenar el tanque; de lo contrario, comienzan a conducir. Cada vez que un automóvil conduce, pierde un poco de gasolina, por lo que cuando regresa a la estación de servicio nuevamente, se llena nuevamente.