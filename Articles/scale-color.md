*** Machine Translated
`scale-color` es una primitiva que informa un tono de un color proporcional al valor de un número dado. Por ejemplo, en un modelo de tráfico, se podría usar `scale-color` para colorear los carros con un tanque lleno de gasolina más brillantes que aquellos con un tanque de gasolina más vacío, o, en un modelo de un rebaño de ovejas, colorear áreas más frondosas de hierba. más brillantes que los que ya se han comido.

En la práctica, usas el `scale-color` así:

`scale-color color number range1 range2`

donde el `color` es el tono base deseado (rojo, azul, verde, etc.), el `number` es el valor por el que desea escalar (generalmente una tortuga o una variable de parche), y `range1` y `range2` son parámetros para describir los valores mínimo y máximo de `number` . Si `range1` es menor que `range2` , los números más grandes dan como resultado colores más brillantes, pero si `range2` es menor que `range` , los números más grandes dan como resultado colores más oscuros. Si el `number` está fuera del rango, se elige el tono más claro u oscuro.

En este modelo, `scale-color` se utiliza para modelar la intensidad de la señal de la torre celular. Los parches más cercanos a las torres de telefonía móvil tienen una mejor intensidad de señal y, por lo tanto, tienen un color más brillante que los que están demasiado lejos de una torre para recibir señal.