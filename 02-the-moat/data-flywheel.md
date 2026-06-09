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
**Attacker:**
**Vector:**
**Time-to-threat:**
**% of value at risk:**

### 2. Vertical Competitor
**Attacker:**
**Vector:**
**Time-to-threat:**
**% of value at risk:**

### 3. Adjacent Expansion
**Attacker:**
**Vector:**
**Time-to-threat:**
**% of value at risk:**

---

## 90-Day Encroachment Plan

*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:**
**Attack vector (target the weakest loop):**
**Weeks 1-4 - what they ship:**
**Weeks 5-8 - how they poach users:**
**Weeks 9-12 - why users don't come back:**
**Your defense:**
