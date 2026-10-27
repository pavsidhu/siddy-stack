# siddy-stack

My personal agent skills for Claude Code, Codex and Cursor.

## Install

```
npx skills add pavsidhu/siddy-stack -g
```

## Skills

- `siddy-whats-changed`: explains a branch's changes by blast radius, with the data model and new patterns called out.
- `siddy-review`: reviews changes with a second model on a different harness over 3 fix-and-review rounds, then reports what was fixed and dismissed.
- `siddy`: runs `siddy-review` and then `siddy-whats-changed` on the same change, so you get the fixes and a walkthrough of the result.
