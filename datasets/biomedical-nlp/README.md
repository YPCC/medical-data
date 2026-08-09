# Biomedical & Clinical NLP

This section separates the major information-extraction stages that were previously mixed into the EHR section.

| Stage | Page | Typical output |
|---|---|---|
| Named Entity Recognition | [NER](named-entity-recognition.md) | text spans + entity type |
| Entity Linking / Normalization | [Normalization](entity-linking-normalization.md) | span → UMLS/SNOMED/MeSH/RxNorm/etc. |
| Relation / Triple Extraction | [Knowledge Extraction](knowledge-extraction.md) | entity-relation-entity assertions |
| Knowledge Graph Evaluation | [Knowledge Extraction](knowledge-extraction.md) | RDF/KG completion, reasoning, SPARQL |
| QA / Retrieval / Summarization | [BioASQ](../../benchmarks/bioasq.md) | evidence, concepts, answers, summaries |

## Clinical vs biomedical NLP

**Clinical NLP** typically operates on EHR notes, discharge summaries, radiology reports and other patient-care documentation. Access is frequently credentialed because even deidentified corpora are governed by DUAs.

**Biomedical NLP** typically operates on scientific literature such as PubMed abstracts or PMC articles. Many corpora are openly downloadable, although their licenses still vary.

## Recommended benchmark progression

1. Start with an open biomedical corpus such as NCBI Disease, BC5CDR or MedMentions.
2. Add normalization/entity linking if terminology grounding is required.
3. Add relation extraction using BioRED, ChemProt, DDI or ADE.
4. Move to clinical-note benchmarks such as n2c2/i2b2 only when DUA controls can be satisfied.
5. For end-to-end retrieval/QA and information-extraction challenge ecosystems, evaluate against BioASQ/BioCreative tasks.
