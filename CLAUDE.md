# CLAUDE.md

## Contexto del proyecto

Este repositorio contiene un proyecto de transformación y análisis de los microdatos del examen **Saber 11** en Colombia.

El objetivo principal es construir una base de datos limpia y estructurada que permita realizar análisis econométricos y espaciales del desempeño educativo en el país.

El proyecto se enfoca en:

- limpieza y transformación de datos
- construcción de bases agregadas
- análisis econométrico
- análisis espacial del rendimiento académico

---

## Objetivos técnicos del proyecto

1. Transformar los microdatos originales del Saber 11.
2. Construir una base analítica agregada a nivel territorial.
3. Integrar información geográfica para análisis espacial.
4. Analizar desigualdades regionales en el desempeño educativo.
5. Estimar modelos econométricos sobre determinantes del rendimiento académico.

---

## Estructura del repositorio

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
│   │   Datos después del proceso de limpieza
│   │
│   └── analysis
│       Bases finales utilizadas para análisis
│
├── notebooks
│   ├── 01_limpieza_datos.ipynb
│   ├── 02_construccion_base.ipynb
│   └── 03_analisis_espacial.ipynb
│
├── src
│   Scripts reutilizables de transformación de datos
│
└── outputs
    Resultados del análisis (tablas, mapas, gráficos)
```

---

## Flujo de desarrollo esperado

### 1. Limpieza de datos

Los microdatos del Saber 11 se cargan desde `data/raw` y se procesan para:

- limpiar variables
- manejar valores faltantes
- estandarizar nombres de variables
- seleccionar variables relevantes

Los resultados se guardan en `data/cleaned`.

---

### 2. Construcción de base analítica

Los datos se agregan para facilitar análisis territorial.

Ejemplos:

- promedio de puntajes por municipio
- número de estudiantes por municipio
- indicadores socioeconómicos agregados

Los resultados se guardan en `data/analysis`.

---

### 3. Integración espacial

Las bases agregadas se combinan con archivos geográficos (shapefiles de municipios o departamentos de Colombia) para realizar análisis espacial.

---

### 4. Análisis econométrico

Se utilizan modelos econométricos para estudiar determinantes del desempeño educativo.

Ejemplos:

- regresiones lineales
- modelos con variables socioeconómicas
- análisis territorial del desempeño académico

---

## Reglas de desarrollo

1. **No modificar directamente los datos en `data/raw`.**
2. Todas las transformaciones deben generar nuevos archivos en `data/cleaned` o `data/analysis`.
3. Evitar implementar lógica compleja dentro de notebooks.
4. Implementar funciones reutilizables dentro de la carpeta `src`.
5. Usar notebooks principalmente para exploración y visualización.
6. Mantener código claro y documentado.

---

## Variables clave esperadas en los datos

- municipio
- departamento
- periodo
- puntaje matemáticas
- puntaje lectura crítica
- estrato socioeconómico
- nivel educativo de los padres
- tipo de institución educativa
- características del hogar

---

## Librerías principales

El proyecto utiliza principalmente:

- pandas
- numpy
- geopandas
- statsmodels
- matplotlib
- seaborn
- scikit-learn

Para análisis espacial:

- pysal

---

## Convenciones de nombres

Notebooks:

```
01_limpieza_datos
02_construccion_base
03_analisis_espacial
```

Scripts en `src`:

- `limpieza.py`
- `agregaciones.py`
- `spatial.py`

---

## Buenas prácticas

- escribir funciones pequeñas y reutilizables
- documentar funciones con docstrings
- evitar duplicación de código
- mantener notebooks limpios y reproducibles
- separar claramente transformación, análisis y visualización

---

## Objetivo final del proyecto

Construir una base de datos confiable que permita estudiar **desigualdades educativas en Colombia** y analizar patrones territoriales del desempeño académico utilizando herramientas econométricas y espaciales.