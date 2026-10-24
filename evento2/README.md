# Evento evaluativo 2 — Arquitecturas para visión

Este evento corresponde a la sesión 03 del curso y se centra en arquitecturas de aprendizaje profundo para visión por computador, usando **EuroSAT** como conjunto de datos principal.

## Entregables

### Parte A — Lectura de evidencia

La Parte A corresponde al examen individual sobre CNN, BatchNorm, data augmentation, redes residuales, transfer learning y Vision Transformers.

[Ver PDF de la Parte A](parte_a/examen_parte_a.pdf)

### Parte B — Integrador EuroSAT + MLflow

El notebook implementa un problema de clasificación de imágenes satelitales RGB de **64 × 64** en **10 clases**. Se resolvieron los cuatro TODO del ejercicio y se ejecutaron las tres corridas requeridas.

[Ver notebook ejecutado](sesion_03_6_integrador_eurosat.ipynb)

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Momos20/si7011-catano/blob/main/evento2/sesion_03_6_integrador_eurosat.ipynb)

## Implementación

El flujo desarrollado incluye una partición estratificada **70/15/15**, augmentation mediante rotaciones de 90°, flip horizontal y flip vertical, una CNN entrenada desde cero como línea base y una **ResNet-18 preentrenada en ImageNet** ajustada mediante fine-tuning. El entrenamiento de la receta utiliza **AdamW**, learning rates diferenciados para backbone y cabeza, warmup de una época y decaimiento coseno; además, las corridas se registran y comparan con MLflow.

La tercera corrida conserva la misma receta y cambia únicamente el comportamiento de BatchNorm mediante `freeze_bn`, lo que permite evaluar ese factor de forma controlada. Finalmente, `predict_raw` valida el contrato de entrada, reconstruye el modelo desde el artefacto guardado y reproduce las predicciones de prueba con **100 % de consistencia**.

## Resultados

| Corrida | `best_val_loss` | `best_val_acc` | `best_val_macro_f1` |
|---|---:|---:|---:|
| CNN desde cero | 0.199 | 0.930 | 0.927 |
| Fine-tuning ResNet-18 | 0.074 | 0.978 | 0.977 |
| Fine-tuning + BatchNorm congelado | **0.072** | 0.976 | 0.975 |

La selección final se realizó exclusivamente con `best_val_loss`, por lo que se eligió la corrida **3-freeze-bn**. Al evaluarla una sola vez sobre el conjunto de prueba se obtuvo `accuracy = 0.9701` y `macro F1 = 0.9691`.

## Estructura

```text
evento2/
├── README.md
├── parte_a/
│   ├── README.md
│   └── examen_parte_a.pdf
└── sesion_03_6_integrador_eurosat.ipynb
```

Los datos descargados, checkpoints y archivos locales de MLflow no se versionan en el repositorio.