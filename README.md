# TelcomX_LATAM_DataScienceChallenge2
Este proyecto estudia el comportamiento de clientes de Telcom X para predecir su abandono. A partir de un proceso de extracción, transformación y análisis exploratorio de datos, se identifican los factores clave que influyen en su decisión de dejar la compañía.

## 📝 Descripción del proyecto

Este proyecto de ciencia de datos se centra en analizar el comportamiento de los clientes de una empresa de telecomunicaciones para comprender y predecir el abandono (churn). A través de un exhaustivo proceso de extracción, transformación y análisis exploratorio de datos (EDA), se busca identificar los factores más influyentes en la decisión de un cliente de dejar la empresa.

## 📊 Fuente de datos

Los datos utilizados para este análisis provienen de un archivo JSON que contiene información detallada sobre los clientes de TelecomX.

* **URL del dataset:** `https://raw.githubusercontent.com/ingridcristh/challenge2-data-science-LATAM/refs/heads/main/TelecomX_Data.json`

## 🛠️ Metodología y procesamiento de datos

El proceso de preparación y manipulación de datos se realizó siguiendo los siguientes pasos clave:

1.  **Normalización y estructuración de los datos:** Los datos anidados en formato JSON fueron normalizados y transformados en una estructura tabular plana para facilitar su visualización y análisis.
2.  **Manipulación de valores faltantes e inconsistencias:** Se identificaron y eliminaron filas con valores en blanco o inconsistentes en columnas clave como 'CargosTotales' y 'AbandonoEmpresa'.
3.  **Conversión de tipos de datos:** Las columnas numéricas se convirtieron al tipo de dato apropiado (float), y las variables categóricas 'Yes'/'No' se transformaron a formato binario (1/0).
4.  **Generación de nueva columna:** Se creó una nueva columna, 'Cuentas_Diarias', para un análisis posterior más detallado de los costos, calculada como 'CargosMensuales' / 30.
5.  **Estandarización y traducción:** Las columnas y sus valores absolutos fueron renombrados y traducidos del inglés al español para mayor claridad y consistencia en el análisis.

## 🔍 Análisis exploratorio de datos (EDA) y hallazgos clave

Se realizaron diversos análisis para identificar patrones e *insights* clave relacionados con el abandono de clientes. Los hallazgos más relevantes son:

* **Tasa general de abandono:** La empresa presenta una tasa de abandono del 26.5%.
* **Abandono por tipo de contrato:** Los clientes con contratos mensuales ("Month-to-month" / "Mensual") muestran una tasa de abandono significativamente más alta en comparación con aquellos que tienen contratos anuales o de dos años.
* **Pagos y antigüedad:** Un bajo valor en la interacción (CargosMensuales_por_MesesAntiguedad) que puede estar determinado por un corto tiempo de contrato o altos costos mensuales o bien una combinación de ambos, está relacionado a una alta tasa de abandono de empresa. Por lo tanto, tanto nuevos clientes como aquellos con un corto tiempo de contrato representan un perfil de alto riesgo en evasión.
* **Servicio de internet y método de pago:** Aquellos que utilizan fibra óptica y el pago con cheque electrónico están asociados con alta evasión.
* **Demografía y servicios complementarios:** Clientes de la tercera edad, solteros sin dependientes, y aquellos sin servicios adicionales de internet, tienen más probabilidades de cancelar.
* **Facturación:** Los clientes que reciben la factura de en formato electrónico se asocia a una mayor tasa de churn.
  
## ⚙️ Dependencias

Para ejecutar este proyecto, necesitarás las siguientes librerías de Python:

* `requests`
* `pandas`
* `plotly.express`

## 🚀 Cómo ejecutar el proyecto

El proyecto está diseñado como un *notebook* de Colab, lo que facilita su ejecución en el entorno de Google Colaboratory.

1.  Abre el archivo `TelcomX_LATAM_DataScienceChallenge2
.ipynb` en Google Colab (si el archivo actual es un PDF, deberás convertirlo o subirlo como un archivo `.ipynb`).
2.  Asegúrate de tener instaladas todas las dependencias mencionadas.
3.  Ejecuta las celdas del *notebook* secuencialmente para replicar el análisis de datos.

## ❗ Posibles problemas y soluciones

* **Problemas de conexión a la fuente de datos:** Si la URL del dataset cambia o no está disponible, asegúrate de actualizar la URL en el código. O bien descargar el dataset en formato JSON para asegurarse de tenerlo en forma offline.
* **Errores de librerías:** Si encuentras errores relacionados con librerías, verifica que todas las dependencias estén instaladas correctamente en tu entorno de Colab.

