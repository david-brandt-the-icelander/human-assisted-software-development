---
name: describe-use-case
description: Create or maintain .dev use-case.json files when documenting or changing what an actor does, step by step, with a system or folder.
---

# Use cases

Describe one folder's use cases in `<folder>/.dev/use-case.json`: one entity per goal an actor pursues through code in that folder. Each has the actor, the goal, preconditions and postconditions, a `flow` of steps in order, and `alternatives`, each branching off a step with the condition and the outcome. A step names who acts (`participantKind` is `actor` for a person or outside system, `system` for the folder's own code), what they do, and the sources it was read from. Alternatives are only the branches the code has: errors, rejections, early exits. Do not invent a step to complete an expected story, and do not write steps for code that is not in this folder; link to the view that has them in `relatedViews`.

Set `actorDocument` (on the use case and on a step by an actor) to the actor's `Actors/<name>.md`, written with the `describe-actor` skill. Link the operations the steps call, the capability and the features they serve with `relatedViews`, each with the folder, the path of the other view's file and why it is related.

Read the code and existing views first; write following [schema.json](schema.json), and use [example.json](example.json) as a fictional example, not as evidence about this system. `$schema` is the relative path from the file to the schema; every other path is relative to the repository root. Record source paths and symbols enough to verify each step. No secrets or runtime values. Run `python3 Meta/Agents/Skills/validate_diagrams.py`; it checks the schema, unique IDs, that each alternative's `atStep` is a step, and that sources and related views exist. Update the view in the same commit as the code and delete it when it stops applying.
