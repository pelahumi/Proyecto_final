# Proyecto_final
En este proyecto se intentará predecir el precio de una casa en función de sus características utilizando un modelo de regresión lineal.

##Índice
  - [Librerías necesarias](#1)
  - [Limpieza de datos](#2)
  - [Interpretación de los datos](#3)
  - [Modelo de regresión](#4)
  - [Evaluación del modelo](#5)
  
---

## Librerías necesarias<a name="1"></a>
Para este proyecto necesitaremos importar las siguinetes librerías:
```python3
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
from statsmodels.api import add_constant, OLS
import warnings
warnings.filterwarnings('ignore')
```

## Limpieza de datos<a name="2"></a>
Lo primero es leer el archivo donde están los datos (csv o excel):
```
df = pd.read_excel("Ubicación del archivo.xls")
```
Buscaremos valores nulos y, en caso de que los hubiese, o los sustituimos por otros más apropiados o eliminamos la fila entera que los contenga. En nuestro caso no hay ningún valor nulo.
Esto lo podemos ver fácilmente con la siguiente función:
```
df.isna().sum()
```
Sumará los valores nulos que hay en cada columna.

## Interpretación de los datos<a name="3"></a>
Para ver la correlación de las columnas de nuestro dataset podemos usar:
```
df.corr()
```
Sin embargo, para tener una perspectiva más visual e intuitiva podemos usar un gráfico de calor como el siguiente:

![heatmap](https://github.com/pelahumi/Proyecto_final/blob/main/Img/heatmap.png)

O si queremos también podemos graficar un scatter plot con la recta de regresión como esta:

![recta regresion](https://github.com/pelahumi/Proyecto_final/blob/main/Img/regresion.png)

## Modelo de regresión<a name="4"></a>
Para este apartado necesitaremos las siguientes librerías:
```
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler, MinMaxScaler
from sklearn.linear_model import LinearRegression
```
Dividiremos en variables dependientes e independientes y los datos en train (80% de los datos) y test (20% de los datos). 
El modelo que utilizaremos será de regresión lineal.
Los scalers se usan para hacer transforaciones de los datos y  así ajustarlos. Crearemos tres modelos: uno sin scalers, uno con el standard scaler y otro con el min max scaler.
Solo falta entrenar el modelo y realizar las predicciones.

## Evaluación del modelo<a name="5"></a>
Importamos la siguiente librería:
```
from sklearn.metrics import mean_squared_error as mse
```
Por último, calculamos el score de nuestros tres modelos y vemos la precisión de los mismos. También, para asegurarnos con mayor seguridad la veracidad de nuestros modelos podemos calcular el error medio: 
```
mse(y_train, ln.predict(X_train), squared=False)
mse(y_test, preds, squared=False)
