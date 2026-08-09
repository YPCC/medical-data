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

Clinical PHI extraction is normally benchmarked on access-controlled corpora because of the sensitivity of source notes. When navigating clinical NLP datasets, the landscape is commonly split between fully open resources and collections requiring a Data Use Agreement (DUA) due to privacy regulations (e.g., HIPAA).

### Category 1: Open Source & Freely Available (No Restrictions)
These datasets are synthetic, openly licensed, or otherwise available without institutional credentialing — suitable for benchmarking and experimentation without a DUA.

- **ASQ-PHI** (MIT License): a 2026 synthetic benchmark on Mendeley Data featuring adversarial single-turn clinical queries mapped to HIPAA Safe Harbor categories, designed to test over-redaction. Access: https://data.mendeley.com/datasets/csz5dzp7nx/1 `task:de-identification` `access:open` `license:mit` `synthetic`
- **MedAlign & FactEHR** (Non-Commercial Open): longitudinal clinical-data models for medical-NLP development (`access:open-noncommercial`).
- **Synthetic EHR corpora (Hugging Face / GitHub)**: community-generated synthetic clinical text collections that contain no real-patient footprint (`access:open` `synthetic`).

### Category 2: Restricted Access via Data Use Agreement (DUA)
These collections contain authentic clinical notes and require credentialing, human-subjects training (e.g., CITI), and a signed DUA preventing re-identification or public redistribution.

- **n2c2 / i2b2 de-identification corpora** — Gold-standard PHI-annotated discharge summaries and clinical notes. Access and registration: https://n2c2.dbmi.hms.harvard.edu/data-sets `task:de-identification` `access:dua`
- **MIMIC-III / MIMIC-IV** — Large-scale ICU notes, radiology impressions and clinical events. Credentialing and DUA required via PhysioNet: https://physionet.org/ `task:de-identification` `access:dua`
- **CARMEN-I** — Multilingual clinical benchmark (Spanish/Catalan) with PHI annotations. Access: PhysioNet (credentialed) `task:de-identification` `access:dua`

> Do not redistribute DUA-protected data. Obtain files only via the official portals and comply with the data-use terms.

### Open-source tools to benchmark de-identification
Use these tools to evaluate de-identification strategies on synthetic corpora or (internally) on DUA-protected test sets after approval.

- **CliniDeID** — open-source ensemble de-identification (GPL3) combining model-based and rule-based taggers.
- **Philter** — a clinical-text de-identification pipeline targeting common PHI patterns and MongoDB text exports.
- **MIST (MITRE Identity Scrubber Toolkit)** — historically popular for fast i2b2-style evaluation loops.

### Evaluation & practical notes
- For PhysioNet credentialing, verify the required CITI modules and institutional affiliation as part of the sign-up process (see PhysioNet/website). `access:dua`
- Example integrations: a Python script can map i2b2 annotation tags to spaCy or Hugging Face NER formats for training/evaluation; evaluation scripts can measure both recall on PHI categories and over-redaction rates (false positive removal of clinical identifiers).

See the n2c2 / i2b2 overview for challenge archives and access details: ../../benchmarks/n2c2-i2b2.md
