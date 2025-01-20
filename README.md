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

#### **Próximos pasos**
- Refinar los KPIs para análisis más profundo.
- Desarrollar estrategias para reducir el churn en las categorías con mayores tasas.
- Crear un dashboard interactivo para visualizar los resultados de forma dinámica.


