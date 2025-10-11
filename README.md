# Proyecto-MTSK

**Clasificación temática de artículos sobre el Modelo del Conocimiento Especializado del Profesor de Matemáticas (MTSK)**  
_Autor: [Tu nombre]_  
📅 _Año: 2025_  
🔗 [Ver notebook completo en nbviewer](https://nbviewer.org/github/crojasce/Proyecto-MTSK/blob/main/ProyectoFinal.ipynb)

---

## 🎯 Objetivo del proyecto
Este proyecto busca **clasificar artículos académicos sobre el modelo MTSK** mediante técnicas de **procesamiento de lenguaje natural (NLP)** y **modelos de clustering y aprendizaje supervisado**, con el fin de identificar patrones temáticos y validar la coherencia semántica entre los grupos detectados y las categorías teóricas del modelo.

---

## 🧩 Contexto teórico

El **Modelo del Conocimiento Especializado del Profesor de Matemáticas (MTSK)** describe el conocimiento profesional del docente de matemáticas, dividido en diferentes subdominios.  
En la literatura se han identificado **cinco temáticas principales** que agrupan los estudios existentes:

| Código | Temática MTSK | Descripción resumida |
|:------:|:---------------|:----------------------|
| **T1** | Aplicaciones de MTSK en la formación de profesores | Uso del modelo en procesos de formación inicial y continua, análisis de materiales educativos y reflexión sobre el conocimiento docente. |
| **T2** | Investigaciones sobre el formador de profesores de matemáticas | Estudia la identidad profesional y el conocimiento didáctico de los formadores. |
| **T3** | MTSK en relación con distintos tópicos y etapas | Analiza el desarrollo del modelo en temas específicos (funciones, geometría, fracciones, etc.). |
| **T4** | Desarrollo del MTSK | Explora los subdominios del modelo (como el KPM) y su relación con creencias y estructuras cognitivas. |
| **T5** | Extensiones del MTSK | Conecta el modelo con otras teorías y contextos (tecnología, otras disciplinas, etc.). |

---

## 🧮 Metodología

El flujo de trabajo se desarrolló en **Python** utilizando bibliotecas de NLP y análisis de datos.  
A continuación se resumen las principales etapas:

1. **📥 Preprocesamiento de textos**
   - Limpieza y normalización de resúmenes.
   - Eliminación de stopwords en español.
   - Vectorización mediante **TF-IDF**.

2. **📊 Análisis de agrupamientos**
   - Aplicación de modelos **K-Means** y **Gaussian Mixture Models (GMM)**.
   - Selección de número óptimo de clusters (n=5).
   - Visualización de curvas de densidad y asignaciones.

3. **🔍 Validación semántica**
   - Comparación entre clusters GMM y temáticas MTSK teóricas.
   - Cálculo de similitudes de coseno entre documentos y descripciones temáticas.
   - Identificación de correspondencias predominantes.

4. **📈 Visualización**
   - Gráficas de distribución de temáticas por cluster.
   - Mapas conceptuales de correspondencia semántica.
   - Exportación de resultados a CSV (`validacion_semantica_MTSK.csv`).

---

## 🧠 Resultados destacados

- El modelo **GMM (n=5)** mostró la mejor coherencia con las categorías teóricas.
- Predominó la temática **T1: Aplicaciones de MTSK en la formación de profesores**, con alta frecuencia en los clusters principales.
- Se identificaron **zonas de solapamiento semántico** entre T1, T3 y T5, indicando posibles líneas de convergencia temática.

📊 Ejemplo de visualización:

![Distribución de temáticas MTSK dentro de cada cluster](https://raw.githubusercontent.com/crojasce/Proyecto-MTSK/main/img/distribucion_clusters.png)

---

## 🧰 Tecnologías utilizadas
- **Python 3.12**
- **Scikit-learn**
- **Pandas / NumPy**
- **Matplotlib / Seaborn**
- **NLTK / SpaCy**
- **Jupyter / Google Colab**

---

## 🚀 Próximos pasos
1. Entrenamiento de un **modelo supervisado (Transformers)** con los artículos rotulados por temática MTSK.  
2. Implementación de un **clasificador automático** capaz de predecir la categoría temática de nuevos artículos.  
3. Publicación de una **app interactiva** (Streamlit o Gradio) para probar el modelo en tiempo real.  

---

## 🧑‍💻 Reproducir el proyecto

1. Clona este repositorio:
   ```bash
   git clone https://github.com/crojasce/Proyecto-MTSK.git

