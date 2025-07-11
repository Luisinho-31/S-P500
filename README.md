# S-P500
Serie de tiempo para cada acción del S&amp;P 500 utilizando modelos Arima y Prophet 

# S&P 500 Time Series Forecasting 
Este proyecto utiliza modelos de series de tiempo para predecir el comportamiento del índice S&P 500, empleando la librería Prophet. Está desarrollado en Python con Google Colab.


## Herramientas utilizadas

- Python 
- Prophet
- ARIMA
- Pandas y Matplotlib
- Google Colab
- Widgets interactivos para selección de acciones
- Dataset histórico del S&P 500
- Kaggle

## Fuente de datos:
Kaagle:  https://www.kaggle.com/datasets/camnugent/sandp500

## Dataset
Se tiene una variedad de archivos, el archivo que usaremos es el que contiene todas las empresas, el tamaño que se tiene es de 619040 registros, con 7 columnas
al eveluar la calidad de datos nos encontramos 11 valores nulos, pero es una cantidad muy pequeña para la cantidad de registros que tenemos, se realizó una conversion de tipo de dato en la columna de tiempo, para un mejor manejo

## Objetivo 
El objetivo principal es realizar la prediccion a travez de series de tiempo, de acciones de las 500 empresas mas grandes

## Proceso 
El proyecto se realizó en un notebook de Google Colab. Los primeros pasos consistieron en cargar un dataset con los valores históricos de diferentes acciones del índice S&P 500. Se realizó una limpieza de datos, dando formato al tipo de dato de la fecha, tambien se observó la cantidad de nulos existentes, en este caso es minima la cantidad 
Posteriormente, se añadio un menú desplegable que permite seleccionar una acción específica del S&P 500 mediante, una vez seleccionada, se filtra la accion y para poder construir la serie de tiempo.

Posteriormente se entrenó el modelo de Prophet el cual nos ayuda a realizar predicciones a futuro con los datos que se le otorguen, en este caso se le agregaron los ultimos dias para la accion que se desea obtener, al igual se realizó con un menú desplegable para que sea de manera interactiva y asi obtener tanto como nuestra predicción como el historico

Para evaluar el modelo, se calculó el Error Absoluto Medio (MAE), el cual en este caso fue de 1.67% lo cual nos dice que nuestro modelo esta dando buenos resultados o es confiable.

## Estructura del proyecto

 **Carga de datos**  
   Lectura del dataset con valores históricos de diferentes acciones pertenecientes al S&P 500.

 **Selección dinámica de acción**  
   Uso de widgets para elegir una acción específica a analizar.

 **Preprocesamiento**  
   Limpieza y formato de fechas.

 **Modelado con Prophet**  
   Se crea un modelo para cada acción seleccionada y se genera la predicción de los próximos días.

**Visualización**  
   - Gráfica de la predicción completa.
   - Comparación de valores reales vs predichos.
   - Cálculo del **Error Absoluto Medio (MAE)**.



##  Evaluación del modelo

El rendimiento se evalúa con el **MAE (Mean Absolute Error)**.  
Ejemplo:  
> MAE = 21.04  
> Valor promedio del índice = 1259  
> Error relativo = **1.67%**

--
## Autor
Luis Fernando Castillo https://github.com/Luisinho-31
