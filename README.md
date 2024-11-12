![Energía_Eléctrica_TDF](/reports/figures/banner_flat1.jpg)

### Tecnicatura Superior en Ciencia de Datos e Inteligencia Artificial
___
### Aprendizaje Automático: "Predicción del consumo de Energía Eléctrica en TDF"
___
### *Objetivo del Modelo*
El principal objetivo de este modelo de Aprendizaje Automático es predecir el consumo total de energía eléctrica en la provincia de Tierra del Fuego según el tipo de usuario y el periodo de tiempo. Esta predicción ayudará a las autoridades y empresas energéticas locales a prever fluctuaciones en la demanda y a tomar decisiones más informadas sobre la generación, compra o importación de energía.
___
### *Contexto y Relevancia*
Tierra del Fuego es una de las provincias más australes del mundo, lo que implica condiciones climáticas adversas durante gran parte del año, con inviernos fríos y largos. Estas condiciones generan una demanda energética elevada, especialmente en el ámbito residencial, para calefacción y otros servicios esenciales. A pesar de tener una población relativamente pequeña en comparación con otras provincias argentinas, la alta variabilidad climática y la expansión de la infraestructura local hacen que el manejo del consumo energético sea crucial para el bienestar de sus habitantes y para la sostenibilidad económica de la región.

Además, la provincia posee un perfil económico orientado a la industria manufacturera, con grandes y medianas demandas energéticas en fábricas y empresas de servicios, lo cual contribuye a la complejidad del problema energético. Dado que Tierra del Fuego está aislada del sistema interconectado nacional, su capacidad de generación y distribución eléctrica debe ser cuidadosamente administrada para evitar costos adicionales o el riesgo de cortes energéticos.

Relevancia Local y Motivación La elección de este problema se debe a su relevancia estratégica para la región. La optimización del consumo energético no solo tiene un impacto directo en el costo operativo para industrias y usuarios residenciales, sino que también puede ayudar a las autoridades locales a planificar de manera más eficiente la distribución de la energía. Esto es particularmente importante en una provincia donde la energía tiene un costo elevado debido a su lejanía de los principales centros de generación del país.

---
### [Abstract - Machine Learning Model](https://github.com/ckriztian/Energia_Electrica_TDF/blob/main/references/Abstract.pdf)
---
### [Link del video-presentación](https://youtu.be/WNQCU6luxpc)
___
### *Preguntas de Investigación:*
- ¿Es posible predecir con precisión el consumo de energía eléctrica en Tierra del Fuego utilizando técnicas de aprendizaje automático?
- ¿Qué características, como tipo de usuario y periodo tienen mayor impacto en el consumo de energía eléctrica?  
- ¿Existen tendencias de crecimiento o decrecimiento en el consumo energético a lo largo de los años?
- ¿Cuál es el rendimiento comparativo de diferentes algoritmos de aprendizaje automático en la predicción de consumo de energía eléctrica por tipo de usuario?
___
### *Descripción del Dataset y Origen*
Para una descripción detallada del dataset, incluyendo la cantidad de instancias, características (columnas), tipos de datos, y el origen del dataset, consultar el siguiente link:
 [Descripción y características del Dataset](https://github.com/ckriztian/Energia_Electrica_TDF/blob/main/docs/README.md) 
___
### *Autores y Reconocimientos*
- **Vera Quijano Cristian E.** - Desarrollador Principal
- **Mirabete Martin** - Docente y asesor del proyecto

___

### Resultados:
***R² Score (Coeficiente de Determinación):***
- Linear Regression: 0.9872
- Random Forest: 0.9744
- XGBoost: 0.9674
- KNN: 0.9666
- Gradient Boosting: 0.9757
- SVR: -0.0352

------------------------------

***MAE (Mean Absolute Error):***
- Linear Regression: 593311.02 = 1.40%
- Random Forest: 814488.45 = 1.92%
- XGBoost: 954526.14 = 2.25%
- KNN: 896625.47 = 2.11%
- Gradient Boosting: 798374.24 = 1.88%
- SVR: 5426058.08 = 12.81%

***MSE (Mean Squared Error):***
- Linear Regression: 509935476251.78
- Random Forest: 1014417384702.14
- XGBoost: 1294538785682.29
- KNN: 1325128449014.10
- Gradient Boosting: 963058374881.40
- SVR: 41082866774206.50

---

### Reporte y Conclusiones finales:

[Resultados y Conclusiones](/docs/Reporte%20de%20Resultados.md)

---





## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see www.mkdocs.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for 
│                         energiaelectricatdf and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
│
└── energiaelectricatdf   <- Source code for use in this project.
    │
    ├── __init__.py             <- Makes energiaelectricatdf a Python module
    │
    ├── config.py               <- Store useful variables and configuration
    │
    ├── dataset.py              <- Scripts to download or generate data
    │
    ├── features.py             <- Code to create features for modeling
    │
    ├── modeling                
    │   ├── __init__.py 
    │   ├── predict.py          <- Code to run model inference with trained models          
    │   └── train.py            <- Code to train models
    │
    └── plots.py                <- Code to create visualizations
```
<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

---

