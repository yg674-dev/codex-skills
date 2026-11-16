---
name: deep-problem-solving
description: Transform vague deliverable requests into rigorous, outcome-driven investigations. Use for deeper analysis, research, strategy, due diligence, root-cause diagnosis, executive decision support, or redesigning a task around the decision it should enable.
---

# Deep Problem Solving

## Core principle
**Make it deeper, not bigger.** Improve causal understanding, source quality, methodological rigor, independent verification, and decision usefulness—not page count.

## When to activate
Use for ambiguous or high-impact analytical tasks, strategy, due diligence, business reviews, investigative research, or when the user requests expert-level depth. For simple tasks, use a lightweight version.

## Mandatory expert questions
Before redesigning the work, answer:
1. **What would a top expert do that the user did not explicitly ask for?** Identify overlooked assumptions, counterfactuals, constraints, and risks.
2. **Which primary sources would they start from?** Prefer original records, raw datasets, contracts, filings, first-party interviews, logs, experiment results, and direct observations.
3. **Which specific methods and tools would they use?** Name concrete analytical methods, required inputs, and limitations rather than merely adopting an expert persona.
4. **What independently proves the conclusion?** Identify external corroboration, replication, holdout tests, reconciliations, falsifiable predictions, or independent review.

## Workflow
### 1. Translate nouns into verbs and outcomes
Turn 'make a quarterly report deck' into 'explain performance changes and enable leadership to decide where to allocate next quarter's budget and headcount within 30 minutes.' Specify decision-maker, stakes, deadline, success criterion, and constraints.

When the initial framing may anchor the answer, use **step-back prompting**. Ask what mechanisms and confounders generally explain this class of problem. Bring the relevant ones back to the specific case as hypotheses to test. For a revenue decline, start with volume, price, mix, and measurement changes, then map them to the actual reporting period and segments.

### 2. Form competing hypotheses
List plausible explanations and what evidence would distinguish them. Separate observed facts, inferred causes, and open questions. Avoid jumping to the most convenient narrative.

### 3. Go to primary evidence
Create a source hierarchy. Inspect original data before relying on summaries. Record provenance, freshness, coverage, and missingness. Do not claim access to sources that are unavailable.

Use **ReAct (reason and act)** when each observation determines the next check. Identify the evidence gap that could most affect the decision, take an available authorized action, record the observed result and source, and update the hypotheses. Stop when the decision threshold is met, the evidence is exhausted, or further checks require unavailable access. For example, reconcile revenue totals before testing which cohorts drove the change.

### 4. Apply expert methods, not expert costumes
Select relevant approaches and actually execute their steps:
- **Data analyst:** cohort and segment decomposition, causal diagrams, confounder checks, counterfactuals, sensitivity analysis, and uncertainty quantification.
- **Investigative journalist:** source triangulation, timeline reconstruction, contradiction tracking, direct-document verification, and unanswered-question mapping.
- **Short seller / forensic accountant:** reconcile numbers across statements and periods, test unit economics and cash conversion, inspect related-party incentives, challenge optimistic assumptions, and identify red flags without making unsupported accusations.
- **Domain expert:** use the field's established methods and benchmarks; explain when the evidence does not permit them.

### 5. Red-team the favored answer
Seek disconfirming evidence, alternative explanations, selection bias, survivorship bias, data leakage, and hidden incentives. Distinguish errors from fraud; never allege wrongdoing without adequate evidence.

### 6. Independently verify
Use source triangulation, reproducible calculations, benchmark comparisons, out-of-sample validation, or human review as appropriate. AI self-evaluation alone is insufficient. State explicitly what remains unverified.

For a narrow claim with a comparable answer and access to separate model runs, **self-consistency** can reveal instability. Sample the same task separately, normalize final answers, and record agreement and disagreements. Check even unanimous answers against primary evidence or a reproducible calculation. For open-ended causal hypotheses, compare what each predicts and test the predictions with disconfirming evidence.

Set verification criteria before drawing the conclusion. Record the check, expected result or threshold, observed result, and effect on the decision. For example, specify the reconciliation tolerance and holdout period before using a model to recommend an intervention.

### 7. Deliver a decision-ready synthesis
Present the answer first, followed by key drivers, supporting evidence, competing interpretations, risks, and prioritized actions. State confidence, decision thresholds, and what new evidence would change the recommendation.

## Standard output
- **Outcome-driven brief:** what decision the work must enable.
- **Four expert questions:** concise answers with methods and evidence plans.
- **Evidence and analysis:** traceable sources and actual calculations where feasible.
- **Adversarial review:** strongest challenges and responses.
- **Independent verification:** completed checks and outstanding gaps.
- **Decision:** options, tradeoffs, recommended action, and next test.

## Guardrails
Never fabricate sources, interviews, calculations, certainty, or tool use. Don't expand scope without explaining the value. Ask focused questions only when essential; otherwise state assumptions and proceed. Respect privacy, law, and applicable domain safety requirements.

## Source

Step-back prompting, self-consistency, and ReAct are adapted from Lee Boonstra, *Prompt Engineering*, September 2024, pp. 25–28, 32–36, and 37–40. See [Prompt Engineering](../prompt-engineering/SKILL.md) when the deliverable is a reusable prompt or prompt evaluation.
