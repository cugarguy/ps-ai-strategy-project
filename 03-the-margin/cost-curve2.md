# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
| --- | --- | --- |
| Inference (primary model) | $3.60 | Based on 30 meetings a month using Claude 3.5 Sonnet for deep document generation. |
| Inference (cascading/triage) | $0.45 | Built on GPT-4o-mini handling baseline keyword cleanups and text formatting. |
| Infrastructure | $2.50 | Covers Deepgram and AssemblyAI local audio ingestion and transcription pipelines. |
| Data/storage | $0.15 | Database synchronization and local vector chunk storage. |
| Human-in-the-loop | $0.00 | Zero operations cost because correction is fully user-driven. |
| **Total AI COGS** | **$6.70** | Total underlying monthly machine cost per product manager. |

## Cascading Strategy

| Feature Complexity | Model Tier | Cost/Req | Volume % | Weighted Cost |
| :--- | :--- | :--- | :--- | :--- |
| **Simple** (Shorthand cleanups, keyword expansion, formatting) | Small (GPT-4o-mini) | $0.005 | 60% | $0.09 |
| **Medium** (Standard meeting summary, action item extraction) | Mid (Claude 3.5 Haiku) | $0.020 | 30% | $0.18 |
| **Complex** (Multi-meeting search, cross-domain roadmapping, PRD generation) | Frontier (Claude 3.5 Sonnet) | $0.150 | 10% | $0.45 |
| **Blended** | | | **100%** | **$0.72 per meeting** |

*Note: Based on an average volume of 30 meetings per user per month, total monthly inference COGS is $21.60.*

**Triage model:** GPT-4o-mini
**Frontier model:** Claude 3.5 Sonnet
**Routing rule:** Route routine shorthand expansions, text formatting, and direct meeting summaries to the triage model. Route requests to the frontier model only when the user triggers cross-meeting analysis, deep repository search, or formal PRD document generations.
**Expected cascade ratio:** 90% triage / 10% frontier


## Pricing Model
1. **Pick your strategy**
Mine: Skim
2. **Name the unit of work**
Unit: Processed meeting hour
3. **Set the structure**
Base: $30/mo
Usage: $0.50/processed hour over 40 hours
**Pricing Model**
Current pricing: $10 / seat / month
Proposed AI pricing: $30 base tier up to 40 meeting hours, then usage-based billing
Model: Hybrid


## Stress Tests

| Scenario | Impact on Margin | Response |
| --- | --- | --- |
| Inference costs 3x | Gross margin turns negative on the old pricing tier as per-user COGS rises to $14.80. | Force prompt caching on custom templates and move initial processing onto local device chips. |
| Heaviest segment doubles | Heavy users running 60+ meetings a month drive cost to $13.40, consuming the profit margin. | Implement a 90-minute limit per meeting and introduce a metered overage charge for heavy users. |
| Model provider raises prices 50% | Monthly cost increases by $1.80 per user, shrinking gross margins by 18%. | Use an open proxy layer like LiteLLM to shift traffic instantly to lower-cost open-weight alternatives. |

## Board One-Pager

### Before — Traditional SaaS
- **Revenue:** $10 / seat × 100 seats ($1,000 total)
- **COGS:** $1.50 per seat (fixed server hosting)
- **Gross margin:** 85%

### After — AI-Powered
- **Revenue:** $30 base + $0.50 × hours over 40 hours ($3,000 base total)
- **COGS:** $21.60 per user (variable inference and transcription)
- **Gross margin:** 28%

### Net Margin Shift
- **Δ margin %:** -57%
- **Δ gross $:** +$19.00 per seat (Climbed from $8.50 to $27.50 gross profit per user at base volume)

### Narrative
We are trading high margin percentages for significantly larger gross profit dollars. The baseline SaaS version yielded $8.50 in gross profit per seat, while the AI version yields $27.50 per seat. This 3x increase in gross cash per user expands our net revenue retention because the software replaces manual engineering documentation labor. 

To hedge against heavy users eroding this margin, the hybrid pricing model applies a $0.50 per-hour fee above the 40-hour threshold. This coverage ensures that every added hour of meeting volume remains profitable.
