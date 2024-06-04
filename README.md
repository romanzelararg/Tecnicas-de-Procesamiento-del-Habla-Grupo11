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
      
- **Impacto en la solución propuesta** :
  * En este caso, el procesamiento de habla se utiliza para preparar los datos de texto para su uso en un modelo de clasificación de sentimientos. Esto puede ayudar a comprender las intenciones de los clientes, extraer información valiosa de datos no estructurados, y mejorar el rendimiento general del modelo.

- **Avances y posible división de trabajo de procesamiento del habla entre integrantes** :
    * Preprocesamiento de texto: Un miembro del equipo se encarga de la limpieza y tokenización del texto.
    * Lematización y Vectorización: Otro miembro del equipo se encarga de la lematización de los tokens y de su vectorización.
    * Construcción y Entrenamiento del Modelo: Un tercer miembro del equipo se encarga de la construcción del modelo de red neuronal y de su entrenamiento.
    * Evaluación del Modelo y Ajuste de Hiperparámetros: Un cuarto miembro del equipo se encarga de la evaluación del modelo y del ajuste de hiperparámetros para mejorar su rendimiento.

### El cuaderno "Proc_Habla_RN.ipynb" se centra en el análisis de sentimientos de un libro llamado "24 horas en la vida de una mujer". Aquí están los puntos clave:
1. **Preparación del área de trabajo**:
   - Se importaron las librerías necesarias, como `nltk`, `sklearn`, y `keras`.
   - Se carga el documento.
   - Se descargaron recursos léxicos, como stopwords y lematización.

2. **Limpieza y tokenización de texto**:
   - Se leyó y limpió el texto del archivo "24 horas en la vida de una mujer.txt".
   - Se eliminaron caracteres especiales y espacios extra.
   - Se realizó la tokenización del texto.

3. **Análisis de sentimientos**:
   - Se etiquetaron palabras o frases en categorías de sentimiento positivo o negativo.
   - Se utilizó la matriz TF-IDF para vectorizar el texto.
   - Se construyó un modelo de red neuronal secuencial para clasificación binaria.
   - Se entrenó y evaluó el modelo.

4. **Resultados**:
   - Se obtuvo una precisión del modelo en los datos de prueba.
   - Se mostró la matriz de confusión y la curva ROC.
