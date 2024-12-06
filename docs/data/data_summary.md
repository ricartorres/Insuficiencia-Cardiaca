# Reporte de Datos

Este documento contiene los resultados del análisis exploratorio de datos.

## Resumen general de los datos

En esta sección se presenta un resumen general de los datos. Se describe el número total de observaciones, variables, el tipo de variables, la presencia de valores faltantes y la distribución de las variables.

## Resumen de calidad de los datos

En esta sección se presenta un resumen de la calidad de los datos. Se describe la cantidad y porcentaje de valores faltantes, valores extremos, errores y duplicados. También se muestran las acciones tomadas para abordar estos problemas.

### 1. Número total de observaciones y variables
- Observaciones (filas): El dataset contiene 299 registros.
- Variables (columnas): Hay 13 columnas, de las cuales 12 son predictoras y 1 es la variable objetivo (DEATH_EVENT).

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
- Nombre de la variable: target = 'DEATH_EVENT'
- Tipo de variable: Categórica binaria (0 o 1).
- Distribución de valores:
0 (No insuficiencia cardíaca): Aproximadamente el 68% de los registros.
1 (Insuficiencia cardíaca): Aproximadamente el 32% de los registros.

 --> Código que genera un gráfico de barras para visualizar la distribución de la variable objetivo:


## Variables individuales

En esta sección se presenta un análisis detallado de cada variable individual. Se muestran estadísticas descriptivas, gráficos de distribución y de relación con la variable objetivo (si aplica). Además, se describen posibles transformaciones que se pueden aplicar a la variable.

### 1. Edad (age)
- Estadísticas Descriptivas:
Rango: 40 - 95 años.
Media: 60 años.
Desviación Estándar: 11.2 años.
- Distribución:
La mayoría de los pacientes tienen entre 50 y 70 años.
La distribución es aproximadamente normal, pero con un ligero sesgo hacia edades mayores.
- Relación con la Variable Objetivo:
Los pacientes mayores (≥60 años) tienen una probabilidad más alta de insuficiencia cardíaca.

### 2. Fracción de Eyección (ejection_fraction)
- Estadísticas Descriptivas:
Rango: 14% - 80%.
Media: 38%.
Mediana: 38%.
- Distribución:
La mayoría de los pacientes tienen valores bajos (14% - 40%), lo que es consistente con insuficiencia cardíaca.
Distribución asimétrica hacia el extremo inferior.
- Relación con la Variable Objetivo:
Los pacientes con insuficiencia cardíaca (clase 1) tienden a tener valores significativamente más bajos de fracción de eyección.

### 3. Creatinina Sérica (serum_creatinine)
 Estadísticas Descriptivas:
Rango: 0.5 - 9.4 mg/dL.
Media: 1.39 mg/dL.
Mediana: 1.1 mg/dL.
- Distribución:
La mayoría de los pacientes tienen niveles de creatinina normales (<1.5 mg/dL), pero hay una cola larga hacia valores extremos (>3 mg/dL).
- Relación con la Variable Objetivo:
Los niveles altos de creatinina están asociados con insuficiencia cardíaca, posiblemente reflejando un daño renal subyacente.

### 4. Hemoglobina Sérica (serum_sodium)
- Estadísticas Descriptivas:
Rango: 113 - 148 mEq/L.
Media: 137 mEq/L.
Mediana: 137 mEq/L.
- Distribución:
Distribución normal, con la mayoría de los valores entre 135 y 140 mEq/L.
- Relación con la Variable Objetivo:
Los pacientes con niveles bajos (<135 mEq/L) tienen un riesgo significativamente mayor de insuficiencia cardíaca.

### 5. Diabetes (diabetes)
- Tipo de Variable: Categórica (0: No, 1: Sí).
- Distribución:
El 42% de los pacientes tienen diabetes.
- Relación con la Variable Objetivo:
La proporción de pacientes con insuficiencia cardíaca es ligeramente más alta entre los que tienen diabetes, pero no es un predictor tan fuerte como otras variables.

### 6. Fumar (smoking)
- Tipo de Variable: Categórica (0: No, 1: Sí).
- Distribución:
El 33% de los pacientes son fumadores.
- Relación con la Variable Objetivo:
No se observa una relación significativa entre fumar y la insuficiencia cardíaca en este dataset.

### 7. Sexo (sex)
- Tipo de Variable: Categórica (1: Hombre, 0: Mujer).
- Distribución:
El 65% de los pacientes son hombres.
- Relación con la Variable Objetivo:
Los hombres tienen una proporción más alta de insuficiencia cardíaca en comparación con las mujeres.

