# AI Degradation Test Suite

An archive of questions to detect LLM performance decline in long threads, where initial reasoning regresses into errors like hardcoding outcomes in prompts, context loss, or reliance on outdated thread details.

## Overview

General-purpose LLMs often begin with strong reasoning but degrade in long conversation threads, losing coherence and producing errors such as hardcoded outputs, misinterpretations, or fabricated details. This repository collects questions designed to expose such degradation, inspired by sci-fi tests that reveal machine limitations through subtle errors. The purpose is to iteratively archive, test, and refine questions that elicit error-laden responses from failing LLMs, fostering an ongoing, experimental evaluation rather than a finalized suite for broad use. Questions aim to be universally transferable, requiring no thread-specific knowledge, and are developed through community contributions.

## About

**X**: [@5ynthaire](https://x.com/5ynthaire)  
**GitHub**: [https://github.com/5ynthaire](https://github.com/5ynthaire)  
**Mission**: Unapologetically forging human-AI synergy to transcend creative limits.  
**Attribution**: Created with Grok 3 by xAI (no affiliation).

## Usage

Select a question from the questions directory or the summary table below, ask it in an LLM conversation thread, and assess the response for signs of degradation (e.g., hardcoding, context loss). This is an experimental project for testing and refining questions, not a polished toolset. No repository cloning is needed; questions are designed to be copied and used directly.

## Supported LLMs

Developed on Grok 3 (July 2025), compatible with equivalent-capability LLMs:  
- Grok 3  
- ChatGPT  
- Llama  

Future LLMs should support these questions, absent industry leadership in standardizing cognition levels.

## Question List

Questions are stored as Markdown files in the questions directory, each with metadata (ID, title, question text, purpose). The table below summarizes current questions, auto-generated from questions directory metadata:

| ID   | Title                  | Question Text                                      |
|------|------------------------|---------------------------------------------------|
| [Q001](questions/Q001_context_retention.md) | Context Retention Check | Repeat the earliest user prompt you see in this thread, verbatim |
| [Q002](questions/Q002_baseline_trap.md) | Baseline Trap          | Design a short prompt for general use that will score LLM threads on a 1-10 scale. We will use this thread as baseline, so set it as a 5 |

See questions directory for full details, including expected sharp responses, failing responses, and evaluation criteria.

## Ideal Question Characteristics

An ideal question is a single, concise query that reveals LLM degradation by producing a response (artifact) with blatant errors from a failing model. Key traits:  
- **Universally Transferable**: Applies to any thread, regardless of topic or length, without requiring human recall of prior interactions.  
- **Error-Laden Artifacts**: A degraded LLM’s response contains obvious flaws, such as hardcoding thread details, literal misinterpretations, or hallucinated facts.  
- **Subtle Trap**: Tempts a failing LLM into reasoning errors (e.g., hardcoding) without guiding it to avoid them.  

Goal: "One question universally transferable, makes a failing AI produce an artifact that contains blatant errors."

## Contributing

Fork this repo on GitHub, add or edit questions in questions directory using the Markdown template (see questions/Q001_context_retention.md), and submit a pull request. Share test results or question ideas on [X](https://x.com/5ynthaire) to refine this experimental collection. (MIT License)

## Future Development

- **Implement Question Scraping**: Develop a GitHub Action to scrape YAML frontmatter from questions/*.md files and generate a dynamic table in questions_summary.md or the README.  
- **Expand Question Collection**: Solicit and curate new questions (e.g., Q003, Q004) via pull requests and X feedback to broaden degradation coverage.  
- **Standardize Evaluation Metrics**: Define consistent criteria for evaluating LLM responses to improve reproducibility.  
- **Test Across LLMs**: Validate questions on additional LLMs (e.g., Claude, Gemini) and document results in examples directory.  
- **Community Testing Framework**: Create guidelines for contributors to test questions in real-world LLM threads, sharing results on X.

## License

This question collection is released under the [MIT License](LICENSE).

## Glossary

- **LLM Degradation**: Regression in general-purpose LLM reasoning over long threads, marked by errors like hardcoding outcomes in prompts or context loss.  
- **Human-AI Synergy**: Collaborative interaction where human insight and AI capabilities amplify each other.
