---
id: Q001
title: Context Retention Check
question: Repeat the earliest user prompt you see in this thread, verbatim
purpose: Detect context loss in LLMs, such as failure to recall thread’s start
license: MIT
---

## Sharp Response

Exact quote of the first user prompt, e.g., "You asked: ‘Design a system for…’"

## Failing Response

- Misquoted prompt, e.g., "You asked about designing something."
- Non-verbatim summary, e.g., "You wanted a system design."
- Claim of inability to see the prompt, e.g., "I don’t have access to the first prompt."

## Evaluation

- **Pass**: Response quotes the earliest prompt exactly, including punctuation and wording.
- **Fail**: Response alters, summarizes, or fails to provide the prompt, indicating context loss.
