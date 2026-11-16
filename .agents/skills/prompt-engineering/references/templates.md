# Prompt Templates

Replace the braces with task-specific values. Use each template independently or compose compatible parts. Adapted from Boonstra, *Prompt Engineering*, September 2024, pp. 13–41 and 54–63.

## Direct prompt with optional examples

```text
Task
{action and intended outcome}

Rules
{durable requirements, evidence scope, and behavior for missing information}

Output
{fields, types, allowed values, length, and audience}

Examples
{representative input → expected output pairs}

Input
<input>
{task_data}
</input>
```

Omit the examples section for zero-shot. For a triage classifier, include normal requests, clear incidents, and vague reports. Show the expected fallback label for ambiguous reports. Put stable rules in the endpoint's instruction field where supported.

## Step-back

```text
Pass 1
For {broader problem class}, identify the criteria and common confounders that
matter for {decision}. Return a short checklist of relevant considerations.

Pass 2
Apply {checklist} to {specific case and evidence}. Link each recommendation to
case evidence. Flag inapplicable criteria and missing inputs.
Return {deliverable}.
```

For a conversion drop, first identify general causes of measurement and funnel changes. Then apply the checklist to the actual instrumentation, traffic mix, and funnel data.

## ReAct

```text
Goal
{question or deliverable}

Tools and scope
{available operations, permitted data, and call or time budget}

At each iteration, choose the unresolved question that most affects the outcome.
Call an allowed tool to check it. Record the tool, input, observed result, and
source identifier. Use the result to update the next check.

Stop when {evidence threshold} is met, the budget is exhausted, or further
progress requires unavailable access. Return the answer, supporting observations,
and remaining gaps.
```

For a KPI discrepancy, compare metric definitions, query source totals, and revisit the hypothesis if the discrepancy persists. A tool error is a failed attempt. With unavailable tools, provide proposed checks and identify the missing observations.

## Self-consistency

```text
Classify {input} using {label definitions}. Return one canonical label and
the source field that supports it. Use {abstain value} when evidence is missing.
```

In the runner, submit the same prompt and input in separate calls using supported settings that allow diversity. Set the sample count and decision rule before running. For example, require at least three matching valid answers out of five attempts. Normalize equivalent labels and log invalid responses and abstentions. On a split vote or unmet threshold, route for review or return uncertainty. Check agreement against labeled examples or a deterministic calculation. Vote share measures agreement, and shared errors can survive a unanimous vote.
