# Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional

En este proyecto se busca un modelo que pueda identificar monedas peruanas (10 céntimos y 20 céntimos), además de entender que características de la moneda está tomando el modelo para poder definir a que categoría pertenece la predicción.

Contamos con estos datos de entrada.

![alt text](https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/Datos.png)

Que se realizó con 50 fotos de monedas de 10 y 20 céntimos y a dichas monedas se les rotó 5 grados en una escala de grises, obteniendo unas 7200 imágenes. Las fotos de las monedas se recortaron, para obtener solo el centro de la moneda, esto se realizó con el siguiente criterio:

  - Se recortó la foto para obtener toda la imagen de la moneda.
  - Se escaló la imagen con OpenCV para que tenga 500 píxeles tanto de altura como de anchura.
  - Se recortó la imagen para obtener solo la imagen de las monedas, calculando las coordenadas tomando el radio de la imagen que sería 250 píxeles y calculando la distancia para poder recortar solo la parte del centro.
  - Se escaló en grises, para bajar el costo computacional al momento de realizar las convoluciones, y calculos.

![alt text](http://1.bp.blogspot.com/_J6WT_LBxSss/ShmPGq671uI/AAAAAAAAGgw/rjRxGhgbXas/s400/squareround%5B1%5D.gif)

## Modelo

La red neuronal convolucional que se utilizó se detalla en la siguiente imagen:

