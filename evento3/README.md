# Evento evaluativo 3 — Secuencias y modelos fundacionales

Este evento corresponde a las sesiones 05 y 06 del curso y se centra en modelado secuencial, mecanismos de atención, Transformers y adaptación eficiente de modelos preentrenados.

## Entregables

### Parte A — Examen individual

La evaluación aborda partición temporal y fugas de información, RNN/LSTM/GRU, embeddings y orden en texto, seq2seq con atención, máscaras y posiciones, costo de la autoatención, ajuste supervisado y LoRA.

El PDF diligenciado se conserva en:

`parte_a/examen_parte_a_3.pdf`

### Parte B — Integrador de modelos fundacionales

La Parte B corresponde al ejercicio integrador de la sesión 06, donde se adapta un modelo de lenguaje mediante LoRA para responder con un estilo específico y se registran los experimentos con MLflow.

Archivo de entrega:

`sesion_06_6_integrador_estilo_llm.ipynb`

[![Abrir Evento 3 en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Momos20/si7011-catano/blob/main/evento3/sesion_06_6_integrador_estilo_llm.ipynb)

La Parte B requiere resolver los cuatro TODO, ejecutar los dos entrenamientos solicitados, completar las verificaciones de `responder_raw` y responder las cinco preguntas finales con evidencia de las corridas.

## Estructura

```text
evento3/
├── README.md
├── parte_a/
│   ├── README.md
│   └── examen_parte_a_3.pdf
└── sesion_06_6_integrador_estilo_llm.ipynb
```

No se versionan datasets, modelos completos, adaptadores ni artefactos locales de MLflow; únicamente los entregables solicitados por el curso.
