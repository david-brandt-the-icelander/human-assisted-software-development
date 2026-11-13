# Coding agent

**Kind:** agent
**Evidence:** `Agents/Skills/README.md` (`Agent skills`: skills that tell an agent how to do one job in a repository, in a format Claude Code and Codex read), the front matter (`name`, `description`) of each `Agents/Skills/*/skill.md`, `Agents/Skills/populate-dev/skill.md` (`Checking`: run both validators and fix what they report), `AGENTS.md` (`Architecture diagrams and knowledge files`)

## What they want from the system

- To know that the views, knowledge files and actor files it wrote are well-formed, or which file to fix: [Check a repository's .dev folders](../Agents/.dev/use-case.json), `check-dev-folders`.

## How they reach it

A checkout of the repository: the `skill.md` files it reads, matching a task against each skill's `description`, and the two validators it runs with Python and the `jsonschema` package. In a repository that has adopted HASD, the same files under `Meta/Agents/`.

Nothing here tells an agent from a person: anyone with a checkout can read the skills and run the validators. The skills and `AGENTS.md` are written to agents.
