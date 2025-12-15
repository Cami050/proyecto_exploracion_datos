# Proyecto Final -- Análisis de Datos: Delitos Informáticos en Colombia

## Bitácora, Plan de Trabajo y Estructura del Proyecto

## 1. Introducción del Proyecto

Este proyecto tiene como objetivo analizar los delitos informáticos en
Colombia utilizando el dataset oficial disponible en Datos Abiertos:
"DELITOS INFORMÁTICOS" (https://www.datos.gov.co/Seguridad-y-Defensa/DELITOS-INFORM-TICOS/4v6r-wu98/about_data).
Se aplicará la metodología **ASUM‑DM**, desarrollando todas sus fases:
- Comprensión del negocio
- Comprensión de los datos
- Preparación de los datos
- Modelado
- Evaluación
- Despliegue / Comunicación de resultados

El equipo está conformado por:
- **Camila Rivera**
- **Andrés Padilla**
- **Alejandro Soa**
- **Nick Durán**

------------------------------------------------------------------------

# 2. Stack Tecnológico

  Herramienta                Uso
  -------------------------- -------------------------------------------
  **Google Drive**           Almacenamiento del dataset y recursos
  **Google Colab**           Notebook principal del análisis
  **Python**                 Lenguaje principal para análisis
  **Pandas**                 Limpieza y manipulación de datos
  **Matplotlib / Seaborn**   Visualizaciones estadísticas
  **Plotly / GeoPandas**     Mapa coroplético
  **GitHub**                 Control de versiones, repositorio público
  **PDF + Presentación**     Entregables finales

------------------------------------------------------------------------

# 3. Fases ASUM‑DM Documentadas

## 3.1 Comprensión del Negocio

El objetivo es comprender cómo evolucionan los delitos informáticos, su
Distribución por regiones y cómo cambian en el tiempo.

| Compañero | Gráfica Asignada | Pregunta de las graficas |
| :--- | :--- | :--- |
| Andrés Padilla | Gráfico de Barras | ¿Qué tipos de delitos informáticos se presentan con mayor frecuencia según la descripción de la conducta registrada? |
| Camila Rivera | Gráfico de Líneas | ¿Cómo ha evolucionado el número total de delitos informáticos a lo largo de los años según la fecha del hecho? |
| Alejandro Soa | Gráfico de Pastel | ¿Cómo se distribuyen los casos de delitos informáticos entre los cinco departamentos con mayor número de registros? |
| Nick Duran | Gráfico de Barras Apiladas | ¿Cómo varía el tipo de delito informático más común entre los diferentes departamentos del país? |
| Andrés Padilla | Mapa Coroplético | ¿En qué departamentos o municipios se concentra geográficamente la mayor cantidad de delitos informáticos? |
| Camila Rivera | Gráfico de Dispersión | ¿Existe alguna relación entre la cantidad de delitos informáticos registrados y el tiempo transcurrido entre los hechos? |



------------------------------------------------------------------------

## 3.2 Comprensión de los Datos

El dataset contiene: 
- **FECHA HECHO**
- **DEPARTAMENTO / MUNICIPIO**
- **DESCRIPCION CONDUCTA**
- **CANTIDAD**

Actividades: 
- Verificar valores faltantes
- Identificar inconsistencias en nombres de municipios/departamentos
- Revisar formatos de fechas
- Realizar primeras estadísticas descriptivas
- Identificar anomalías y patrones

------------------------------------------------------------------------

## 3.3 Preparación de los Datos

Incluye: 
- Conversión de fechas a formato datetime
- Generación de columnas derivadas: **AÑO**, **MES**, **MES_AÑO**
- Limpieza de texto en campos categóricos
- Agrupaciones y sumatorias por variables clave
- Validación de tipos de datos
- Eliminación de filas duplicadas

------------------------------------------------------------------------

## 3.4 Modelado (En este proyecto: Analítica y visualización)

Cada integrante desarrolla una visualización estadística:

  ------------------------------------------------------------------------
  Integrante                Gráfica            Descripción
  ------------------------- ------------------ ---------------------------
  **Andrés Padilla**        Barras             Cantidad total por tipo de
                                               delito

  **Camila Rivera**         Línea              Serie de tiempo: delitos
                                               por año

  **Alejandro Soa**         Pastel             Distribución por top 5
                                               departamentos

  **Nick Durán**            Barras apiladas    Delitos por departamento +
                                               tipo

  **Andrés Padilla**        Mapa               Concentración geográfica
                                               por región

  **Camila Rivera**         Dispersión         Relación cantidad vs tiempo
                                               o matriz
  ------------------------------------------------------------------------

------------------------------------------------------------------------

## 3.5 Evaluación

Incluye: - Validación visual de gráficos
- Interpretación estadística
- Consistencia entre resultados y preguntas del negocio
- Cruce entre variables para detectar correlaciones útiles

------------------------------------------------------------------------

## 3.6 Despliegue / Comunicación

Entregables obligatorios: 
- Informe PDF documentado (ASUM‑DM completo).
- Notebook en Google Colab
- Repositorio GitHub con código, datos y documentación
- Presentación tipo elevator pitch

Entregable opcional: - Dashboard interactivo (Power BI o equivalente)

------------------------------------------------------------------------

# Plan de Trabajo del Proyecto Integrado de Análisis, Modelado y Optimización de Datos

## Enfoque por Entregables, Roles y Mecanismos de Control de Calidad

Este documento presenta un plan de trabajo formal, estructurado y orientado a entregables para el desarrollo del proyecto según la metodología **ASUM-DM**. El propósito es garantizar una ejecución organizada, coherente y verificable, donde cada miembro del equipo cuente con responsabilidades claramente definidas y espacios de revisión que aseguren avances alineados.

---

## 1. Selección y Justificación del Dataset

### Objetivo

Identificar, evaluar y seleccionar un conjunto de datos pertinente para el enfoque analítico del proyecto, asegurando relevancia social, viabilidad técnica y potencial de modelado.

### Responsables

* **Trabajo colectivo del equipo**.

### Entregables

* Dataset seleccionado desde *datos.gov.co* u otra fuente oficial.
* Planteamiento formal del problema a resolver.
* Justificación analítica y contextual del dataset.
* Definición del objetivo general y objetivos específicos.

### Revisión de Control

* Sesión de análisis conjunto para validar pertinencia, tamaño del dataset, granularidad y capacidad para soportar un modelo.

---

## 2. Exploración de Datos (EDA) y Conclusiones Iniciales

### Objetivo

Examinar las características internas del dataset para identificar su estructura, calidad, patrones, anomalías y oportunidades analíticas.

### Responsables

* **Nick:** Revisión de calidad de datos (nulos, duplicados) y estructura.
* **Soa:** Estadística descriptiva, análisis univariado y detección de outliers.
* **Andrés:** Visualizaciones interpretativas (tendencias, correlaciones, distribuciones).
* **Camila:** Integración de hallazgos y redacción de conclusiones generales del EDA.

### Entregables

* Sección EDA del notebook, documentada y reproducible.
* Conjunto de visualizaciones fundamentales.
* Más de cinco conclusiones analíticas clave, basadas en evidencia.

### Revisión de Control

* Validación técnica del equipo para asegurar coherencia entre visualizaciones, estadísticas y conclusiones.

---

## 3. Preparación, Transformación e Ingeniería de Datos

### Objetivo

Optimizar los datos para el modelado mediante técnicas de limpieza, transformación y enriquecimiento, con justificación analítica de cada decisión.

### Responsables

* **Nick:** Imputación de valores faltantes.
* **Soa:** Codificación de variables categóricas.
* **Andrés:** Normalización, escalamiento y creación de nuevas variables según necesidad.
* **Camila:** Documentación formal y explicación de cada transformación.

### Entregables

* Pipeline completo de preparación en el notebook.
* Sección del informe describiendo metodologías empleadas, motivaciones, efectos esperados y riesgos.

### Revisión de Control

* Revisión técnica conjunta sobre la coherencia del pipeline y su impacto en el futuro modelado.

---

## 4. Modelado Inicial

### Objetivo

Construir una primera versión del modelo seleccionado para establecer un punto de referencia (baseline) en rendimiento y comportamiento.

### Responsables

* **Andrés:** Selección del tipo de modelo según el objetivo (clasificación, regresión o clustering).
* **Nick:** Entrenamiento del modelo base, ejecución de pruebas y extracción de métricas.
* **Soa:** Análisis crítico de errores, métricas y limitaciones detectadas.
* **Camila:** Redacción de la sección del informe correspondiente a esta etapa.

### Entregables

* Modelo base funcional.
* Métricas iniciales (accuracy, F1-score, RMSE, etc., según corresponda).
* Tabla o apartado con observaciones técnicas.

### Revisión de Control

* Revisión rápida para acordar las direcciones de mejora del modelo.

---

## 5. Optimización del Modelo

### Objetivo

Mejorar el desempeño del modelo base mediante ajustes justificados y técnicamente sustentados.

### Responsables

* **Andrés:** Definición de estrategias de optimización e hiperparámetros a ajustar.
* **Nick:** Implementación técnica de la optimización (GridSearch, RandomSearch, regularizaciones, entre otros).
* **Soa:** Comparación entre modelo base y optimizado, análisis cuantitativo y cualitativo.
* **Camila:** Redacción de la justificación formal del proceso.

### Entregables

* Modelo optimizado.
* Tabla comparativa con métricas antes/después.
* Explicación fundamentada del porqué de las mejoras.

### Revisión de Control

* Revisión del equipo verificando que la optimización esté sustentada y aporte valor real.

---

## 6. Informe Técnico Final (PDF)

### Objetivo

Compilar un documento formal, claro y profesional que refleje todas las fases del proyecto bajo la metodología ASUM-DM.

### Responsables

* **Camila (coordinación):** Ensamble y redacción final del documento.
* **Nick:** Sección de preparación y calidad del dato.
* **Soa:** Sección EDA y visualizaciones.
* **Andrés:** Secciones de modelado y optimización.

### Entregables

* Informe PDF con estructura formal, narrativa coherente y conclusiones sólidas.
* Recomendaciones finales basadas en los hallazgos.

### Revisión de Control

* Lectura grupal final y ajustes de estilo, coherencia y formato.

---

## 7. Notebook Final

### Objetivo

Presentar un cuaderno completamente funcional, limpio y replicable que documente el flujo analítico de principio a fin.

### Responsables

* **Trabajo conjunto del equipo.**

### Entregables

* Notebook ordenado por secciones.
* Celdas limpias, sin errores y con explicaciones claras.

### Revisión de Control

* Ejecución completa del notebook desde cero para validar reproducibilidad.

---

## 8. Presentación Final (Elevator Pitch)

### Objetivo

Comunicar de manera breve, impactante y profesional el valor del proyecto, las decisiones técnicas y los resultados obtenidos.

### Responsables

* **Camila:** Guion del pitch.
* **Nick:** Diseño y estructura de diapositivas.
* **Soa:** Elementos visuales y narrativa gráfica.
* **Andrés:** Presentación de resultados y valor del modelo.

### Entregables

* Presentación de máximo 6 diapositivas.
* Exposición clara, concisa y profesional.

### Revisión de Control

* Ensayo final del equipo para garantizar coherencia y fluidez.

---

## 9. (Opcional) Dashboard Analítico para Recuperación de Nota

### Objetivo

Complementar el proyecto con una visualización interactiva que fortalezca la comunicación de resultados.

### Responsables

* **Camila** o el integrante interesado en recuperar nota.

### Entregables

* Dashboard funcional (Power BI u otra herramienta equivalente).
* Integración coherente con el informe final.

### Revisión de Control

* Validación del diseño, funcionalidad e interpretación.

------------------------------------------------------------------------

# 5. Bitácora del Equipo

Cada integrante documentará diariamente: - Actividad realizada.
- Código implementado.
- Hallazgos relevantes.
- Problemas encontrados y soluciones.
- Capturas de gráficas y explicaciones.

------------------------------------------------------------------------

# 6. Conclusiones Esperadas

-   El hurto por medios informáticos es el delito dominante.
-   Bogotá concentra la mayor cantidad de casos.
-   Crecimiento notorio en delitos de acceso abusivo y violación de
    datos.
-   Patrones fuertes en phishing y suplantación digital.
-   Impacto económico significativo por transferencias no autorizadas.
-   Tendencia creciente de ciberdelitos en la última década.

------------------------------------------------------------------------
## Diagrama RACI (Roles y Responsabilidades)

**Leyenda:**

* **R** = Responsable directo
* **A** = Aprueba o valida
* **C** = Consultado
* **I** = Informado

| Actividad / Integrante                 | Camila | Andrés | Soa | Nick |
| -------------------------------------- | ------ | ------ | --- | ---- |
| Selección del dataset                  | C      | C      | C   | R    |
| Limpieza de datos (fechas y geografía) | R      | R      | I   | C    |
| Exploración de datos (EDA)             | R      | R      | R   | C    |
| Visualizaciones                        | R      | R      | R   | R    |
| Construcción del notebook              | C      | C      | I   | R    |
| Documentación final (PDF y README)     | R      | C      | C   | C    |
| Presentación final                     | R      | R      | R   | R    |
| Organización del repositorio GitHub    | C      | I      | I   | R    |

---

## Cuadro de Entregables por Integrante

### **Camila Rivera**

* Gráfico de líneas (tendencia temporal).
* Gráfico de dispersión o matriz de correlación.
* Limpieza y transformación de fechas (FECHA HECHO → AÑO, MES_AÑO).
* Redacción de conclusiones relacionadas con series de tiempo.
* Sección correspondiente del informe y bitácora personal.

### **Andrés Padilla**

* Gráfico de barras por tipo de delito.
* Mapa coroplético por departamento o municipio.
* Verificación de consistencia geográfica en el dataset.
* Aportes al análisis descriptivo geográfico del informe.
* Documentación en bitácora.

### **Alejandro Soa**

* Gráfico de pastel sobre los Top 5 departamentos.
* Análisis descriptivo regional.
* Conclusiones del EDA geográfico.
* Sección correspondiente de la bitácora.

### **Nick Duran**

* Definición del stack tecnológico (Colab, Drive, Python, librerías).
* Gráfico de barras apiladas (departamento vs tipo de delito).
* Gestión y configuración del entorno técnico.
* Garantizar reproducibilidad del notebook completo.
* Documentación técnica en bitácora y apoyo en integración final.
## Diagrama RACI (Roles y Responsabilidades)

**Leyenda:**

* **R** = Responsable directo
* **A** = Aprueba o valida
* **C** = Consultado
* **I** = Informado

| Actividad / Integrante                 | Camila | Andrés | Soa | Nick |
| -------------------------------------- | ------ | ------ | --- | ---- |
| Selección del dataset                  | C      | C      | C   | R    |
| Limpieza de datos (fechas y geografía) | R      | R      | I   | C    |
| Exploración de datos (EDA)             | R      | R      | R   | C    |
| Visualizaciones                        | R      | R      | R   | R    |
| Construcción del notebook              | C      | C      | I   | R    |
| Documentación final (PDF y README)     | R      | C      | C   | C    |
| Presentación final                     | R      | R      | R   | R    |
| Organización del repositorio GitHub    | C      | I      | I   | R    |


------------------------------------------------------

# 7. Organización del Repositorio GitHub

    /Proyecto-Delitos-Informaticos
    │
    ├── data/
    │   └── delitos_informaticos.csv
    │
    ├── notebooks/
    │   └── analisis_delitos.ipynb
    │
    ├── docs/
    │   ├── informe_ASUM_DM.pdf
    │   └── plan_trabajo.md
    │
    ├── presentacion/
    │   └── elevator_pitch.pdf
    │
    └── README.md

------------------------------------------------------------------------

# 8. Cierre

Este documento resume de forma clara, completa y organizada el plan de
trabajo, la metodología ASUM‑DM, la bitácora del proyecto, las
responsabilidades del equipo y los compromisos del entregable final.
