# SpaceX Launch Analysis & Prediction

### Proyecto final del IBM Data Science

**Stack principal:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Plotly, Dash, Folium, BeautifulSoup, SQLite

---

## Objetivo

Predecir la probabilidad de aterrizaje exitoso del primer estadio del cohete **Falcon 9** de SpaceX, utilizando datos públicos obtenidos de la API oficial y de la página de Wikipedia.

SpaceX puede reducir drásticamente los costos de lanzamiento gracias a la reutilización de los cohetes. Poder predecir el éxito de un aterrizaje permite estimar el costo de un lanzamiento y apoyar la toma de decisiones comerciales.

---

## Descripción del Proyecto

Este proyecto integra un pipeline completo de **adquisición, limpieza, exploración, visualización y modelado predictivo de datos**, aplicado al caso SpaceX.

### Etapas del flujo de trabajo

#### 1. **Data Collection**
- Obtención de datos desde la **API REST de SpaceX** mediante `requests`.
- Web scraping de la tabla de lanzamientos desde **Wikipedia** con `BeautifulSoup`.
- Exportación de datasets intermedios en formato `.csv`.

#### 2. **Data Wrangling**
- Identificación y tratamiento de valores faltantes.
- Creación de nuevas variables (por ejemplo, etiqueta binaria `Landing_Outcome`).
- Normalización de tipos y exportación del dataset limpio.

#### 3. **Exploratory Data Analysis (EDA)**
- Análisis exploratorio con **Pandas, Matplotlib y Seaborn**.
- Consultas SQL con **SQLite** para análisis adicional.
- Visualización de correlaciones y tendencias de lanzamiento, payload y éxito.

#### 4. **Geospatial Analysis**
- Creación de mapas interactivos con **Folium** para visualizar ubicaciones de lanzamiento y resultados de misión.
- Cálculo de distancias y georreferenciación de los sitios de lanzamiento.

#### 5. **Dashboard Development**
- Construcción de un **dashboard interactivo** con **Plotly Dash**.
- Componentes: dropdown de sitios de lanzamiento, range slider de payload, pie chart y scatter plot.
- Callbacks dinámicos para filtrado en tiempo real.

#### 6. **Predictive Modeling**
- Entrenamiento de modelos de clasificación:
  - Logistic Regression  
  - Support Vector Machine (SVM)  
  - Decision Tree  
  - K-Nearest Neighbors (KNN)
- Optimización de hiperparámetros con **GridSearchCV**.
- Evaluación de modelos con matriz de confusión y accuracy score.

---

## Resultados Destacados

- Todos los modelos alcanzaron una **accuracy promedio de 0.83**.  
- Variables con mayor influencia: **payload mass**, **orbit type**, y **launch site**.  
- El sitio **KSC LC-39A** mostró el mayor índice de éxito en aterrizajes.  
- Se observó una tendencia positiva en la tasa de éxito anual (2013–2017).  

---

## Principales Herramientas y Librerías

| Categoría | Librerías / Herramientas |
|------------|---------------------------|
| **Procesamiento y análisis** | `pandas`, `numpy`, `scikit-learn` |
| **Visualización** | `matplotlib`, `seaborn`, `plotly`, `folium` |
| **Web scraping** | `requests`, `BeautifulSoup` |
| **Bases de datos** | `sqlite3` |
| **Dashboard** | `Dash` |
| **Entorno** | `Jupyter Notebook` |

---

[Ver presentación del proyecto (PDF)](./presentation/Presentation.pdf)

La presentación resume la metodología, visualizaciones y resultados del modelo predictivo. Incluye diagramas de flujo, consultas SQL, dashboards y análisis final.

---

## Conclusiones

- Se logró reproducir un flujo de trabajo de ciencia de datos completo, desde la adquisición hasta la predicción.  
- La reutilización de etapas y modularidad del código permite escalar el proyecto fácilmente.  
- Este análisis puede servir como punto de partida para desarrollar modelos más avanzados de predicción de costos y desempeño de misiones.

---
