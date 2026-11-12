# human-assisted-software-development
A methodology for software development in an age where AI has taken the driver's seat, and humans have become the tour guides

## Layout

```
.dev/                      what this repository records about itself, as the skills below describe
Actors/                    the actors its .dev files name, one file each
AGENTS.md                  instructions for agents working in this repository
Agents/
  Knowledge/               the catalogue of knowledge files kept in .dev/ folders (vision, backlog,
                           plans, decisions, requirements, delivery, operation and the rest): a schema
                           and a fictional example per kind, and validate_knowledge.py
  Skills/                  agent skills: the diagrams and behavior views kept in .dev/ folders, with
                           their schemas, examples and validate_diagrams.py; describe-knowledge for
                           the knowledge files; and populate-dev, which decides what a folder needs
  .dev/                    the validators' views, and the records about Skills/ and Knowledge/, which
                           hold no .dev folder of their own because other repositories copy them whole
```

[`Agents/Skills/`](Agents/Skills/README.md) and [`Agents/Knowledge/`](Agents/Knowledge/README.md) each have a `README.md` saying what is in them and how to use them.

The page that shows a repository's `.dev/` folders, [Cyberspace explorer](https://github.com/david-brandt-the-icelander/cyberspace-explorer), lives in its own repository, at <https://icelander.net/v1/apps/cyberspace-explorer>.
