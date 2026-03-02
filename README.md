# Regresion lineal
## Tema Principal: Precificación inmobiliaria

## Descripción
Este proyecto, titulado "Precificación inmobiliaria", tiene como objetivo estimar los precios de las propiedades. Los objetivos principales incluyen identificar los aspectos más influyentes en la precificación de bienes raíces, comprender cuál de estos aspectos es el más relevante y, en última instancia, precificar una nueva propiedad. Este cuaderno sirve como una aplicación práctica de las técnicas de regresión lineal dentro de un contexto de curso de ciencia de datos, centrándose en la comprensión y construcción de modelos predictivos para los precios de la vivienda.

## Conceptos Cubiertos
*   **Regresión Lineal (OLS)**: Construcción de modelos para establecer relaciones lineales entre variables.
*   **Análisis de Correlación**: Medición de la fuerza y dirección de las relaciones lineales entre variables utilizando el coeficiente de correlación de Pearson y visualización con mapas de calor.
*   **División de Datos**: División de conjuntos de datos en conjuntos de entrenamiento y prueba para evaluar el rendimiento y la generalización del modelo (`train_test_split`).
*   **Evaluación del Modelo**: Evaluación del rendimiento del modelo utilizando métricas como R-squared (coeficiente de determinación).
*   **Análisis de Residuos**: Examen de la distribución y los patrones de los residuos para verificar los supuestos del modelo (normalidad, homocedasticidad).
*   **Multicolinealidad**: Detección de alta correlación entre variables independientes utilizando el Factor de Inflación de la Varianza (VIF) y comprensión de sus implicaciones.
*   **Heterocedasticidad**: Identificación de la varianza no constante de los residuos, a menudo visualizada a través de diagramas de dispersión de valores predichos frente a residuos.
*   **Preprocesamiento de Datos**: Pasos como eliminar columnas irrelevantes ('Id') y agregar un término constante para `statsmodels`.
*   **Visualización de Datos**: Uso de diagramas de dispersión, histogramas y `pairplots` para explorar relaciones y distribuciones dentro de los datos.

## Herramientas y Librerías Utilizadas
*   **pandas**: Para manipulación y análisis de datos.
*   **numpy**: Para operaciones numéricas, especialmente con arreglos.
*   **matplotlib.pyplot**: Para visualización básica de datos.
*   **seaborn**: Para crear gráficos estadísticos informativos y atractivos.
*   **plotly.express**: Para visualizaciones de datos interactivas.
*   **sklearn.model_selection.train_test_split**: Para dividir datos en conjuntos de entrenamiento y prueba.
*   **statsmodels.formula.api.ols**: Para ajustar modelos de Mínimos Cuadrados Ordinarios (OLS) utilizando sintaxis de fórmula.
*   **statsmodels.api**: Para modelado estadístico, incluida la adición de constantes a las matrices de características.
*   **sklearn.metrics.r2_score**: Para calcular la métrica R-squared para la evaluación del modelo.
*   **statsmodels.stats.outliers_influence.variance_inflation_factor (VIF)**: Para evaluar la multicolinealidad entre las variables predictoras.

## Conjuntos de Datos
*   `/content/drive/MyDrive/Regresion Lineal/precios_casas.csv`: Conjunto de datos principal para la precificación de bienes raíces.
*   `/content/drive/MyDrive/Regresion Lineal/hoteis.csv`: Conjunto de datos utilizado para una actividad sobre la precificación de hoteles.
*   `/content/drive/MyDrive/Regresion Lineal/nuevas_casas.csv`: Conjunto de datos que contiene nuevos datos de casas para la predicción.
*   `/content/drive/MyDrive/Regresion Lineal/usina.csv`: Conjunto de datos para una actividad sobre la eficiencia de la planta de energía, utilizado para el análisis de multicolinealidad y residuos.
*   **Todos se encuentran en el repositorio para su descarga**

## Estructura del Cuaderno
El cuaderno está organizado en varias secciones clave:
1.  **Ajustando una recta**: Introduce el conjunto de datos, realiza la inspección inicial de los datos y explora la correlación entre variables, particularmente `area_primer_piso` y `precio_de_venta`.
2.  **Explicando la recta**: Detalla el proceso de dividir los datos en conjuntos de entrenamiento y prueba, construir un modelo de regresión lineal simple (`model_0`), analizar sus coeficientes y R-squared, y examinar los residuos.
3.  **Añadiendo otras características**: Amplía el análisis explorando otros factores que influyen en el precio, construyendo múltiples modelos de regresión lineal con características adicionales (`model_1`, `model_2`, `model_3`) y comparando su rendimiento.
4.  **Precificando las casas**: Demuestra cómo usar el modelo de mejor rendimiento (`model_3`) para predecir precios de propiedades nuevas individuales y un lote de propiedades nuevas.
5.  **Investigando el modelo**: Se centra en diagnósticos avanzados del modelo, incluida la verificación de multicolinealidad utilizando VIF y el análisis de residuos para heterocedasticidad, aplicado al conjunto de datos `usina.csv`.
6.  **Actividades**: Ejercicios prácticos para que los usuarios apliquen los conceptos aprendidos a nuevos conjuntos de datos (`hoteis.csv` y `usina.csv`) realizando un análisis inicial, construyendo modelos de regresión y comparándolos, así como realizando análisis de multicolinealidad y residuos.
