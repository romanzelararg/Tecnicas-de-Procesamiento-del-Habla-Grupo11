# Tecnicas-de-Procesamiento-del-Habla_-Grupo11

Análisis de Sentimientos de Texto de un libro "24 horas en la vida de una mujer.txt", clasificando las palabras o frases en categorías de sentimiento positivo o negativo.

- *Descripción del problema abordado*: Abordamos el problema de la clasificación de sentimientos basada en texto. El objetivo es procesar un texto, en este caso, el libro "24 horas en la vida de una mujer.txt", y clasificar las palabras o frases en categorías de sentimiento positivo o negativo.

- *Metodología y técnicas de procesamiento del Habla aplicadas*: 
    * *Preprocesamiento de texto*: Se realiza una limpieza del texto eliminando caracteres especiales y espacios extra, y luego se tokeniza. Se calcula la cantidad de tokens únicos y se determina la fracción de stopwords en el corpus.
    * *Lematización*: Se realiza la lematización de los tokens para llevarlos a su forma base o lema.
    * *Vectorización*: Se filtran los tokens para crear etiquetas de sentimiento y se vectoriza el texto utilizando TF-IDF (Term Frequency-Inverse Document Frequency).
    * *Construcción del Modelo de Red Neuronal*: Se divide el conjunto de datos en entrenamiento y prueba, se normalizan los datos y se define la arquitectura del modelo de red neuronal para clasificación binaria.
    * *Entrenamiento y Evaluación*: Se entrena el modelo con los datos normalizados y se evalúa su precisión. Se muestra la matriz de confusión y la curva ROC para analizar el rendimiento del modelo.
    * *Ajuste de Hiperparámetros*: Se ajustan hiperparámetros y se añade Dropout al modelo para mejorar su rendimiento. Se entrena nuevamente y se evalúa la precisión.
 *Impacto en la solución propuesta*: En este caso, el procesamiento de habla se utiliza para preparar los datos de texto para su uso en un modelo de clasificación de sentimientos. Esto puede ayudar a comprender las intenciones de los clientes, extraer información valiosa de datos no estructurados, y mejorar el rendimiento general del modelo.

- *Avances y posible división de trabajo de procesamiento del habla entre integrantes*: La división del trabajo podría ser la siguiente:
    * Preprocesamiento de texto: Un miembro del equipo podría encargarse de la limpieza y tokenización del texto.
    * Lematización y Vectorización: Otro miembro del equipo podría encargarse de la lematización de los tokens y de su vectorización.
    * Construcción y Entrenamiento del Modelo: Un tercer miembro del equipo podría encargarse de la construcción del modelo de red neuronal y de su entrenamiento.
    * Evaluación del Modelo y Ajuste de Hiperparámetros: Un cuarto miembro del equipo podría encargarse de la evaluación del modelo y del ajuste de hiperparámetros para mejorar su rendimiento.
      

