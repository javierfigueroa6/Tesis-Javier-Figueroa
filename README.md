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
```

## ▶️ Orden de Ejecución del Pipeline

Para asegurar la **reproducibilidad completa del análisis**, los scripts y notebooks deben ejecutarse **estrictamente en el siguiente orden**, ya que cada etapa depende de los resultados generados en la anterior.

### 🧬 Etapa 1: Preparación y Procesamiento de Datos (R)

1. **`librerias.R`**  
   Instalación y carga de todas las librerías necesarias para el pipeline completo.

2. **`lectura_secuencias.R`**  
   Lectura de archivos de secuenciación 16S rRNA (FASTQ) y carga de metadatos asociados a las muestras.

3. **`taxonomia.R`**  
   Implementación del pipeline **DADA2**, incluyendo:
   - Filtrado y trimming de secuencias  
   - Modelado de errores  
   - Inferencia de ASV  
   - Eliminación de quimeras  
   - Asignación taxonómica utilizando la base de datos de referencia **SILVA**

4. **`normalizaciones.R`**  
   Normalización de los conteos de ASV y construcción de matrices de abundancia listas para análisis ecológico.

---

### 📊 Etapa 2: Análisis Ecológico y Estadístico (R)

5. **`composicion_taxonomica.R`**  
   Análisis exploratorio de la composición bacteriana a distintos niveles taxonómicos  
   (*Phylum, Class, Order, Family y Genus*).

6. **`diversidad_alfa.R`**  
   Cálculo de métricas de diversidad alfa, incluyendo:
   - Sobs (especies observadas)  
   - Shannon  
   - Simpson  
   - Otros índices complementarios

7. **`diversidad_beta_y_L2FC.R`**  
   - Análisis de diversidad beta  
   - Reducción de dimensionalidad  
   - Cálculo de **Log2 Fold Change (L2FC)** entre los grupos CAN y NOC

---

### 🤖 Etapa 3: Análisis Avanzado y Modelamiento (Python)

8. **`analisis_estadistico.ipynb`**  
   Análisis estadístico avanzado y selección de marcadores taxonómicos mediante:
   - Pruebas estadísticas  
   - Random Forest Classifier  
   - Regularización Lasso y Ridge  

9. **`CAN_NetAna.ipynb`**  
   Análisis de **redes de coocurrencia bacteriana**, incluyendo:
   - Construcción de grafos por grupo  
   - Análisis de centralidad  
   - Detección de comunidades mediante el algoritmo de **Louvain**  
   - Comparación estructural entre redes CAN y NOC

> ⚠️ **Nota:** No se recomienda ejecutar los scripts de forma aislada ni alterar el orden indicado, ya que cada archivo depende de los objetos y resultados generados en las etapas previas.



## 📊 Resultados Principales

El análisis permitió identificar **diferencias significativas en la microbiota gástrica** entre los grupos CAN y NOC.  
Entre los géneros bacterianos destacados como potenciales marcadores se encuentran:

- *Fusobacterium*  
- *Lactobacillus*  
- *Neisseria*  
- *Prevotella*

Estos resultados sugieren un posible rol de la microbiota en la patogénesis del cáncer gástrico y su utilidad como **herramienta complementaria para la detección temprana**.

---

## 🛠️ Requisitos Técnicos

- **R** ≥ 4.0  
- **Python** ≥ 3.8  

### Librerías principales
- `dada2`, `phyloseq`, `vegan`, `ggplot2`  
- `scikit-learn`, `pandas`, `numpy`, `networkx`

Se recomienda ejecutar los scripts en un entorno controlado para asegurar compatibilidad de versiones.

---

## 📄 Referencia

Si utilizas este repositorio o parte del pipeline, por favor cita la tesis:

**Figueroa Quintana, J. A. (2024).**  
*Métodos Estadísticos Aplicados a la Detección de Marcadores Taxonómicos Asociados a Cáncer Gástrico*.  
Universidad Adolfo Ibáñez.

---

## 📬 Contacto

**Javier Agustín Figueroa Quintana**  
📧 [correo institucional o personal]  
🔗 GitHub / LinkedIn (opcional)




