*** Machine Translated
`move-to` permite que una tortuga establezca sus coordenadas xey para que sean las mismas que las de otra tortuga o parche sin alterar las otras variables de la tortuga (por ejemplo, rumbo, color, tamaño). Su sintaxis es:

`move-to desired-agent`

Por ejemplo, si quisiéramos que cada conejo se moviera a la ubicación exacta de un parche verde elegido al azar, diríamos: 

```
ask rabbits [
	move-to one-of patches with [pcolor = green]
	eat-grass
]
```
 **Tenga en cuenta** que si la tortuga o el parche de destino no existe, el modelo dará un error. En el modelo a continuación, hay una familia y su casa. Queremos que la familia esté en su casa y que usemos la `move-to` mudanza para mudarlos allí.