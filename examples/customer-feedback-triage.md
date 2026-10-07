# Example: AI-Assisted Customer Feedback Triage

> Illustrative prototype. This is a demonstration of the workflow framework, not a claim of a deployed production system.

## Situation

A product organization receives customer feedback through support tickets, surveys, account teams, and free-text forms. Analysts manually read and categorize entries before recurring issues can be surfaced to Product and Operations.

## Constraint

The bottleneck is not collecting feedback. It is converting unstructured feedback into a consistent, decision-ready view quickly enough for teams to act.

## Current-State Friction

- inconsistent categorization
- duplicate issues described in different language
- manual summarization
- slow identification of emerging themes
- limited visibility into severity and frequency
- analysts spend time organizing information instead of interpreting it

## Redesigned Workflow

### 1. Ingest
Collect feedback into a common queue with source, account/customer segment, date, and free-text content.

### 2. Normalize
Use deterministic rules to clean metadata and remove obvious duplicates where possible.

### 3. AI Classification
Have an LLM return structured fields such as:
- category
- subcategory
- issue vs. request
- severity signal
- product area
- concise summary
- confidence
- suggested duplicate/theme cluster

### 4. Human Review
Route:
- low-confidence classifications
- high-severity items
- new/unrecognized themes
- sampled normal items

to an analyst for review.

### 5. Aggregate
Create a recurring view of:
- top issue themes
- fastest-growing themes
- high-severity clusters
- affected customer segments
- feature-request frequency

### 6. Decision Support
Generate a short evidence-backed weekly summary for Product and Operations, with links to the underlying feedback rather than unsupported conclusions.

## Example Structured Output

```json
{
  "type": "issue",
  "category": "billing",
  "subcategory": "invoice_export",
  "severity": "medium",
  "summary": "Customer cannot export invoices in the required format.",
  "confidence": 0.91,
  "requires_human_review": false
}
```

## MVP Success Metrics

Compare against the current baseline:
- time from feedback receipt to categorization
- analyst minutes per 100 entries
- agreement between AI classification and human review
- percentage requiring manual correction
- time to identify a recurring theme
- user adoption by Product/Operations stakeholders

## What I Would Test First

Start with one feedback source and a limited taxonomy. Do not attempt full automation initially.

A successful first test should demonstrate that the redesigned workflow reduces organization time without reducing classification quality. Only then expand sources, categories, or automation.
