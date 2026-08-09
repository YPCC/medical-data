# Clinical & Biomedical Named Entity Recognition (NER)

NER identifies spans such as **diseases, medications, tests, symptoms, procedures, genes/proteins, chemicals, variants, species and PHI**.

## Open biomedical-literature corpora

### NCBI Disease Corpus
Gold-standard disease recognition and concept-normalization corpus.

- 793 PubMed abstracts
- 6,892 disease mentions
- 790 unique disease concepts
- Concepts link to MeSH and/or OMIM
- Source: https://www.ncbi.nlm.nih.gov/research/bionlp/Data/disease/
- `task:ner` `task:normalization` `entity:disease` `access:open`

### BC5CDR
1,500 PubMed abstracts annotated for chemicals, diseases and chemical–disease relations, with MeSH identifiers.

- BioCreative: https://biocreative.bioinformatics.udel.edu/tasks/biocreative-v/track-3-cdr/
- `task:ner` `task:relation-extraction` `entity:chemical` `entity:disease`

### MedMentions
4,392 PubMed abstracts densely annotated with UMLS concepts. The ST21pv subset is commonly used for biomedical entity-linking evaluation.

- Data: https://github.com/chanzuckerberg/MedMentions
- `task:ner` `task:entity-linking` `terminology:umls` `access:open`

### JNLPBA / GENIA
Classic biomedical NER resource derived from GENIA, with entity types such as protein, DNA, RNA, cell line and cell type.

- Shared-task information: https://www.geniaproject.org/shared-tasks/bionlp-jnlpba-shared-task-2004
- `task:ner` `modality:biomedical-literature`

### BC2GM
BioCreative II Gene Mention corpus for identifying gene/protein mentions in biomedical text.

- BioCreative: https://biocreative.bioinformatics.udel.edu/
- `task:ner` `entity:gene-protein`

### CRAFT
Colorado Richly Annotated Full Text corpus: biomedical full-text articles with syntactic and semantic annotation grounded in multiple biomedical ontologies.

- Project: https://craft-shared-task.github.io/
- `task:ner` `modality:full-text` `task:ontology-grounding`

## Clinical-note NER corpora

### i2b2 2010 Concepts, Assertions & Relations
Clinical notes annotated for **Problem, Treatment, Test**, assertions and relations.

- Access: n2c2/i2b2 portal
- `task:ner` `task:assertion` `task:relation-extraction` `access:dua`

### n2c2 2018 Track 2 — ADE & Medication Extraction
505 MIMIC-III discharge summaries annotated for medication-related attributes, ADE and Reason.

- Access: https://n2c2.dbmi.hms.harvard.edu/
- `task:ner` `entity:medication` `entity:ade` `access:dua`

### MADE 1.0
EHR notes from cancer patients annotated for medication attributes, indication, ADE, severity and signs/symptoms/diseases.

- Access: challenge/organizer request
- `task:ner` `entity:medication` `entity:ade` `access:request`

### ShARe/CLEF eHealth
Clinical disorder mentions with normalization to UMLS concepts.

- Access: shared-task / PhysioNet controls may apply
- `task:ner` `task:normalization` `access:dua-or-registration`

## BioASQ clinical/biomedical NER families

BioASQ has hosted multiple entity-recognition and normalization tasks, including disease/procedure-focused tasks and nested biomedical entity recognition. See the dedicated [BioASQ page](../../benchmarks/bioasq.md) for the current task family.

## PHI / de-identification datasets

Clinical PHI extraction is normally benchmarked on access-controlled corpora because of the sensitivity of source notes.

- i2b2 2006 de-identification
- i2b2/UTHealth 2014 de-identification and heart-disease risk factors
- other n2c2 de-identification challenge corpora

See [n2c2 / i2b2](../../benchmarks/n2c2-i2b2.md).

> Do not redistribute n2c2/i2b2 data files. Each approved user must obtain them through the designated portal under the applicable DUA.
