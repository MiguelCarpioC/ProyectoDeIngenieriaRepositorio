# ProyectoDeIngenieriaRepositorio# pythonCRYPTUE - Análisis y Predicción de Criptomonedas

Proyecto de análisis exploratorio y predicción de precios de Bitcoin (BTC) y Ethereum (ETH) utilizando modelos de Machine Learning.

## Estructura del Proyecto

| Archivo | Descripción |
|---|---|
| `analisis_crypto1(NO TOCAR NI CAMBIAR).ipynb` | Análisis exploratorio de datos: evolución de precios, rendimientos diarios, correlación BTC-ETH y visualizaciones con Plotly y Matplotlib |
| `Modelo_predictivo.ipynb` | Modelo LSTM multivariante (TensorFlow/Keras) que usa BTC y ETH conjuntamente para predecir precios con ventana de 60 días |
| `predicciones BITCOIN.ipynb` | Modelo XGBoost para predicción univariante de Bitcoin con horizontes de 1, 5, 10 y 15 días |
| `predicciones etherium.ipynb` | Modelo XGBoost para predicción univariante de Ethereum con horizontes de 1, 5, 10 y 15 días |

## Tecnologías

- **Python** con Jupyter Notebook / Google Colab
- **yfinance** - Descarga de datos históricos de criptomonedas
- **pandas, numpy** - Manipulación de datos
- **matplotlib, plotly, seaborn** - Visualización
- **scikit-learn** - Preprocesamiento (MinMaxScaler) y métricas (MAE, RMSE, R²)
- **TensorFlow/Keras** - Red LSTM multivariante
- **XGBoost** - Modelo de gradient boosting para predicción univariante

## Modelos

### LSTM Multivariante (`Modelo_predictivo.ipynb`)
- Arquitectura: 2 capas LSTM (60 unidades) + Dropout + Dense
- Input: precios de BTC y ETH (ventana de 60 días)
- Output: precio predicho de BTC
- Evaluación con MAE en múltiples horizontes temporales

### XGBoost Univariante (`predicciones BITCOIN.ipynb` y `predicciones etherium.ipynb`)
- Modelo: XGBRegressor con 1000 estimadores
- Ventana temporal: 10 días
- Split train/test: 90/10
- Predicción recursiva para horizontes de 1, 5, 10 y 15 días

## Requisitos

```
yfinance
pandas
numpy
matplotlib
seaborn
plotly
scikit-learn
tensorflow
xgboost
```

## Uso

1. Abrir los notebooks en Google Colab o Jupyter Notebook
2. Ejecutar las celdas en orden
3. Los datos se descargan automáticamente desde Yahoo Finance

> **Nota:** El archivo `analisis_crypto1(NO TOCAR NI CAMBIAR).ipynb` es la base del análisis y no debe modificarse.
