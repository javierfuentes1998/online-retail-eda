[README.md](https://github.com/user-attachments/files/25496947/README.md)
Autor: Javier Fuentes Pastor
Máster en Data Science & AI

# Online Retail II — Análisis exploratorio y pipeline reproducible


## Objetivo
Realizar un análisis exploratorio reproducible sobre un dataset real de transacciones de e-commerce, aplicando limpieza de datos, creación de variables y visualizaciones que permitan extraer conclusiones basadas en evidencia.

## Dataset
- Fuente: Online Retail II (UCI Machine Learning Repository)
- Enlace: https://archive.ics.uci.edu/dataset/502/online+retail+ii
- Periodo analizado: 2010–2011
- Formato: CSV convertido desde Excel

Variables principales:
Invoice, StockCode, Description, Quantity, InvoiceDate, Price, Customer ID, Country.

## Preguntas del análisis
1. ¿Cómo evolucionan los ingresos a lo largo del tiempo?
2. ¿Qué países generan más ingresos?
3. ¿Qué productos generan más revenue?
4. ¿Cómo se distribuye el total por factura?

## Limpieza aplicada
- Eliminación de duplicados
- Conversión de fechas a datetime
- Eliminación de cancelaciones (Invoice empieza por C)
- Eliminación de Quantity negativas
- Eliminación de Customer ID nulos

## Features creadas
- `revenue = Quantity * Price`
- `year_month` (mes de la transacción)

## Estructura del proyecto
data/
  raw/
  processed/
notebooks/
  eda.ipynb
src/
  config.py
  data_io.py
  cleaning.py
main.py
requirements.txt
README.md

## Pipeline reproducible
Para ejecutar el pipeline completo:

python main.py

Esto genera:
data/processed/clean_dataset.csv

## Hallazgos principales
- Se observa un crecimiento del revenue durante 2011, con un pico en noviembre.
- El Reino Unido concentra la mayoría de los ingresos.
- Existen productos estrella que concentran gran parte del revenue.
- El total por factura muestra una distribución sesgada con presencia de outliers.

## Conclusión
Este proyecto demuestra la construcción de un pipeline reproducible de análisis de datos, desde la ingestión hasta la generación de insights, siguiendo buenas prácticas de organización de código y limpieza de datos.
