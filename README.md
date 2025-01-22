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
- Se realizaron análisis descriptivos y visualizaciones para identificar patrones:
  - **Group/Churn:** Distribución del churn por pertenencia a grupos.
  - **Cluster Age/Churn:** Proporción de churn según rango de edad.
  - **Contract Type/Payment Method/Churn:** Relación entre contratos, métodos de pago y churn.
  - **Customers Calls/Churn:** Impacto del número de llamadas al servicio en el churn.
  - **Number of Complaints/Churn:** Relación entre quejas y churn.
  - **Last Transaction Date/Churn:** Tendencias temporales en el churn.
  - **Churn Category & Reason:** Razones y categorías principales detrás del churn.

#### **Paso 5: Creación de KPIs**
- Se creó una nueva hoja llamada `KPIs` para centralizar los indicadores clave de desempeño:
  1. **Tasa de Churn Total:** `(Clientes con Churn / Total de Clientes) * 100`.
  2. **Churn por Grupo:** `(Clientes con Churn en un Grupo / Total de Clientes en ese Grupo) * 100`.
  3. **Churn por Rango de Edad:** `(Clientes con Churn en un Rango de Edad / Total de Clientes en ese Rango) * 100`.
  4. **Churn por Tipo de Contrato y Método de Pago:** `(Clientes con Churn en un Tipo o Método / Total de Clientes en ese Tipo o Método) * 100`.
  5. **Promedio de Llamadas antes del Churn:** `(Total de Llamadas de Clientes con Churn / Total de Clientes con Churn)`.
  6. **Tasa de Churn por Número de Quejas:** `(Clientes con Churn por Quejas / Total de Clientes por Quejas) * 100`.
  7. **Razones de Churn más comunes:** `(Clientes por Razón / Total de Clientes con Churn)`.
  8. **Tendencia Temporal de Churn:** `(Clientes con Churn en un Mes / Total de Clientes Activos en ese Mes) * 100`.

#### **Paso 6: Creación del Dashboard y Conclusiones**
- Se utilizó el archivo `Datos_dashboard/Dashboard.xlsx` como base para construir un dashboard interactivo en Excel.
- El dashboard incluye las siguientes métricas e insights clave:
  1. **Tasa de Churn Total:** Visualización del porcentaje de clientes que abandonaron la plataforma.
  2. **Razones de Churn:** Gráfico con las principales razones de abandono según los datos.
  3. **Segmentación por Edad:** Proporción de churn en diferentes rangos de edad (Under 30, Senior, Mid Age).
  4. **Análisis de Llamadas y Churn:** Relación entre el número de llamadas al servicio y el churn.
  5. **Métodos de Pago y Contratos:** Comparativa del churn según métodos de pago y tipo de contrato.
  6. **Tendencia Temporal:** Evolución del churn a lo largo del tiempo.
- **Conclusiones del Dashboard:**
  - El dashboard confirma que los contratos de largo plazo (un año o más) tienen tasas de churn significativamente menores.
  - Las llamadas al servicio están relacionadas con un mayor churn, lo que indica posibles problemas en la experiencia del cliente.
  - Los métodos de pago más tradicionales (débito/tarjetas) están asociados con mayores tasas de churn en comparación con pagos automáticos o digitales.

## Estructura del Proyecto
```plaintext
Proyecto_Guiado_Amazon/
├── Data/
│   ├── Data_analysis/ - Archivos con análisis descriptivo categórico y numérico del churn.
│   │   ├── amazon_churn_analysis_descriptivo_cat_temp_churn.xlsx
│   │   ├── análisis_descriptivo_num_churn.xlsx
│   ├── Data_raw/ - Datos en bruto sin procesar.
│   │   ├── amazon_churn_datosbrutos.xlsx
│   │   ├── amazon_churn_datosbrutos_copia.xlsx
│   ├── Datos_dashboard/ - Archivos del dashboard interactivo.
│   │   ├── Dashboard.xlsx
│   ├── Datos_transformados/ - Datos que han pasado por un proceso de limpieza y transformación.
│       ├── amazon_churn_transformacion.xlsx
├── Documentos/ - Resúmenes y notas de cada sesión del proyecto.
│   ├── Recap primera sesión.docx - Introducción al conjunto de datos y limpieza inicial.
│   ├── Recap segunda sesión.docx - Identificación de columnas críticas y preprocesamiento.
│   ├── Recap tercera sesión.docx - Análisis descriptivo inicial de datos categóricos.
│   ├── Recap cuarta sesión.docx - Profundización en datos numéricos y patrones.
│   ├── Recap quinta sesión.docx - Análisis de correlaciones.
│   ├── Recap sexta sesión.docx - Creación de nuevas variables y ajuste de KPIs.
│   ├── Recap séptima sesión.docx - Preparación de datos para el dashboard.
├── Img/ - Imágenes del proyecto.
│   ├── dashboard.png
│   ├── portada.jpg
├── README.md - Documentación principal del proyecto.
```

## Conclusiones
- Tenemos una tasa de abandono del 27%.
- El gasto promedio de las personas que abandonan el servicio es un 6% superior a la media de gasto mensual, mientras que para las personas que siguen en la plataforma es un 2% inferior.
- La principal razón de este abandono es una mejor oferta de la competencia.
- Hemos observado cómo al aumentar el número de llamadas a servicio al cliente aumenta el porcentaje de abandono de la plataforma.
- Los contratos de larga duración (un año/dos años) tienen un efecto beneficioso para nuestra empresa, ya que disminuye drásticamente la tasa de abandonos.
- El abandono está estrechamente relacionado con el método de pago (aumentando en el caso de débito y tarjetas) y con las multicuentas (aumentando en el caso de las cuentas individuales).

---
