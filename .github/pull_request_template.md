<!--
Title in Conventional Commits format: <type>(<scope>): <description>
Types: feat, fix, refactor, test, docs, chore, build, ci
Examples: "feat(checkout): show shipping estimate before payment", "fix(auth): keep session after refresh"
The PR title check fails if the title does not follow this format.
-->

## What changes
<!-- Summary in 1-3 sentences. -->

## Why
<!-- Problem or motivation. Link the issue and the spec, if any. -->

## How to test
<!-- Steps to validate locally: pages to open, actions to take, accounts or data needed. -->

## Screenshots
<!-- Before and after, for visible UI changes. Delete if not applicable. -->

## Checklist
- [ ] Full test command passes locally (see docs/development.md)
- [ ] Features import each other only through their public entry point
- [ ] No new or upgraded dependency without approval
- [ ] README "Configure" table and `.env.example` updated, if variables changed
- [ ] Documentation created or updated (spec, architecture, api, decisions)
