# Patient Acuity, ML Evaluation & Agentic-AI Benchmarks

This material was previously embedded inside the EHR section. It is retained here as an **evaluation resource**, not a dataset category.

## Patient acuity / early warning scores

- NEWS / NEWS2
- MEWS
- qSOFA / SOFA
- APACHE II / III / IV
- SAPS
- Patient Acuity Rating (PAR)
- HAVEN
- Acute Care for Elders (ACE) risk models
- COVID acuity scores
- Nursing acuity scales

These scores have different intended populations, inputs and validation contexts. Do not treat them as interchangeable labels without clinical validation.

## Standard ML / clinical-AI evaluation metrics

- Classification: accuracy, precision, recall, F1, sensitivity, specificity, PPV, NPV
- Discrimination: AUROC, AUPRC
- Calibration: Brier score, calibration error / reliability
- NER: exact/relaxed entity-level precision, recall and F1
- Relation extraction: relation-level precision/recall/F1
- Linking/ranking: MRR, Hits@K, top-k accuracy
- Agreement: Cohen's kappa / inter-annotator agreement

## General agentic-AI benchmark families

These are **not medical datasets by default**, but can be useful for evaluating general agent capabilities before domain-specific clinical validation:

- AgentBench
- τ-bench / τ²-bench
- BrowseComp
- SWE-bench Verified
- MultiAgentBench
- Agent-SafetyBench
- WebArena
- GAIA
- AppWorld

Keep medical/clinical safety evaluation separate from generic agent success metrics.
