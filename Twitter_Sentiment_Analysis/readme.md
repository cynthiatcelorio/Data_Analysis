# Twitter Sentiment Analysis

## Introduction
### Origen
Hacer una introducción diciendo de qué va el dataset, el objetivo y de qué va cada columna etc
### Dataset


## Análisis y limpieza

En primer lugar eliminamos las columnas ___ y ___ que no son utiles

```python
df = df.drop(columns=['ItemID', 'SentimentSource'])
```

Hacer un analisis de la dispersion de datos
![image](https://github.com/user-attachments/assets/879eca0e-7e1a-4cdd-8e0e-b152634b296c)




![image](https://github.com/user-attachments/assets/bc001b16-1d73-453b-9f78-ec102fb3b2c2)


Analizamos las palabras más frecuentes tanto en los casos positivos como los negativos

![image](https://github.com/user-attachments/assets/c6653048-9ced-44af-abba-3c847ba61bb0)

![image](https://github.com/user-attachments/assets/eb0c022f-d6b1-44ae-a266-c14f4ab9c825)

Vemos que antes de limpiar el texto las palabras mas comuness son aticulos o palabras de esas. Este es el caso de las palabras negativas, pero en las positivas se encuentran palabras del mismo tipo

Ahora vamos a analizar lo que vamos a quiitar en la limpieza del texto de los tweets.

Analizamos palabras comunes de los tweets como los # @ y links, estos elemenos hay que eliminarlos ya que no influyen en el signitifcado del texto:

HASHTAG, ARROBAS and URLs

![image](https://github.com/user-attachments/assets/4541874b-418a-4378-a87f-5b8bc63d07a1)


EMOJIS y lista de pabras positivas y negativas

Aquellas palabras que ya sabemos de antemano que son positivas o negativas, las vamos a sustituor por una apalabra clave según su tipo, lo mismo haremos ocn los emoticnos,q ue aumnque no hya muchos los camos a incluir






ESTUDIAR EL USO DE LOS EMOTICONOS. [:), :-), etc] cuantas veces sale eso en el data set

Bag of words 900

## Entrenamiento
# Entrenamiento 1
Tipo, features, resultados
Matriz de confusion

# Conclusion final
