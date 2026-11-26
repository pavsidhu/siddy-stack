---
name: siddy-review
description: Use when reviewing changes with a second model. Triggers on "review this", "review my changes", "review the branch".
---

# Overview

Review the changes with two reviewers running in parallel: ChatGPT Astra 6.2 and Cursor Grok 4.7.

Use the T3 Code tools (`delegate_task`) to run both reviewers as subagents at the same time.

# Review process

Keep reviewing in rounds until both reviewers agree the change is ready. In each round:

1. Both reviewers produce a list of security vulnerabilities, performance issues, bugs and other issues found in the change, ordered from highest to lowest priority.
2. You go through both lists, merge duplicates and evaluate whether each issue is valid. For each valid issue, make the smallest possible change required to address it. Ignore extreme edge cases and be careful of scope creep.
3. Ask both reviewers whether the change is now ready. If both say yes, stop. Otherwise, start another round.

If the reviewers still disagree after 5 rounds, stop and ask the user how to proceed.

# Report

When the reviewers agree, finish with a table of every issue raised:

| | Issue | Decision |
|---|---|---|
| ✅ | Issue that was fixed | What was changed |
| ❌ | Issue that was dismissed | Why it was dismissed |
