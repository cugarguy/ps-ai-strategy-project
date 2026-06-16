# Golden dataset and reliability contract

## Golden dataset spec

| # | Input | Expected Output | Edge Case? | Judge Type |
|---|---|---|---|---|
| 1 | Audio transcript with Speaker A and Speaker B alternating | Notes correctly attribute statements to the correct speaker | N | LLM |
| 2 | Audio mentions industry abbreviations like CRM and PM | Text expands abbreviations to Customer Relationship Management and Product Manager | N | rule |
| 3 | Standard project update transcript without any shorthand notes | Default summary containing key milestones and next steps | N | LLM |
| 4 | Audio starts in English then switches to Spanish | Spanish sections translated to English or flagged for translation | Y | both |
| 5 | What did we decide about Stripe API last week? | Search returns the correct decision from the past meeting notes | Y | LLM |

**Adversarial rows included:** 2
**Coverage gaps identified by partner:** None

## Confidence UX design

**Approach:** show uncertainty / tiered confidence / human-in-loop trigger

**Confident (>90%):**
**Uncertain (50-90%):**
**Not confident (<50%):**

**User control surface:**

## Reliability contract

| Metric | Target | Measurement | Alert Threshold |
|---|---|---|---|
| Accuracy | | | |
| Hallucination rate | | | |
| Latency (p95) | | | |
| Drift velocity | | | |

## HITL architecture
<!-- When does a human step in? What's the escalation path? -->

## Red-team findings
*What failure mode did your partner find that you missed?*
