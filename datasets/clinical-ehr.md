# Clinical & EHR Data

## Building the graph of medicine from millions of clinical narratives
Co-occurrence statistics for medical terms extracted from large-scale clinical narratives.

- Paper: http://www.nature.com/articles/sdata201432
- Data: http://datadryad.org/resource/doi:10.5061/dryad.jp917
- `modality:clinical-text` `task:graph`

## Learning Low-Dimensional Representations of Medical Concepts
Medical concept embeddings constructed from claims/clinical data.

- Paper: http://cs.nyu.edu/~dsontag/papers/ChoiChiuSontag_AMIA_CRI16.pdf
- Data: https://github.com/clinicalml/embeddings
- `modality:claims` `task:embedding`

## MIMIC-III
Anonymized critical-care EHR database containing ICU admissions and longitudinal clinical data.

- Paper: http://www.nature.com/articles/sdata201635
- PhysioNet: https://physionet.org/content/mimiciii/
- `modality:ehr` `domain:critical-care` `access:dua`

## Clinical Concept Embeddings / cui2vec
Concept embeddings learned from large claims, literature and clinical-note sources.

- Paper: https://arxiv.org/abs/1804.01486
- Embeddings: https://figshare.com/s/00d69861786cd0156d81
- Interactive tool: http://cui2vec.dbmi.hms.harvard.edu/
- `task:embedding`

## Clinical text extraction datasets

Clinical NER and concept-normalization corpora have moved to dedicated pages:

- [Clinical & Biomedical NER](biomedical-nlp/named-entity-recognition.md)
- [Entity Linking & Normalization](biomedical-nlp/entity-linking-normalization.md)
- [n2c2 / i2b2](../benchmarks/n2c2-i2b2.md)

This separation is intentional: access-controlled clinical notes should not be confused with open biomedical-literature corpora.
