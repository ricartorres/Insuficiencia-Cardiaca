# Definición de los datos

## Origen de los datos

- [ ] Los datos se obtienen del repositorio de Datos Kaggle y son datos clinicos de insuficiencia cardíaca.
- [ ] La forma en que se obtuvieron los datos en kaggle lleva a una serie de pasos que son:
      
      Registrarse en Kaggle.
      Acceso a los datasets.
      Descargar archivo (Primer iteración proyecto)
      Conectar Kaggle con Google Colab (Segunda iteración proyecto)
      Cargar los Archivos de Datos en Python
      

## Especificación de los scripts para la carga de datos

- [ ] Para cargar los datos desde Kaggle vamos a utiliar la API de Kaggle mediante los siguientes pasos, que se evidencian en el script de preprocessing:

      Importar librerias
      Obtener el archivo
      Instalar la Librería de Kaggle
      Autenticar la API de Kaggle
      Descargar el Dataset insuficiencia cardiaca

## Referencias a rutas o bases de datos origen y destino

- [ ] A continuación daremos a conocer la ruta y origen del archivo, cual es la estructura de ese archivo y el proceso que realizaremos de procesamiento de los datos para obtener una limpieza de los datos.
      

### Rutas de origen de datos

- [ ] La ruta de origen de los datos es la siguiente:

      https://www.kaggle.com/datasets/andrewmvd/heart-failure-clinical-data?resource=download&select=heart_failure_clinical_records_dataset.csv

      
- [ ] La estructura de los archivos de origen de los datos es un archivo CSV que contiene registros de pacientes con información clínica relacionada con insuficiencia cardíaca. La estructura general del archivo CSV es la siguiente:

      age: Edad del paciente.
      anemia: Booleano (0 o 1), indica si el paciente tiene anemia.
      creatinine_phosphokinase: Nivel de la enzima creatinina fosfoquinasa (CPK) en sangre.
      diabetes: Booleano (0 o 1), indica si el paciente tiene diabetes.
      ejection_fraction: Fracción de eyección del corazón, que indica la eficiencia del bombeo del corazón.
      high_blood_pressure: Booleano (0 o 1), indica si el paciente tiene hipertensión.
      platelets: Conteo de plaquetas en la sangre.
      serum_creatinine: Nivel de creatinina en la sangre, indicador de función renal.
      serum_sodium: Nivel de sodio en la sangre.
      sex: Género del paciente (0 = femenino, 1 = masculino).
      smoking: Booleano (0 o 1), indica si el paciente es fumador.
      time: Duración de la observación en días.
      DEATH_EVENT: Booleano (0 o 1), indica si el paciente ha tenido un evento fatal relacionado con insuficiencia cardíaca (1 = sí, 0 = no).
      
- [ ] Revisión de valores faltantes

       Revisar si hay valores faltantes en el dataset y tratarlos adecuadamente (eliminarlos o reemplazarlos con un valor significativo).
      
- [ ] Revisión de valores atípicos

      Los valores atípicos pueden distorsionar el análisis, se realizará su correspondiente análisis y tratamiento.
      
- [ ] Conversión de columnas categóricas

      Las columnas categóricas deben estar correctamente codificadas.

- [ ] Normalización y escalado de características numéricas

      Realizar el escalado de características.

### Versionado de los datos
      Los datos extraidos de kaggle definidos en los puntos anteriores, se versionaron por DVC a un repositorio de google drive, a continuacipon los pasos que se realizaron

- [ ] Instalar DVC y dependencias
      Se instala en google collab el DVC
- [ ] Inicializar DVC en el proyecto
      Ejecutar el inicio de DVC
- [ ] Configurar el remote en Google Drive
      Se configurar un remoto de DVC para Google Drive.
- [ ] Guardar el DataFrame en un archivo.
      Se guarda tu DataFrame en un archivo.
- [ ] Agregar el archivo al control de versiones de DVC.
      Se agrega el archivo del DataFrame al control de versiones.
- [ ] Hacer commit de los cambios de DVC
      Se realiza un commit para versionar el archivo en DVC.
- [ ] Subir el archivo a Google Drive
      Se sube el archivo al remoto configurado en Google Drive
