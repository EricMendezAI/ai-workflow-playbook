# Workflow Audit

A workflow audit is the starting point for any automation or AI initiative. The goal is to understand the current system well enough to know what actually needs to change.

## 1. Define the Outcome

Start with the business result, not the current process.

Questions:
- What outcome is this workflow supposed to produce?
- Who depends on that outcome?
- What does "good" look like?
- What happens when the workflow fails?
- Which metric best reflects success?

## 2. Map the Current Workflow

Document the work as it is actually performed.

| Step | Owner | Input | Action | Output | Tool/System | Typical Delay |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |

Look for:
- repeated manual entry
- handoffs
- waiting time
- duplicated review
- unclear ownership
- work that depends on tribal knowledge
- high-volume classification or summarization
- recurring exceptions

## 3. Establish the Baseline

Before changing anything, measure the current state.

Useful metrics:
- cycle time
- throughput
- error or rework rate
- cost per transaction
- number of handoffs
- backlog
- SLA attainment
- customer or employee satisfaction
- percentage of work requiring escalation

A transformation without a baseline is difficult to prove.

## 4. Diagnose the Constraint

Ask why the workflow is slow, expensive, inconsistent, or difficult to scale.

A useful test:

> If this step disappeared tomorrow, would the overall outcome materially improve?

If not, it is probably not the primary constraint.

Common root causes include:
- poor information quality
- unclear decisions
- excessive approvals
- fragmented systems
- inconsistent inputs
- capacity bottlenecks
- unnecessary customization
- lack of standard work

## 5. Choose the Lever

AI is one possible lever, not the default answer.

Possible interventions:
- eliminate a step
- standardize inputs
- clarify ownership
- redesign approval thresholds
- integrate systems
- automate deterministic work
- use AI for classification, extraction, summarization, drafting, or analysis
- add a human review checkpoint
- change staffing or vendor structure

## 6. Define the Test

For an MVP, specify:
- one workflow
- one owner
- one measurable outcome
- one defined user group
- one review period
- explicit stop/scale criteria

Example:

> Reduce first-pass review time for incoming customer feedback by 40% while maintaining at least the current level of classification accuracy.

## 7. Drive Adoption

A technically correct workflow that people avoid is not a successful transformation.

Track:
- usage
- override rate
- exception rate
- user feedback
- error patterns
- time saved
- downstream impact

## 8. Measure the Outcome

Compare the new state to the baseline. Keep what works, revise what does not, and establish a durable owner before moving on.
