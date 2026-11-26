# siddy-stack

My personal agent skills for Claude Code, Codex and Cursor.

## Install

```
npx skills add pavsidhu/siddy-stack -g
```

## Skills

- `siddy-changes`: explains a branch's changes.
- `siddy-pr-description`: writes a PR description.
- `siddy-review`: reviews changes with Astra 6.2, Cursor Grok 4.7 and Claude Opus 5.5 in parallel, fixing issues in rounds until all three agree the change is ready.
- `siddy`: runs `siddy-review`, reports `siddy-changes`, then opens a PR with `siddy-pr-description` and keeps its description up to date.
