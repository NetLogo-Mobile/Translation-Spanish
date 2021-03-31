`move-to` permite que una tortuga establezca sus coordenadas xey para que sean las mismas que las de otra tortuga o parcela sin alterar las otras variables de la tortuga (por ejemplo, rumbo, color, tamaño). Su sintaxis es:

```move-to desired-agent ```

Por ejemplo, si quisiéramos que cada conejo se moviera a la ubicación exacta de una parcela verde elegido al azar, diríamos: 

```
ask rabbits [
	move-to one-of patches with [pcolor = green]
	eat-grass
]
```
 **Tenga en cuenta** que si la tortuga o la parcela de destino no existe, el modelo dará un error. En el modelo a continuación, hay una familia y su casa. Queremos que la familia esté en su casa y que usemos la `move-to` mudanza para mudarlos allí.