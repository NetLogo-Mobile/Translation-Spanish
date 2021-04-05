`let` crea una nueva variable local y establece su valor inicial. Una variable local es una variable que solo existe dentro del procedimiento en el que se creó o entre paréntesis de una declaración específica de `ask`. Similar a una variable `global`, el valor de una variable local es el mismo para todas las tortugas.



```
ask turtles [
	let people-nearby (other turtles in-radius 2)
  if any? people-nearby [
  	let new-friend one-of people-nearby
  	set my-friends (lput new-friend my-friends)
  ]
]
```



Una vez que creas una variable local con `let`, puedes usar la primitiva `set` para asignarle un nuevo valor. `let` es muy útil para calcular valores temporales o crear conjuntos de agentes temporales. Por ejemplo, si quisiéramos que una tortuga lanzara 6 dados e informara la suma de los dados, podríamos usar `let` como se muestra a continuación:



```
to-report roll-six
	let total-outcome 0
	repeat 6 [
		let new-outcome (one-of [1 2 3 4 5 6])
		set total-outcome (total-outcome + new-outcome)
	]
	report total-outcome
end
```



En el ejemplo de modelo a continuación, tenemos algunas tortugas felices y otras tristes. Cada vez que dos tortugas están en la misma parcela, una le pedirá a la otra que cambie su forma. En cierto modo, una tortuga triste entristecerá a su amigo, o una tortuga feliz hará feliz a su amigo. Usamos `let` en este modelo porque nos permite no reescribir un fragmento de código más largo una y otra vez (`other turtles-here`).