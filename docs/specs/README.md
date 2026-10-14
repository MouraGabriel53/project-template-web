# Specs

A spec describes a change **before** it is built: the problem, the goals, what
is out of scope, the design and the open questions. It is reviewed before any
code is written and keeps a multi-session change on track.

- One file per change, named after it.
- **Status** at the top: `draft`, `approved`, `implemented` or `dropped`.
- When the change is merged, fill in **Result** and record each non-obvious
  choice as a decision in [decisions/](../decisions/README.md).

Template:

```markdown
# Spec: Title

- **Status:** draft
- **Origin:** where the need came from, with the date.

## Problem
## Goals
## Non-goals
## Design
## Open questions
## Result
```

| Spec | Status |
| --- | --- |
