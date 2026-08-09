# Entity Linking & Medical Concept Normalization

This task maps extracted mentions to controlled biomedical concepts such as **UMLS, SNOMED CT, RxNorm, MeSH, OMIM, MedDRA or LOINC**.

## Core resources

### NCBI Disease Corpus
Disease mentions normalized to MeSH/OMIM.

- https://www.ncbi.nlm.nih.gov/research/bionlp/Data/disease/
- `entity:disease` `terminology:mesh` `terminology:omim` `access:open`

### MedMentions / ST21pv
Biomedical mentions linked to UMLS concepts.

- https://github.com/chanzuckerberg/MedMentions
- `terminology:umls` `access:open`

### BC5CDR
Chemical and disease annotations grounded in MeSH.

- https://biocreative.bioinformatics.udel.edu/tasks/biocreative-v/track-3-cdr/
- `terminology:mesh`

### n2c2 2019 Clinical Concept Normalization
Clinical problem/treatment/test mentions normalized to UMLS-derived concepts using SNOMED CT and RxNorm subsets.

- https://n2c2.dbmi.hms.harvard.edu/
- `terminology:umls` `terminology:snomed-ct` `terminology:rxnorm` `access:dua`

### ShARe/CLEF
Clinical disorder mentions linked to UMLS.

- `terminology:umls` `access:dua-or-registration`

### BELB — Biomedical Entity Linking Benchmark
Unified evaluation across multiple biomedical entity types and knowledge bases.

- Paper/search entry point: https://github.com/sg-wbi/belb
- `task:entity-linking`

### SNOMED CT Entity Linking from clinical notes
MIMIC-IV–based clinical-note entity-linking resources have been developed for SNOMED CT concept grounding.

- Access commonly depends on PhysioNet credentialing and source-resource licenses.
- `terminology:snomed-ct` `access:dua`

## Evaluation dimensions

Do not evaluate concept normalization only with exact string matching. Useful dimensions include:

- mention detection F1
- concept accuracy / micro-F1
- top-k accuracy
- MRR / Hits@K for candidate ranking
- hierarchical distance or ontology-aware similarity
- NIL / out-of-KB handling
- exact vs relaxed span matching
- cross-institution/domain generalization

For end-to-end IE, pair this page with [NER](named-entity-recognition.md) and [Knowledge Extraction](knowledge-extraction.md).
