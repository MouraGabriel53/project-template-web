# <Project name>

<!-- One or two sentences: what the product is and who it is for. -->

## Stack

<!-- Language and version, build tool, framework. -->

## Commands

- Build:
- Unit tests:
- Full test:
- Run locally:

## Constraints

<!-- Project-specific rules only. General rules live in ~/.claude/CLAUDE.md. -->

## Documentation

- `docs/` is in Portuguese (pt-BR); start from [docs/README.md](docs/README.md).
- Each domain context has `docs/<context>/000_<context>_context.md` and one
  spec per operation, `NNN_<operation>.md`, created from `docs/_templates/` (which also has the decision model).
- Read the spec and `docs/architecture.md` before changing structure or
  interfaces, and update them in the same change as the code.
- When the code starts or stops reading an environment variable, update
  `.env.example` and the "Configure" table in `README.md` in the same change.
