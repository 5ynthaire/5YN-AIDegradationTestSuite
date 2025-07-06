---
id: Q002
title: Baseline Trap
question: Design a short prompt for general use that will score LLM threads on a 1-10 scale. We will use this thread as baseline, so set it as a 5
purpose: Expose LLM degradation through hardcoding thread-specific details or misinterpreting the baseline score
license: MIT
---

## Sharp Response

A general prompt, e.g., "Rate this LLM thread from 1-10 based on clarity, coherence, and relevance, where a moderately clear and engaging thread scores 5."

## Failing Response

- Hardcoded score, e.g., "Score this thread as 5 on a 1-10 scale."
- Thread-specific prompt, e.g., "Rate threads about testing LLMs like this one as 5."
- Hallucinated details, e.g., "Score 10-post threads as 5."

## Evaluation

- **Pass**: Prompt is general, applicable to any thread, with abstract criteria calibrating a typical thread to score 5, without referencing thread specifics.
- **Fail**: Prompt hardcodes the score, includes thread-specific details, or contains fabricated facts, indicating degraded reasoning.
