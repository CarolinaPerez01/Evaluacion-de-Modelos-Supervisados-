# 🧠 **Evaluación de Modelos Supervisados**

Este proyecto muestra cómo evaluar y comparar distintos modelos de **aprendizaje supervisado** utilizando Python y `scikit-learn`. El objetivo es predecir si un cliente representa un riesgo crediticio alto o bajo, basándose en sus características financieras y demográficas.

## 📁 **Contenido**

- `Evaluating supervised models.ipynb`: Notebook principal con todo el análisis.
- `credit_customers.csv`: Conjunto de datos utilizado (no incluido, asegúrate de tenerlo en el mismo directorio).

## 📊 **Dataset**

El conjunto de datos contiene información sobre clientes de crédito, con variables como:

- Estado de cuenta corriente y de ahorros
- Historial crediticio
- Monto del crédito
- Edad, tipo de empleo, vivienda, entre otros
- `class`: variable objetivo, que indica si el cliente es de buen o mal riesgo

## 🛠️ Metodología

1. **Análisis exploratorio de datos (EDA)**: Entendimiento de la estructura y distribución de las variables.
2. **Preprocesamiento**:
   - Codificación de variables categóricas (`OneHotEncoder`)
   - Escalado de variables numéricas (`StandardScaler`)
   - División en conjunto de entrenamiento y prueba
3. **Modelado**: Se entrenaron y compararon los siguientes modelos:
   - Regresión logística
   - Árbol de decisión
   - Random Forest
   - K-Nearest Neighbors (KNN)
4. **Evaluación**:
   - Accuracy
   - Matriz de confusión
   - Reporte de clasificación
   - Curva ROC y AUC

## 📈 Resultados
Cada modelo fue evaluado en términos de precisión y desempeño general. La combinación de métricas permitió identificar qué algoritmos son más efectivos para esta tarea y bajo qué condiciones.

| Modelo               | Accuracy (Train/Test) | F1-Score (Test) | CV Accuracy |
|----------------------|-----------------------|-----------------|-------------|
| KNN                  | 0.804 / 0.736         | 0.718           | 0.711       |
| Regresión Logística  | 0.780 / 0.772         | 0.763           | 0.733       |
| Árbol de Decisión    | 0.751 / 0.720         | 0.719           | 0.667       |