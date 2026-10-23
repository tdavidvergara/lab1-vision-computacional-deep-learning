# Laboratorio 1: Clasificación de Imágenes mediante Bag of Visual Words (BoVW)

**Asignatura:** Visión Computacional con Deep Learning  
**Institución:** Universidad Autónoma de Occidente (UAO)  
**Profesor:** Nicolas Llanos Neuta  
**Semestre:** 2026-1
**Integrantes:** Sebastián Giraldo, Luis Murillo, David Vergara

---

## Descripción del proyecto

Este repositorio contiene la implementación y documentación del Laboratorio 1 de la asignatura Visión Computacional con Deep Learning. El proyecto aborda la clasificación automática de imágenes mediante la metodología **Bag of Visual Words (BoVW)**, una técnica de representación de imágenes basada en la extracción de características locales y la construcción de un vocabulario visual.

El objetivo principal es desarrollar un pipeline de clasificación que permita analizar y comparar el desempeño de diferentes extractores de características locales, utilizando **SIFT** como método de referencia y un extractor alternativo, como **ORB, BRISK o SURF**, según la configuración implementada.

Las representaciones visuales obtenidas se emplean para entrenar y evaluar dos algoritmos de clasificación:

- **SVM lineal (Support Vector Machine):** clasificador basado en la búsqueda de un hiperplano que permita separar las clases.
- **k-NN (k-Nearest Neighbors):** clasificador basado en las etiquetas de los ejemplos más cercanos dentro del espacio de características.

Finalmente, se comparan los resultados obtenidos para estudiar cómo la elección del extractor, el tamaño del vocabulario visual y el algoritmo de clasificación influyen en el rendimiento del sistema.

## Objetivos

### Objetivo general

Implementar un sistema de clasificación de imágenes basado en Bag of Visual Words y evaluar experimentalmente el desempeño de diferentes extractores de características locales y algoritmos de clasificación.

### Objetivos específicos

- Explorar y preparar un conjunto de imágenes organizado por categorías.
- Extraer características locales mediante SIFT y un extractor alternativo.
- Visualizar y comparar los puntos clave (*keypoints*) detectados por cada método.
- Construir un vocabulario visual mediante algoritmos de agrupamiento como K-Means o MiniBatchKMeans.
- Representar cada imagen mediante un histograma de frecuencias de palabras visuales.
- Entrenar clasificadores SVM lineal y k-NN utilizando las representaciones BoVW.
- Evaluar los modelos mediante métricas de clasificación y matrices de confusión.
- Analizar las ventajas, limitaciones y diferencias de rendimiento de los métodos evaluados.

## Fundamentos teóricos

### 1. Bag of Visual Words (BoVW)

Bag of Visual Words es una técnica que representa una imagen mediante la frecuencia de aparición de patrones visuales locales. Su funcionamiento es análogo al modelo Bag of Words utilizado en procesamiento de lenguaje natural, donde los documentos se representan mediante frecuencias de palabras.

En BoVW, los descriptores visuales extraídos de las imágenes se agrupan para construir un vocabulario de patrones representativos. Posteriormente, cada imagen se representa mediante un histograma que indica cuántas veces aparecen los elementos de dicho vocabulario.

### 2. SIFT y extractores alternativos

- **SIFT (Scale-Invariant Feature Transform):** detecta puntos de interés y genera descriptores de 128 dimensiones, diseñados para ofrecer robustez ante cambios de escala y rotación.
- **ORB (Oriented FAST and Rotated BRIEF):** combina detección de puntos clave con descriptores binarios, ofreciendo una alternativa computacionalmente eficiente.
- **BRISK (Binary Robust Invariant Scalable Keypoints):** utiliza descriptores binarios y un mecanismo de muestreo diseñado
