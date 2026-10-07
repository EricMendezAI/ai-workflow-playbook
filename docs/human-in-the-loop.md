# Human-in-the-Loop Design

The useful question is not "Can AI do this?" It is "What should AI do, what should a person own, and where should review occur?"

## Four Roles for AI

### 1. Assist
AI supports a person without taking an action.

Examples:
- summarize a long document
- draft an internal update
- organize notes
- identify themes

### 2. Recommend
AI proposes a decision, but a person approves it.

Examples:
- suggest lead priority
- classify a customer issue
- recommend a response category
- identify likely root causes

### 3. Execute With Review
AI performs a bounded action and routes exceptions or samples for human review.

Examples:
- draft standardized responses
- enrich structured records
- route work to predefined queues

### 4. Execute Automatically
AI or automation completes the action without routine review.

This should be reserved for work with:
- low downside
- clear rules
- strong monitoring
- reversible outcomes
- reliable exception handling

## Review Design

Define review based on risk rather than habit.

| Risk Level | Suggested Review |
|---|---|
| Low | periodic sampling |
| Moderate | exception-based review plus sampling |
| High | approval before action |
| Critical | human decision; AI may assist only |

## Escalation Rules

Every AI-enabled workflow should answer:
- What triggers human review?
- Who owns the exception?
- What happens when confidence is low?
- How are repeated failures identified?
- How is the workflow stopped if quality degrades?

## Measure the Whole System

Do not measure only model output.

Measure:
- end-to-end cycle time
- human review time
- override rate
- error/rework rate
- adoption
- exception volume
- customer/business outcome

The goal is a better operating system, not a higher AI utilization rate.
