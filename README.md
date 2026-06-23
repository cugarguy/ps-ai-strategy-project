# My AI product strategy
> A living strategy built across 6 sessions. Each module adds one component.

## Strategy at a glance

| Component | Module | Status | Key Artifact |
|---|---|---|---|
| The bet | M1 | [x] Complete | `01-the-bet/` |
| The moat | M2 | [x] Complete | `02-the-moat/` |
| The margin | M3 | [x] Complete | `03-the-margin/` |
| The contract | M4 | [x] Complete | `04-the-contract/` |
| The guardrails | M5 | [ ] Pending | `05-the-guardrails/` |
| The pitch | M6 | [ ] Pending | `06-the-pitch/` |

---

## The bet (M1)
What we are building, for whom, and why now.
- Product: Granola AI is an AI-powered notepad for product managers. It records computer audio locally to convert shorthand notes into formatted documents.
- Value archetype: Automator
- Vulnerability scores: Moat 3/5 | Data 2/5 | Platform 4/5
- Top risk: Apple and Microsoft are adding free, native audio recording into their operating systems.
- Confidence: M
- Prototype: https://lovable.dev/projects/b4a5bced-1aac-493c-8945-6eaa4987e015
- Kill criteria: We stop development if operating systems release native audio transcription for all third-party software.

---

## The moat (M2)
Why this will not get copied in six months.
- Data flywheel score: 9/20
- Weakest loop: Network loop (1/5)
- Competitive position: The text editor is sticky, but the software cannot aggregate data across different companies.
- Encroachment defense: Granola will open-source a Model Context Protocol server framework to feed meeting data to engineering tools.
- Vendor portability: Partial
  - Rationale: Granola stores files locally, but the formatting logic belongs to third-party APIs.

---

## The margin (M3)
Will this make money or bleed it?
- Gross margin (current): 98.9%
- Gross margin (AI-adjusted): 83.5%
- Pricing model: Hybrid ($14/mo seat + outcome-based CRM updates)
- Cascading strategy: 80% triage / 20% frontier
- Break-even at: ~1,500 active paid seats

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The contract (M4)
Why users will trust a probabilistic system.
- Reliability target: 95% accuracy
- Golden dataset: 5 rows, 2 adversarial
- Confidence UX: Tiered highlighting and Spanish translation flag
- HITL architecture: Desktop inbox review queue
- Failure mode coverage: Speaker attribution and acronym expansion

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales — and what compounds.**

* **Compounding System:** The platform faces active cross-domain transfer compounding, where prior meeting data, calendar context, and unresolved action items enrich pre-meeting briefs and surface patterns across customer calls. However, recursive learning and network intelligence loops are currently broken because user corrections to notes and formatting are not reliably captured as durable preferences or evaluation data. Workflow completion remains a missing loop, leaving meeting intelligence trapped in notes instead of turning into completed downstream steps.

* **Governance Posture:** Features operating on authorized data run autonomously—including note generation, summarization, permissions-grounded Q&A, and draft suggestions. However, strict human approval is required for external sharing, message delivery, tool writes, and long-term personalization loops. Escalation triggers route tasks immediately to human review if system confidence drops below 70%, ungrounded outputs occur, sensitive content (legal, HR, financial) is detected, or the user attempts to execute high-risk external commitments.

* **Shadow AI Status:** 10 tools found, 10 triaged

* **Agent Boundaries:** Boundary enforcement utilizes four distinct agent typologies: the *Notes Agent* handles localized transcription and summarization but cannot modify external systems; the *Memory Agent* provides context-bounded Q&A without inferring ungrounded facts; the *Workflow Agent* drafts downstream tickets and updates without direct write authority; and the *Governance Agent* oversees security parameters, blocks risky outputs, and flags escalations.

* **Regulatory Exposure:** Financial and consumer data fall under GDPR, UK GDPR, CCPA/CPRA, and regional call-recording consent rules. Under the EU AI Act, the application operates within a "limited-risk" tier for standard meeting assistance, utilizing user-initiated capture, clear notice flows, private-by-default configurations, and enterprise-level training opt-outs to maintain compliance.
→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):**
- **Horizon 2 (Next):**
- **Horizon 3 (Bet):**
- **Board Narrative:** [1-sentence thesis]
- **Key Metric:**

→ Details: [`06-the-pitch/`](06-the-pitch/)
