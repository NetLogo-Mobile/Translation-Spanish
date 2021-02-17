*** Machine Translated
`Member?` se puede usar con **listas** o conjuntos de **agentes** , pero se usa más comúnmente con listas. `Member?` informa **True** si el valor o agente dado aparece en la lista o conjunto de agentes dados, y toma la forma:

`member? value list or member? agent agentset`

Por ejemplo, `show member? 5 [ 3 4 5 6 ]` reportaría **Verdadero** y `show member? 5 [1 3 2 ]` reportaría **Falso** ; `show member? turtle 0 turtle` reportaría **Verdadero** , mientras que `show member? patch 0 turtles` reportarían **Falso** .

En el modelo a continuación, hay un club exclusivo al que solo puede ingresar si está en la Lista de miembros. Cuando una tortuga se acerca al club, ¿solo si es `member? self members-list` devuelve verdadero si pueden entrar.