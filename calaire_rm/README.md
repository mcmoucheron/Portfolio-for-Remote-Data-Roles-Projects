# Air Quality Analysis in Santiago (2018-2024) / Análisis de Calidad del Aire en Santiago (2018-2024)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mcmoucheron/GitHub-Portfolio-for-Remote-Data-Roles/blob/main/calidad-aire-santiago/notebooks/analisis_calidad_aire_santiago.ipynb)

---

### Project Overview / Resumen del Proyecto

**[EN]** This project, titled "Monthly Evolution of Air Quality in Santiago (2018-2024) with an Environmental Inequality Focus", analyzes the evolution of fine particulate matter (PM2.5) pollution in five communes of Santiago, Chile. The main objective is to build a reproducible data workflow using Google Colab and PostgreSQL to analyze and visualize environmental inequality and the impact of the COVID-19 pandemic. The analysis addresses key questions, including:

* **KPI 1:** Monthly average of PM2.5 per commune.
* **KPI 2:** Percentage of critical days per commune and month.
* **KPI 3:** Comparison by temporal blocks: pre-COVID (2019), COVID (2020-2021), and post-COVID (2022-2024).

**[ES]** Este proyecto, titulado "Evolución mensual de la calidad del aire en Santiago (2018-2024) con enfoque de desigualdad ambiental", analiza la evolución de la contaminación por material particulado fino (PM2.5) en cinco comunas de Santiago, Chile. El objetivo principal es construir un flujo de trabajo de datos reproducible usando Google Colab y PostgreSQL para analizar y visualizar la desigualdad ambiental y el impacto de la pandemia de COVID-19. El análisis responde a preguntas clave, que incluyen:

* **KPI 1:** Promedio mensual de PM2.5 por comuna.
* **KPI 2:** % de días críticos por comuna y mes.
* **KPI 3:** Comparación por bloques temporales: pre-COVID (2019), COVID (2020-2021) y post-COVID (2022-2024).

---

### Key Objectives / Objetivos Clave

**[EN]**
* **ETL Pipeline:** Load raw data from CSV files, clean it, and load it into a PostgreSQL (Neon) database.
* **Compliance Analysis:** Validate the data according to Chilean environmental regulations to ensure statistical robustness.
* **Statistical Analysis:** Utilize a linear regression model to isolate the effect of the pandemic from meteorological variables.
* **Visualization:** Communicate findings through time series and bar charts.

**[ES]**
* **Pipeline ETL:** Cargar datos brutos desde archivos CSV, limpiarlos y cargarlos en una base de datos PostgreSQL (Neon).
* **Análisis de Cumplimiento:** Validar los datos de acuerdo con las regulaciones ambientales chilenas para asegurar la robustez estadística.
* **Análisis Estadístico:** Utilizar un modelo de regresión lineal para aislar el efecto de la pandemia de las variables meteorológicas.
* **Visualización:** Comunicar los hallazgos a través de series de tiempo y gráficos de barras.

---

### Project Structure / Estructura del Proyecto

**[EN]** The project is organized as follows:

* `notebooks/`: Contains the main Jupyter Notebook for the analysis.
    * `analisis_calidad_aire_santiago.ipynb`: The primary notebook to run the analysis.
* `data/`: Stores the raw data files used for the analysis.
    * `datos_SINCA/`: The raw data folder.

**[ES]** El proyecto se organiza de la siguiente manera:

* `notebooks/`: Contiene el Jupyter Notebook principal para el análisis.
    * `analisis_calidad_aire_santiago.ipynb`: El notebook principal para ejecutar el análisis.
* `data/`: Almacena los archivos de datos brutos utilizados para el análisis.
    * `datos_SINCA/`: La carpeta de datos brutos.

---

### Tech Stack / Stack Tecnológico

* **Language / Lenguaje:** Python
* **Libraries / Librerías:** Pandas, SQLAlchemy, Matplotlib, Seaborn, Statsmodels
* **Database / Base de Datos:** PostgreSQL (Neon)
* **Environment / Entorno:** Google Colab

---

### Key Findings / Hallazgos Principales

**[EN]** The analysis concluded that, even after controlling for meteorological factors, the pandemic period (2020-2021) had a statistically significant reduction in PM2.5 levels. Additionally, a severe environmental inequality was quantified, with communes like Pudahuel and Quilicura showing systematically higher pollution levels than Las Condes.

**[ES]** El análisis concluyó que, incluso después de controlar por factores meteorológicos, el periodo de la pandemia (2020-2021) tuvo una reducción estadísticamente significativa en los niveles de PM2.5. Adicionalmente, se cuantificó una severa desigualdad ambiental, con comunas como Pudahuel y Quilicura mostrando niveles de contaminación sistemáticamente más altos que Las Condes.

---

### How to Run This Project / Cómo Ejecutar Este Proyecto

**[EN]** To reproduce this analysis, please follow these steps:

