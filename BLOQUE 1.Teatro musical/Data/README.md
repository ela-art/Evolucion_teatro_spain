# Análisis del Teatro Musical en España (2010–2025)

## Objetivo
Este proyecto analiza la evolución del teatro musical en España entre 2010 y 2025 con el objetivo de identificar patrones de producción, consumo y tendencias estructurales del sector.

Está orientado a aportar **criterio para la toma de decisiones culturales, de programación y de negocio**, combinando análisis de datos con conocimiento experto del sector.

Proyecto cerrado a nivel de **preparación de datos y análisis exploratorio**.  
Pendiente de posibles ampliaciones en visualización y storytelling.

---

## Fuentes de datos

### Fuentes institucionales
- **Anuario de Estadísticas Culturales – Ministerio de Cultura**  
  Hábitos de consumo cultural y asistencia a espectáculos.
- **Anuario SGAE de las Artes Escénicas**  
  Información agregada sobre el sector y su evolución temporal.

### Fuentes sectoriales y públicas
- Carteleras de teatro musical y webs especializadas.
- Información pública de productoras y teatros.
- Curación manual basada en conocimiento profesional del sector.

---

## Proceso de trabajo

El proyecto sigue un flujo clásico de análisis de datos orientado a negocio:

### 1. ETL (Extract · Transform · Load)

**Extracción**
- Integración de múltiples fuentes heterogéneas: institucionales, sectoriales y curación manual.

**Transformación y limpieza**
- Normalización de nombres de obras, productoras y teatros.
- Unificación de marcas históricas de productoras bajo su denominación oficial actual.
- Eliminación de duplicados por `obra + productora`.
- Conversión y validación de tipos (`anio_inicio`, `anio_fin`, `duracion`).
- Homogeneización de estados (activa, gira).
- Enriquecimiento del dataset con variables estratégicas:
  - `genero`
  - `origen` (Franquicia / Creación Propia)

**Carga**
- Generación de un dataset maestro consolidado como *single source of truth*:
  - `maestro_musicales_final.csv`

---

### 2. EDA (Exploratory Data Analysis)

**Calidad de datos**
- Dataset curado manualmente para asegurar coherencia sectorial.
- Alta cobertura en variables clave (obra, productora, años, origen).

**Análisis realizados**
- Distribución de musicales por origen y género.
- Actividad actual vs histórico.
- Análisis de duración media.
- Giras como indicador de escalabilidad y alcance territorial.
- Concentración de productoras y estructuras dominantes del mercado.

**Enfoque**
- Análisis exploratorio orientado a **insights accionables**, no solo descriptivos.

## Tecnologías y herramientas

- **Python**
- **Pandas** (manipulación, limpieza y estructuración de datos)
- **NumPy** (soporte numérico)
- **Matplotlib** y **Seaborn** (visualización y análisis exploratorio)
- **Jupyter Notebook** (EDA y documentación)
- **ETL pipelines manuales**
- **Data Cleaning & Data Quality**
- **Análisis Exploratorio de Datos (EDA)**
- **Git & GitHub** (control de versiones y documentación)
---

## Principales insights

- **Dominio de las franquicias**: ~73% de los musicales analizados lo son, concentrando el riesgo creativo en pocos actores.
- **La creación propia es minoritaria** (~27%) y más fragmentada, asociada a productoras pequeñas o proyectos puntuales.
- **Alta rotación del sector**: solo 13 de 71 musicales siguen activos.
- **La gira como palanca estratégica**: ~58% de los títulos han salido de gira, ampliando impacto más allá de la cartelera madrileña.
- **Estandarización del producto**: duración media ~138 minutos, señal de madurez del sector.
- **Concentración de poder**: pocas productoras acumulan los títulos de mayor recorrido.
- **Predominio de la comedia y el formato familiar**, priorizando accesibilidad y público amplio.

---

## Estructura del repositorio
── Data/
├── Notebooks/
│ └── EDAs finales documentados
│ └── Datasets finales consolidados
└── README.md


Los procesos intermedios (ETL, datasets temporales y EDAs exploratorios) **no se incluyen** para mantener claridad, foco y legibilidad del proyecto.

---

## Alcance y consideraciones

El análisis se basa en una **muestra representativa** de producciones de teatro musical en España entre 2010 y 2025.  
El objetivo no es la exhaustividad absoluta, sino la identificación de **patrones y tendencias estructurales** del sector.

---

## Estado del proyecto
✔ Dataset maestro finalizado  
✔ ETL documentado  
✔ EDA completado  
⏳ Posibles ampliaciones futuras en visualización y storytelling