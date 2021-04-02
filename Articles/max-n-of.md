*** Machine Translated
`Max-n-of` informa un conjunto de agentes que contiene un **número específico de agentes** con el **valor más alto de un reportero determinado** . Toma la forma de:

```max-n-of number agentset [ reporter ]```

Por ejemplo, `max-n-of 3 patches [ count turtles-here ]` devolvería un conjunto de agentes de los tres parches que tienen la mayor cantidad de tortugas. Si hay menos del número especificado de tortugas en un conjunto de agentes dado, `max-n-of` devolverá el conjunto de agentes completo. Por ejemplo, si solo tenemos 5 tortugas en un modelo y ejecutamos un `max-n-of 10 turtles [ size ]` , las 5 tortugas serían devueltas. Los lazos se rompen al azar.

En el modelo siguiente, hay células que crecen y se dividen. Cada décimo tic, pedimos a las tres células más grandes que se dividan usando `max-n-of` .