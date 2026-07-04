# 📔 Bitácora de Aprendizaje — Unidad de Inferencia Estadística

**Estudiante:** Lenin Fabricio Macas Cabrera

**Materia:** Teoría de la Distribución y Probabilidad

**Ciclo:** II

**Docente:** Ing. Cristian Narváez

---

## 🎯 1. Resumen del Aprendizaje Alcanzado

Durante el desarrollo de esta unidad enfocada en la inferencia estadística, logré consolidar el flujo metodológico completo para contrastar hipótesis científicas sobre datos reales. Los puntos clave de aprendizaje incluyen:

* **Formulación de Hipótesis:** Comprender la diferencia estructural entre la Hipótesis Nula ($H_0$), que representa el statu quo o la igualdad, y la Hipótesis Alterna ($H_1$), que carga con la inferencia o sospecha del investigador.
* **Selección de Pruebas Paramétricas:** Identificar cuándo aplicar un test *T de Student* unimuestral en contextos de muestras pequeñas ($n < 30$) frente a la distribución *Z*.
* **Comparación de Poblaciones Independientes:** Implementar la prueba *T de Welch* para el diseño de experimentos o $A/B\ Testing$, asumiendo la robustez del estadístico cuando las varianzas y tamaños de los subgrupos son heterogéneos.
* **Automatización con Python:** Utilizar librerías avanzadas como `scipy.stats` para realizar cálculos exactos de estadísticos de prueba y la obtención algorítmica del *p-valor*.

---

## 🛠️ 2. Dificultades Algorítmicas Superadas

El paso de la teoría matemática al código en Python presentó retos específicos que fueron resueltos sistemáticamente:

1. **Segmentación Dinámica del Dataset:** Inicialmente, el dataset `datos_loja2.csv` presentaba variables continuas y absolutas. La principal dificultad algorítmica fue vectorizar y segmentar correctamente el dataframe utilizando máscaras lógicas en `pandas` (basadas en el umbral poblacional de $15,000$ habitantes) para construir los dos grupos independientes sin duplicar información ni corromper el cálculo.
2. **Direccionalidad de la Prueba Unimuestral:** Configurar la prueba unilateral (*one-tailed test*) en `scipy.stats`. Por defecto, las versiones anteriores calculaban valores p bidireccionales; se superó esta limitación implementando el argumento exacto `alternative='greater'` para evaluar rigurosamente si el promedio superaba el $32\%$.
3. **Manejo de Heterocedasticidad:** Al comparar cantones de escalas poblacionales drásticamente opuestas, las varianzas diferían. Se solucionó configurando el parámetro `equal_var=False` dentro de `ttest_ind` para forzar la corrección de Welch en lugar de la T clásica de Student.

---

## 5. Autoevaluación

| Criterio | Valoración (1-5) | Comentario |
|---|---|---|
| Comprensión teórica | 4 | Me falta aun un poco comprender mejor los temas y contenidos teoricos |
| Aplicación práctica | 4 | Soy capaz de aplicar conceptos teoricos aunque no con la efectividad que se necesita |
| Resolución de problemas | 5 | Me considero capaz para resolver problemas de la materia teniedno las herramientas necesarias |
| Autonomía en el aprendizaje | 4 | Me considero con la responsabilidad y la toma de decisiones sobre qué aprender |

---

## 6. Conclusión personal
Esta experiencia consolidó mi capacidad para orquestar el flujo completo de la ciencia de datos: desde la curación del dataset original (source), pasando por el rigor del formalismo matemático en LaTeX, hasta la automatización del código. Me queda claro que las decisiones de inversión pública y planificación territorial deben estar estrictamente respaldadas por la inferencia estadística, pues es la única herramienta capaz de transformar datos aislados en evidencia científica contundente para el desarrollo regional."
