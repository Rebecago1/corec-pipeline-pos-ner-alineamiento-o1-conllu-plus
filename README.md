# COREC Pipeline POS–NER y alineamiento O(1) a CoNLL-U Plus

Pipeline de procesamiento lingüístico desarrollado para el proyecto COREC.

## Funcionalidades

- Etiquetado automático POS y NER
- Conversión a formato CoNLL-U
- Extensión a CoNLL-U Plus
- Alineamiento determinista entre tokens y formas originales
- Sistema de clave triple estable (id_archivo, id_ud, id_conllu)
- Índices en memoria con acceso O(1)

## Salidas

El pipeline genera:

- archivos CoNLL-U
- archivos CoNLL-U Plus enriquecidos con:
  - COREC:NER
  - COREC:DISFL
  - COREC:FORM_ORIG

## Objetivo

Garantizar trazabilidad completa entre:

forma_original → forma_resultante → token CoNLL-U

mediante un sistema de alineamiento estable basado en índices en memoria.

## Tecnologías

- Python
- Stanza
- Universal Dependencies
- CoNLL-U / CoNLL-U Plus
