# Analisis-y-clasificacion-de-eventos-de-cancer-de-mama
<p align="center">
  <img src="cancermama.jpg" alt="Texto alternativo" width="500"/>
</p>

## Integrantes del Equipo:
Jesus David Franco, Angel David Quintero, José Francisco Escudero & Oscar David Ulloa.


### Contexto y problemática

Este dominio de cáncer de mama se obtuvo del Centro Médico Universitario, Instituto de Oncología, Ljubljana, Yugoslavia (1988). Este es uno de los tres dominios proporcionados por el Instituto de Oncología que han aparecido repetidamente en la literatura sobre aprendizaje automático. La dificultad para predecir con precisión si un paciente con cáncer de mama experimentará eventos recurrentes o no recurrentes plantea un desafío clave en oncología. Esto se debe a la heterogeneidad del cáncer, la presencia de factores de riesgo desconocidos, la subjetividad en la evaluación del tratamiento y las limitaciones en la vigilancia post-tratamiento. Mejorar la precisión en la clasificación de eventos recurrentes y no recurrentes es esencial para mejorar el manejo y los resultados en pacientes con cáncer de mama. En base a esta problemática se tiene como propósito principal clasificar si el cáncer de mama puede presentar eventos recurrentes o no recurrentes en el paciente, lo que hace referencia a que el cáncer pueda tener una probabilidad significativa de volver a aparecer después de un tratamiento previo o si este no tiene un índice significativo para que pueda reaparecer, respectivamente. Para lograr los objetivos de análisis y clasificación se plantearon las siguientes preguntas de investigación:

 1. ¿Qué factores están más asociados con la recurrencia del cáncer de mama?
 2. ¿Qué método de aprendizaje automático es el mejor para predecir la recurrencia de cáncer de mama?
 3. ¿Es posible predecir si un paciente experimentará una recurrencia del cáncer de mama basado en sus características?

###  Contenido

Para llevar a cabo el proceso de análisis exploratorio de los datos y realizar la clasificación del modelo se hizo uso de la metodología CRISP-DM en el cual se basa en 4 grandes procesos para realizar el proyecto, los cuales son:

1. Entendimiento del negocio: En este apartado se formularon 3 preguntas de investigación para tener unos objetivos para alcanzar a medida que se vaya progresando en el proyecto.
2. Entendimiento de los datos: En el entendimiento de los datos de llevó a cabo todo el proceso del EDA de los datos. Es importante resaltar que al tener un Dataset cuyas variables son de tipo categóricas (a excepción de una variable) el análisis univariado y bivariado se limitó únicamente a análisis de tablas de frecuencia y gráficos como diagramas de barras y de pastel (para ello se utilizó la librería Plotly Express), ante la ausencia de variables numéricas no se pudo realizar un análisis de correlación o pruebas de hipótesis entre estas para determinar un patrón de distribución entre las variables. En base a ello, se realizaron múltiples actividades tales como:
  -  Diccionario de variables.
  -  Imputación de datos nulos.
  -  Corrección de formato de datos.
  -  Feature engineering (ingeniería de características).
  -  Creación de datos sintéticos.
  -  Análisis univariado.
  -  Análisis bivariado.

3. Etapa de modelado:   Para llevar a cabo esta etapa, previamente se realizaron unas transformaciones de algunas variables para tratar de mejorar el rendimiento de los algoritmos, las transformaciones que se realizaron fueron:
   - Categóricas a numéricas: Al tener variables numéricas discretizadas, se realizó la separación de los intervalos y se crearon dos variables nuevas que correspondían al valor mínimo      y el valor máximo de dichos datos discretizados.
   - Categóricas a dummy: Para las variables categóricas se realizó la conversión de estas a tipo Dummy para mejorar la compatibilidad y rendimiento de los algoritmos a utilizar.
   
Posteriormente se llevó a cabo la selección y uso de algoritmos de ML que sean capaces de predecir la variable objetivo en base a el tipo de características del Dataset; cabe resaltar, que cada uno de los algoritmos fueron seleccionados con un propósito de acuerdo a la naturaleza de los datos. Para ello es importante saber que al tener una variable objetivo, los modelos que se requieren utilizar deben ser modelos de aprendizaje supervisado. En donde de acuerdo con el conjunto de datos establecido y teniendo en cuenta que las variables en gran proporción son de tipo categóricas, se requiere utilizar algoritmos que sean sensibles a este tipo de características; por lo tanto, los modelos a utilizar para cumplir el propósito establecido son:

- Random Forest.
- SVM.
- Naive Bayes.

Luego de eso se hicieron uso de los algoritmos de aprendizaje por refuerzo para determinar si sus métricas de clasificación tenían un mejor rendimiento que los algoritmos descritos anteriormente, los algoritmos de aprendizaje por refuerzo que se utilizaron fueron:

- XGBoost.
- ADABOOST (haciendo uso de la base del algoritmo de SVM y Naive Bayes).

Para la clasificación del modelo se realizó la separación 80/20 de los datos para el entrenamiento y testeo respectivamente. Luego de ello se realizó un proceso de tuning de hiperparámetros en cada algoritmo para verificar cuáles son los mejores hiperparámetros seleccionados que optimicen las métricas de clasificación.
  
  4. Métricas: Una vez realizada la clasificación, se llevó a cabo la formulación e interpretación de las métricas de clasificación; al tratarse de una clasificación se utilizaron las métricas de la matriz de confusión tales como la exactitud, precisión, especificidad y sensibilidad.
    
  5. Conclusiones: Finalmente se plantearon las conclusiones obtenidas del trabajo realizado.

###  Conclusiones.

