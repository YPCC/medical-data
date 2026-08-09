# BioASQ

[BioASQ](https://bioasq.org/) is a long-running biomedical semantic indexing and question-answering challenge ecosystem. It is useful to treat BioASQ as a **family of tasks and data assets**, not as a single dataset.

## Why it belongs in this repository

BioASQ spans multiple stages of the biomedical AI pipeline:

```text
Literature / Clinical Text
   ├─ Entity recognition & normalization
   ├─ Information / relation extraction
   ├─ Semantic indexing
   ├─ Evidence retrieval
   ├─ Biomedical question answering
   └─ Clinical summarization
```

## Current 2026 / Challenge 14 family

The official participant area lists the following task families for 2026:

### Task 14b — Biomedical Question Answering
Large-scale biomedical QA using questions, concepts/documents/snippets and exact/ideal answers, depending on phase.

- Participant area: https://participants-area.bioasq.org/Tasks/14b/
- `task:biomedical-qa` `task:retrieval`

### Synergy
Iterative biomedical QA in which expert feedback can be incorporated across rounds.

- https://participants-area.bioasq.org/
- `task:qa` `task:human-feedback`

### BioNNE-R
Biomedical nested named-entity / relation-oriented challenge family.

- https://participants-area.bioasq.org/
- `task:ner` `task:relation-extraction`

### ELCardioCC
Clinical/cardiology entity-linking/coding challenge family.

- https://participants-area.bioasq.org/
- `task:entity-linking` `domain:cardiology`

### GutBrainIE
Information extraction around the gut-brain domain, including entity/relation-oriented biomedical extraction.

- https://participants-area.bioasq.org/
- `task:information-extraction` `task:relation-extraction`

### MultiClinSum-2
Multilingual / multi-document clinical summarization challenge family.

- https://participants-area.bioasq.org/
- `task:clinical-summarization`

## Important historical BioASQ task families

### DisTEMIST
Disease mention recognition and terminology normalization.

- `task:ner` `task:normalization` `entity:disease`

### MedProcNER
Medical-procedure NER, SNOMED CT normalization and document indexing.

- `task:ner` `task:normalization` `terminology:snomed-ct`

### MultiCardioNER
Multilingual clinical entity recognition in cardiology, including entities such as diseases, symptoms, procedures and medications.

- `task:clinical-ner` `domain:cardiology`

### BioNNE
Nested biomedical NER.

- `task:nested-ner`

### MESINESP
Biomedical semantic indexing in Spanish.

- `task:semantic-indexing` `language:spanish`

## Access strategy

- Registration is typically required for full challenge participation/data.
- Sample data for some tasks is available without registration through the participant area.
- Dataset terms vary by task and year.
- Cite the specific challenge edition and task when publishing results.

## Recommended use

BioASQ is especially useful when evaluating a pipeline beyond isolated NER:

1. NER / normalization
2. relation or information extraction
3. semantic indexing / retrieval
4. evidence grounding
5. biomedical QA / summarization

That makes BioASQ complementary to static corpora such as NCBI Disease, BC5CDR and BioRED.