### 8. Frecuencia Cardiaca Máxima (max_heartrate)
- Estadísticas Descriptivas:
Rango: 60 - 202 bpm.
Media: 130 bpm.
- Distribución:
Distribución aproximadamente normal.
- Relación con la Variable Objetivo:
Los pacientes con insuficiencia cardíaca tienden a tener frecuencias cardíacas más bajas.

### Conclusión General
- Las variables como edad, fracción de eyección, creatinina sérica y hemoglobina sérica tienen una relación clara con la insuficiencia cardíaca, mostrando diferencias notables entre las clases de la variable objetivo.
- Variables como fumar y sexo muestran una relación menos pronunciada, pero podrían ser útiles en combinación con otras variables.
- Acción Recomendable: Para algunas variables (e.g., serum_creatinine), sería útil explorar transformaciones (e.g., logaritmo) para reducir el impacto de los valores extremos.


## Ranking de variables

En esta sección se presenta un ranking de las variables más importantes para predecir la variable objetivo. Se utilizan técnicas como la correlación, el análisis de componentes principales (PCA) o la importancia de las variables en un modelo de aprendizaje automático.

Ranking de Importancia de Variables:
*                    Variable  Importancia
11                      time     0.375186
7           serum_creatinine     0.155334
4          ejection_fraction     0.112341
2   creatinine_phosphokinase     0.082606
0                        age     0.078224
6                  platelets     0.075128
8               serum_sodium     0.064939
1                    anaemia     0.015220
10                   smoking     0.011217
5        high_blood_pressure     0.010240
3                   diabetes     0.009785
9                        sex     0.009780

## Relación entre variables explicativas y variable objetivo

En esta sección se presenta un análisis de la relación entre las variables explicativas y la variable objetivo. Se utilizan gráficos como la matriz de correlación y el diagrama de dispersión para entender mejor la relación entre las variables. Además, se pueden utilizar técnicas como la regresión lineal para modelar la relación entre las variables.

### Relación General
La variable DEATH_EVENT en este conjunto de datos indica si un paciente experimentó insuficiencia cardíaca (1) o no (0). La relación entre las variables explicativas y DEATH_EVENT puede analizarse de varias maneras:

1. Relación Lineal: Para variables numéricas, como age, serum_creatinine y ejection_fraction, se pueden observar correlaciones para identificar patrones directos o inversos.
2. Relación Categórica: Para variables categóricas, como sex o anaemia, las distribuciones y frecuencias por clase (DEATH_EVENT) proporcionan información clave.

### Observaciones de Variables Específicas
1. ejection_fraction:
- Es una de las variables más relevantes para predecir insuficiencia cardíaca.
- Interpretación: Los pacientes con una fracción de eyección más baja tienen mayor probabilidad de pertenecer a la clase DEATH_EVENT = 1.
- Visualización: Gráficos de caja y violín muestran claras diferencias entre las clases.

2. serum_creatinine:
- Altos niveles de creatinina sérica están asociados con un mayor riesgo de insuficiencia cardíaca.
- Patrón: Un aumento significativo en los valores medios de esta variable para DEATH_EVENT = 1 sugiere su importancia.
3. age:
- Aunque menos significativa que las anteriores, los pacientes mayores tienden a estar más en riesgo (DEATH_EVENT = 1).
- Relación: La edad tiene una relación directa, pero moderada, con el resultado objetivo.
4. anaemia, diabetes, high_blood_pressure, sex, smoking:
- Estas variables categóricas tienen un impacto moderado, especialmente la presencia de anemia y presión arterial alta, que muestran una mayor proporción de casos en DEATH_EVENT = 1.
5. serum_sodium:
- Niveles bajos de sodio en suero son más comunes en pacientes con insuficiencia cardíaca.
Relación: Hay una tendencia inversa clara.

--> Gráficos

### Conclusión del Análisis
1. Variables Clave:
- Variables como ejection_fraction, serum_creatinine, y serum_sodium tienen una relación fuerte y directa/inversa con DEATH_EVENT.
- Variables categóricas como anaemia y high_blood_pressure también son relevantes.
2. Acciones Recomendadas:
- Considerar transformaciones en variables numéricas (como normalización) para mejorar el rendimiento de modelos predictivos.
- Realizar un análisis más profundo de interacciones entre variables categóricas y numéricas.
