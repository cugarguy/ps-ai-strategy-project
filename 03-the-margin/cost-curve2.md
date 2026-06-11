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

**Triage model:** GPT-4o-mini
**Frontier model:** Claude 3.5 Sonnet
**Routing rule:** Route routine transcripts and direct formatting requests to the triage model. Scale to the frontier model only when the user triggers cross-meeting analysis, workspace search, or large PRD generations.
**Expected cascade ratio:** 80% triage / 20% frontier

## Pricing Model

**Current pricing:** $10 / seat / month
**Proposed AI pricing:** $30 / seat / month
**Model:** Seat-based with a soft usage cap at 40 meetings a month.

## Stress Tests

| Scenario | Impact on Margin | Response |
| --- | --- | --- |
| Inference costs 3x | Gross margin turns negative on the old pricing tier as per-user COGS rises to $14.80. | Force prompt caching on custom templates and move initial processing onto local device chips. |
| Heaviest segment doubles | Heavy users running 60+ meetings a month drive cost to $13.40, consuming the profit margin. | Implement a 90-minute limit per meeting and introduce a metered overage charge for heavy users. |
| Model provider raises prices 50% | Monthly cost increases by $1.80 per user, shrinking gross margins by 18%. | Use an open proxy layer like LiteLLM to shift traffic instantly to lower-cost open-weight alternatives. |

## Board One-Pager

**Before (traditional SaaS):** Flat $10 monthly seat price for basic local note storage. Low server cost but limited expansion.
**After (AI-enabled):** Premium $30 monthly tier providing automatic PRD creation and institutional product memory.
**Net margin shift:** Gross profit climbs from $3.30 to $23.30 per seat. Shifting 80% of routine processing to the triage model protects this margin at scale.
