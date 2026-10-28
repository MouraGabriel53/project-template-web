# <Project name>

**<Tagline: the promise of the project in one short line.>**

<What it is and the problem it solves, in one or two sentences.> Built for
<who uses it>, so they can <the goal they reach with it>.

## Getting started

### 1. Prerequisites

<!-- One line per tool, with the minimum version and the command that checks it. -->

- <Tool> <version>: check with `<tool> --version`

### 2. Get the code

```bash
git clone https://github.com/MouraGabriel53/<repo>.git
cd <repo>
```

### 3. Configure

```bash
cp .env.example .env
```

Then fill in `.env`:

<!--
One row per variable in .env.example, in the same order.
- Required: "yes" if the app does not start without it.
- Secret: "yes" if the value must never be committed or shared.
- How to get it: one of
    "Default works locally"
    "Generate: `<command>`"
    "<Service> → <menu> → <page>"
If the project reads no configuration, replace this whole step with
"Nothing to configure." and delete .env.example.
-->

| Variable | Required | Secret | How to get it |
| --- | --- | --- | --- |
| `<VARIABLE>` | yes | no | Default works locally |
| `<SECRET>` | yes | yes | Generate: `openssl rand -base64 32` |
| `<API_KEY>` | no | yes | <Service> → <menu> → API keys |

### 4. Run

<!-- The exact commands, e.g. `pnpm install` and `pnpm dev`. -->

```bash
<install command>
<run command>
```

Open <http://localhost:3000>.

## Documentation

Internal documentation is written in Portuguese (pt-BR).

- [Architecture](docs/architecture.md): overview, stack, dependencies, features and routes
- [API](docs/api.md): the APIs the app consumes and their Swagger
- [Contexts and operations](docs/README.md#contextos): one spec per operation, with its flow
- [Decisions](docs/decisions/README.md): why things are the way they are

## Development

System requirements, every command (build, tests, run), CI and the commit
conventions are in [docs/development.md](docs/development.md).
