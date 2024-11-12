Reporte de Resultados: Consumo de Energía eléctrica de TDF
---

## Análisis Exploratorio de Datos

Selecciona las característica (columnas) Año, Grandes Demandas, Uso Residencial, Uso General y la variable objetivo Total:

## Modelos de Aprendizaje automático: supervisados:

## **R² Score (Coeficiente de Determinación):**
- Linear Regression: 0.9872
- Random Forest: 0.9744
- XGBoost: 0.9674
- KNN: 0.9666
- Gradient Boosting: 0.9757
- SVR: -0.0352

## **MAE (Mean Absolute Error)**
- Linear Regression: 593311.02 = 1.40%
- Random Forest: 814488.45 = 1.92%
- XGBoost: 954526.14 = 2.25%
- KNN: 896625.47 = 2.11%
- Gradient Boosting: 798374.24 = 1.88%
- SVR: 5426058.08 = 12.81%

## **MSE (Mean Squared Error):**
- Linear Regression: 509935476251.78
- Random Forest: 1014417384702.14
- XGBoost: 1294538785682.29
- KNN: 1325128449014.10
- Gradient Boosting: 963058374881.40
- SVR: 41082866774206.50


## **Análisis de Modelos**

- **Regresión Lineal:**

Este modelo mostró el mejor rendimiento en todas las métricas evaluadas. Con un R² de 0.9872, la Regresión Lineal es capaz de explicar el 98.7% de la variabilidad en el consumo de energía. Además, tiene el MAE más bajo (1.40%), lo que indica que sus predicciones son muy precisas, y el MSE más bajo de todos los modelos, reflejando una baja penalización por errores grandes. Estos resultados sugieren que la Regresión Lineal es un modelo robusto y adecuado para predecir el consumo energético en el dataset analizado.

- **Random Forest:**

El modelo de Random Forest tuvo un buen rendimiento, con un R² de 0.9744, lo que indica que puede explicar el 97.4% de la variabilidad del consumo de energía. Sin embargo, su MAE fue de 1.92%, y su MSE superó al de la Regresión Lineal y Gradient Boosting, indicando que este modelo tiene una menor precisión al predecir el consumo. A pesar de ser un modelo no lineal y más complejo, no logró superar a la Regresión Lineal, aunque sigue siendo una opción válida debido a su buena capacidad de ajuste y robustez.

- **XGBoost:**

El modelo XGBoost mostró un desempeño aceptable con un R² de 0.9674, lo que significa que explica el 96.7% de la variabilidad. Sin embargo, presentó un MAE relativamente alto (2.25%) y uno de los mayores MSE entre los modelos evaluados, lo que indica menor precisión. XGBoost es conocido por su capacidad de manejar datos con alta dimensionalidad y relaciones no lineales, pero en este caso, no se benefició tanto de esas características, quedando por detrás de la Regresión Lineal y otros modelos como Gradient Boosting.

- **KNN (K-Nearest Neighbors):**

El modelo KNN tuvo un rendimiento moderado, con un R² de 0.9666. Aunque explica el 96.6% de la variabilidad, su MAE fue de 2.11%, lo que indica un error de predicción mayor que el de los modelos de Regresión Lineal y Random Forest. Además, su MSE fue relativamente alto, lo que sugiere que el modelo tiende a cometer errores más grandes. KNN puede ser menos efectivo en datasets con muchos puntos de datos o características complejas, lo que podría explicar su desempeño inferior en este análisis.

- **Gradient Boosting:**

Gradient Boosting fue uno de los modelos más competitivos, con un R² de 0.9757, superando ligeramente a Random Forest. Su MAE fue de 1.88%, y su MSE fue inferior al de Random Forest, lo que muestra que es un modelo preciso y efectivo. Aunque no logró superar a la Regresión Lineal, se desempeñó de forma similar y puede considerarse una alternativa fuerte. Gradient Boosting aprovecha bien las relaciones no lineales en los datos, pero en este caso, la Regresión Lineal sigue siendo superior.

- **SVR (Support Vector Regressor):**

El modelo SVR presentó el peor rendimiento de todos los evaluados, con un R² negativo (-0.0352), lo que indica que es menos efectivo que simplemente usar la media del consumo como predicción. Su MAE fue extremadamente alto (12.81%), al igual que su MSE, lo que muestra grandes errores en sus predicciones. Estos resultados sugieren que SVR no es adecuado para este tipo de datos, posiblemente debido a su dificultad para capturar la complejidad y las variaciones del consumo de energía en este dataset.

---

### Conclusiones:

1. ¿Es posible predecir con precisión el consumo de energía eléctrica en Tierra del Fuego utilizando técnicas de aprendizaje automático?

Sí, es posible predecir el consumo de energía eléctrica con buena precisión. El mejor rendimiento lo obtuvo el modelo de Regresión Lineal, con un R² de 0.987, lo que indica que el modelo explica el 98.7% de la variabilidad en el consumo total de energía. Aunque otros modelos como Random Forest y XGBoost también mostraron resultados aceptables, la Regresión Lineal destacó como el modelo más preciso.

---

2. ¿Qué características, como tipo de usuario y periodo, tienen mayor impacto en el consumo de energía eléctrica?

En este análisis, las características utilizadas fueron:

- Grandes Demandas
- Uso Residencial
- Uso General
- Año (con un impacto negativo)

De acuerdo con los coeficientes del modelo de Regresión Lineal, Grandes Demandas fue la característica con mayor influencia positiva en el consumo total de energía, seguida por Uso Residencial y Uso General. Sin embargo, se observó un coeficiente negativo para la variable Año, lo que indica una posible tendencia a la baja en el consumo a medida que pasan los años, después de un período de crecimiento.

---

3. ¿Existen tendencias de crecimiento o decrecimiento en el consumo energético a lo largo de los años?

Según la visualización de la tendencia de consumo de energía eléctrica en Tierra del Fuego, se observa una tendencia general al crecimiento a lo largo de los años. Aunque hay periodos donde el consumo disminuye, estas bajas son temporales y no afectan la tendencia alcista predominante. El pico histórico de consumo se alcanzó en el año 2022, lo cual podría estar asociado a factores específicos como condiciones climáticas extremas, un aumento en la actividad industrial o cambios en el comportamiento de los usuarios.

---

4. ¿Cuál es el rendimiento comparativo de diferentes algoritmos de aprendizaje automático en la predicción de consumo de energía eléctrica por tipo de usuario?
Los modelos evaluados mostraron el siguiente rendimiento:

Regresión Lineal fue el mejor, con un R² de 0.987, un MAE más bajo de 1.40%, y un MSE de 509,935,476,251.
Random Forest también mostró un buen rendimiento, pero con un R² más bajo (0.977) y un mayor MAE (753,412).
XGBoost y Gradient Boosting presentaron resultados similares con R² cercanos a 0.97, pero con mayor error absoluto (MAE) comparado con la Regresión Lineal.
KNN tuvo un rendimiento similar al de XGBoost, pero levemente inferior.
SVR fue el peor modelo, con un R² negativo, lo que indica que no fue capaz de capturar la relación entre las variables predictoras y el consumo total.

---