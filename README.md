# Proyecto_final
En este proyecto se intentará predecir el precio de una casa en función de sus características utilizando un modelo de regresión lineal.

### Limpieza de datos
Buscaremos valores nulos y, en caso de que los hubiese, o los sustituimos por otros más apropiados o eliminamos la fila entera que los contenga. En nuestro caso no hay ningún valor nulo.
Esto lo podemos ver fácilmente con la siguiente función:

´´´
df.isna().sum()
´´´

Sumara los valores nulos que hay en cada columna.
