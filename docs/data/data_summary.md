# Reporte de Datos

Este documento contiene los resultados del análisis exploratorio de datos.

## Resumen general de los datos

En esta sección se presenta un resumen general de los datos. Se describe el número total de observaciones, variables, el tipo de variables, la presencia de valores faltantes y la distribución de las variables.

## Resumen de calidad de los datos

En esta sección se presenta un resumen de la calidad de los datos. Se describe la cantidad y porcentaje de valores faltantes, valores extremos, errores y duplicados. También se muestran las acciones tomadas para abordar estos problemas.

### 1. Número total de observaciones y variables
- Observaciones (filas): El dataset contiene 299 registros.
- Variables (columnas): Hay 13 columnas, de las cuales 12 son predictoras y 1 es la variable objetivo (target).

### 2. Tipos de variables
- Variables numéricas:
Incluyen valores como edad, fracción de eyección, y niveles de creatinina. Ejemplo: age, ejection_fraction, serum_creatinine.
- Variables categóricas:
Representan valores discretos como fumar o si el paciente tiene diabetes. Ejemplo: smoking, diabetes. 

### 3. Presencia de valores faltantes
- Resumen de valores faltantes:
Este dataset no tiene valores faltantes explícitos en las columnas (¡excelente calidad de datos!).

### 4. Distribución de las variables
- Edad
Rango: 40 a 95 años.
Media: 60 años.
Desviación estándar: 11.2 años.
Gráfico: La edad sigue una distribución aproximadamente normal, con un ligero sesgo hacia edades más avanzadas.

- Fracción de Eyección
Rango: 14% a 80%.
Media: 38%.
Gráfico: Una distribución asimétrica con más pacientes en rangos bajos (indicativo de insuficiencia cardíaca).

- Variables categóricas (e.g., Género, Fumar)
Género:
Hombres: 194 (65%).
Mujeres: 105 (35%).
Fumar:
No: 201 (67%).
Sí: 98 (33%).


## Variable objetivo

En esta sección se describe la variable objetivo. Se muestra la distribución de la variable y se presentan gráficos que permiten entender mejor su comportamiento.

### Descripción de la Variable Objetivo
- Nombre de la variable: target
- Tipo de variable: Categórica binaria (0 o 1).
- Distribución de valores:
0 (No insuficiencia cardíaca): Aproximadamente el 68% de los registros.
1 (Insuficiencia cardíaca): Aproximadamente el 32% de los registros.

 --> Código que genera un gráfico de barras para visualizar la distribución de la variable objetivo:


## Variables individuales

En esta sección se presenta un análisis detallado de cada variable individual. Se muestran estadísticas descriptivas, gráficos de distribución y de relación con la variable objetivo (si aplica). Además, se describen posibles transformaciones que se pueden aplicar a la variable.

## Ranking de variables

En esta sección se presenta un ranking de las variables más importantes para predecir la variable objetivo. Se utilizan técnicas como la correlación, el análisis de componentes principales (PCA) o la importancia de las variables en un modelo de aprendizaje automático.

## Relación entre variables explicativas y variable objetivo

En esta sección se presenta un análisis de la relación entre las variables explicativas y la variable objetivo. Se utilizan gráficos como la matriz de correlación y el diagrama de dispersión para entender mejor la relación entre las variables. Además, se pueden utilizar técnicas como la regresión lineal para modelar la relación entre las variables.
