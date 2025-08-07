Procesamiento de Datos para Fine-Tuning de Modelos de Chat Este repositorio contiene un Jupyter Notebook (data_preparation.ipynb) diseñado para preparar y validar datasets en formato JSONL, específicamente para fine-tuning de modelos de chat como los de OpenAI. El dataset utilizado abarca a la serie de televisión "Rick and Morty".

📌 Características principales Validación de estructura: Verifica que los datos cumplan con el formato requerido para fine-tuning.

Análisis de tokens: Calcula la distribución de tokens por mensaje y conversación.

Estimación de costos: Proporciona una proyección del costo de entrenamiento basado en el volumen de tokens.

Detección de problemas: Identifica ejemplos con formatos incorrectos o que exceden el límite de tokens.

🛠️ Funcionalidades implementadas Carga y validación de datos:

Verificación de claves obligatorias (role, content).

Validación de roles permitidos (system, user, assistant, function).

Detección de mensajes faltantes (ej: ausencia de respuestas del asistente).

Análisis de tokens:

Conteo de tokens usando la codificación cl100k_base de OpenAI.

Distribución estadística (min/max, media/mediana, percentiles).

Identificación de conversaciones que exceden el límite de 4096 tokens.

Estimación de costos:

Cálculo de tokens facturables.

Estimación automática de épocas de entrenamiento.

Proyección del costo total basado en el volumen de datos.

📊 Resultados destacables Dataset analizado: 1,261 ejemplos (todos válidos).

Longitud promedio por ejemplo: 134 tokens (68-206 tokens).

Tokens de asistente promedio: 70 tokens por ejemplo.

0 ejemplos exceden el límite de tokens.

Costo estimado: ~506,466 tokens para 3 épocas de entrenamiento.
