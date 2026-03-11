# Análisis de Datos Saber 11 – Colombia

Este proyecto construye una base de datos analítica a partir de los microdatos del examen **Saber 11** en Colombia con el objetivo de realizar análisis econométricos y espaciales del desempeño educativo.

El repositorio contiene el pipeline de transformación de datos, construcción de bases agregadas y herramientas para análisis estadístico y geoespacial.

---

# Objetivos del proyecto

1. Transformar y limpiar los microdatos del examen Saber 11.
2. Construir una base de datos agregada a nivel territorial (municipio / departamento).
3. Integrar información geográfica para análisis espacial.
4. Analizar desigualdades regionales en el desempeño académico.
5. Estimar modelos econométricos sobre determinantes del rendimiento educativo.

---

# Estructura del proyecto

```
.
├── README.md
├── CLAUDE.md
├── requirements.txt
├── .gitignore
│
├── data
│   ├── raw
│   │   Datos originales del Saber 11
│   │
│   ├── cleaned
│   │   Datos procesados después de limpieza
│   │
│   └── analysis
│       Bases finales utilizadas en análisis
│
├── notebooks
│   ├── 01_limpieza_datos.ipynb
│   ├── 02_construccion_base.ipynb
│   └── 03_analisis_espacial.ipynb
│
├── src
│   Scripts reutilizables del proyecto
│
└── outputs
    ├── tablas
    └── mapas
```

---

# Flujo de trabajo

## 1. Limpieza de datos

Se cargan los microdatos originales del Saber 11 y se realizan procesos de:

- limpieza de variables
- manejo de valores faltantes
- estandarización de nombres de variables
- selección de variables relevantes

Resultado: dataset limpio en `data/cleaned`.

---

## 2. Construcción de base analítica

Los microdatos se agregan a nivel territorial para permitir análisis regional.

Ejemplos de agregación:

- promedio de puntajes por municipio
- número de estudiantes por región
- indicadores socioeconómicos promedio

Resultado: base final en `data/analysis`.

---

## 3. Integración geográfica

Se integran las bases agregadas con información geográfica (municipios o departamentos de Colombia) para realizar análisis espacial.

Se utilizan archivos geográficos del DANE.

---

## 4. Análisis econométrico y espacial

El proyecto busca analizar:

- desigualdad regional en resultados educativos
- determinantes socioeconómicos del desempeño académico
- patrones espaciales del rendimiento educativo

Los análisis incluyen:

- regresiones econométricas
- visualización espacial
- estadísticas espaciales

---

# Tecnologías utilizadas

- Python
- pandas
- numpy
- geopandas
- statsmodels
- matplotlib
- seaborn
- scikit-learn

Para análisis espacial avanzado:

- pysal

---

# Instalación

Instalar dependencias:

```bash
pip install -r requirements.txt
```

---

# Datos

Los microdatos del Saber 11 deben descargarse desde las fuentes oficiales del ICFES.

Por razones de tamaño y licenciamiento, los datos originales no se incluyen en este repositorio.

---

# Estado del proyecto

Proyecto en desarrollo orientado a análisis econométrico y espacial de datos educativos en Colombia.