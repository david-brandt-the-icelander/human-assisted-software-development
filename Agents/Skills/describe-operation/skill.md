---
name: describe-operation
description: Create or maintain .dev operation.json files when documenting or changing a folder's callable entrypoints: routes, commands, handlers and messages.
---

# Operations

Describe in `<folder>/.dev/operation.json` the entrypoints a caller can invoke: one entity per route, command, message handler or exported function that is part of the folder's contract. Each has an `action` (the verb or method, such as `GET`, `POST`, `command`, `message`), the `entrypoint` as source and symbol, the `authorization` the code checks, the `result` and the `failures`, each a condition and what the caller sees. Read authorization and failures from the code, not from convention: if nothing checks, say so. Leave out internal helpers. Link the capability that offers each operation and the use cases that call it with `relatedViews`.

Read the code and existing views first; write following [schema.json](schema.json), and use [example.json](example.json) as a fictional example, not as evidence about this system. `$schema` is the relative path from the file to the schema; other paths are relative to the repository root. No secrets, tokens or example credentials. Run `python3 Meta/Agents/Skills/validate_diagrams.py`. Update the view in the same commit as the code and delete it when it stops applying.
