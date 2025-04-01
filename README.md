# Análisis de Clientes y Cancelación de Membresía – Model Fitness

[![Licencia MIT](https://img.shields.io/badge/Licencia-MIT-blue.svg)](LICENSE)
[![Python Version](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)

## Descripción del Proyecto
El presente proyecto tiene como objetivo analizar los datos de los clientes de la cadena de gimnasios **Model Fitness**. Se busca identificar target groups y desarrollar propuestas de marketing estratégicas basadas en los resultados obtenidos, con énfasis en la predicción de cancelación de membresías (churn) y la segmentación de clientes mediante técnicas de clustering.

## Contenido
- [Inicialización](#inicialización)
- [Exploración y Preprocesamiento de Datos](#exploración-y-preprocesamiento-de-datos)
- [Análisis y Visualización](#análisis-y-visualización)
- [Modelo de Predicción de Cancelación de Membresía](#modelo-de-predicción-de-cancelación-de-membresía)
- [Clustering y Estrategias de Marketing](#clustering-y-estrategias-de-marketing)
- [Conclusiones y Propuestas](#conclusiones-y-propuestas)
- [Aplicaciones en Negocios y Finanzas](#aplicaciones-en-negocios-y-finanzas)
- [Instalación y Uso](#instalación-y-uso)
- [Contribución](#contribución)
- [Licencia](#licencia)
- [Contacto](#contacto)

---

## Inicialización
En esta primera etapa se cargan las librerías necesarias y se importa el dataset (`gym_churn_us.csv`), que contiene 4,000 filas y 14 columnas. Los nombres de las columnas se estandarizan a minúsculas para facilitar su manipulación. Las librerías utilizadas incluyen:

- **pandas** y **numpy** para la manipulación y análisis de datos.
- **matplotlib** y **seaborn** para la visualización.
- **scikit-learn** para la creación de modelos predictivos y segmentación (Logistic Regression, Random Forest, KMeans).
- **scipy** para el análisis jerárquico y la creación de dendrogramas.

---

## Exploración y Preprocesamiento de Datos
La exploración inicial del dataset permitió identificar y validar los siguientes aspectos:

- **Estructura de los Datos:**  
  Se muestran ejemplos de las primeras filas para conocer el formato de cada variable (género, ubicación, edad, etc.).
  
- **Estandarización:**  
  Se convierten los nombres de las columnas a minúsculas, lo que facilita el posterior manejo y análisis de la información.

- **Validación:**  
  Se verificó que los datos no contengan valores nulos, ausentes ni duplicados, asegurando la calidad para el análisis posterior.

---

## Análisis y Visualización
Se llevaron a cabo diversas exploraciones de los datos para comprender relaciones entre variables, entre ellas:

- **Comparación de Clientes Activos vs. Cancelados:**  
  Se agruparon los datos según la variable `churn` para obtener estadísticas promedio de las demás variables.

- **Visualización de Correlaciones:**  
  Se generó un mapa de calor para identificar relaciones significativas entre las variables del dataset.

- **Distribución de Variables:**  
  Se utilizaron histogramas para visualizar la distribución de cada variable en función de la segmentación por clusters (obtenidos posteriormente).

---

## Modelo de Predicción de Cancelación de Membresía
El proyecto desarrolla un modelo predictivo para identificar la probabilidad de cancelación de membresía. Entre los pasos realizados se incluyen:

1. **Selección de Variables:**  
   Se separó la variable objetivo `churn` y se utilizaron las restantes como predictores.

2. **División del Dataset:**  
   Se dividieron los datos en conjuntos de entrenamiento y validación (80/20).

3. **Construcción del Modelo:**  
   Se implementó un modelo de Regresión Logística para predecir la cancelación, evaluando métricas como accuracy, precision y recall.

---

## Clustering y Estrategias de Marketing
Para segmentar la clientela, se aplicaron técnicas de clustering:

- **Estandarización:**  
  Se utilizaron escaladores (StandardScaler) para normalizar los datos.

- **Análisis Jerárquico:**  
  Con el método *linkage* de SciPy se generó un dendrograma, identificándose cinco clusters de clientes.

- **Análisis de Clusters:**  
  Se analizó la distribución de variables por cluster, en particular la tasa de cancelación (`churn`), lo cual permitió identificar grupos con comportamientos diferenciados.

### Estrategias de Marketing Propuestas
Con base en los análisis, se sugieren las siguientes estrategias:

1. **Para Grupos Grandes (Clusters 0, 2 y 4):**  
   - Ofrecer descuentos mensuales y promociones en contratos a largo plazo para incentivar la retención.
   
2. **Para Grupos con Mayor Gasto (Clusters 1 y 3):**  
   - Proporcionar servicios exclusivos (entrenamiento personal, acceso prioritario a clases, paquetes de bienestar) para aumentar la percepción de valor agregado.

3. **Incentivar la Constancia:**  
   - Implementar programas de recompensas que premien la asistencia regular al gimnasio.

4. **Fomentar la Asistencia de Clientes Cercanos:**  
   - Enviar recordatorios y organizar eventos locales para reforzar el vínculo con el gimnasio.

---

## Conclusiones y Propuestas
El análisis de los datos de Model Fitness permitió identificar segmentos de clientes con distintos patrones de cancelación y consumo. Se evidenció que:

- La probabilidad de churn se asocia con variables como la duración del contrato y el gasto adicional.
- Existen diferencias notables entre clientes activos y aquellos que cancelan la membresía, lo que permite diseñar estrategias de retención y marketing personalizadas.

Estas conclusiones sirven de base para proponer acciones orientadas a mejorar la retención de clientes y optimizar las estrategias de marketing de la cadena.

---

## Aplicaciones en Negocios y Finanzas
Las técnicas aplicadas en este proyecto tienen amplia aplicación en el análisis de datos para la toma de decisiones en negocios y finanzas:

- **Predicción de Riesgos y Cancelaciones:**  
  Modelos predictivos ayudan a anticipar comportamientos que pueden afectar la rentabilidad de una empresa.

- **Segmentación de Clientes:**  
  La aplicación de clustering permite identificar segmentos con características comunes, facilitando estrategias de marketing y promociones dirigidas.

- **Optimización de Recursos:**  
  El análisis de datos y la estandarización de información permiten realizar proyecciones más precisas y tomar decisiones informadas sobre inversiones y asignación de recursos.

---

## Instalación y Uso

### Requisitos
- Python 3.x
- pandas, numpy, matplotlib, seaborn, scikit-learn, scipy

### Pasos para Ejecutar el Proyecto
1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/tu_usuario/model_fitness_analysis.git

