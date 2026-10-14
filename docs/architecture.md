# Architecture

<!-- One paragraph: what the app is, who uses it, and how it is split. Then a diagram of the main flow. -->

```
<!-- e.g. Route -> feature page -> feature hooks/services -> backend API -->
```

## Structure

The code is organized by feature: everything a feature needs (UI, state,
data access, types, tests) lives in its own folder. Code shared by several
features lives in `shared/`. Where routes, layouts and framework entry points
go depends on the framework; record it in the table below.

<!-- Keep this table in sync with the folders. Add one row per feature. -->

| Path | Role | May import |
| --- | --- | --- |
| `<routes>` | Framework entry points (pages, layouts, routing): thin, compose features | features, `shared` |
| `features/<name>` | One feature: its components, state, data access, types and tests | its own files, `shared`, other features' public entry point |
| `shared` | Code used by more than one feature: UI primitives, utilities, clients | `shared` |

Rules:

- A feature exposes what others may use through one public entry point
  (e.g. `features/<name>/index.ts`). Other code never imports a feature's
  internal files.
- `shared` never imports a feature.
- Code moves to `shared` only when a second feature needs it.

## Components (React)

When the app uses React, build components with the composition pattern:
pass content and behavior through `children`, slots and compound components
(`<Card>`, `<Card.Header>`, `<Card.Body>`) instead of adding a configuration
prop for each variant.

- A new variant is a new composition, not a new boolean or `variant` prop on
  an existing component.
- Compound components share state through context set by the parent, not
  through props passed down by the caller.
- Prefer passing a rendered element (`icon={<Icon />}`) or `children` over
  passing data that the component must know how to render.

## Features

<!-- One row per feature: what it does and what it exposes. -->

| Feature | What it does | Public entry point exports |
| --- | --- | --- |

## Flows

<!-- The main flows step by step: first load, authentication, the main user journey, errors. -->

## Adding a feature

<!-- Checklist of the files to touch for the most common kind of change. -->
