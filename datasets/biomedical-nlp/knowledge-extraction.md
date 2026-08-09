# Biomedical Knowledge Extraction, Relation Extraction & Knowledge Graphs

This page covers **relation extraction, triple generation, KG population, completion, reasoning, RDF/SPARQL evaluation and biomedical knowledge graphs**.

## Relation / triple extraction datasets

### BioRED
Document-level biomedical relation-extraction corpus spanning genes/proteins, diseases, chemicals, variants, species and cell lines, with entity normalization and relation/novelty annotations.

- NCBI project: https://ftp.ncbi.nlm.nih.gov/pub/lu/BC8-BioRED-track/
- BioCreative VIII used an expanded BioRED track.
- `task:ner` `task:normalization` `task:relation-extraction` `task:triple-extraction`

### ChemProt
PubMed abstracts annotated for chemical–protein interactions.

- BioCreative: https://biocreative.bioinformatics.udel.edu/
- `task:relation-extraction` `entity:chemical` `entity:protein`

### DDI Corpus
DrugBank/MedLine text annotated for drug–drug interactions.

- `task:relation-extraction` `entity:drug`

### ADE Corpus
Case-report text annotated for drug–adverse-event relations.

- `task:relation-extraction` `entity:drug` `entity:ade`

### GIT / biomedical triple extraction datasets
General biomedical relation/triple extraction resources retained from the previous catalog; verify the specific source/version before benchmarking.

## Integrated biomedical knowledge graphs

### PrimeKG
Precision-medicine KG integrating multiple biomedical sources and disease-centric relations.

- https://github.com/mims-harvard/PrimeKG
- `task:kg-completion` `domain:precision-medicine`

### Hetionet
Heterogeneous biomedical network widely used for drug-repurposing experiments.

- https://het.io/
- `task:link-prediction` `domain:drug-repurposing`

### BioKG / DRKG / OREGANO / PharMeBINet / Know2BIO
Large integrated biomedical KGs covering drugs, proteins, diseases, pathways and related entities. Evaluate provenance, licensing, release date and mapping quality independently for each KG.

### Clinical Trials Knowledge Graph
Knowledge-graph constructions combining ClinicalTrials.gov and biomedical terminologies/resources can support trial search and semantic analytics.

## RDF / semantic-web benchmarks

### RDF Reification Benchmark using BKR
Biomedical Knowledge Repository variants for comparing classic RDF reification, Singleton Property and RDF-star/Turtle* approaches.

- Zenodo: https://zenodo.org/records/4148888
- `task:rdf-modeling` `task:sparql`

### LargeRDFBench
Federated SPARQL benchmark with interconnected datasets including life-science/biomedical sources.

- https://github.com/dice-group/LargeRDFBench
- `task:sparql-federation`

### kgbench
RDF-encoded knowledge graphs for node classification and multimodal/relational evaluation.

- https://github.com/pbloem/kgbench
- `task:node-classification`

## Useful KG evaluation tasks

- text → entity → normalized entity → relation → triple
- knowledge graph construction/population
- link prediction / graph completion
- relation classification
- novelty/evidence classification
- ontology alignment
- SHACL/constraint validation
- provenance and statement-level metadata
- RDF-star/reification modeling
- SPARQL query correctness/performance
- temporal KG reasoning
- KGQA / graph-grounded RAG
- multi-model consensus validation of extracted assertions
