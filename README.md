# Monografia_especializacion

📘 Predicción del Precio de la Acción del Grupo Bancolombia usando RNN, LSTM, GRU y Análisis de Sentimiento

Este repositorio contiene un proyecto de predicción del precio de apertura de la acción de Bancolombia en la bolsa de New York (CIB) utilizando diferentes arquitecturas de redes neuronales recurrentes (RNN): RNN Simple, GRU, LSTM, y versiones de estos modelos que incorporan una variable de sentimiento generada a partir del análisis de noticias.

El enfoque es multivariante, integrando variables económicas y una variable binaria que representa el sentimiento (1 = positivo, 0 = negativo).

📁 Estructura del Proyecto
📂 /
├── baseline.ipynb
├── modelo_solo_rnn.ipynb
├── modelo_solo_gru.ipynb
├── modelo_solo_lstm.ipynb
└── modelo_sentimiento.ipynb

Notebook	Descripción
baseline.ipynb	Modelo baseline utilizado como referencia.
modelo_solo_rnn.ipynb	Modelo basado en Simple RNN sin la variable de sentimiento.
modelo_solo_gru.ipynb	Modelo GRU sin la variable de sentimiento.
modelo_solo_lstm.ipynb	Modelo LSTM sin la variable de sentimiento.
modelo_sentimiento.ipynb	Versiones RNN, GRU y LSTM incluyendo la variable de sentimiento.
🧠 Modelos Implementados
🔹 Baseline

Modelo simple utilizado para establecer un punto mínimo de comparación.

🔹 Modelos sin Sentimiento

Se entrenaron tres modelos independientes:

RNN Simple

GRU

LSTM

Cada uno predice el precio sin usar la variable de sentimiento.

🔹 Modelos con Sentimiento

En modelo_sentimiento.ipynb se entrenan nuevamente los modelos:

RNN + sentimiento

GRU + sentimiento

LSTM + sentimiento

La variable de sentimiento se define como:

sentimiento ∈ {0, 1}

🛠 Metodología

Escalado con MinMaxScaler.

Construcción de ventanas temporales para series de tiempo.

División en datos de entrenamiento y prueba.

Entrenamiento con Adam + MSE.

Aplicación de EarlyStopping.

Evaluación con MAE y RMSE.

Gráficas comparativas entre valores reales y predichos.

📊 Métricas
MAE — Mean Absolute Error
\[
MAE = \frac{1}{N} \sum_{i=1}^{N} \left| \hat{y}_i - y_i \right|
\]

RMSE — Root Mean Squared Error
\[
RMSE = \sqrt{ \frac{1}{N} \sum_{i=1}^{N} (\hat{y}_i - y_i)^2 }
\]

📈 Visualizaciones

Los notebooks generan:

Gráfica de pérdida vs. épocas

Comparación entre precio real y predicho

Resultados por arquitectura

Comparación con y sin sentimiento

✅ Conclusiones Generales

LSTM fue la arquitectura más precisa.

GRU logró un rendimiento muy cercano con menor costo computacional.

RNN simple mostró limitaciones frente a GRU/LSTM.

La variable de sentimiento mejora el desempeño, especialmente en GRU y LSTM.

Todos los modelos avanzados superan al baseline.

▶️ Cómo Ejecutar el Proyecto
Instalar dependencias:
pip install tensorflow pandas numpy matplotlib scikit-learn

Ejecutar los notebooks:
jupyter notebook modelo_solo_lstm.ipynb
