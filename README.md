# Proyecto de Análisis de Ventas, Clientes y Marketing

Este proyecto es una pre-entrega de análisis de datos que cubre el proceso completo de ingesta, limpieza, procesamiento y análisis (ETL y EDA) de tres fuentes de datos de una empresa: Ventas, Clientes y Marketing.

**Autora:** Jennifer Franco

**Curso:** Data Analytics con Python - Talento Tech

---

## Objetivo del Proyecto

El objetivo principal es limpiar y preparar los datos crudos para el análisis, con el fin de extraer insights accionables sobre el rendimiento de los productos, la composición de los clientes y la efectividad de las campañas de marketing.

## 1. Conjuntos de Datos (Datasets)

Se utilizan tres archivos CSV como fuentes de datos:

* **`ventas.csv`**: Contiene el registro transaccional de las ventas, incluyendo `id_venta`, `producto`, `precio`, `cantidad` y `fecha_venta`.
* **`clientes.csv`**: Contiene información demográfica de los clientes, como `id_cliente`, `nombre`, `edad`, `ciudad` e `ingresos`.
* **`marketing.csv`**: Contiene datos sobre las campañas de marketing, detallando `id_campanha`, `producto`, `canal`, `costo` y fechas de la campaña.

## 2. Metodología y Pasos del Análisis

El análisis se estructura en el notebook `preentrega-data-analytics.ipynb` y sigue los siguientes pasos:
 
### 1. Configuración y Carga
* Importación de librerías (Pandas, Numpy).
* Montaje de Google Drive y carga de los tres archivos CSV.

### 2. Análisis Exploratorio de Datos (EDA)
* Revisión inicial de la estructura (`.shape`, `.info()`, `.head()`).
* Identificación de tipos de datos incorrectos.
* Análisis de valores nulos (`.isna().sum()`).
* Detección de duplicados (filas exactas y por clave primaria).

### 3. Limpieza y Preprocesamiento
* **Eliminación de duplicados** en el set de ventas.
* **Normalización de texto**: Limpieza de espacios extra, caracteres invisibles y estandarización a formato Título.
* **Corrección de Tipos de Datos**:
    * Conversión de columnas de fecha (`fecha_venta`, `fecha_inicio`, `fecha_fin`) a formato `datetime`.
    * Conversión de columnas numéricas (`precio`, `cantidad`) a formato numérico, eliminando símbolos (`$`) y gestionando nulos.
* **Manejo de Nulos**: Eliminación de filas en `ventas` donde `precio` o `cantidad` eran nulos, ya que son inutilizables para el análisis de ingresos.

### 4. Transformación y Análisis
* **Ingeniería de Características**: Creación de la columna `ingreso_total` (`precio` * `cantidad`).
* **Análisis de Productos**: Identificación de productos de alto rendimiento (aquellos por encima del percentil 80 de ingresos).
* **Análisis de Categorías**: Agregación de ingresos, ventas promedio y conteo de transacciones por categoría.
* **Análisis de Marketing (ROI)**: Integración de los datos de `ventas` y `marketing` para calcular la ganancia neta por producto (Ingresos Totales - Costo de Marketing).

## 3. Tecnologías Utilizadas

* **Lenguaje**: Python 3
* **Librerías**: Pandas, Numpy
* **Entorno**: Google Colab / Jupyter Notebook

## 4. Cómo Ejecutar el Proyecto

1.  Clonar este repositorio.
2.  Asegurarse de tener los datasets (`ventas.csv`, `clientes.csv`, `marketing.csv`) en la ruta especificada en el notebook (ej. `/content/drive/MyDrive/datasets/`).
3.  Abrir el notebook (`/notebooks/preentrega-data-analytics.ipynb`) en Google Colab o un entorno Jupyter.
4.  Ejecutar las celdas en orden.
3.  Asegurarse de tener los datasets (`ventas.csv`, `clientes.csv`, `marketing.csv`) en la ruta especificada en el notebook (ej. `/content/drive/MyDrive/datasets/`).
4.  Abrir el notebook (`/notebooks/analisis_ventas.ipynb`) en Google Colab o un entorno Jupyter.
5.  Ejecutar las celdas en orden.
