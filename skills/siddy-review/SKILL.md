---
name: siddy-review
description: Use when reviewing changes with a second model. Triggers on "review this", "review my changes", "review the branch".
---

# Overview

Review the changes with three reviewers running in parallel: ChatGPT Astra 6.2, Cursor Grok 4.7 and Claude Opus 5.5.

Use the T3 Code tools (`delegate_task`) to run all three reviewers as subagents at the same time.

# Review process

Keep reviewing in rounds until all three reviewers agree the change is ready. In each round:

1. Each reviewer produces a list of security vulnerabilities, performance issues, bugs and other issues found in the change, ordered from highest to lowest priority.
2. You go through all three lists, merge duplicates and evaluate whether each issue is valid. For each valid issue, make the smallest possible change required to address it. Ignore extreme edge cases and be careful of scope creep.
3. Ask all three reviewers whether the change is now ready. If all three say yes, stop. Otherwise, start another round.

If the reviewers still disagree after 5 rounds, stop and ask the user how to proceed.

# Report

When the reviewers agree, finish with a table of every issue raised:

| | Issue | Decision |
|---|---|---|
| ✅ | Issue that was fixed | What was changed |
| ❌ | Issue that was dismissed | Why it was dismissed |
