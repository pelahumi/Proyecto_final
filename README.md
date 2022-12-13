# Proyecto_final
En este proyecto se intentará predecir el precio de una casa en función de sus características utilizando un modelo de regresión lineal.

## Librerías necesarias
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

### Limpieza de datos
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

## Interpretación de los datos
Para ver la correlación de las columnas de nuestro dataset podemos usar:
```
df.corr()
```
Sin embargo, para tener una perspectiva más visual e intuitiva podemos usar un gráfico de calor como el siguiente:

![heatmap](https://github.com/pelahumi/Proyecto_final/blob/main/Img/heatmap.png)

O si queremos también podemos graficar un scatter plot con la recta de regresión como esta:

![recta regresion](https://github.com/pelahumi/Proyecto_final/blob/main/Img/regresion.png)









