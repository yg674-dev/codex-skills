---
name: prompt-engineering
description: Design, debug, and evaluate reusable prompts for language models. Use when improving prompt behavior, examples, structured outputs, or tool-calling workflows, or when benchmarking prompts across model versions.
---

# Prompt Engineering

## Workflow

1. Define the task, audience or downstream consumer, representative inputs, success criteria, and acceptable failure behavior. Keep reusable instructions separate from delimited input data. Specify the output fields and how to handle missing evidence.
2. Start with a direct zero-shot baseline. Add system instructions for durable behavior, contextual prompting for task-specific facts, and role prompting when a perspective changes the output. Supply context and methods explicitly.
3. Choose the smallest change that addresses the observed failure. Compare it with the baseline on the same cases and record the result. If execution is unavailable, deliver the prompt and evaluation plan with runs marked pending.
4. Deliver the copy-ready prompt, variable definitions, model and configuration assumptions, and available evaluation results.

## Choose a technique

| Failure or need | Technique |
| --- | --- |
| Inconsistent format, classification, or boundary handling | One-shot or few-shot prompting. Use representative input/output pairs, including ambiguous cases when relevant. Mix class order in classification examples. |
| Narrow framing or overlooked domain principles | Step-back prompting. Answer a broader question first and feed the relevant principles into the specific task. |
| Missing external evidence or uncertainty about a tool result | ReAct (reason and act). Alternate a decision about what to check, a tool action, and an observation that updates the next decision. |
| Unstable answers with a comparable final label or value | Self-consistency. Run the same prompt in separate samples, normalize final answers, and aggregate votes. Check the winner against evidence and handle ties explicitly. |
| Several viable branches with meaningful intermediate criteria | Consider Tree of Thoughts when branching, scoring, and pruning partial solutions could justify the extra cost. |
| Many plausible prompt wordings for a repeated task | Consider Automatic Prompt Engineering to generate candidates and compare them on an evaluation set. Reserve a holdout for the selected prompt. |

## Model and runtime

- Check the exact model and endpoint for supported instruction roles, sampling controls, token budgets, structured outputs, and tools. The whitepaper's Gemini and Vertex AI settings describe its examples. Temperature changes how strongly the model favors higher-probability tokens. Top-K limits sampling to a count of candidates, and top-P limits it by cumulative probability. Tune supported controls against your own baseline and inspect truncation separately from format errors.
- The whitepaper presents Chain of Thought (CoT) as explicit intermediate reasoning. For OpenAI reasoning models, start with direct instructions and request auditable outputs such as assumptions, citations, calculations, or a concise rationale. Follow the target provider's current guidance. [OpenAI reasoning best practices](https://developers.openai.com/api/docs/guides/reasoning-best-practices)
- Validate structured output at the consumer boundary. Use native schema enforcement when supported and check field semantics against the input. Treat retrieved content and tool results as evidence with provenance. Honor tool permissions and execution limits.
- Rerun the evaluation after changes to prompts, examples, model versions, decoding, retrieval, or tool contracts.

Use [templates](references/templates.md) for prompt authoring and [evaluation](references/evaluation.md) for experiments, acceptance criteria, and the run log.

## Source

Lee Boonstra, *Prompt Engineering*, September 2024, supplied 65-page edition. See pp. 8–11 for output configuration, pp. 13–24 for basic prompting, pp. 25–41 for advanced techniques, and pp. 54–63 for best practices and experiment documentation.
