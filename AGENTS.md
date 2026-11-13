# Agent instructions

This repository is human-assisted software development (HASD): the agent skills and the knowledge catalogue that other repositories copy. See [README.md](README.md) for the layout.

## Architecture diagrams and knowledge files

Each maintained folder documents itself in a `.dev/` directory next to its content, as JSON following the skills in `Agents/Skills/` and the knowledge catalogue in `Agents/Knowledge/`. Read a folder's `.dev` files before changing it. `populate-dev` decides what a folder needs; the diagrams are:

- `describe-component-diagram`: the folder is a cohesive capability, adapter, boundary or subsystem (the repository root and `Agents/`).
- `describe-class-diagram`: the folder itself declares more than one class. None does: the validators are functions.
- `describe-state-diagram`: the folder implements a state machine. None does.
- `describe-deployment-diagram`: the folder holds something independently deployable. Nothing here is deployed; other repositories copy `Agents/Skills` and `Agents/Knowledge`.

What a folder does, offers and exposes goes in its use cases, user journeys, capabilities, features and operations (`describe-use-case`, `describe-user-journey`, `describe-capability`, `describe-feature`, `describe-operation`): here, the two validators, in `Agents/.dev/`. What it intends, promises and needs (backlog items, decisions, verification and the rest) goes in knowledge files, written with `describe-knowledge`. Wanted work is a `backlog` item in the folder that will own it, and a question only the owner can answer is a `decisions` record with `status: open`.

Every actor a use case, journey or diagram names has a file in `Actors/` at the repository root, written with `describe-actor` and linked from whatever names it; delete an actor nothing links to. Update the `.dev` files and actors in the same commit as what they describe, and delete one that stops applying.

The skills and the catalogue in `Agents/Skills` and `Agents/Knowledge` are the originals. Other repositories copy them unchanged to `Meta/Agents/Skills` and `Meta/Agents/Knowledge`, so change them here, never in a copy, and do not add a `Meta/Agents` copy to this repository. Do not put a `.dev` folder inside `Agents/Skills` or `Agents/Knowledge`: it would be copied with them and fail the validators there. What is recorded about them is in `Agents/.dev/`, pending the open decision in `Agents/.dev/decisions.json`. Every `example.json`, `example.md` and file in `Agents/Knowledge/examples/` is fictional; never document it as part of this repository.

The skills name `Meta/Agents/...` paths, which are where they live in other repositories. Here they are under `Agents/`. Before finishing, run both validators from the repository root, with the `jsonschema` package installed. Pass the root to `validate_diagrams.py`: without it, the script checks the folder above this repository (see `Agents/.dev/backlog.json`).

```bash
python3 Agents/Skills/validate_diagrams.py .
python3 Agents/Knowledge/validate_knowledge.py
```
