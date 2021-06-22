# Clasificacion de monedas peruanas con una Red Neuronal Convolucional desde cero

**Nota**: Los notebooks que contiene el código y los resultados se encuentran en este repositorio como **Coin Recognition Neural Network Convolutional.ipynb** y **HeatMap.ipynb**

En este proyecto se busca un modelo que pueda identificar monedas peruanas (10 céntimos y 20 céntimos), además de entender que características de la moneda está tomando el modelo para poder definir a que categoría.

Contamos con estos datos de entrada.

<p align="center">
  <img width="500" height="500" src="https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/Datos.png">
</p>

Que se realizó con 50 fotos de monedas de 10 y 20 céntimos y a dichas monedas se les rotó 5 grados en una escala de grises, obteniendo unas 7200 imágenes. Las fotos de las monedas se recortaron, para obtener solo el centro de la moneda, esto se realizó con el siguiente criterio:

  - Se recortó la foto para obtener toda la imagen de la moneda.
  - Se escaló la imagen con OpenCV para que tenga 500 píxeles tanto de altura como de anchura.
  - Se recortó la imagen para obtener solo la imagen de las monedas, calculando las coordenadas tomando el radio de la imagen que sería 250 píxeles y calculando la distancia para poder recortar solo la parte del centro.
  - Se escaló en grises, para bajar el costo computacional al momento de realizar las convoluciones, y calculos.

![alt text](http://1.bp.blogspot.com/_J6WT_LBxSss/ShmPGq671uI/AAAAAAAAGgw/rjRxGhgbXas/s400/squareround%5B1%5D.gif)

## Modelo

La red neuronal convolucional que se utilizó se detalla en la siguiente imagen:

<p align="center">
  <img width="160" height="2000" src="https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/modelo.png">
</p>

## Resultados del modelo

<p align="center">
  <img width="500" height="350" src="https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/plot.png">
</p>
  

<p align="center">
  <img width="500" height="500" src="https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/mc.png">
</p>

## Capas Convolucionales

Para las pruebas de las capas convolucionales se utilizó la imagen de una moneda de 20 céntimos, se puede observar como a más capas convolucionales, las características se reducen.

<p align="center">
  <img width="800" height="360" src="https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/conv2d.jpg">
</p>

<p align="center">
  <img width="800" height="360" src="https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/conv2d_1.jpg">
</p>

<p align="center">
  <img width="800" height="360" src="https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/max_pooling2d.jpg">
</p>

<p align="center">
  <img width="800" height="360" src="https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/conv2d_2.jpg">
</p>

<p align="center">
  <img width="800" height="360" src="https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/conv2d_3.jpg">
</p>

<p align="center">
  <img width="800" height="360" src="https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/max_pooling2d_1.jpg">
</p>

## Heatmap

Podemos observar que el modelo toma las curvas de la moneda como características para definir a que clase pertenece. Y finalmente, podemos obtener la imagen real, con el heatmap encima para diferenciar en que se basó el modelo para definir la clase de la moneda.

<p align="center">
  <img width="800" height="290" src="https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/HeatMap.png">
</p>

Y finalmente, podemos observar como predice el modelo con un 99.999% a la clase de 20 céntimos.

<p align="center">
  <img width="500" height="350" src="https://github.com/cesar-yaranga/Clasificacion-de-monedas-peruanas-con-Red-Neuronal-Convolucional/blob/master/Prediccion.png">
</p>
