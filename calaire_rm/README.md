# Air Quality Analysis in Santiago (2018-2024) / Análisis de Calidad del Aire en Santiago (2018-2024)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mcmoucheron/GitHub-Portfolio-for-Remote-Data-Roles/blob/main/calidad-aire-santiago/notebooks/analisis_calidad_aire_santiago.ipynb)

---

### Project Overview / Resumen del Proyecto

**[EN]** This project analyzes the evolution of fine particulate matter (PM2.5) pollution in five key communes of Santiago, Chile, from 2018 to 2024. The core objective is to investigate two critical questions: the extent of environmental inequality across the city and the true impact of the COVID-19 pandemic on air quality, once meteorological factors are controlled for.

**[ES]** Este proyecto analiza la evolución de la contaminación por material particulado fino (PM2.5) en cinco comunas clave de Santiago, Chile, entre 2018 y 2024. El objetivo central es investigar dos preguntas críticas: la magnitud de la desigualdad ambiental en la ciudad y el verdadero impacto de la pandemia de COVID-19 en la calidad del aire, una vez que se controlan los factores meteorológicos.

---

### Key Features / Características Clave

**[EN]**
*   **Reproducible ETL Pipeline:** A robust Python script loads raw data from the `datos_SINCA/` folder, cleans it, and loads it into a PostgreSQL (Neon) database, creating a reliable single source of truth.
*   **Legally Compliant Validation:** The analysis is strictly grounded in Chilean environmental law, using the standards from **D.S. N° 12/2011 (MMA)** and **D.S. N° 61/2008 (MINSAL)** to validate daily data.
*   **Advanced Statistical Modeling:** A Multiple Linear Regression (OLS) model is used to scientifically isolate the effect of the pandemic from meteorological variables, providing quantifiable and defensible insights.
*   **Clear Visual Communication:** The findings are presented through a series of clear visualizations, including time series plots, heatmaps, and a final regression coefficient plot.

**[ES]**
*   **Pipeline ETL Reproducible:** Un script robusto de Python carga los datos crudos desde la carpeta `datos_SINCA/`, los limpia y los carga en una base de datos PostgreSQL (Neon), creando una fuente única y fiable de verdad.
*   **Validación Conforme a la Normativa:** El análisis se basa estrictamente en la legislación ambiental chilena, utilizando los estándares de los **D.S. N° 12/2011 (MMA)** y **D.S. N° 61/2008 (MINSAL)** para validar los datos diarios.
*   **Modelado Estadístico Avanzado:** Se utiliza un modelo de Regresión Lineal Múltiple (OLS) para aislar científicamente el efecto de la pandemia de las variables meteorológicas, proporcionando insights cuantificables y defendibles.
*   **Comunicación Visual Clara:** Los hallazgos se presentan a través de una serie de visualizaciones claras, incluyendo series de tiempo, mapas de calor y un gráfico final de coeficientes de regresión.

---

### Tech Stack / Stack Tecnológico
*   **Language / Lenguaje:** Python
*   **Libraries / Librerías:** Pandas, SQLAlchemy, Matplotlib, Seaborn, Statsmodels, PyProj
*   **Database / Base de Datos:** PostgreSQL (cloud-native with Neon)
*   **Environment / Entorno:** Google Colab

---

### How to Run This Project / Cómo Ejecutar Este Proyecto

**[EN]** This project is designed to be fully reproducible.

1.  **Open in Colab:** Click the "Open in Colab" badge at the top of this README. This will launch the main notebook in a Google Colab session with this repository already cloned.
2.  **Set Up a Database:** You will need a PostgreSQL database. The code is configured to connect using a Neon connection string stored as a Colab Secret named `NEON_DB_URL`.
3.  **Run the Notebook:** Execute the notebook cells in order. The first block handles the entire ETL process, and the subsequent blocks perform the analysis and generate the visualizations.

**[ES]** Este proyecto está diseñado para ser completamente reproducible.

1.  **Abrir en Colab:** Haz clic en el ícono "Open in Colab" en la parte superior de este README. Esto abrirá el notebook principal en una sesión de Google Colab con este repositorio ya clonado.
2.  **Configurar una Base de Datos:** Necesitarás una base de datos PostgreSQL. El código está configurado para conectarse usando una cadena de conexión de Neon almacenada como un Secreto de Colab llamado `NEON_DB_URL`.
3.  **Ejecutar el Notebook:** Ejecuta las celdas del notebook en orden. El primer bloque se encarga de todo el proceso ETL, y las celdas siguientes realizan el análisis y generan las visualizaciones.

---

### Legal and Data Sources / Fuentes de Datos y Legales

**[EN]** The analysis adheres to the following Chilean environmental regulations:
*   **D.S. N° 12/2011 (MMA):** [Primary Air Quality Standard for PM2.5](https://www.bcn.cl/leychile/navegar?idNorma=1025202)
*   **D.S. N° 61/2008 (MINSAL):** [Regulation for Air Pollutant Measurement Stations](https://www.bcn.cl/leychile/navegar?idNorma=281728)

**[ES]** El análisis se adhiere a las siguientes normativas ambientales chilenas:
*   **D.S. N° 12/2011 (MMA):** [Establece Norma Primaria de Calidad Ambiental para MP2,5](https://www.bcn.cl/leychile/navegar?idNorma=1025202)
*   **D.S. N° 61/2008 (MINSAL):** [Aprueba Reglamento de Estaciones de Medición de Contaminantes Atmosféricos](https://www.bcn.cl/leychile/navegar?idNorma=281728)