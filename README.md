# Análisis Estadístico de Secuencias 16S rRNA  
### Detección de Marcadores Taxonómicos Asociados a Cáncer Gástrico

Este repositorio contiene el **pipeline completo de análisis bioinformático y estadístico** desarrollado en la tesis de Magíster:

> **“Métodos Estadísticos Aplicados a la Detección de Marcadores Taxonómicos Asociados a Cáncer Gástrico”**  
> *Javier Agustín Figueroa Quintana*  
> Master of Science in Data Science – Universidad Adolfo Ibáñez (2024)

El objetivo del estudio es **identificar diferencias significativas en la composición de la microbiota gástrica** entre pacientes con cáncer gástrico (CAN) y sujetos sanos (NOC), utilizando datos de secuenciación **16S rRNA** y métodos estadísticos y de machine learning.

---

## 🧬 Descripción General del Estudio

- **Tipo de estudio:** Observacional transversal  
- **Datos:** Secuenciación 16S rRNA de tejido gástrico  
- **Unidad de análisis:** Variantes de Secuencia de Amplicón (ASV)  
- **Pipeline bioinformático:** DADA2  
- **Nivel taxonómico principal:** Género bacteriano  
- **Lenguajes utilizados:** R y Python  

Se aplican técnicas de:
- Análisis de composición taxonómica  
- Abundancias relativas  
- Log2 Fold Change  
- Diversidad alfa y beta  
- Reducción de dimensionalidad  
- Selección de características (Random Forest, Lasso, Ridge)  
- Análisis de redes de coocurrencia bacteriana  

---

## 🧪 Estructura del Pipeline Analítico

El flujo de trabajo se divide en **dos grandes etapas**:

### 1️⃣ Preparación y Procesamiento de Datos
Incluye limpieza, corrección de errores y construcción de ASV.

### 2️⃣ Análisis Ecológico y Estadístico
Incluye análisis taxonómico, diversidad, selección de marcadores y análisis de redes.

---

## 📂 Estructura del Repositorio

```text
├── librerias.R
├── lectura_secuencias.R
├── taxonomia.R
├── normalizaciones.R
├── composicion_taxonomica.R
├── diversidad_alfa.R
├── diversidad_beta_y_L2FC.R
├── analisis_estadistico.ipynb
├── CAN_NetAna.ipynb
└── README.md
