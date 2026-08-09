# Contributing

Contributions are welcome.

## Add a dataset in the right place

Prefer **task/modality-oriented organization** over adding new top-level sections for every source website.

A dataset entry should ideally include:

```markdown
### Dataset name
One- or two-sentence description.

- Source: https://...
- Paper: https://...   # when available
- `task:ner` `modality:clinical-text` `access:dua`
```

## Suggested metadata tags

- Task: `task:ner`, `task:entity-linking`, `task:relation-extraction`, `task:segmentation`, `task:qa`
- Modality: `modality:clinical-text`, `modality:imaging`, `modality:ehr`, `modality:speech`
- Domain: `domain:oncology`, `domain:cardiology`, etc.
- Terminology: `terminology:umls`, `terminology:snomed-ct`, `terminology:rxnorm`, `terminology:mesh`
- Access: `access:open`, `access:registration`, `access:dua`, `access:request`, `access:restricted`

## Access and licensing

Do not upload third-party datasets to this repository unless redistribution is explicitly permitted.

For controlled clinical datasets:
1. Link to the authoritative access portal.
2. State the access requirement.
3. Do not copy samples that could violate the DUA or license.

## Maintenance

Prefer canonical HTTPS URLs. If preserving a historical URL, label it **Historical access** and, where known, add the current canonical portal.
