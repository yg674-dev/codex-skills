# Evaluate and Version a Prompt

Boonstra's experiment log (September 2024, pp. 62–63, Table 21) records goal, model, configuration, prompt, and output. Extend it with case-level checks and deployment tradeoffs.

1. Write expected outcomes or a rubric before comparing prompts. Include typical inputs, edge cases, missing evidence, and malformed inputs relevant to the workflow. Keep examples used in the prompt out of the holdout.
2. Run the baseline and candidate on the same inputs with matched settings, unless a setting is the variable under test. Repeat stochastic runs when variance affects the decision. Track tool errors, invalid output, and truncation in the denominator.
3. Score deterministic properties first, such as schema validity, exact match, and tool arguments. For open-ended quality, rate each criterion with anchored examples and use human review or source checks for disputed judgments. For ReAct, check tool choice, provenance, recovery from empty or failed responses, and the stop condition.
4. Compare per-case results and aggregate metrics. Report coverage, accuracy or rubric scores, regressions by case type, and latency or cost when relevant. Use predeclared acceptance gates and run the selected version on the holdout before adoption.

## Run log

| Field | Record |
| --- | --- |
| Identity | Goal, prompt ID and version, date, full rendered prompt or reproducible version and inputs |
| Runtime | Provider, model ID and version, endpoint, supported decoding and token settings, tool and retrieval configuration |
| Case | Dataset version, case ID, expected result or rubric, and repetition number |
| Result | Output or redacted trace, finish status, tool outcomes, scores, latency, and usage |
| Decision | Pass/fail, regression and failure category, follow-up, and version selected |

For example, a ticket classifier might require 100% schema validity, zero missed urgent cases in a labeled holdout, and a latency budget. Record the number of urgent cases and any abstentions so the result can be interpreted. For a model upgrade, rerun the saved baseline and holdout before switching.
