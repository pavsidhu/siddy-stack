---
name: siddy-whats-changed
description: Use when the user asks to explain changes on a branch, PR, or specific files or features. Triggers on "what changed", "what's changed", "explain this branch", "summarise this PR", "walk me through the changes", "what did I change", "what's the blast radius".
---

Explain the changes on the whole branch against its merge-base. If the user specifies particular files or features, review only those.

Keep your delivery concise, simple and jargon-free.

## How to present

- Always reference changes to services, including new or changed services and their methods. Ideally link to them if possible like [UserService.create()](/absolute/path/to/file/with/line/number)
- Skip any sections that are not relevant. For example, a small UX change may just need an overview, whereas a new feature may need everything.
- Write the reply section by section, calling `html_render` only once you reach a diagram's section so it appears inline, not above the text.

Use the format below. Lines in `<!-- -->` are instructions for you; don't copy them into the reply.

```
# Title of the change

## Overview

<!-- An overview of the changes made and why they were made. Attach inline screenshots and videos as evidence. -->

## Risks

<!--
Think about what could go wrong once this change goes into production.
Group related edits, with the highest blast radius first.
- 🔴 High: can cause a major break in production (data loss, auth, billing, outage, bad migration).
- 🟡 Medium: the product stays up, but a real user path is wrong.
- 🟢 Low: a small UI bug.
-->

| # | Level | Description |
|---|---|---|
| 1 | 🔴 | <!-- A description of the risk. --> |

## Pipelines

<!--
If the change touches a flow, copy `pipelines.html` from this skill's folder and fill in `ROWS` only. Its comment explains the format.
- One row per pipeline: main paths, then failures, then one-off scripts.
- Short plain step names. Keep the unchanged steps around the change.
- Code names and numbers go in the pop-ups.
- Check it with `html_preview`, then show it with `html_render`.
-->

## Data model

<!--
If the database schema changed, copy `datamodel.html` from this skill's folder and fill in `TABLES` only. Its comment explains the format.
- Show every new, changed or deleted table, column, extension or enum, plus the tables they link to.
- Code names and numbers go in the pop-ups.
- Check it with `html_preview`, then show it with `html_render`.
-->

## New patterns

<!-- Compare the changes with the rest of the codebase. Are there new code or architecture patterns that we use in the change? -->

| # | New pattern |
|---|---|
| 1 | <!-- A description of the new pattern. --> |
```
