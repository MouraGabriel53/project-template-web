# Development

## Stack

<!-- Framework and version, language, package manager, main libraries. -->

## Commands

```bash
# install dependencies
# run locally
# lint
# type check
# unit tests
# all tests (lint, type check, tests, build)
# production build
```

## Continuous integration

<!-- One row per workflow job. -->

| Workflow | What it does |
|---|---|
| `.github/workflows/conventions.yml` | fails if the pull request title or any of its commits does not follow Conventional Commits |

Dependabot (`.github/dependabot.yml`) opens weekly pull requests for dependency updates.

## Commit and pull request conventions

Commit messages and pull request titles follow
[Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<optional scope>): <description>
```

Types: `feat`, `fix`, `refactor`, `test`, `docs`, `chore`, `build` (build
system and dependencies) and `ci` (CI workflows). Add `!` before `:` for a
breaking change. Use the feature name as the scope when the change belongs to
one feature.

Run once after cloning to check messages locally and get the message template
in the editor:

```bash
git config core.hooksPath .githooks       # rejects commits outside the convention
git config commit.template .gitmessage    # opens the template on `git commit`
```

New pull requests are filled with `.github/pull_request_template.md`.

## Documentation

- Change [architecture.md](architecture.md) and [contracts.md](contracts.md)
  in the same pull request as the code they describe.
- Plan large changes as a spec in [specs/](specs/README.md) before coding.
- Record non-obvious choices in [decisions/](decisions/README.md).
