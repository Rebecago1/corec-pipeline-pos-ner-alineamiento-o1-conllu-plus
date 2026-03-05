# ***Pipeline* de PLN para el Corpus Oral de Referencia del Español en Contacto (COREC): etiquetado automático POS/NER, alineamiento determinista O(1) mediante triple clave estable y generación de CoNLL-U Plus**
## Descripción

Este *pipeline*, desarrollado en el contexto del **Corpus Oral de Referencia del Español en Contacto (COREC) Fase II: lenguas minoritarias**, tiene por objetivo la implementación de un **algoritmo de alineamiento determinista** entre las formas originales presentes en las transcripciones ortográficas del corpus y los tokens generados por el etiquetado automático mediante la librería de PLN Stanza.

El sistema se basa en una **clave triple estable** (`id_archivo`, `id_ud`, `id_conllu`), que recupera determinados tokens del corpus mediante consultas en **tiempo constante (O(1))** y preserva la **trazabilidad entre las representaciones originales y normalizadas del texto.**.

Asimismo, el flujo de trabajo incluye **etiquetado morfosintáctico (POS) en el marco *Universal Dependencies* (UD)**, **reconocimiento de entidades nombradas (NER)** y **generación de salidas estructuradas en formato CoNLL-U y CoNLL-U Plus**.

La extensión del formato **CoNLL-U a CoNLL-U Plus** enriquece las anotaciones lingüísticas mediante columnas específicas del proyecto, como **`COREC:NER`**, **`COREC:DISFL`** y **`COREC:FORM_ORIG`**, y amplía las posibilidades de análisis y explotación del corpus.


## Archivos del repositorio

**09_COREC_etiquetado_Stanza_alineamiento_CoNLL-U Plus.ipynb**  

Cuaderno de Jupyter que contiene la implementación del *pipeline*.
Durante su ejecución se generan varios archivos y salidas:

- **Log_4_9_11_merged_con_id_conllu_final.csv**: registro que incluye el resultado del **alineamiento entre las formas resultantes y los identificadores de token (`id_conllu`)**.
- **archivos en formato CoNLL-U**: salida del etiquetado automático POS y NER mediante Stanza.
- **archivos en formato CoNLL-U Plus**: versión extendida del formato CoNLL-U que incorpora las columnas `COREC:NER`, `COREC:DISFL` y `COREC:FORM_ORIG`.


## Librerías, herramientas y estándar de etiquetado empleados

- **Python**
- **pandas**
- **Stanza (Stanford NLP)**
- **Universal Dependencies (UD)**
- **Formato CoNLL-U y CoNLL-U Plus**
