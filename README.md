# proyectos-NLP-machine-learning

Colección de notebooks de práctica en Procesamiento de Lenguaje Natural, pensados para correr en Google Colab (free tier).

## Notebooks

### 1. Clasificación de emociones con BERT
`Clasificación_de_emociones_BERT.ipynb`

Fine-tuning de `bert-base-uncased` para clasificar texto en 6 emociones (sadness, joy, love, anger, fear, surprise) usando el dataset [`dair-ai/emotion`](https://huggingface.co/datasets/dair-ai/emotion) de HuggingFace.

**Contenido:**
- Tokenización con el tokenizer de BERT
- Cabezal de clasificación lineal sobre el embedding `[CLS]`
- Entrenamiento con `AdamW` + scheduler lineal con warmup
- Evaluación con matriz de confusión y `classification_report`
- Visualización de cabezales de atención
- Inferencia sobre frases nuevas

**Stack:** PyTorch, HuggingFace `transformers` y `datasets`, scikit-learn, seaborn.

---

### 2. Traducción Francés → Español con arquitectura Transformer
`Tatoeba_Traduccion_frances_espanol.ipynb`

Implementación desde cero (en PyTorch puro) de la arquitectura Transformer original (*Attention Is All You Need*) para traducción francés-español, entrenada sobre el dataset [Tatoeba](https://tatoeba.org/es).

> Basado en un notebook del curso de NLP de [Instituto Humai](https://github.com/institutohumai/cursos-python), adaptado de inglés-español a francés-español.

**Contenido:**
- Preprocesamiento y construcción de vocabularios
- Implementación manual de encoder, decoder y atención multi-cabezal
- Loop de entrenamiento con seguimiento de perplejidad (PPL)
- Visualización de mapas de atención por cabezal
- Evaluación con BLEU score (`sacrebleu`)
- Ejemplos de traducción sobre frases de train, validación y test

**Stack:** PyTorch, torchtext, sacrebleu.

## Cómo correrlos

Cada notebook está pensado para abrirse directamente en Google Colab y ejecutarse de arriba hacia abajo (las celdas son idempotentes). No requieren credenciales ni configuración adicional: los datasets se descargan públicamente dentro del propio notebook. Para realizar modificaciones, se recomienda realizar primero una copia personal del notebook.
