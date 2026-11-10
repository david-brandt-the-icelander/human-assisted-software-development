# human-assisted-software-development
A methodology for software development in an age where AI has taken the driver's seat, and humans have become the tour guides

## Layout

```
Actors/                    the people who use the software system browser, one file each, linked from its
                           use cases and journeys
Agents/
  Knowledge/               the catalogue of knowledge files kept in .dev/ folders (vision, backlog,
                           plans, decisions, requirements, delivery, operation and the rest): a schema
                           and a fictional example per kind, and validate_knowledge.py
  Skills/                  agent skills: the diagrams and behavior views kept in .dev/ folders, with
                           their schemas, examples and validate_diagrams.py; describe-knowledge for
                           the knowledge files; and populate-dev, which decides what a folder needs
software-system-browser/   a static page that draws a repository's .dev/ diagrams and shows its use
                           cases, journeys, capabilities, features, operations and knowledge files,
                           live at https://icelander.net/v1/apps/architecture-browser; its own .dev/ folder
                           describes it
```

Each directory has its own `README.md` saying what is in it and how to use it.
