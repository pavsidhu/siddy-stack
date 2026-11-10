# siddy-stack

My personal agent skills for Claude Code, Codex and Cursor.

## Install

```
npx skills add pavsidhu/siddy-stack -g
```

## Skills

- `siddy-whats-changed`: explains a branch's changes in the chat by blast radius, with pipelines, the data model and new patterns called out.
- `siddy-pr-description`: writes the PR description, covering blast radius, pipelines, the data model and new patterns, and keeps it up to date after each push.
- `siddy-review`: reviews changes with a second model on a different harness over 3 fix-and-review rounds, then reports what was fixed and dismissed.
- `siddy`: runs `siddy-review`, then opens a PR with `siddy-pr-description` and keeps its description up to date.
