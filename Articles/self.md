`self` es un elemento primitivo que es útil cuando necesitamos que un agente se refiera a sí mismo dentro de una declaración `ask` `self` es muy útil para asignar una tortuga a una variable global. Por ejemplo, si tuviéramos una parcela de restaurante al que todos nuestros clientes tuvieran que ir, escribiríamos el siguiente código 

```
globals [the-restaurant]
to setup
 	ask one-of patches [
 		set color yellow
 		set the-restaurant self
 	]
end
to go 
	ask turtles [
		facer the-restaurant
		forward 1
	]
end
```


En el ejemplo de modelo a continuación, tenemos un modelo que es similar al popular juego en línea [*agar.io.*](https://en.wikipedia.org/wiki/Agar.io) Tenemos muchas tortugas que representan círculos y se mueven al azar. Cuando dos tortugas se tocan, la tortuga más grande se *come a* la tortuga pequeña. Usamos `self` para dos propósitos: primero para comparar las dos tortugas en contacto dentro de una `ask` para elegir la más grande, y luego para agregar los tamaños de las dos tortugas en contacto.