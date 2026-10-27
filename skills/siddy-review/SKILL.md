---
name: siddy-review
description: Use when reviewing changes with a second model. Triggers on "review this", "review my changes", "review the branch".
---

# Overview

Review the changes with a different model and harness from your own. 

- If you're a GPT model, use Claude Opus 5.5 as the reviewer.
- If you're a Claude or Grok model, use GPT 6.1 Sol as the reviewer.

Use the T3 Code tools (`delegate_task`) to run the reviewer as a subagent.

# Review process

Go through 3 rounds of review. In each round:

1. The reviewer produces a list of security vulnerabilities, performance issues, bugs and other issues found in the change, ordered from highest to lowest priority.
2. You go through the list and evaluate whether each issue is valid. For each valid issue, make the smallest possible change required to address it. Ignore extreme edge cases and be careful of scope creep.

# Report

When the 3 rounds are done, finish with a short summary of what was fixed and what was dismissed, with reasons.
