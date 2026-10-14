# project-template-web

Shared conventions for new web apps: Conventional Commits checked locally and
in CI, a pull request template, and a `docs/` structure for architecture,
contracts, specs and decisions.

The code is organized by feature (package-by-feature). The template does not
pick a framework: build tooling, routing and the folder for framework entry
points are added when the project is created.

## What is included

| Path | Purpose |
| --- | --- |
| `.githooks/commit-msg` | Rejects commits that do not follow Conventional Commits |
| `.gitmessage` | Commit message template opened by `git commit` |
| `.github/pull_request_template.md` | Default pull request description |
| `.github/workflows/conventions.yml` | Checks the PR title and every commit of the PR, using the reusable workflow from `MouraGabriel53/project-template` |
| `.github/dependabot.yml` | Weekly updates for GitHub Actions; add `npm` once `package.json` exists |
| `docs/` | `architecture.md`, `contracts.md`, `development.md`, `specs/`, `decisions/` |
| `CLAUDE.md` | Project-specific instructions for Claude Code |

## New project

```bash
gh repo create <name> --private --template MouraGabriel53/project-template-web --clone
cd <name>
git config core.hooksPath .githooks
git config commit.template .gitmessage
```

Then scaffold the framework in the repository, and fill in `README.md`,
`CLAUDE.md` and `docs/`.

## Commit rules

The allowed types live in `MouraGabriel53/project-template`: the CI check
calls its reusable workflow, so changing them there changes them here too.
The local hook (`.githooks/commit-msg`) is a copy; update it when the rules
change.
