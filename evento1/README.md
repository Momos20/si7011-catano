# Evento evaluativo 1 — Aprendizaje y entrenamiento

Evento correspondiente a las sesiones **01 y 02** del curso SI7011 — Deep Learning.

El evento está compuesto por dos partes: una evaluación individual y un ejercicio integrador de entrenamiento y despliegue con **PyTorch** y **MLflow**.

## Parte A — Preguntas

La evaluación individual se conserva como evidencia en:

`parte_a/examen_parte_a.pdf`

## Parte B — Ejercicio integrador Covertype

Notebook de entrega:

`sesion_02_6_integrador_covertype.ipynb`

El notebook fue ejecutado de principio a fin e incluye:

- partición estratificada y escalado sin fuga de información;
- definición y validación de una arquitectura neuronal propia;
- optimización con AdamW, warmup lineal y decaimiento cosenoidal;
- tres corridas registradas y comparadas con MLflow;
- selección del mejor modelo usando validación;
- evaluación final sobre el conjunto de prueba;
- implementación y validación de `predict_raw`;
- respuestas de la sección 11 sustentadas con los resultados obtenidos.

## Resultados principales

| Corrida | val_loss | val_acc | F1 macro |
|---|---:|---:|---:|
| Línea base | 1.1963 | 0.488 | 0.094 |
| Mi receta | 0.3406 | 0.867 | 0.771 |
| Sin BatchNorm | 0.3906 | 0.842 | 0.717 |

La mejor corrida fue **Mi receta**. Su evaluación final en prueba obtuvo:

- `loss`: **0.3433**
- `accuracy`: **0.8656**
- `F1 macro`: **0.7701**

La verificación de despliegue mostró una consistencia del **100 %** entre las predicciones generadas desde el artefacto guardado y las obtenidas durante la evaluación.

## Estructura

```text
evento1/
├── README.md
├── parte_a/
│   ├── README.md
│   └── examen_parte_a.pdf
└── sesion_02_6_integrador_covertype.ipynb
```

Los datos, checkpoints y archivos locales de MLflow no se versionan en el repositorio.