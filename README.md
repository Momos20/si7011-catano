<p align="center">
  <img src="https://latimpacto.org/wp-content/uploads/2023/11/Eafit.png" width="38%">
</p>

<h1 align="center">SI7011 — Deep Learning</h1>

<p align="center">
Repositorio académico para el desarrollo de los eventos evaluativos y ejercicios integradores del curso <strong>SI7011 — Deep Learning</strong> de la Universidad EAFIT.
</p>

## Autor

**Juan Camilo Cataño Zuleta**

## Sobre el repositorio

Este repositorio reúne el trabajo práctico desarrollado durante el curso, con énfasis en la construcción, entrenamiento, evaluación y análisis experimental de modelos de aprendizaje profundo.

Los notebooks integradores combinan conceptos vistos en clase como inicialización de redes, optimización, regularización, normalización, diagnóstico de entrenamiento, seguimiento de experimentos e inferencia reproducible.

El trabajo se desarrolla principalmente con **PyTorch**, **scikit-learn** y **MLflow**, utilizando notebooks ejecutables como evidencia de cada experimento y de las decisiones tomadas durante el modelado.

## Eventos evaluativos

### Evento 1 — Aprendizaje y entrenamiento

El primer evento se concentra en los fundamentos del entrenamiento de redes neuronales y en la interpretación de evidencia experimental.

**Parte A — Lectura de evidencia**  
Examen individual orientado al diagnóstico de curvas de entrenamiento, inicialización, propagación de varianza, tamaño de lote, profundidad y regularización.

Archivo: [`evento1/parte_a/examen_parte_a.pdf`](evento1/parte_a/examen_parte_a.pdf)

**Parte B — Integrador Covertype + MLflow**  
Problema de clasificación multiclase sobre el dataset **Covertype**, con 54 variables de entrada y 7 tipos de cobertura forestal. El ejercicio integra:

- partición estratificada y preprocesamiento sin fuga de información;
- construcción de un MLP en PyTorch;
- inicialización He, normalización y regularización;
- optimización con AdamW y programación de la tasa de aprendizaje;
- seguimiento y comparación de corridas con MLflow;
- evaluación mediante `accuracy` y `macro F1`;
- selección del modelo mediante validación;
- construcción de una función de inferencia sobre observaciones crudas.

Notebook: `evento1/sesion_02_6_integrador_covertype.ipynb`

### Evento 2 — Arquitecturas para visión

El segundo evento aborda modelos de visión profunda mediante el dataset **EuroSAT**. El integrador trabaja con imágenes satelitales y experimentación controlada sobre arquitecturas convolucionales y estrategias vistas durante la sesión de visión.

Notebook: `evento2/sesion_03_6_integrador_eurosat.ipynb`

## Organización

```text
si7011-catano/
├── README.md
├── .gitignore
├── evento1/
│   ├── parte_a/
│   │   └── examen_parte_a.pdf
│   └── sesion_02_6_integrador_covertype.ipynb
├── evento2/
│   └── sesion_03_6_integrador_eurosat.ipynb
└── evento3/
```

## Enfoque experimental

Los entregables buscan que cada decisión de modelado pueda justificarse a partir de evidencia observable. Por ello, los notebooks conservan las métricas, curvas de entrenamiento, comparaciones entre corridas y resultados necesarios para analizar el comportamiento de los modelos, no solo su implementación final.

---

**Universidad EAFIT**  
**Curso:** SI7011 — Deep Learning  
**Profesor:** Juan David Martínez Vargas
