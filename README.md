# human-assisted-software-development
A methodology for software development in an age where AI has taken the driver's seat, and humans have become the tour guides

## Layout

```
Agents/
  Knowledge/               the catalogue of knowledge files kept in .dev/ folders (vision, backlog,
                           plans, decisions, requirements, delivery, operation and the rest): a schema
                           and a fictional example per kind, and validate_knowledge.py
  Skills/                  agent skills: the diagrams and behavior views kept in .dev/ folders, with
                           their schemas, examples and validate_diagrams.py; describe-knowledge for
                           the knowledge files; and populate-dev, which decides what a folder needs
```

Each directory has its own `README.md` saying what is in it and how to use it.

The page that shows a repository's `.dev/` folders, [Cyberspace explorer](https://github.com/david-brandt-the-icelander/cyberspace-explorer), lives in its own repository, at <https://icelander.net/v1/apps/cyberspace-explorer>.
