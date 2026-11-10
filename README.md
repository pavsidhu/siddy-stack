# siddy-stack

My personal agent skills for Claude Code, Codex and Cursor.

## Install

```
npx skills add pavsidhu/siddy-stack -g
```

## Skills

- `siddy-whats-changed`: explains a branch's changes.
- `siddy-pr-description`: writes a PR description.
- `siddy-review`: reviews changes with a second model on a different harness over 3 fix-and-review rounds.
- `siddy`: runs `siddy-review`, reports `siddy-whats-changed`, then opens a PR with `siddy-pr-description` and keeps its description up to date.
