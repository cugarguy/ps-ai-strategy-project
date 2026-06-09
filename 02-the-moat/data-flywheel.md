# Data Flywheel Map

> Score each loop 1-5. Your weakest loop is where competitors attack first.
> The four loops below are the M2 starting point - adapt if your product has 2 or 6 loops instead of 4.

## Flywheel Loops

| Loop | What It Measures | Score 1 | Score 5 | Score |
|------|------------------|---------|---------|-------|
| **Correction** | Do users fix AI outputs? Is that signal captured and reused? | No capture | Automated retraining | 3/5 |
| **Preference** | Does the product learn individual / team preferences over time? | Stateless | Deep personalization | 3/5 |
| **Domain Context** | Does usage in one area improve quality in adjacent areas? | Siloed | Cross-domain transfer | 2/5 |
| **Network** | Does each new user / team make the product better for everyone? | Isolated | Strong network effects | 1/5 |

### Correction Loop - 3/5
**What you capture today:** Granola captures inline edits when a PM overwrites generated bullet points, updates a user story, or manually rewrites an AI-generated PRD summary.
**How it compounds:** These edits change the current document immediately and adjust the user prompt's few-shot examples for the next meeting. However, because Granola doesn't train underlying foundational models due to strict enterprise privacy agreements, this signal remains locked in a local prompt-engineering feedback loop rather than building a compounding, generalized model edge.

### Preference Loop - 3/5
**What you capture today:** Custom user-defined "Recipes" (e.g., “Format this like a Linear ticket” or “Extract tech debt mentions”), alongside frequent acronyms, slang, and team-specific technical jargon.
**How it compounds:** It creates a highly sticky, deeply personalized local translation layer. The more a product team populates their specific formatting recipes, the harder it is for them to transition to a generic out-of-the-box system notetaker without rebuilding that structural template layout.

### Domain Context Loop - 2/5
**What you capture today:** Historical context across sequential team meetings within a single project directory or "Space." 
**How it compounds:** If a user mentions a feature discussed three weeks ago, Granola can link back to that specific historical context through cross-meeting semantic search. The failure point is adjacent transfer: insights gathered by Product Team A during user interviews do not automatically or intelligently enrich the roadmap assumptions or engineering constraints of Product Team B without manual sharing.

### Network Loop - 1/5
**What you capture today:** Shared workspaces, comments, and collaborative note cleanups.
**How it compounds:** here is virtually no true data network effect. A team of 50 PMs using Granola does not make the underlying core utility inherently more intelligent or predictive for a new 51st user. The value scales linearly with deployment size, not exponentially. 

**Total Flywheel Score: 9/20**
**Weakest Loop:** Network loop
**Fix for weakest loop:** Transform Granola from a passive workspace collector into an active Internal Product Knowledge Graph. Instead of treating meetings as isolated text assets, Granola needs to automatically extract and map entities (e.g., cross-referencing “Feature X” mentioned by a client in a sales call with a “blocker” logged in an engineering syncing session). By automatically constructing an organizational Model Context Protocol (MCP) server that exposes these interconnected relationships, each new team member joining the workspace instantly increases the accuracy and context windows of everyone else's autonomous AI workflows.

---

## Encroachment Threat Assessment

### 1. Platform Encroachment
**Attacker:** Apple / Microsoft (System OS level)
**Vector:** Implementing native, local system-audio recording wrappers directly into the kernel architecture (e.g., Apple Intelligence native audio routing or Windows Recall API extensions). This entirely bypasses the need for an application to handle audio loopback routing.
**Time-to-threat:** 6–12 months
**% of value at risk:** 65% (Destroys Granola’s core client acquisition engine: "the transcription utility without a bot").

### 2. Vertical Competitor
**Attacker:** Productboard / Dovetail
**Vector:** Adding an un-intrusive desktop audio recording application that directly drops transcribed, synthesized user feedback into their existing, deeply entrenched product roadmapping and telemetry dashboards.
**Time-to-threat:** 3–6 months
**% of value at risk:** 45% (Poaches high-value enterprise product organizations who want a tight link between raw audio text and formal feature roadmap tracking).

### 3. Adjacent Expansion
**Attacker:** Notion / Slack
**Vector:** Launching a native huddle or scratchpad recorder that syncs perfectly with enterprise wikis. Notion AI natively expanding sparse bullet points inside a team workspace removes the need to copy-paste data out of Granola entirely.
**Time-to-threat:** 6 months
**% of value at risk:** 0% (Eliminates downstream workflow integration value).

---

## 90-Day Encroachment Plan

*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:** Microsoft (Teams Ecosystem + Copilot Studio)
**Attack vector (target the weakest loop):** Exploding the Network Loop. Microsoft weaponizes its native enterprise graph data, combining local Teams system audio capture with existing Outlook emails, Azure DevOps logs, and Word docs—providing a unified context layer Granola cannot match.
**Weeks 1-4 - what they ship:** 
- The "Ghost Recorder" Feature: Microsoft ships a quiet update to the Windows/Teams ecosystem allowing background local-audio transcription without an inviting bot, entirely neutralizing Granola's primary UX hook.
- Inline "Shorthand" Capture: They introduce a minimalist text widget overlay inside Teams called "Copilot Scratchpad" that copies Granola’s core interaction loop: type 3 words during a call, and Copilot expands it using local context.
**Weeks 5-8 - how they poach users:**
- The Downstream Multi-Silo Stitch: Microsoft hooks this local transcription data directly into Azure DevOps, Loop, and Outlook. If a PM types a shorthand note during a call, Copilot automatically generates the formal epic, links it to active engineering sprint items, and drafts the release email in Outlook with zero copy-pasting.
- Zero-Dollar Pricing: They offer this functionality completely free within standard enterprise E5 licenses, framing Granola as an unnecessary, redundant per-seat cost.
**Weeks 9-12 - why users don't come back:** 
**Your defense:** 
- The Organizational Data Gravity: Because Microsoft's tool actively populates the enterprise-wide knowledge base across all departments (Sales, Engineering, Support), it builds a compounding organizational data moat.
- A PM cannot return to Granola because Granola only knows what the PM typed, whereas Microsoft's ecosystem knows what the client told the sales rep, what engineering logged in a ticket, and what the executive team outlined in a strategy brief.
