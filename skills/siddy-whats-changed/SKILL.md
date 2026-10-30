---
name: siddy-whats-changed
description: Use when the user asks to explain changes on a branch, PR, or specific files or features. Triggers on "what changed", "what's changed", "explain this branch", "summarise this PR", "walk me through the changes", "what did I change", "what's the blast radius".
---

Explain the changes on the whole branch against its merge-base. If the user specifies particular files or features, review only those.

Keep your delivery concise, simple and jargon-free.

## How to present

Start with a short overview of what the change is from a product perspective.

Next, group related edits, with the highest blast radius first. Skip empty levels. Ignore style nits.

- **High**: can cause a major break in production (data loss, auth, billing, outage, bad migration).
- **Medium**: the product stays up, but a real user path is wrong.
- **Low**: a small UI bug.

Also:

- Always highlight changes to the data model.
- Name new modules, services and repositories, plus important methods, and explain how the feature works.
- Choose the visual that fits what changed, not a fixed layout. For changes across services, draw one map of the real system, mark what changed, let the reader switch between scenarios, and pin each risk where it happens. If the change produces something visible, show the real output.
- Compare the change with the rest of the codebase. Does it introduce any new patterns? A new pattern increases the risk of the change.
