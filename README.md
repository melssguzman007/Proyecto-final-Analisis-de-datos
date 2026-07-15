# 📊 Análisis de Rendimiento Comercial e Integración de Campañas de Marketing

## 📝 Descripción del Proyecto
Este proyecto consiste en el desarrollo de un pipeline de datos de extremo a extremo (ETL y EDA) utilizando **Python** y **Pandas**. El objetivo principal es consolidar información dispersa proveniente de tres fuentes de datos distintas (Ventas, Clientes y Marketing) para evaluar la performance comercial de un catálogo de productos, identificar patrones de consumo y auditar el Retorno de la Inversión (ROI) de las campañas publicitarias durante el período de Enero 2025.

---

## 🛠️ Tecnologías y Herramientas Utilizadas
*   **Lenguaje:** Python 3
*   **Procesamiento y Transformación de Datos:** Pandas, OS
*   **Visualización de Datos Estática:** Matplotlib, Seaborn
*   **Visualización de Datos Interactiva:** Plotly Express
*   **Entorno de Desarrollo:** Jupyter Notebook / Google Colab

---

## 🚀 Estructura del Pipeline (Etapas del Proyecto)

### 🔹 Etapa 1: Recopilación y Preparación de Datos
*   Carga automatizada e inteligente de datasets en formato `.csv` (`ventas.csv`, `clientes.csv`, `marketing.csv`) mediante búsquedas semánticas en directorios.
*   Primer diagnóstico estructural de las dimensiones (filas y columnas), tipos de datos iniciales e identificación de anomalías tipográficas.

### 🔹 Etapa 2: Preprocesamiento, Limpieza y Transformación
*   Estandarización de tipos de datos (*casting* de precios a flotantes y cantidades a enteros).
*   Tratamiento de valores nulos y remoción de registros corruptos/sesgados financieros mediante `.dropna()`.
*   **Ingeniería de Características (Feature Engineering):** Creación de la métrica calculada `total_ventas` ($Precio \times Cantidad$).
*   Segmentación avanzada para aislar transacciones de "Alto Rendimiento" (monto $\ge$ \$50.00).
*   **Integración de Datos:** Fusión relacional (*inner merge*) utilizando el identificador del producto como clave común entre ventas y marketing.

### 🔹 Etapa 3: Análisis Exploratorio de Datos (EDA)
*   **Estadística Descriptiva:** Obtención de métricas de tendencia central (media, mediana) y dispersión (desviación estándar).
*   **Análisis de Correlación:** Cálculo numérico del coeficiente de correlación de Pearson entre las variables *Precio* y *Cantidad*.
*   Mapeo de la participación porcentual de ingresos agrupados por categorías clave del negocio.

### 🔹 Etapa 4: Visualización Avanzada y Consolidación
*   Generación de gráficos combinados (Boxplots + Stripplots) para evaluar la dispersión de la facturación.
*   Diseño de un gráfico de torta interactivo (*Donut Chart*) con Plotly para representar la cuota de mercado interna por categorías.
*   Cálculo del **ROI Porcentual** final por producto/canal.

---

## 📈 Principales Hallazgos e Insights
1.  **Líderes de Facturación:** Las categorías de **Ropa** (\$186.00) y **Electrónica** (\$180.00) se consolidan como los pilares comerciales de la empresa.
2.  **Elasticidad de Precio-Demanda:** Se detectó un coeficiente de correlación de Pearson de **-0.94**, demostrando una correlación negativa casi perfecta: a menor precio unitario, el volumen de unidades vendidas por transacción se incrementa drásticamente.
3.  **Auditoría de Marketing (Alerta de ROI):** Aunque los canales digitales (Redes Sociales y Email Marketing) muestran una excelente tracción de volumen, los costos de adquisición históricos en canales tradicionales (como los \$3000.00 invertidos en TV para el Producto C) resultan desproporcionados frente a la conversión real de ingresos de este período, sugiriendo una inmediata redistribución del presupuesto publicitario.

---

## 💻 Cómo Ejecutar el Proyecto
1. Clona este repositorio:
   ```bash
   git clone [https://github.com/TU_USUARIO/TU_REPOSITORIO.git](https://github.com/TU_USUARIO/TU_REPOSITORIO.git)
