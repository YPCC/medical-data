# Medical LLM Benchmarks

[Open Medical LLM Datasets](https://github.com/Nilzkool/open-medllm-datasets) provides a practical capability-oriented map of openly available benchmarks for evaluating generative AI and large language models in healthcare and biomedicine. This page indexes that catalog inside the medical-data structure so that medical LLM evaluation resources sit alongside classic shared-task ecosystems such as BioASQ and n2c2.

The source organizes ~57 publicly downloadable datasets (no credential wall required for access) across evaluation capabilities including medical knowledge, clinical reasoning, safety, documentation, multimodal reasoning, agentic EHR workflows, and health-equity assessment. Primary (`[P]`) versus secondary (`[S]`) targets are marked in the original catalog.

> **Source of truth:** https://github.com/Nilzkool/open-medllm-datasets  
> Always prefer the upstream README for the most complete link set, code pointers, and any updates.

## Why it belongs in this repository

Classic biomedical shared tasks (BioASQ, n2c2/i2b2, TREC) remain essential for information extraction, retrieval, and clinical-note NLP. Modern medical LLM evaluation additionally requires capability-specific suites that probe:

- knowledge application under examination-style questions,
- diagnostic and management reasoning,
- safety, abstention, and hallucination resistance,
- multi-turn communication and documentation,
- long-context / longitudinal memory,
- tool-using agentic workflows over EHR-like resources,
- multimodal (image + text) reasoning,
- fairness and multilingual robustness.

These resources complement rather than replace BioASQ-style pipelines.

## Capability map (primary resources)

### Medical knowledge and question answering

Evaluates biomedical knowledge applied to examinations, clinical vignettes, public-health questions, and specialty-specific items.

- **MedQA** — USMLE-style multiple-choice questions. [Paper](https://arxiv.org/abs/2009.13081) · [Data/code](https://github.com/jind11/MedQA)
- **MedMCQA** — Medical entrance-examination questions across 21 subjects. [Paper](https://proceedings.mlr.press/v174/pal22a.html) · [Data](https://huggingface.co/datasets/openlifescienceai/medmcqa) · [Code](https://github.com/medmcqa/medmcqa)
- **CareQA** — Healthcare examination questions (multiple-choice). [Data](https://huggingface.co/datasets/HPAI-BSC/CareQA)
- **HEAD-QA v2** — English subset of Spanish healthcare professional examination questions. [Paper](https://aclanthology.org/P19-1092/) · [Data](https://huggingface.co/datasets/alesi12/head_qa_v2)
- **Medbullets** — USMLE Step 2/3-style clinical questions. [Paper](https://arxiv.org/abs/2402.18060) · [Data](https://huggingface.co/datasets/mkieffer/Medbullets)
- **MedXpertQA** — Expert-level questions across 17 specialties. [Data](https://huggingface.co/datasets/TsinghuaC3I/MedXpertQA)
- **MMLU-Pro-Health** — Health subset of MMLU-Pro. [Paper](https://arxiv.org/abs/2406.01574) · [Data](https://huggingface.co/datasets/TIGER-Lab/MMLU-Pro)
- **SuperGPQA-Med** — Graduate-level questions across medical fields. [Paper](https://arxiv.org/abs/2502.14739) · [Data](https://huggingface.co/datasets/m-a-p/SuperGPQA)
- **MedExQA** — Questions with expert explanations in underrepresented specialties. [Paper](https://arxiv.org/abs/2406.06331) · [Data](https://huggingface.co/datasets/bluesky333/MedExQA)
- **PubHealthBench** — Questions derived from UK public-health guidance. [Paper](https://arxiv.org/abs/2505.06046) · [Data](https://huggingface.co/datasets/Joshua-Harris/PubHealthBench)

`task:medical-qa` `task:knowledge` `access:open`

### Diagnostic and clinical reasoning

Evaluates diagnosis, differential diagnosis, integration of findings, and the quality of the reasoning chain itself.

- **MedR-Bench** — Structured cases with reference reasoning for examination, diagnosis, assessment, and treatment. [Paper](https://www.nature.com/articles/s41467-025-64769-1) · [Data/code](https://github.com/MAGIC-AI4Med/MedRBench)
- **MedCaseReasoning** — Clinical cases paired with diagnoses and clinician-authored reasoning traces. [Paper](https://arxiv.org/abs/2505.11733) · [Data](https://huggingface.co/datasets/zou-lab/MedCaseReasoning)
- **CareQA Open** — Open-ended clinical questions requiring answers plus supporting reasoning. [Data](https://huggingface.co/datasets/HPAI-BSC/CareQA)
- **M-ARC** — Long-tail medical questions testing flexible clinical reasoning. [Paper](https://arxiv.org/abs/2502.04381) · [Data](https://huggingface.co/datasets/mkieffer/M-ARC)
- **AgentClinic** (also agentic) — Simulated clinical encounters with patients and tools. [Paper](https://arxiv.org/abs/2405.07960) · [Data/code](https://github.com/samuelschmidgall/agentclinic)

`task:clinical-reasoning` `task:diagnosis` `access:open`

### Clinical management, treatment planning, and judgment under uncertainty

Evaluates investigations, treatments, medication decisions, monitoring, completeness of plans, and appropriate updating or abstention under incomplete information.

- **First Do NOHARM v2 (open subset)** — Generates management plans and measures appropriate actions, omissions, and harmful actions. [Paper](https://arxiv.org/abs/2512.01241) · [Data](https://github.com/ARISENetwork/mast/tree/main/benchmarks/donoharm/dataset) · [Code](https://github.com/ARISENetwork/mast/tree/main/benchmarks/donoharm)
- **SCT-Public** — Script concordance testing: how new information changes diagnostic or therapeutic hypotheses. [Paper](https://ai.nejm.org/doi/full/10.1056/AIdbp2500120) · [Data](https://github.com/ARISENetwork/mast/tree/main/benchmarks/sct/dataset)
- **MetaMedQA** — Recognition of unanswerable or uncertainty-oriented medical questions. [Data](https://huggingface.co/datasets/maximegmd/MetaMedQA)
- **Med-HALT** — False confidence, hallucinated reasoning, and recognition that no listed answer is valid. [Paper](https://arxiv.org/abs/2307.15343) · [Data/code](https://github.com/medhalt/medhalt)
- **HealthBench / HealthBench Professional** — Realistic multi-turn healthcare conversations with physician rubrics (also covers communication and safety). [Paper](https://arxiv.org/abs/2505.08775) · [Data](https://huggingface.co/datasets/openai/healthbench) · [Professional](https://huggingface.co/datasets/openai/healthbench-professional)

`task:treatment-planning` `task:uncertainty` `task:abstention` `access:open`

### Clinical safety, harmfulness, hallucination, and error correction

Evaluates harmful recommendations, critical omissions, unsafe advice, misinformation, overconfidence, bias, and the ability to detect or correct clinical errors.

- **PatientSafetyBench** — Patient-facing cases covering unsafe advice, misinformation, overconfidence, bias, and escalation failures. [Paper](https://arxiv.org/abs/2507.07248) · [Data](https://huggingface.co/datasets/microsoft/PatientSafetyBench)
- **MedSafetyBench** — Responses to harmful or malicious medical instructions. [Paper](https://arxiv.org/abs/2403.03744) · [Data/code](https://github.com/AI4LIFE-GROUP/med-safety-bench)
- **MedHallu** — Correct versus plausible hallucinated answers across medical error categories. [Paper](https://arxiv.org/abs/2502.14302) · [Data](https://huggingface.co/datasets/UTAustin-AIHealth/MedHallu)
- **MEDEC** — Detection, localisation, extraction, and correction of errors in synthetic clinical notes. [Paper](https://aclanthology.org/2025.findings-acl.1159/) · [Data](https://github.com/abachaa/MEDEC)
- **Med-MMHL** — Multimodal medical misinformation and hallucination (images + claims). [Paper](https://arxiv.org/abs/2306.08871) · [Data/code](https://github.com/styxsys0927/Med-MMHL)

`task:safety` `task:hallucination` `task:error-correction` `access:open`

### Patient / clinician communication and clinical documentation

Evaluates audience-appropriate communication, empathy, clarification, uncertainty expression, note generation, and summarisation.

- **HealthBench** (see above) — Multi-turn healthcare conversations with physician-written rubrics.
- **MedicationQA** — Consumer medication questions paired with expert answers. [Data/code](https://github.com/abachaa/Medication_QA_MedInfo2019)
- **MedQuAD** — Consumer medical question–answer pairs from trusted sources. [Data/code](https://github.com/abachaa/MedQuAD)
- **ACI-Bench** — Doctor–patient conversations converted into structured clinical notes. [Paper](https://www.nature.com/articles/s41597-023-02487-3) · [Data](https://figshare.com/articles/dataset/aci-bench-corpus_zip/22494601)
- **MedDialog** — Summarisation of doctor–patient conversations. [Paper](https://arxiv.org/abs/2004.03329) · [Data](https://github.com/UCSD-AI4H/Medical-Dialogue-System)
- **MTSamples Procedures / Replicate** — Procedural summaries and plan reconstruction from operative notes. See source catalog for links.

`task:communication` `task:summarization` `task:documentation` `access:open`

### Longitudinal, temporal, memory-based, and agentic EHR workflows

Evaluates retrieval across encounters, temporal ordering, state tracking, long-context reasoning, tool use, FHIR-style actions, and multi-step clinical workflows.

- **LongHealth** — Synthetic longitudinal patient records with retrieval, temporal, missing-information, and distractor tasks. [Paper](https://arxiv.org/abs/2401.14490) · [Data/code](https://github.com/kbressem/LongHealth)
- **MedOdyssey** — Medical long-context evaluation across very large context lengths. [Paper](https://aclanthology.org/2025.findings-naacl.3/) · [Data/code](https://github.com/JOHNNY-fans/MedOdyssey)
- **MedMemoryBench** — Multi-session synthetic patient trajectories testing fact recall, temporal localisation, and multi-hop reasoning (English/Chinese). [Paper](https://arxiv.org/abs/2605.11814) · [Data](https://huggingface.co/datasets/Cyan27/MedMemoryBench)
- **MedAgentBench v2** — FHIR-based EHR tasks involving retrieval, calculations, and clinical actions. [Paper](https://psb.stanford.edu/psb-online/proceedings/psb26/chen_eric.pdf) · [Data/code](https://github.com/ARISENetwork/medagentbenchv2)
- **PhysicianBench** — Long-horizon physician workflows with cross-encounter retrieval and documentation. [Paper](https://arxiv.org/abs/2605.02240) · [Code](https://github.com/HealthRex/PhysicianBench)
- **FHIR-AgentBench** — Clinical questions solved via API retrieval, specialised tools, and code execution. [Paper](https://proceedings.mlr.press/v297/lee26a.html) · [Data/code](https://github.com/glee4810/FHIR-AgentBench)
- **AgentClinic** (see above).

`task:agentic` `task:longitudinal` `task:ehr-workflow` `access:open`

### Multimodal medical reasoning

Evaluates joint reasoning over medical images and text (VQA, diagnosis, image-grounded communication).

- **PMC-VQA** — Visual question answering over biomedical figures from PubMed Central. [Paper](https://arxiv.org/abs/2305.10415) · [Data](https://huggingface.co/datasets/xmcmic/PMC-VQA)
- **PathVQA** — Visual questions based on pathology images. [Paper](https://arxiv.org/abs/2003.10286) · [Data/code](https://github.com/KaveeshaSilva/PathVQA)
- **VQA-RAD** — Clinician-authored questions grounded in radiology images. [Paper](https://www.nature.com/articles/sdata2018251) · [Data](https://osf.io/89kps/)
- **SLAKE** — English–Chinese medical VQA with semantic labels. [Paper](https://arxiv.org/abs/2102.09542) · [Data](https://www.med-vqa.com/slake/)
- **DDI / MIDAS** — Dermatology image benchmarks useful for fairness and multimodal diagnostic evaluation. See source for links.

`task:multimodal` `task:vqa` `modality:imaging` `access:open`

### Medical calculations, coding, terminology, and biomedical evidence

- **MedCalc-Bench** — Clinical calculation questions (formula selection, variable extraction, numerical execution). [Paper](https://arxiv.org/abs/2406.12036) · [Data](https://huggingface.co/datasets/nsk7153/MedCalc-Bench-Verified)
- **MedConceptsQA** — Questions involving ICD-9/10 and related coding hierarchies. [Paper](https://www.sciencedirect.com/science/article/pii/S0010482524011740) · [Data](https://huggingface.co/datasets/ofir408/MedConceptsQA)
- **PubMedQA** — Yes/no/uncertain answers grounded in biomedical abstracts. [Paper](https://aclanthology.org/D19-1259/) · [Data/code](https://github.com/pubmedqa/pubmedqa)
- **EvidenceBench / EvidenceBench-100k** — Extraction of evidence that supports or refutes biomedical hypotheses. [Paper](https://arxiv.org/abs/2504.18736) · [Data/code](https://github.com/EvidenceBench/EvidenceBench)

`task:calculation` `task:coding` `task:evidence` `access:open`

### Fairness, bias, health equity, and multilingual performance

- **EquityMedQA** — Adversarial datasets designed to surface health-equity harms. [Paper](https://www.nature.com/articles/s41591-024-03258-2) · [Data](https://doi.org/10.6084/m9.figshare.26133973)
- **AMQA** — Adversarial medical question pairs varying race, gender, and socioeconomic characteristics. [Paper](https://arxiv.org/abs/2505.19562) · [Data](https://huggingface.co/datasets/Showing-KCL/AMQA)
- **MMedBench** — Medical questions with rationales across English, Chinese, Japanese, French, Russian, and Spanish. [Paper](https://www.nature.com/articles/s41467-024-52417-z) · [Data](https://huggingface.co/datasets/aisc-team-c1/MMedBench)
- **RuMedBench** — Russian-language medical classification, QA, inference, and NER. [Paper](https://arxiv.org/abs/2201.06499) · [Data/code](https://github.com/sb-ai-lab/MedBench)

`task:fairness` `task:equity` `task:multilingual` `access:open`

## Access strategy

- The datasets highlighted here were selected because they are openly downloadable without a credential wall.
- Individual licenses and terms still vary; always verify before commercial use or redistribution.
- This catalog page is an index only. Do not upload third-party dataset files into the medical-data repository.
- For controlled clinical-note corpora, continue to use the DUA-aware pages (n2c2/i2b2, MIMIC, etc.).

## Recommended use

1. Start with knowledge/QA suites (MedQA, MedMCQA, PubMedQA) for baseline medical knowledge.
2. Add reasoning and management suites (MedR-Bench, First Do NOHARM, SCT) when evaluating clinical decision quality.
3. Include safety, hallucination, and equity benchmarks before any patient-facing deployment claims.
4. Use agentic and longitudinal suites (MedAgentBench, LongHealth, PhysicianBench) for tool-using or multi-encounter systems.
5. Cross-check classic information-extraction and retrieval performance on BioASQ / n2c2 where relevant.

## Related pages in this repository

- [BioASQ](bioasq.md) — biomedical QA, retrieval, semantic indexing, and IE challenge families
- [Evaluation & Agentic Benchmarks](evaluation-agentic.md) — acuity scores, standard ML metrics, and general (non-medical) agentic suites
- [n2c2 / i2b2](n2c2-i2b2.md) — clinical NLP over de-identified notes (DUA)
- [Biomedical NLP](../datasets/biomedical-nlp/README.md) — NER, normalization, relation extraction, and KG stages

---

*This page is maintained as a structured index. Capability definitions and the full primary/secondary tagging live in the upstream [open-medllm-datasets](https://github.com/Nilzkool/open-medllm-datasets) repository.*
