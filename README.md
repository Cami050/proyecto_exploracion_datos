# ANÁLISIS DE DATOS: DELITOS INFORMÁTICOS EN COLOMBIA

**Integrantes:** Camila Rivera, Andrés Padilla, Alejandro Soa, Nick Duran

---

## Introducción al Proyecto

Este proyecto tiene como objetivo principal realizar un **análisis exploratorio y visualización de datos** sobre incidentes de delitos informáticos en Colombia, basándose en el documento `DELITOS_INFORMÁTICOS_20251208.csv`. Nuestro propósito es transformar datos crudos en información clave que permita identificar **tendencias**, **patrones geográficos** y la **distribución** de los tipos de conducta delictiva a lo largo del tiempo.

El proyecto está estructurado en torno a la generación de **seis visualizaciones estadísticas fundamentales** que serán desarrolladas por el equipo de cuatro compañeros, asegurando una cobertura exhaustiva del *dataset*.

---

## Tecnologías y Herramientas

Para garantizar la eficiencia y reproducibilidad del análisis, utilizaremos un entorno de **Google Colab**, lo que permite la ejecución de código **Python** basado en la nube. Las principales librerías que se emplearán para el procesamiento, manipulación y visualización de los datos son:

| Tecnología | Propósito Principal |
| :--- | :--- |
| **Python** | Lenguaje de programación base. |
| **Pandas** | Manipulación y limpieza de *DataFrames* (estructura del archivo CSV). |
| **Matplotlib / Seaborn** | Generación de gráficos de Barras, Líneas, Pastel y Dispersión. |
| **Plotly / GeoPandas** | Creación del **Mapa Coroplético** geográfico interactivo (visualización por Departamento/Municipio). |

---

## Estructura del Documento y Metodología de Bitácora

Este *notebook* está organizado por secciones de código y texto que siguen la estructura de una **bitácora de proyecto**. Esto nos permite documentar cada paso, desde la carga de datos hasta las conclusiones. Cada compañero registrará el progreso de sus tareas asignadas, incluyendo los desafíos, las soluciones y los hallazgos en las celdas de texto correspondientes.

La bitácora facilitará la trazabilidad de las siguientes **tareas clave**:

1.  Carga y Exploración Inicial de Datos.
2.  Limpieza y Transformación de Datos.
3.  Generación de las **6 Gráficas Asignadas**.
4.  Conclusiones y Resumen de Hallazgos.

### Asignación de Gráficas y Responsables

| Compañero | Gráficas Asignadas | Tarea Específica | Variables Clave (Sugeridas) |
| :--- | :--- | :--- | :--- |
| **Andrés Padilla** | 1. Gráfico de Barras | Conteo de casos por **Tipo de Delito** (`DESCRIPCION CONDUCTA`). | `DESCRIPCION CONDUCTA` y `CANTIDAD` |
| **Camila Rivera** | 2. Gráfico de Líneas | Análisis de **Serie de Tiempo**: Total de casos por **Año** (extrayendo del campo `FECHA HECHO`). | `FECHA HECHO` y `CANTIDAD` |
| **Alejandro Soa** | 3. Gráfico de Pastel | Distribución de casos en los **Top 5 Departamentos** (`DEPARTAMENTO`). | `DEPARTAMENTO` y `CANTIDAD` |
| **Nick Duran** | 4. Gráfico de Barras Apiladas | Conteo de casos por **Departamento** y **Tipo de Delito** más común. | `DEPARTAMENTO`, `DESCRIPCION CONDUCTA`, `CANTIDAD` |
| **Andrés Padilla** | 5. Mapa Coroplético | Visualización de la **Concentración Geográfica** de delitos por **Departamento** o **Municipio**. | `DEPARTAMENTO` / `MUNICIPIO` y `CANTIDAD` |
| **Camila Rivera** | 6. Gráfico de Dispersión | Exploración de la **Dispersión/Burbujas**: Relación entre la `Cantidad de Delitos` y el `Tiempo transcurrido`. | Depende del análisis exploratorio; quizás un conteo por municipio para el tamaño de la burbuja. |

---

## Datos del Documento y Preparación

### Variables Clave del Dataset

El archivo CSV contiene un registro detallado de los incidentes de delitos informáticos, con las siguientes columnas principales:

| Columna | Descripción | Tipo de Dato (Esperado) |
| :--- | :--- | :--- |
| `FECHA HECHO` | Fecha completa en que ocurrió el incidente. | Cadena de texto / Fecha |
| `COD_DEPTO` | Código del departamento. | Categórico |
| `DEPARTAMENTO` | Ubicación geográfica del incidente. | Categórico |
| `COD_MUNI` | Código del municipio. | Categórico |
| `MUNICIPIO` | Ubicación geográfica detallada del incidente. | Categórico |
| `DESCRIPCION CONDUCTA` | Tipo específico de delito informático (ej. Hurto, Acceso Abusivo). | Categórico |
| `CANTIDAD` | Número de casos reportados. | Numérico (Entero) |

### Proceso de Limpieza y Transformación de Datos

La calidad de la visualización depende directamente de la limpieza de los datos. El paso inicial se centrará en los siguientes aspectos críticos:

1.  **Limpieza de la Columna `FECHA HECHO`:**
    * La columna será convertida del formato de cadena de texto (ej., `"2006 May 13 12:00:00 AM"`) a un formato de **fecha/hora (`datetime`)** estándar de Python.
    * Se extraerán dos nuevas columnas: **`AÑO`** y **`MES_AÑO`**. Estas son cruciales para generar el **Gráfico de Líneas (Serie de Tiempo)** y el análisis de la tendencia temporal.

2.  **Estandarización Geográfica y Numérica:**
    * Se verificará la consistencia en la escritura de los nombres de **`DEPARTAMENTO`** y **`MUNICIPIO`** para evitar errores al agrupar los datos y al generar el Mapa Coroplético.
    * Se asegurará que la columna **`CANTIDAD`** sea tratada como un valor **numérico entero** para permitir sumas y conteos precisos.
