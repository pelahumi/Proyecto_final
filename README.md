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
Buscaremos valores nulos y, en caso de que los hubiese, o los sustituimos por otros más apropiados o eliminamos la fila entera que los contenga. En nuestro caso no hay ningún valor nulo.
Esto lo podemos ver fácilmente con la siguiente función:
```
df.isna().sum()
```
Sumará los valores nulos que hay en cada columna.
