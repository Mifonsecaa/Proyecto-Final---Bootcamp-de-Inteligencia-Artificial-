# Clasificación de Tumores Cerebrales mediante Imágenes MRI

## Descripción del Proyecto

Este proyecto se enfoca en la clasificación de tumores cerebrales a partir de imágenes de Resonancia Magnética (MRI). El objetivo principal es desarrollar un sistema capaz de distinguir entre diferentes tipos de tumores (glioma, meningioma, pituitary) y la ausencia de tumor, utilizando técnicas de procesamiento de imágenes y aprendizaje automático. El notebook `Untitled13.ipynb` detalla las fases iniciales de preparación y preprocesamiento de los datos, fundamentales para el entrenamiento de un modelo de clasificación basado en Redes Neuronales Convolucionales (CNN).

## Características Principales

*   **Carga y Preprocesamiento de Datos**: Implementación de funciones para cargar imágenes MRI y sus etiquetas correspondientes, redimensionamiento a un tamaño uniforme (128x128 píxeles) y conversión a escala de grises.
*   **Codificación de Etiquetas**: Transformación de etiquetas categóricas a formatos numéricos y one-hot encoding, adecuados para el entrenamiento de modelos de aprendizaje profundo.
*   **Normalización de Imágenes**: Escalado de los valores de píxeles de las imágenes a un rango de 0 a 1 para optimizar el rendimiento del modelo.
*   **División de Datos**: Preparación de conjuntos de datos de entrenamiento y prueba para la validación del modelo.
*   **Visualización de Datos**: Inclusión de ejemplos visuales de las imágenes preprocesadas para verificar la correcta carga y transformación de los datos.
*   **Tecnologías**: Desarrollado en Python, utilizando bibliotecas clave como `TensorFlow`, `Keras`, `OpenCV`, `NumPy`, `Pandas` y `Matplotlib`.

## Dataset

El proyecto utiliza el **Brain Tumor MRI Dataset** disponible en Kaggle [1]. Este conjunto de datos contiene imágenes MRI de cerebros clasificadas en cuatro categorías:

*   **Glioma**
*   **Meningioma**
*   **No Tumor**
*   **Pituitary**

El dataset se organiza en carpetas separadas para entrenamiento (`Training`) y prueba (`Testing`), con subcarpetas para cada clase de tumor.

## Preparación y Preprocesamiento de Datos

El notebook `Untitled13.ipynb` cubre los siguientes pasos para la preparación de datos:

1.  **Descarga del Dataset**: Utilización de `kagglehub` para descargar el dataset directamente.
2.  **Carga de Imágenes**: Las imágenes se cargan desde las carpetas de entrenamiento y prueba, se convierten a escala de grises y se redimensionan a 128x128 píxeles.
3.  **Codificación de Etiquetas**: Las etiquetas de clase se transforman usando `LabelEncoder` y luego se convierten a formato one-hot con `to_categorical`.
4.  **Normalización**: Los valores de píxeles de las imágenes se normalizan dividiéndolos por 255.0.
5.  **Expansión de Dimensiones**: Se añade una dimensión de canal a las imágenes (de `(height, width)` a `(height, width, 1)`) para que sean compatibles con las capas de entrada de los modelos CNN en Keras/TensorFlow.

## Uso

Para replicar el preprocesamiento de datos, siga estos pasos:

1.  **Descargar el Notebook**: Obtenga el archivo `Untitled13.ipynb`.
2.  **Configurar Entorno**: Asegúrese de tener un entorno Python con las dependencias listadas instaladas (ver `requirements.txt` si estuviera disponible, o instalar manualmente las bibliotecas mencionadas).
3.  **Ejecutar el Notebook**: Abra y ejecute el notebook en un entorno como Jupyter Lab, Jupyter Notebook o Google Colab. Las celdas se encargarán de descargar el dataset y realizar todo el preprocesamiento.

## Autor

Miguel Fonseca  
David Urrego (www.linkedin.com/in/david-urrego-serna-78561325b)
Maria Aristizabal

## Referencias

[1] [Brain Tumor MRI Dataset - Kaggle](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)
