# 📊 Predicción del Abandono Escolar en Nivel Secundario – Tierra del Fuego

Este proyecto analiza el fenómeno del abandono escolar en la educación secundaria de la provincia de Tierra del Fuego, Argentina, mediante técnicas de aprendizaje automático y análisis exploratorio de datos educativos oficiales.

El trabajo permite identificar patrones relevantes, evaluar modelos predictivos de abandono y comprender mejor la relación entre variables como repitencia, sobreedad y promoción efectiva.

---

## 📁 Contenido del repositorio

- `AbandonoEscolaar.ipynb`: notebook principal con todo el flujo de análisis, visualización y modelado.
- `/data`: carpeta sugerida para ubicar los datasets originales en formato `.xlsx`.
- `/img`: visualizaciones exportadas del análisis.
- `README.md`: este archivo.

---

## 🧪 Tecnologías utilizadas

- Python 3.10+
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 📈 Análisis exploratorio

Durante la exploración se observaron patrones crecientes de abandono en los cursos superiores y una fuerte relación con la repitencia.

### Evolución del abandono por curso

![Evolución por curso](reports/figures/abandono_por_curso.png)

### Relación entre repitencia y abandono

![Repitencia vs abandono](reports/figures/repitencia_vs_abandono.png)

---

## 🤖 Modelado predictivo

Se entrenaron y compararon tres modelos de regresión:
- Regresión Lineal
- Árbol de Decisión
- Random Forest Regressor

El modelo de Random Forest logró el mejor desempeño en términos de R² y RMSE. A continuación, se muestra la comparación entre las tasas reales y predichas de abandono en los datos de entrenamiento:

![Predicción vs real](reports/figures/rf_real_vs_pred.png)

Además, se evaluó la importancia relativa de las variables predictoras en el modelo, destacándose la repitencia y la sobreedad como factores clave.

---

## 📌 Conclusión

Este proyecto demuestra cómo las herramientas de aprendizaje automático pueden aportar valor al análisis de problemas educativos, permitiendo identificar variables críticas y construir modelos predictivos útiles. Si bien no se realizaron proyecciones hacia años futuros, el modelo entrenado permite estimar con precisión el comportamiento del abandono en el período observado.

El trabajo sienta una base sólida para futuros análisis más amplios que incorporen otras variables contextuales (como factores socioeconómicos o institucionales), así como más años de datos para mejorar la generalización de los modelos.

---

## 🧠 Autoría
Proyecto académico realizado por Maricel Rausch
Desarrollado en el marco de la materia **Aprendizaje Automático – 2° Año**  
Carrera de Ciencias de Datos e Inteligencia Artificial.