1.  **Open in Colab:** Click the "Open in Colab" badge at the top of this README to launch the main notebook in Google Colab.
2.  **Get the data:** This analysis requires hourly data from January 1, 2018, to December 31, 2024. You'll need PM2.5 data for five stations and temperature, wind speed, and wind direction data for four of the five stations (excluding Las Condes). You'll need to download the CSV files for each station from the official SINCA website.
    * Go to the SINCA website: [https://sinca.mma.gob.cl/index.php/region/index/id/V#](https://sinca.mma.gob.cl/index.php/region/index/id/V#).
    * Select the following stations: **Las Condes, Parque O'Higgins, Puente Alto, Pudahuel, and Quilicura**.
    * Download the data for PM2.5, temperature, wind speed (`VV`), and wind direction (`DV`).
    * Make sure to save each file with the correct naming format (e.g., `las_condes.csv`, `t_las_condes.csv`, `vv_las_condes.csv`, etc.).
3.  **Upload the data to Colab:** To make the notebook work, you must upload the downloaded files.
    * In the Colab file explorer (folder icon on the left), click the "Upload" button (page icon with an up arrow).
    * Upload all the CSV files you downloaded. The code will handle creating the `datos_SINCA` folder and moving the files to that location.
4.  **Update Connection String:** In the first code block, replace the placeholder for the `neon_connection_string` with your own PostgreSQL database connection string.
5.  **Run the Notebook:** Run the notebook cells in order from top to bottom. The first cell will handle the entire ETL process, and the subsequent cells will perform the analysis and generate the visualizations.

---

**[ES]** Para reproducir este análisis, por favor sigue estos pasos:

1.  **Abrir en Colab:** Haz clic en el ícono "Open in Colab" en la parte superior de este README para abrir el notebook principal en Google Colab.
2.  **Obtener los datos:** El análisis requiere datos desde el 1 de enero de 2018 hasta el 31 de diciembre de 2024. Necesitarás datos de PM2.5 para las cinco estaciones, y datos de temperatura, velocidad y dirección del viento para **cuatro de las cinco estaciones** (excluyendo Las Condes). Deberás descargar los archivos CSV para cada estación desde el sitio web oficial de SINCA.
    * Ve al sitio web de SINCA: [https://sinca.mma.gob.cl/index.php/region/index/id/V#](https://sinca.mma.gob.cl/index.php/region/index/id/V#).
    * Selecciona las estaciones: **Las Condes, Parque O'Higgins, Puente Alto, Pudahuel y Quilicura**.
    * Descarga los datos de las variables PM2.5, temperatura, velocidad del viento (`VV`) y dirección del viento (`DV`).
    * **Guarda los archivos con el formato correcto**. Por ejemplo: `las_condes.csv`, `t_las_condes.csv`, `vv_las_condes.csv`, etc.
3.  **Subir los datos a Colab:** Para que el notebook funcione, debes subir los archivos descargados.
    * En el explorador de archivos de Colab (ícono de carpeta a la izquierda), haz clic en el botón "Subir" (ícono de página con una flecha hacia arriba).
    * Sube todos los archivos CSV que descargaste. El código se encargará de crear la carpeta `datos_SINCA` y de mover los archivos a esa ubicación.
4.  **Actualizar la Cadena de Conexión:** En el primer bloque de código, reemplaza el marcador de posición de `neon_connection_string` con tu propia cadena de conexión a la base de datos PostgreSQL.
5.  **Ejecutar el Notebook:** Ejecuta las celdas del notebook en orden, de arriba hacia abajo. La primera celda se encargará de todo el proceso ETL, y las celdas siguientes realizarán el análisis y generarán las visualizaciones.
---

### Link to Notebook / Enlace al Notebook

**[EN]** You can find the full analysis notebook directly at:
[https://github.com/mcmoucheron/Portfolio-for-Remote-Data-Roles-Projects/blob/main/calaire_rm/notebooks/analisis_calidad_aire_aistudio.ipynb](https://github.com/mcmoucheron/Portfolio-for-Remote-Data-Roles-Projects/blob/main/calaire_rm/notebooks/analisis_calidad_aire_aistudio.ipynb)

**[ES]** Puedes encontrar el notebook completo del análisis directamente en:
[https://github.com/mcmoucheron/Portfolio-for-Remote-Data-Roles-Projects/blob/main/calaire_rm/notebooks/analisis_calidad_aire_aistudio.ipynb](https://github.com/mcmoucheron/Portfolio-for-Remote-Data-Roles-Projects/blob/main/calaire_rm/notebooks/analisis_calidad_aire_aistudio.ipynb)

---

### Project Brief / Enunciado del Proyecto

**[EN]** The full project brief from which this analysis was developed is available in the `Enunciado del ejercicio.pdf` file in this repository.
**[ES]** El enunciado completo del proyecto a partir del cual se desarrolló este análisis está disponible en el archivo `Enunciado del ejercicio.pdf` en este repositorio.
