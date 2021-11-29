`any?` se usa para determinar si hay al menos un agente dentro de un conjunto de agentes determinado. Si los hay, devolverá **verdadero** ; de lo contrario, devolverá **falso**.



Por ejemplo, el siguiente código repetiría la ejecución del `go` de forma repetida siempre que haya al menos 1 tortuga en el modelo. Si, digamos, hubiera muchas tortugas pero pudieran `die`, el modelo se detendría cuando todas las tortugas murieran.



```
to go
	if not any? turtles [
		stop
	]
	tick
end
```



Podemos combinar `any?` con un reportero condicional que usa la `with` como el siguiente ejemplo que detiene el modelo si alguna de las tortugas en el modelo es menor que 1 unidad:



```
if any? turtles with [size < 1] [stop]
```



¿Cosas a tener en cuenta al usar `any?` :

- No te olvides del signo de interrogación (`?`) al final.
- Puedes usar el `not` primitivo, como en el ejemplo anterior, para revertir el resultado de `any?`.
- `any?` en sí mismo no hace nada; debe usarlo dentro de una declaración condicional como `if` y `if-else` u otras primitivas que requieren valores verdadero-falso como `while` .



El siguiente ejemplo de modelo representa la propagación de una enfermedad contagiosa dentro de una población sana. Usamos el primitivo `any?` para ejecutar el modelo siempre que haya al menos un individuo sano (verde) en el modelo. Una vez que todos los individuos se ponen rojos, el modelo se detiene automáticamente.