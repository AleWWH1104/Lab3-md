# Lab 3 – Modelos de Regresión para House Prices

Este repositorio contiene el cuaderno `avances.ipynb`, donde se desarrolla el flujo completo para la competencia **House Prices: Advanced Regression Techniques** de Kaggle.

## Estructura

- `avances.ipynb`: notebook con el análisis exploratorio, preprocesamiento y modelos (OLS, Ridge, Lasso).
- `data/`: carpeta con los archivos `train.csv`, `test.csv`, `sample_submission.csv` y la descripción de variables.
- `requirements.txt`: dependencias mínimas para reproducir el notebook.

## Requisitos

```bash
python -m venv .venv
.\.venv\Scripts\activate
pip install -r requirements.txt
```

## Uso

1. Coloca los archivos del dataset de Kaggle dentro de `data/` (ya incluidos en este repo).
2. Abre VS Code o Jupyter Lab y ejecuta el notebook `avances.ipynb` paso a paso.
3. El flujo incluye:
   - Análisis exploratorio y correlaciones.
   - Limpieza e imputación de valores nulos.
   - Selección de variables y escalamiento.
   - Entrenamiento y comparación de modelos OLS/Ridge/Lasso.
   - Diagnóstico de residuos y métricas (R², MAE, MSE, RMSE, etc.).

## Notas

- Se utiliza `SalePrice_log = log1p(SalePrice)` para estabilizar la varianza; recuerda transformar de regreso con `expm1` para interpretar errores en dólares.
- Ajusta hiperparámetros (`alpha` en Ridge/Lasso) según los resultados de validación que obtengas.
- El notebook fija `random_state=42` para garantizar reproducibilidad.
