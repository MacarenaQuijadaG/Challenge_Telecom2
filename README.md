# 📡 Telecom X - Parte 2: Predicción de Churn

## 📌 Propósito del proyecto

Este proyecto tiene como objetivo **predecir la cancelación de clientes (churn)** en una compañía de telecomunicaciones. Se parte de datos históricos para analizar y modelar factores clave que influyen en la decisión de los clientes de abandonar el servicio. Los hallazgos permitirán diseñar estrategias de retención más efectivas y modelos predictivos que anticipen la evasión de clientes.

---
## ⚙️ Preparación y tratamiento de datos

### 📑 Clasificación de variables

- **Variables categóricas:** Gender, Partner, Dependents, PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies, Contract, PaperlessBilling, PaymentMethod, Churn.
- **Variables numéricas:** Tenure, MonthlyCharges, TotalCharges, DailyCharges.

### 🔄 Normalización y codificación

- Columnas anidadas (`customer`, `phone`, `account`, `internet`) se desglosaron y se fusionaron en un único DataFrame.
- Se revisaron valores nulos y duplicados: no se encontraron.
- Columnas de texto con números (`Charges.Total`, `Charges.Monthly`) se transformaron a `float`.
- Se generó la variable `DailyCharges` dividiendo `MonthlyCharges` entre 30.
- Variables binarias se mapearon a 1/0.
- Variables categóricas multiclase (`Contract`) se codificaron numéricamente.

### 🔑 Separación de datos

Se dividieron los datos en conjuntos de **entrenamiento (train)** y **prueba (test)** usando técnicas de validación cruzada para evaluar el rendimiento de los modelos de predicción de churn.

### 💡 Justificaciones

- La codificación binaria permite un procesamiento más eficiente en modelos de machine learning.
- Se creó la variable `DailyCharges` para observar patrones de gasto más finos.
- La separación en train/test asegura una evaluación justa del modelo, evitando sobreajuste.

---

## 📊 Análisis exploratorio de datos (EDA)

Durante el EDA se generaron insights clave:

- **Gráfico de torta:** muestra la proporción de clientes que abandonaron vs. los que permanecen.
- **Mapa de calor:** relaciona género, contrato e InternetService, usando escala de colores.
- **Boxplots:** evidencian que quienes abandonan tienden a tener cargos mensuales mayores y menor tiempo de permanencia.

---

## 🚀 Ejecución del proyecto

### 📦 Requisitos

Asegúrate de tener Python instalado con las siguientes bibliotecas:

 ```bash
  pip install pandas numpy seaborn matplotlib scikit-learn
   ```



## ▶️ Cómo ejecutar
Clona el repositorio.

Coloca los archivos de datos en la carpeta data/.

Abre el cuaderno Challenge_Telecom_X2.ipynb en Jupyter Notebook o Google Colab.

Ejecuta las celdas en orden para reproducir el análisis, las transformaciones y los gráficos.

El archivo procesado se guarda como Clientes.json o Clientes.csv según la exportación.

## ✅ Resultado
Este proyecto establece las bases para construir un modelo predictivo robusto de churn. Gracias a la limpieza de datos, la exploración profunda y la correcta preparación, los próximos pasos pueden centrarse en seleccionar y entrenar algoritmos de clasificación adecuados.

Autor: Macarena Quijada G
