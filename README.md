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

Los notebooks integradores combinan conceptos vistos en clase como inicialización de redes, optimización, regularización, normalización, diagnóstico de entrenamiento, seguimiento de experimentos, arquitecturas para visión, transfer learning, modelado secuencial, atención, Transformers y adaptación eficiente de modelos preentrenados.

El trabajo se desarrolla principalmente con **PyTorch**, **scikit-learn**, **torchvision**, **Transformers**, **PEFT** y **MLflow**, utilizando notebooks ejecutados como evidencia de cada experimento y de las decisiones tomadas durante el modelado.

## Eventos evaluativos

### Evento 1 — Aprendizaje y entrenamiento

El primer evento se concentra en los fundamentos del entrenamiento de redes neuronales y en la interpretación de evidencia experimental.

**Parte A — Examen individual**  
Evaluación sobre fundamentos del entrenamiento de redes neuronales: curvas de aprendizaje, inicialización, propagación de varianza, tamaño de lote, profundidad y regularización.

[Ver Parte A](evento1/parte_a/examen_parte_a.pdf)

**Parte B — Integrador Covertype + MLflow**  
Problema de clasificación multiclase sobre el dataset **Covertype**, con 54 variables de entrada y 7 tipos de cobertura forestal; el ejercicio integra partición estratificada, preprocesamiento sin fuga, construcción y entrenamiento de redes en PyTorch, seguimiento de corridas con MLflow, evaluación con `accuracy` y `macro F1`, selección por validación e inferencia sobre observaciones crudas.

[Ver notebook ejecutado](evento1/sesion_02_6_integrador_covertype.ipynb)

[![Abrir Evento 1 en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Momos20/si7011-catano/blob/main/evento1/sesion_02_6_integrador_covertype.ipynb)

[Ver README del Evento 1](evento1/README.md)

### Evento 2 — Arquitecturas para visión

El segundo evento aborda modelos de visión profunda mediante **EuroSAT**, un conjunto de 27 000 imágenes satelitales RGB clasificadas en 10 tipos de uso del suelo.

**Parte A — Examen individual**  
Evaluación sobre arquitecturas de visión por computador, incluyendo CNN, BatchNorm, data augmentation, redes residuales, transfer learning y Vision Transformers.

[Ver Parte A](evento2/parte_a/examen_parte_a.pdf)

**Parte B — Integrador EuroSAT + MLflow**  
El ejercicio compara una CNN entrenada desde cero con estrategias de fine-tuning sobre ResNet-18 preentrenada en ImageNet; además, incorpora augmentation, AdamW con learning rates diferenciados, warmup y cosine decay, una ablación controlada sobre BatchNorm y un flujo de inferencia reproducible mediante `predict_raw`.

[Ver notebook ejecutado](evento2/sesion_03_6_integrador_eurosat.ipynb)

[![Abrir Evento 2 en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Momos20/si7011-catano/blob/main/evento2/sesion_03_6_integrador_eurosat.ipynb)

[Ver README del Evento 2](evento2/README.md)

### Evento 3 — Secuencias y modelos fundacionales

El tercer evento reúne contenidos de las sesiones 05 y 06, incluyendo series de tiempo, RNN/LSTM/GRU, embeddings, seq2seq con atención, autoatención, Transformers, ajuste supervisado y LoRA.

**Parte A — Examen individual**  
Evaluación sobre secuencias y modelos fundacionales, con preguntas de partición temporal, RNN/LSTM/GRU, embeddings, atención, Transformers, SFT y LoRA.

Archivo: `evento3/parte_a/examen_parte_a_3.pdf`

**Parte B — Integrador de modelos fundacionales**  
El ejercicio adapta un modelo de lenguaje mediante LoRA, compara condiciones experimentales con MLflow y culmina con un flujo de inferencia reproducible mediante `responder_raw`.

Notebook previsto: `evento3/sesion_06_6_integrador_estilo_llm.ipynb`

[![Abrir Evento 3 en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Momos20/si7011-catano/blob/main/evento3/sesion_06_6_integrador_estilo_llm.ipynb)

[Ver README del Evento 3](evento3/README.md)

## Organización

```text
si7011-catano/
├── README.md
├── .gitignore
├── evento1/
│   ├── README.md
│   ├── parte_a/
│   │   └── examen_parte_a.pdf
│   └── sesion_02_6_integrador_covertype.ipynb
├── evento2/
│   ├── README.md
│   ├── parte_a/
│   │   ├── README.md
│   │   └── examen_parte_a.pdf
│   └── sesion_03_6_integrador_eurosat.ipynb
└── evento3/
    ├── README.md
    ├── parte_a/
    │   ├── README.md
    │   └── examen_parte_a_3.pdf
    └── sesion_06_6_integrador_estilo_llm.ipynb
```

---

**Universidad EAFIT**  
**Curso:** SI7011 — Deep Learning  
**Profesor:** Juan David Martínez Vargas
