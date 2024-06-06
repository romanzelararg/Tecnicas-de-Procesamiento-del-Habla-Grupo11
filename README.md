# GRUPO-11

<h1 align="center"> PROYECTO FINAL </h1>
<h1 align="center"> Tecnicas de Procesamiento del Habla </h1>

### COHORTE 2022

### :globe_with_meridians: TECNICATURA EN CIENCIAS DE DATOS E INTELIGENCIA ARTIFICIAL

### *Colaboradores:*

- [Hanun Romina](https://github.com/RomiHanun) 
- [Kanneman Samuel](https://github.com/samuelkanneman)
- [Zelarayán Román ](https://github.com/romanzelararg)
- [Mansilla Leonardo Matias ](https://github.com/LMmansilla)
- [Lucero Carla](https://github.com/CarlaLucerocd)
- [Juchniewicz Federico](https://github.com/FJISPC) 

### Análisis de Sentimientos de Texto de un libro "24 horas en la vida de una mujer.txt", clasificando las palabras o frases en categorías de sentimiento positivo o negativo.

- **Descripción del problema abordado** :

  * Abordamos el problema de la clasificación de sentimientos basada en texto. El objetivo es procesar un texto, en este caso, el libro "24 horas en la vida de una mujer.txt", y clasificar las palabras o frases en categorías de sentimiento positivo o negativo.

- **Metodología y técnicas de procesamiento del Habla aplicadas**:
  
    * *Preprocesamiento de texto*: Se realiza una limpieza del texto eliminando caracteres especiales y espacios extra, y luego se tokeniza. Se calcula la cantidad de tokens únicos y se determina la fracción de stopwords en el corpus.
    * *Lematización*: Se realiza la lematización de los tokens para llevarlos a su forma base o lema.
    * *Vectorización*: Se filtran los tokens para crear etiquetas de sentimiento y se vectoriza el texto utilizando TF-IDF (Term Frequency-Inverse Document Frequency).
    * *Construcción del Modelo de Red Neuronal*: Se divide el conjunto de datos en entrenamiento y prueba, se normalizan los datos y se define la arquitectura del modelo de red neuronal para clasificación binaria.
    * *Entrenamiento y Evaluación*: Se entrena el modelo con los datos normalizados y se evalúa su precisión. Se muestra la matriz de confusión y la curva ROC para analizar el rendimiento del modelo.
    * *Ajuste de Hiperparámetros*: Se ajustan hiperparámetros y se añade Dropout al modelo para mejorar su rendimiento. Se entrena nuevamente y se evalúa la precisión.
      
**Relevancia del Proyecto**
  El proyecto específico de clasificar los sentimientos en el libro "24 horas en la vida de una mujer.txt" se enmarca dentro de esta evolución tecnológica. Utilizar técnicas avanzadas de NLP y machine learning para analizar un texto literario permitirá no solo la identificación de sentimientos a nivel de palabras y frases, sino también la comprensión de los matices emocionales y psicológicos presentes en la obra.
Este enfoque no solo contribuirá al campo del análisis literario, sino que también podrá ser una referencia para el desarrollo de herramientas similares en otros contextos, demostrando la versatilidad y potencia de las tecnologías de procesamiento de lenguaje natural en la clasificación de sentimientos.

**Descripción del problema abordado**
  Abordamos el problema de la clasificación de sentimientos basada en texto. El objetivo es procesar un texto, en este caso, el libro "24 horas en la vida de una mujer.txt", y clasificar las palabras o frases en categorías de sentimiento positivo o negativo.
En primera instancia realizamos el proyecto de Clasificación de Sentimientos con Bosque Aleatorio,  utilizando un conjunto de datos textual, específicamente el libro "24 horas en la vida de una mujer", para entrenar un modelo de aprendizaje automático capaz de clasificar palabras según su connotación sentimental. El algoritmo empleado es el Bosque Aleatorio.
 *Objetivo del Proyecto*
El objetivo es desarrollar un clasificador que pueda identificar y categorizar palabras en dos clases de sentimientos: positivos y negativos. Esto es útil para diversas aplicaciones, como el análisis de sentimientos en textos literarios o redes sociales.

**Metodologías**
En el presente informe se aplicaron dos tipos de algoritmo de aprendizaje automático:
Modelo clasificador de Bosque Aleatorio (Random Forest) 
Combina múltiples modelos para mejorar el rendimiento y la precisión de la predicción.
Modelo de Red Neuronal Feedforward con Capas Densas.
Esta red utilizará las características TF-IDF como entradas en una estructura de capas densas para realizar tareas de clasificación o regresión, según el problema específico que se desea resolver.

MODELO CLASIFICADOR DE BOSQUE ALEATORIO
Se aplican las siguientes etapas:
1. Preprocesamiento de Datos
Primero, se utiliza la librería `nltk` para el procesamiento de texto. El texto del libro se carga en una variable y luego se divide en palabras individuales mediante la tokenización. La tokenización es el proceso de dividir el texto en palabras o tokens.
2. Extracción de Características
Luego, se emplea la técnica TF-IDF (Term Frequency-Inverse Document Frequency) para transformar las palabras en vectores numéricos. Este método permite representar cada palabra en función de su frecuencia relativa en el documento y en el corpus, destacando las palabras más relevantes.

3. Definición de Etiquetas
Se asignan etiquetas a las palabras según su connotación sentimental utilizando un diccionario predefinido. Las palabras con connotación positiva se etiquetan como `1`, y las palabras con connotación negativa se etiquetan como `0`. Las palabras que no están en el diccionario reciben una etiqueta especial para ser filtradas posteriormente.

4. Filtrado de Datos
Las palabras con la etiqueta especial, que indica que no están en el diccionario de sentimientos, se eliminan del conjunto de datos para asegurar que solo se utilicen palabras con etiquetas claras.

5. División del Conjunto de Datos
El conjunto de datos se divide en dos partes: un conjunto de entrenamiento y un conjunto de pruebas. El conjunto de entrenamiento contiene el 80% de los datos y se utiliza para entrenar el modelo, mientras que el conjunto de prueba contiene el 20% restante y se utiliza para evaluar el rendimiento del modelo.

6. Entrenamiento del Modelo
 Se crea y entrena un clasificador de Bosque Aleatorio con 100 árboles. El Bosque Aleatorio es un algoritmo de aprendizaje supervisado que combina múltiples árboles de decisión para mejorar la precisión y evitar el sobreajuste.

7. Predicción y Evaluación
Una vez entrenado el modelo, se realizan predicciones sobre el conjunto de prueba. La precisión del modelo se evalúa mediante la métrica de exactitud, que mide el porcentaje de predicciones correctas. Además, se pueden generar informes de clasificación y matrices de confusión para un análisis más detallado del rendimiento del modelo.

Resultados
El clasificador logró una precisión del 100%



*Conclusiones*
El proyecto demuestra la viabilidad de usar algoritmos de aprendizaje automático, como el Random Forest, para la clasificación de sentimientos en palabras individuales. La precisión obtenida indica que el modelo es capaz de distinguir entre palabras positivas y negativas con un grado razonable de exactitud. Sin embargo, la limitación principal es que el diccionario de etiquetas es muy básico y puede ser mejorado para aumentar la precisión del modelo.

MODELO DE RED NEURONAL CON CAPAS DENSA
Descripción detallada de cada paso:
Limpieza y Tokenización de texto
La sección de "Limpieza y Tokenización de texto" se refiere al procesamiento previo de un texto antes de aplicar técnicas de análisis o modelado. A continuación, se proporciona una breve descripción de lo que hace ese código:
1. Limpieza de Texto:
   - El código comienza definiendo una función llamada `limpiar_texto`. Esta función toma un texto como entrada y realiza las siguientes operaciones:
 	- Convierte todo el texto a minúsculas.
 	- Elimina caracteres especiales (como signos de puntuación).
 	- Elimina espacios en blanco adicionales.
   - Luego, el código lee un archivo de texto (probablemente un libro) y aplica la función de limpieza al contenido del archivo.
2. Tokenización:
   - Después de limpiar el texto, se realiza la tokenización. La tokenización es el proceso de dividir el texto en unidades más pequeñas llamadas "tokens" (generalmente palabras o frases).
   - El código utiliza la biblioteca NLTK para tokenizar el texto limpio en palabras individuales. El resultado es una lista de tokens.
3. Fracción de Stopwords en un Corpus:
   - Los "stopwords" son palabras comunes (como "el", "de", "y", etc.) que generalmente no aportan información significativa en el análisis de texto.
   - El código calcula la fracción de stopwords en el corpus (el conjunto de tokens después de la limpieza y tokenización).
   - En este caso, la fracción de stopwords es aproximadamente 0.52, lo que significa que alrededor del 52% de los tokens son stopwords.
En resumen, el código prepara un texto para su posterior análisis al limpiarlo, dividirlo en palabras individuales y calcular la fracción de stopwords presentes en el corpus. Esto es útil para tareas como análisis de sentimientos, clasificación de texto o cualquier otro procesamiento basado en texto.
4. Lematización:
   - La lematización es el proceso de reducir las palabras a su forma base o raíz.
   - Se utiliza el lematizador de WordNet para convertir palabras a su forma lematizada.
   - Por ejemplo, "corriendo" se lematiza como "correr".
5. Vectorización (TF-IDF):
   - La vectorización convierte el texto en una representación numérica que los algoritmos de aprendizaje automático pueden procesar.
   - En este caso, se utiliza la técnica TF-IDF (Term Frequency-Inverse Document Frequency).
   - TF-IDF asigna un valor a cada palabra según su frecuencia en el documento y su rareza en el corpus completo.
   - El resultado es una matriz donde cada fila representa un documento (en este caso, fragmentos de texto) y cada columna representa una palabra, con valores que indican la importancia relativa de cada palabra en el documento.


MODELO ACTUALIZADO DE RED NEURONAL CON CAPAS DENSAS 
En este modelo solo se realizó una modificación en la etapa de etiquetado de palabras para valorar el sentimiento. Para esto se utiliza la biblioteca VADER (Valence Aware Dictionary and sEntiment Reasoner). Es un modelo pre-entrenado que puede entender y evaluar el sentimiento de textos.
Esto se hace para evaluar si es posible mejorar el modelo agregando un dataset más amplio de palabras con su etiquetado correspondiente.
Se detallan los cambios realizados en la etapa de Análisis de Sentimiento, luego de realizar la etapa de lematización:
En primer lugar se trae la herramienta de análisis de sentimiento VADERanalyzer = SentimentIntensityAnalyzer() 
Se crea la Función: analizar_sentimiento(tokens) 
	Esta función es el corazón del código, ya que recibe tokens. Los tokens suelen ser palabras individuales, pero podrían ser frases cortas dependiendo de cómo se haya procesado el texto previamente. 
Crea una lista vacía: etiquetas_sentimiento = [] donde se guardarán las etiquetas de sentimiento (positivo, negativo o neutral) para cada token. 
Itera sobre los tokens: El bucle for token in tokens: recorre cada token de la lista uno por uno.
	Dentro del bucle, ocurre lo siguiente:
	score = analyzer.polarity_scores(token): VADER analiza el token y devuelve un diccionario (score) con varias puntuaciones de sentimiento. La más importante aquí es score['compound'], que es una puntuación general que va desde -1 (muy negativo) hasta 1 (muy positivo).
	Luego se procede al Etiquetado:
	Si score['compound'] es mayor o igual a 0.05, se etiqueta el token como positivo (1).
	Si score['compound'] es menor o igual a -0.05, se etiqueta el token como negativo (-1).
	Si no se cumple ninguna de las anteriores, se etiqueta como neutral (0).
Finalmente, la función devuelve la lista etiquetas sentimiento, que contiene una etiqueta de sentimiento para cada token de la lista original.
En resumen: Estas modificaciones al código toma un texto, lo divide en tokens (palabras o frases) y usa VADER para determinar si cada token tiene un sentimiento positivo, negativo o neutral. 
Luego se continúa con la Construcción del Modelo de Red Neuronal similar al Modelo anterior.
Para finalizar se entrena y evalúa la RN, obteniendo un Accuracy: 0.99, la cual es una mejora considerable. Aunque también se corre el riesgo de sobre entrenado, por lo cual sería considerable a futuro, tener otro tipo de métricas para evaluar la precisión, o realizar un ajuste más en detalle de los hiperparametros. 
Resumen de las Metodologías y técnicas de procesamiento del Habla aplicadas
Preprocesamiento de texto: Se realiza una limpieza del texto eliminando caracteres especiales y espacios extra, y luego se tokeniza. Se calcula la cantidad de tokens únicos y se determina la fracción de stopwords en el corpus.
Lematización: Se realiza la lematización de los tokens para llevarlos a su forma base o lema.
Vectorización: Se filtran los tokens para crear etiquetas de sentimiento y se vectoriza el texto utilizando TF-IDF (Term Frequency-Inverse Document Frequency).
Construcción del Modelo clasificador de Bosque Aleatorio: Se crea un clasificador de Bosque Aleatorio con 100 árboles. Se entrena el clasificador utilizando los datos de entrenamiento.
Construcción del Modelo de Red Neuronal: Se divide el conjunto de datos en entrenamiento y prueba, se normalizan los datos y se define la arquitectura del modelo de red neuronal para clasificación binaria.
Entrenamiento y Evaluación: Se entrena el modelo con los datos normalizados y se evalúa su precisión. Se muestra la matriz de confusión y la curva ROC para analizar el rendimiento del modelo.
Ajuste de Hiperparámetros: Se ajustan hiperparámetros y se añade Dropout al modelo para mejorar su rendimiento. Se entrena nuevamente y se evalúa la precisión.
 
**Impacto en la solución propuesta**
  En este caso, el procesamiento de habla se utiliza para preparar los datos de texto para su uso en un modelo de clasificación de sentimientos. Esto puede ayudar a comprender las intenciones de los clientes, extraer información valiosa de datos no estructurados, y mejorar el rendimiento general del modelo.

**Conclusiones**
La detección de emociones utilizando la inteligencia artificial es un campo en constante evolución que implica el uso de algoritmos y técnicas de aprendizaje automático para analizar y clasificar las emociones humanas. Mediante el uso de técnicas de procesamiento de lenguaje natural (NLP) que permiten identificar patrones lingüísticos y emociones subyacentes en textos y conversaciones. 

Durante ese proceso, llevamos a cabo distintas fases: División del texto en palabras claves (tokens); la eliminación de palabras o términos que no aportan ningún valor; la lematización para evitar duplicados. Luego se cuenta la frecuencia de cada palabra en el texto creando un vector para cada palabra (donde cada elemento del vector representa la frecuencia de esa palabra en el texto) y luego  se vectoriza utilizando TF-IDF para convertir el texto en una representación numérica. Se define, a continuación, un modelo de red neuronal con capas densas utilizando la biblioteca Keras que compila los parámetros necesarios para su entrenamiento, como la función de pérdida, el optimizador y las métricas de evaluación.

En conclusión, por medio de este proyecto se ha evidenciado cómo procesando un texto y clasificando palabras o frases en diferentes categorías, se puede comprender las intenciones de los clientes, extraer información valiosa de datos no estructurados, y mejorar el rendimiento general del modelo. Además, este modelo podrá ser replicado y utilizado para otras aplicaciones o contextos futuros, como en seguridad (identificar posibles amenazas o situaciones de riesgo), en Relaciones Públicas y Diplomacia (comprender las actitudes e intenciones de la otra parte), y en marketing (interpretar mejor el flujo de datos de las redes sociales para comprender mejor a los posibles clientes y de esa manera perfeccionar las técnicas para la creación de contenidos y el desarrollo de sus productos).

