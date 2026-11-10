---
name: describe-capability
description: Create or maintain .dev capability.json files when documenting or changing what a folder can do and who may ask for it.
---

# Capabilities

Describe in `<folder>/.dev/capability.json` what the folder can do, as a noun phrase per entity (`name`), with the `responsibility` in a sentence, who may use it (`access`, one line per rule, as the code enforces it) and the `operations` through which it is reached, as source and symbol. A capability is something the code does for someone, not a module: do not make one per class or namespace, and leave out what the code does not enforce or do. Link the features that make it up, the operations that expose it and the use cases that use it with `relatedViews`.

Read the code and existing views first; write following [schema.json](schema.json), and use [example.json](example.json) as a fictional example, not as evidence about this system. `$schema` is the relative path from the file to the schema; other paths are relative to the repository root. No secrets or runtime values. Run `python3 Meta/Agents/Skills/validate_diagrams.py`. Update the view in the same commit as the code and delete it when it stops applying.
