# Breast-cancer
El objetivo del proyecto es **predecir si un tumor es benigno o maligno**, a partir de características morfológicas obtenidas de muestras celulares.

---

## 📊 Dataset

📦 Fuente: [Breast Cancer Wisconsin (Diagnostic) Dataset – UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic))

El dataset contiene información sobre características microscópicas de células tumorales, utilizadas para determinar la naturaleza del tumor.

**Variables principales:**
- `Cl.thickness` – Grosor de las células epiteliales  
- `Cell.size` – Tamaño de las células  
- `Cell.shape` – Forma de las células  
- `Marg.adhesion` – Adhesión marginal  
- `Epith.c.size` – Tamaño de células epiteliales  
- `Bare.nuclei` – Núcleos desnudos  
- `Bland.chromatin` – Cromatina blanda  
- `Normal.nucleoli` – Presencia de nucléolos normales  
- `Mitoses` – Tasa de mitosis  
- `Class` – Variable objetivo (`benign` / `malignant`)

---

## 🧹 Limpieza de datos

- Sin **valores faltantes significativos**  
- Se normalizaron variables numéricas para mejorar el desempeño del modelo  
- Se eliminaron duplicados y se codificó la variable objetivo como binaria (0 = benigno, 1 = maligno)

---

## 🔍 Insights Principales

- Tumores con valores **altos de `Cl.thickness`, `Cell.size`, `Marg.adhesion`, `Epith.c.size`, `Bare.nuclei`, `Bland.chromatin`, `Normal.nucleoli` y `Mitoses`** tienen mayor probabilidad de ser **malignos**.  
- Las variables **`Bare.nuclei`** y **`Cl.thickness`** son las más determinantes según la importancia del modelo.  
- No hay diferencias significativas entre muestras por paciente, lo que sugiere un dataset bien balanceado.
 ![Boxplot](Boxplots.png)

---

## 🤖 Modelado Predictivo

Se probaron distintos modelos de clasificación supervisada.

**Mejor modelo:** `Gradient Boosting`

| Modelo | Accuracy | Precision | Recall | F1 Score |
|---------|-----------|-----------|---------|-----------|
| Gradient Boosting | **0.985** | **1.00** | 0.97 | 0.985 |

Otros modelos evaluados: Logistic Regression, Random Forest, SVM, XGBoost.

---

## 🧰 Tecnologías utilizadas

- **Lenguaje:** Python  
- **Bibliotecas:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `xgboost`  
- **Técnicas:**  
  - Normalización de datos  
  - Feature importance  
  - Validación cruzada  
  - Evaluación de métricas de clasificación (Precision, Recall, F1, ROC AUC)  
  - Visualización de resultados  

---
