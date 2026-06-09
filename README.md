# My AI Product Strategy
> A living strategy built across 6 sessions. Each module adds one component. By Module 6, this repo IS your strategy — version-controlled, board-ready, portable.

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|-----------|--------|--------|-------------|
| **The Bet** | M1 | [x] Complete | `01-the-bet/` |
| **The Moat** | M2 | [x] Complete | `02-the-moat/` |
| **The Margin** | M3 | [ ] Pending | `03-the-margin/` |
| **The Contract** | M4 | [ ] Pending | `04-the-contract/` |
| **The Guardrails** | M5 | [ ] Pending | `05-the-guardrails/` |
| **The Pitch** | M6 | [ ] Pending | `06-the-pitch/` |

---

## The Bet (M1)
**What we're building, for whom, why now.**
- **Product:** Granola AI is an AI-powered notepad for product managers. It records computer audio locally and converts short, handwritten notes into formatted product documents like roadmaps and PRDs.
- **AI Value Archetype:** Automator
- **Vulnerability Scores:** Moat 3/5 | Data 2/5 | Platform 4/5
- **Top Risk:** Apple and Microsoft are adding free, native audio recording into their operating systems. This destroys Granola's main reason to exist, which is capturing meeting audio without a bot joining the call.
- **Confidence:** M
- **Prototype:** https://lovable.dev/projects/b4a5bced-1aac-493c-8945-6eaa4987e015
- **Kill Criteria:** We stop development if Apple or Microsoft release full system-level audio transcription for all third-party software, or if standard models can replicate this workflow out-of-the-box.

---

## The Moat (M2)
**Why this won't get copied in 6 months.**
- **Data Flywheel Score:** 9/20
- **Weakest Loop:** Network Loop (1/5)
- **Competitive Position:** The text editor is sticky because users must type while listening. However, the software cannot aggregate data across different companies, leaving it exposed to larger enterprise platforms.
- **Encroachment Defense:** Granola will stop acting as a standard document editor. It will become an open server framework using the Model Context Protocol. This lets developers feed accurate meeting data straight into engineering tools like Cursor or Claude Code.
- **Vendor Portability:** Partial
  - *Rationale:* Granola stores audio files and text notes locally on the user's computer. This data is easy to move. However, the logic that formats the notes belongs to OpenAI and Anthropic APIs. Changing those models will alter the output quality.

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):**
- **Gross Margin (AI-adjusted):**
- **Pricing Model:**
- **Cascading Strategy:**
- **Break-even at:**

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:**
- **Golden Dataset:** __ rows, __ adversarial
- **Confidence UX:** [approach]
- **HITL Architecture:**
- **Failure Mode Coverage:**

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales — and what compounds.**

- **Compounding System:** [describe feedback loops]
- **Governance Posture:** [approach]
- **Shadow AI Status:** __ tools found, __ triaged
- **Agent Boundaries:**
- **Regulatory Exposure:**

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
