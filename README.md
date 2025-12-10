# 📊 Análisis Integral de Rendimiento Comercial: Ventas, Clientes y Marketing

Este proyecto abarca el ciclo completo de un análisis de datos de retail (Ciencia de Datos aplicada), desde la ingesta de datos crudos hasta la generación de insights estratégicos de negocio. Se enfoca en la limpieza modular, validación estadística y visualización de datos para entender el comportamiento de productos y clientes.

**Autora:** Jennifer Franco
**Curso:** Data Analytics con Python - Talento Tech
**Estado:** Entrega Final

---

## 🎯 Objetivo del Proyecto

Transformar datos transaccionales desconectados en un **tablero de control estratégico**. El objetivo no es solo limpiar datos, sino validar hipótesis de negocio mediante estadística robusta (detección de outliers, correlaciones) para identificar productos estrella (`High Performers`) y optimizar la inversión en marketing.

## 📂 1. Conjuntos de Datos (Datasets)

Se procesaron tres fuentes de información:

* **`ventas.csv`**: Registro transaccional (`id_venta`, `producto`, `precio`, `cantidad`, `fecha`).
* **`clientes.csv`**: Perfil demográfico (`id_cliente`, `edad`, `ciudad`, `ingresos`).
* **`marketing.csv`**: Inversión publicitaria (`costo`, `canal`, `campaña`).

## ⚙️ 2. Metodología y Flujo de Trabajo

El análisis se estructura modularmente en el notebook `Entrega_Final_Data_Analilytics_Franco.ipynb`, siguiendo un enfoque de **validación visual continua**:

### 🔹 Etapa 1 y 2: Ingeniería y Calidad de Datos
* **Limpieza Modular:** Implementación de funciones personalizadas (`limpiar_precio`, `limpiar_cantidad`) para eliminar caracteres no numéricos y normalizar tipos de datos.
* **Feature Engineering:** Creación del KPI `ingreso_total` (Precio × Cantidad) para medir el impacto real en facturación.
* **Segmentación Automática:** Aplicación de filtros de **Alto Rendimiento** basados en percentiles (Top 20% / Principio de Pareto) para aislar los productos más relevantes.
* **Validación:** *Gráfico de Barras* (Ranking) para confirmar visualmente los líderes del mercado.

### 🔹 Etapa 3: Análisis Estadístico y Exploratorio (EDA)
* **Análisis Granular vs. Agregado:** Diferenciación entre métricas por *Producto* y por *Categoría* para evitar sesgos de agregación.
* **Detección de Anomalías (Outliers):** Cálculo del **Rango Intercuartílico (IQR)** para identificar matemáticamente productos con ventas excepcionales.
* **Visualización de Distribución:** Uso de *Boxplots* (Diagramas de Caja) para confirmar que los outliers detectados (ej. Lámparas, Auriculares) son casos de éxito y no errores.
* **Correlación de Pearson:** Análisis de la relación Precio vs. Demanda, validado mediante *Scatter Plots* (Gráficos de Dispersión).

## 🧠 3. Síntesis de Resultados

| Concepto Técnico | Aplicación en el Proyecto | Insight de Negocio |
| :--- | :--- | :--- |
| **Limpieza de Datos** | Funciones propias reutilizables | Base sólida para decisiones financieras reales. |
| **Agregación** | Ranking de Categorías | Identificación instantánea de líderes (Tecnología y Decoración). |
| **Estadística (IQR)** | Cálculo de Outliers | Diferenciación entre anomalía matemática y éxito de ventas. |
| **EDA Visual** | Scatter Plot + Boxplot | Confirmación de que el mercado absorbe precios premium sin caer la demanda. |

## 🛠️ 4. Tecnologías Utilizadas

* **Lenguaje:** Python 3.
* **Manipulación de Datos:** Pandas, NumPy.
* **Visualización:** Matplotlib, Seaborn.
* **Entorno:** Google Colab / Jupyter Notebook.

## 🚀 5. Cómo Ejecutar el Proyecto

1.  Clonar este repositorio.
2.  Asegurarse de tener los datasets (`ventas.csv`, `clientes.csv`, `marketing.csv`) en la carpeta `/data` o en tu Google Drive.
3.  Abrir el notebook `Franco.ipynb`.
4.  Ejecutar las celdas secuencialmente. Las visualizaciones se generarán automáticamente en cada etapa del análisis para validar los resultados.

---
*Proyecto realizado como parte de la certificación en Data Analytics - 2025.*
4.  Abrir el notebook (`/notebooks/analisis_ventas.ipynb`) en Google Colab o un entorno Jupyter.
5.  Ejecutar las celdas en orden.
