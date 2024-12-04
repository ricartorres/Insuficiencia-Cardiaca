# Diccionario de datos

## Base de datos 1

"Heart Failure Prediction" es un dataset tomado de Kaggle. Es un conjunto de datos que contiene información sobre pacientes con insuficiencia cardíaca, con el objetivo de predecir la probabilidad de mortalidad o reingreso hospitalario debido a esta condición.

Este dataset incluye variables como: la edad, el sexo, la presión arterial, el ritmo cardíaco, la función ventricular, entre otras. También incluye una variable objetivo que indica si el paciente falleció o fue reingresado en el hospital debido a insuficiencia cardíaca.


| Variable | Descripción | Tipo de dato | Rango/Valores posibles |
| --- | --- | --- | --- |
| age | Edad | numérica continua | 40-95 años |
| anaemia | Disminución de glóbulos rojos o hemoglobina | categórica binaria | 0 = no, 1 = sí |
| creatinine_phosphokinase | Nivel de la enzima CPK en la sangre | numérica continua | 23-7860 U/L |
| diabetes | Si el paciente tiene diabetes | categórica binaria |0 = no, 1 = sí |
| ejection_fraction | Porcentaje de sangre que sale del corazón en cada contracción | numérica continua | 14-80% |
| high_blood_pressure | Si el paciente tiene hipertensión | categórica binaria | 0 = no, 1 = sí |
| platelets | Recuento de plaquetas en la sangre | numérica continua | 66000-850000 plt/μL |
| serum_creatinine | Nivel de creatinina sérica en la sangre | numérica continua | 0.5-9.4 mg/dL |
| serum_sodium | Level of serum sodium in the blood | numérica continua | 114-148 mmol/L |
| sex | Sexo del paciente | categórica binaria | 0 = masculino, 1 = femenino |
| smoking | Hábito de fumar del paciente | categórica binaria | 0 = no, 1 = sí |
| time | Tiempo de seguimiento del paciente | numérica continua | 4-285 días |
| DEATH_EVENT | Evento de muerte del paciente | categórica binaria | 0 = no, 1 = sí |


### Clasificación de las Variables
Variables categóricas: 7 variables (anaemia, diabetes, high_blood_pressure, sex, smoking, DEATH_EVENT)
Variables numéricas: 6 variables (age, creatinine_phosphokinase, ejection_fraction, platelets, serum_creatinine, serum_sodium, time)

