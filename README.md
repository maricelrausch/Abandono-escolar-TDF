# Predicción del Abandono Escolar en Nivel Secundario - Tierra del Fuego

## Contexto:
Tierra del Fuego presenta desafíos particulares en su sistema educativo debido a su geografía, distribución poblacional y condiciones sociales. Detectar a tiempo los factores que inciden en el abandono puede permitir acciones preventivas por parte de los equipos educativos y de gestión, mejorando la trayectoria escolar de los estudiantes.

Este proyecto aplica técnicas de Aprendizaje Automático para desarrollar un modelo de clasificación supervisada que permita identificar patrones asociados al abandono escolar. El enfoque no es realizar un análisis de la información existente, sino **entrenar un modelo que aprenda a clasificar** los registros en función del nivel de abandono, a partir de variables estructuradas como repitencia, sobreedad, promoción y matrícula.

## Objetivo:
- Desarrollar un modelo de clasificación que determine si un año escolar presenta una alta o baja tasa de abandono, en función de variables como promoción efectiva, sobreedad, repitencia, tipo de gestión educativa y matrícula.
- Identificar las variables que más influyen en esta clasificación, permitiendo reconocer situaciones escolares de mayor riesgo.


## Datasets utilizados:

### 📄 04-1-10-Secundario-comun.-Repitentes-por-sector-de-gestion-y-ano-de-estudio.-2008-2021.xlsx
- Cantidad de instancias: 28
- Cantidad de columnas: 27

**Variables principales:**
- Año
- Sector de gestión (Estatal, Privado)
- Año de estudio (1° a 6°)
- Departamento (Ushuaia, Río Grande)

**Tipos de datos:**
- Numéricos: principalmente enteros (cantidad de repitentes, porcentajes).
- Categóricos: año, sector de gestión, año de estudio, departamento.

---

### 📄 04_01_06-Secundario-comun.-Promocion-efectiva-sobreedad-y-abandono-interanual-por-ano-de-estudio.-TDF.xlsx
- Cantidad de instancias: 9
- Cantidad de columnas: 1

**Variables principales descritas:**
- Tasa de promoción efectiva
- Tasa de sobreedad
- Tasa de abandono interanual

**Tipos de datos:**
- Las variables son categóricas/descriptivas (indicadores sobre tasas específicas). Requiere estructuración y extracción manual de datos numéricos para análisis.

---

### 📄 04-1-09-Secundario-comun.-Matricula-por-sector-de-gestion-ano-de-estudio-y-departamento.-TDF-USH-RGA-y-AA.xlsx
- Cantidad de instancias: 38
- Cantidad de columnas: 18

**Variables principales:**
- Año
- Sector de gestión (Estatal, Privado)
- Año de estudio (1° a 7°)
- Departamento (Ushuaia, Río Grande, Tolhuin, Antártida Argentina)

**Tipos de datos:**
- Numéricos: principalmente matrícula por año y por sector.
- Categóricos: año, sector de gestión, año de estudio, departamento.

---

## Preprocesamiento realizado

- Limpieza individual de cada archivo (columnas innecesarias, filas vacías)
- Renombrado uniforme de variables (`rep_`, `sobr_`, `prom_`, `mat_`, `aband_`)
- Unificación de todos los datasets usando claves compartidas (ej. `año`, `curso`)
- Conversión de tasas de abandono en una variable binaria (`abandono_binario`) que indica si la tasa supera un umbral crítico (>5%)
> 💡 Estos datos se reorganizaron para integrarlos a una única estructura consolidada y numérica, consolidando un nuevo dataset que será el utilizado para modelar. 

### 📄 DatosAbandonoTDF.xlsx
- Instancias: 21 
- Columnas: 55

**Variables principales**:
-	rep_total_pct: porcentaje de repitencia total
-	sobr_total_pct: tasa de sobreedad total
-	prom_total_pct: tasa de promoción efectiva total
-	mat_total_pct: matrícula general
-	aband_total_pct: tasa de abandono general
-	abandono_binario: variable objetivo binaria
-	También se incluyen tasas y cantidades por cursos, tipo de gestión y ciudades (Río Grande/Ushuaia) 

**Tipo de datos**  
- Numéricos (tasas porcentuales y cantidades)
- Categóricos (años)

## Fuente
Portal de Estadísticas Educativas de Tierra del Fuego:  
https://ipiec.tierradelfuego.gob.ar/estadisticas-sociales-y-demograficas/

## Nota
Este proyecto tiene fines académicos y se encuentra en desarrollo. Se contempla la incorporación futura de nuevos datasets que aporten variables demográficas o sociales adicionales.

## Fuente:
[https://ipiec.tierradelfuego.gob.ar/estadisticas-sociales-y-demograficas/](https://ipiec.tierradelfuego.gob.ar/estadisticas-sociales-y-demograficas/)

