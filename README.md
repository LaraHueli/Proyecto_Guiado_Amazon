## Proyecto Guiado Amazon

Este proyecto está elaborado en clase y guiado por los profesores.

### Descripción
El objetivo es analizar datos relacionados con la tasa de abandono de clientes de Amazon.

### Datos
- **Archivo:** `amazon_churn_datosbrutos.xlsx`
- **Ubicación:** Carpeta `Data`

### Pasos realizados en el análisis de datos:

#### **Paso 1: Eliminación de duplicados**
- Se eliminaron filas duplicadas usando herramientas de formato condicional.
- Se verificaron los valores únicos en `Customer ID` para evitar duplicados.

#### **Paso 2: Exploración y limpieza preliminar**
- Se analizaron columnas clave:
  - **`Churn Label` y `Churned`:** Ambas tienen la misma información; se eliminó `Churned`.
  - **`Unlimited Data Plan` y otras binarias:** Se transformaron los valores de `0` y `1` a `Yes` y `No`.
  - Se identificaron celdas vacías y diferentes formatos en columnas críticas como `Payment Method` y `Total Charges`.
  - Se analizaron datos internos (`Internal Notes`) para decidir si eran relevantes.

#### **Paso 3: Establecimiento de tipos de datos y formatos**
- Se asignaron tipos de datos apropiados a cada columna:
  - **`Monthly Charge` y `Total Charges`:** Números decimales.
  - **`Contact Date` y `Last Transaction Date`:** Formato de fecha.
  - **`Customer Segment`:** Categorías.
- Se ajustaron formatos en columnas con datos inconsistentes.
- Se revisaron columnas booleanas (`Yes/No`) para garantizar coherencia.

#### **Paso 4: Análisis descriptivo**
- Se comenzó con un análisis descriptivo para entender la distribución de las variables principales:
  - **Análisis de estadísticas descriptivas:** Media, mediana, moda, desviación estándar y rangos.
  - **Exploración de distribuciones:** Histograma de `Monthly Charges` y `Total Charges`.
  - **Análisis de correlaciones:** Identificación de posibles relaciones entre variables numéricas.
  - **Segmentación inicial:** Agrupación de clientes según características como `Customer Segment` y `Churn Label`.
