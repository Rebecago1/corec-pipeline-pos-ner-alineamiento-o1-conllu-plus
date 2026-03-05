# COREC Pipeline POS–NER y alineamiento O(1) a CoNLL-U Plus

## Descripción
Este proyecto, desarrollado en el contexto del **Corpus Oral de Referencia del Español en Contacto (COREC) Fase II: lenguas minoritarias**, tiene por objetivo la implementación de un **algoritmo de alineamiento determinista** entre las formas originales presentes en las transcripciones ortográficas del corpus y los tokens generados por el etiquetado automático mediante la librería de PLN Stanza.

El sistema se basa en una **clave triple estable** (`id_archivo`, `id_ud`, `id_conllu`), que permite recuperar en **tiempo constante (O(1))** los tokens correspondientes, así como mantener la **trazabilidad entre las distintas representaciones del texto**.

Asimismo, el flujo de trabajo incluye **etiquetado morfosintáctico (POS) en el marco de Universal Dependencies (UD)**, **reconocimiento de entidades nombradas (NER)** y **generación de salidas estructuradas en formato CoNLL-U y CoNLL-U Plus**.

La extensión del formato **CoNLL-U a CoNLL-U Plus** permite enriquecer las anotaciones lingüísticas mediante nuevas columnas específicas del proyecto, como **`COREC:NER`**, **`COREC:DISFL`** y **`COREC:FORM_ORIG`**, lo que amplía las posibilidades de análisis y explotación del corpus.


## Archivos del repositorio

**pipeline_COREC.ipynb**  
Cuaderno de **Jupyter Notebook** que contiene la implementación completa del pipeline: etiquetado automático POS Y NER, alineamiento determinista de tokens mediante clave triple y generación de salidas en formato CoNLL-U y CoNLL-U Plus.

Durante la ejecución del cuaderno se generan distintos archivos intermedios.


## Librerías, herramientas y estándar de etiquetado empleados

- **Python**
- **Stanza (Stanford NLP)**
- **Universal Dependencies (UD)**
- **Formato CoNLL-U y CoNLL-U Plus**
