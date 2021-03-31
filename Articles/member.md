`Member?` se puede usar con **listas** o **conjuntos de agentes** , pero se usa más comúnmente con listas. `Member?` informa **Cierto** si el valor o agente dado aparece en la lista o conjunto de agentes dados, y toma la forma:

```member? value list or member? agent agentset```

Por ejemplo, `show member? 5 [ 3 4 5 6 ]` reportaría **Cierto** y `show member? 5 [1 3 2 ]` reportaría **Falso** ; `show member? turtle 0 turtle` reportaría **Cierto** , mientras que `show member? patch 0 turtles` reportaría **Falso**.

En el modelo a continuación, hay un club exclusivo al que solo puede ingresar si está en la Lista de Miembros. Cuando una tortuga se acerca al club, solo si `member? self members-list` devuelve cierto pueden entrar.