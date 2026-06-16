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

**High Confidence (>99%)**
UI: Green double checkmark "Auto-published".
Behavior: Automatically syncs notes to Jira and Notion.
**Confident (>90%):**
UI: Green checkmark "Synced summary" with a tooltip stating "Matches meeting shorthand and audio."
Behavior: Displays fully formatted markdown notes with inline buttons to sync directly to Jira or Notion.
**Uncertain (50-90%):**
UI: Amber underline on specific sentences with a badge indicating "Verify details."
Behavior: Highlights assumptions. Provides inline links to the transcript timestamps for easy verification.
Copy example: Shorthand keyword "roadmap" was expanded, but the spoken audio segment was brief.
**Not confident (<50%):**
UI: Red warning box around the paragraph with a badge indicating "Low audio match."
Behavior: Blocks external tool exports. Prompts the user to edit shorthand notes or re-run transcription.
Copy example: Poor audio quality prevented matching your shorthand notes to the spoken transcript.
**User control surface:**
Toggle to highlight all AI-generated text in the document.
Inline controls to view transcript sources, choose a different recipe, or report translation errors.

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
