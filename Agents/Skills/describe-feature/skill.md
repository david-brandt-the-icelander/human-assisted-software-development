---
name: describe-feature
description: Create or maintain .dev feature.json files when documenting or changing the behavior a folder offers, its outcome and its limits.
---

# Features

Describe in `<folder>/.dev/feature.json` the behavior the folder offers: one entity per feature, with the `behavior` in the present tense, the `outcome` for the person or system that uses it, the `constraints` that limit it (quotas, ordering, retries, who is excluded) and where it is `implementation`, as source and symbol. State only what the code does today; a planned feature belongs in the knowledge documents with its mark, not here. Link the capability it belongs to, the operations it calls and the use cases that exercise it with `relatedViews`.

Read the code and existing views first; write following [schema.json](schema.json), and use [example.json](example.json) as a fictional example, not as evidence about this system. `$schema` is the relative path from the file to the schema; other paths are relative to the repository root. No secrets or runtime values. Run `python3 Meta/Agents/Skills/validate_diagrams.py`. Update the view in the same commit as the code and delete it when it stops applying.
