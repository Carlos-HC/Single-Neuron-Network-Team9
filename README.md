# **Modelo de una sola neurona - Clasificación de cáncer de mama**  

## **1. Resumen del proyecto**  

Este proyecto implementa un modelo de aprendizaje automático basado en una sola neurona para clasificar tumores de mama como benignos o malignos. Posteriormente se aplica PCA a los datos para reducir la complejidad de el conjunto de datos. Por último se comparan ambos modelos y se determina cuál es mejor para un caso real.   

El modelo se entrena utilizando el Wisconsin Breast Cancer Dataset, el cual contiene características calculadas a partir de imágenes de biopsias de tumores.  

## **2. Descripción del dataset**  

El dataset contiene 569 muestras de tumores de mama con 30 variables predictivas derivadas de 10 características principales:
- radio

- textura

- perímetro

- área

- suavidad

- compacidad

- concavidad

- puntos cóncavos

- simetría

- dimensión fractal

Para cada característica se calculan:

- media

- desviación estándar

- peor valor

La variable objetivo es:

- **Diagnosis:** 0 = Benigno, 1 = Maligno  

## **3. Metodología del entrenamiento**  

**1. Data Cleaning:**  
 Se revisó el dataset para identificar valores faltantes o características irrelevantes que pudieran afectar el entrenamiento del modelo.  

**2. Exploratory Data Analysis:**  
Se analizaron las variables del dataset mediante estadísticas descriptivas y visualizaciones para comprender la distribución de las características y su relación con la variable objetivo.  


**3. Feature Scaling:**  
Las variables predictivas fueron estandarizadas para asegurar que todas las características tengan una escala comparable durante el entrenamiento del modelo.  

**4. Train/Test Split:**  
El dataset se dividió en conjuntos de entrenamiento, validación y prueba para entrenar el modelo y evaluar su desempeño.  

**5. Entrenamiento del modelo:**  
Se implementó un modelo de clasificación binaria basado en una sola neurona.  

**6. Evaluación del modelo:**  
El modelo fue evaluado utilizando el conjunto de prueba mediante métricas de clasificación como precisión, recall, especificidad y F1-score.  

**7. Reducción de dimensionalidad mediante PCA**  
Se aplicó PCA a las variables predictivas estandarizadas para reducir la dimensionalidad del dataset. Se seleccionaron los componentes principales que explican al menos el 95% de la varianza total.

Posteriormente se entrena otro modelo usando los componentes principales obtenidos con el PCA y se compara el desempeño de cada modelo. 


## **4. Requisitos**  
El proyecto utiliza Python y las siguientes librerías:

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- scipy
- jupyterlab
- tensorflow
- plotly.express

## **5. Cómo ejecutar el proyecto**

**1.** Clonar el repositorio usando git clone.  
**2.** Entrar a la carpeta del proyeco.  
**3.** Abrir el notebook "single-neuron.ipynb".  
**4.** Correr todas las celdas.  