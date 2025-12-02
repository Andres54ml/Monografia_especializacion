# Monografia_especializacion

Este repositorio contiene un proyecto de predicción del precio de apertura de la acción de Bancolombia en la bolsa de New York (CIB) utilizando diferentes arquitecturas de redes neuronales recurrentes: Simple RNN, GRU, LSTM, además de modelos que integran una variable de sentimiento generada mediante análisis de noticias.

El enfoque es multivariante, integrando variables económicas y una variable binaria de sentimiento:

1 = positivo

0 = negativo

📁 Estructura del Proyecto
/ 
├── baseline.ipynb
├── modelo_solo_rnn.ipynb
├── modelo_solo_gru.ipynb
├── modelo_solo_lstm.ipynb
├── modelo_sentimiento.ipynb
├── construccion_sentimiento/
│     └── (scripts y notebooks para análisis y clasificación de sentimiento)
└── preprocesamiento_imagen/
      └── (imágenes, gráficas o recursos usados para el informe)

📄 Descripción de Notebooks
Notebook	Descripción
baseline.ipynb	Modelo base utilizado como referencia inicial.
modelo_solo_rnn.ipynb	Implementación de una Simple RNN sin variable de sentimiento.
modelo_solo_gru.ipynb	Implementación de una GRU sin la variable de sentimiento.
modelo_solo_lstm.ipynb	Implementación de una LSTM sin la variable de sentimiento.
modelo_sentimiento.ipynb	Versiones RNN, GRU y LSTM incluyendo la variable binaria de sentimiento.
Carpetas nuevas
Carpeta	Descripción
construccion_sentimiento/	Contiene el proceso de scraping, limpieza, análisis y clasificación de sentimiento usado para generar la variable binaria.
preprocesamiento_imagen/	Almacena recursos visuales utilizados en el proyecto (gráficas, imágenes para la monografía, ejemplos, etc.).
🧠 Modelos Implementados
🔹 Baseline

Modelo simple para establecer un punto mínimo de comparación.

🔹 Modelos sin Sentimiento

Tres modelos independientes:

Simple RNN

GRU

LSTM

🔹 Modelos con Sentimiento

Entrenados en modelo_sentimiento.ipynb:

RNN + sentimiento

GRU + sentimiento

LSTM + sentimiento


🛠 Metodología

Escalado con MinMaxScaler

Construcción de ventanas temporales

División en train / test

Entrenamiento con Adam y pérdida MSE

Aplicación de EarlyStopping

Métricas: MAE y RMSE

Gráficas comparativas entre real vs. predicho


📈 Visualizaciones Generadas

Gráfica de pérdida vs épocas

Comparación precio real vs predicho

Comparación entre modelos

Comparación con y sin sentimiento

✅ Conclusiones Generales

LSTM fue la arquitectura más precisa.

GRU obtuvo resultados muy cercanos con menor costo computacional.

RNN simple mostró limitaciones frente a GRU y LSTM.

La variable de sentimiento mejora el desempeño, especialmente en GRU y LSTM.

Todos los modelos avanzados superan al baseline.

▶️ Cómo Ejecutar el Proyecto
1. Instalar dependencias
pip install tensorflow pandas numpy matplotlib scikit-learn

2. Ejecutar los notebooks
jupyter notebook modelo_solo_lstm.ipynb

