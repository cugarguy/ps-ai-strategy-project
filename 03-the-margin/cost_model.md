Here is the completed form populated for Granola AI, synthesizing our previous unit economics estimations with the framework principles outlined in the AI Product Strategy curriculum.
------------------------------
## Cost Curve & Pricing Strategy## Cost Model

| Cost Category | Per-User/Month | Notes |
|---|---|---|
| Inference (primary model) | $1.30 | Frontier model (e.g., Claude 3.5 Sonnet / GPT-4o) processing ~43.5 core synthesis requests. |
| Inference (cascading/triage) | $0.87 | Lower-tier model / API (e.g., Whisper + GPT-4o-mini) managing audio transcription and formatting. |
| Infrastructure | $0.08 | Fixed cloud costs (AWS/Vercel) for application hosting and background tasks. |
| Data/storage | $0.05 | Minimal storage needed; text-only markdown profiles and vector index syncs. |
| Human-in-the-loop | $0.00 | Fully automated software loop; zero manual review or human annotation layer. |
| Total AI COGS | $2.30 | Variable token overhead represents the vast majority of user cost. |

## Cascading Strategy

* Triage model: OpenAI Whisper (for audio-to-text) + GPT-4o-mini (for rough formatting).
* Frontier model: Claude 3.5 Sonnet / GPT-4o (for final executive summary generation).
* Routing rule: Route 100% of raw audio through Whisper/mini to extract and clean text payload. Apply a semantic compression script, then send only the high-value compressed meeting notes to the Frontier model for template generation and synthesis.
* Expected cascade ratio: 80% of token compute handled on cheap/local triage models, 20% routed to frontier engines.

## Pricing Model

* Current pricing: $14 / user / month (Business Tier).
* Proposed AI pricing: $14 / user / month flat-rate core seat, supplemented by a $35 Enterprise Tier.
* Model: Hybrid. Keep the core AI workspace seat-based since note-taking is a "Leader" feature used by 100% of the active cohort. Charge on an Outcome-based structure for deep downstream automated workflows (e.g., $0.10 per direct CRM/HubSpot field auto-update).

## Stress Tests

| Scenario | Impact on Margin | Response |
|---|---|---|
| Inference costs 3x | Inference jumps to $6.51/mo. Gross margin on a $14 seat drops from 83.5% to 52.8%. | Implement localized on-device quantization models for basic text cleaning; enforce stricter template output token limits. |
| Heaviest segment doubles | Heavy users (20+ meetings/wk) double variable inference to $4.34/mo, compressing margins to ~68%. | Establish a "fair use" monthly meeting soft cap (e.g., 60 meetings/mo), prompting power users to transition to the Enterprise tier. |
| Model provider raises prices 50% | Total COGS climbs by ~$1.09/mo, shifting gross margin down to ~76%. | Swap the triage tier to open-weights models (e.g., Llama 3) hosted on dedicated internal instances to bypass commercial API price shifts. |

## Board One-Pager

* Before (traditional SaaS): Granola acts as a local text editor with simple cloud syncing. Infrastructure cost is a fixed $0.15/user/month. At $14/month revenue, the product enjoys a 98.9% gross margin.
* After (AI-enabled): Granola functions as a full-service automated executive secretary. Variable inference injection introduces a dynamic $2.17 cost per user. Total COGS reaches $2.30/user/month.
* Net margin shift: Gross margins contract from 98.9% down to 83.5%. While the margin profile shifts down, the deep stickiness of the AI workspace increases LTV (Lifetime Value) and dramatically lowers customer churn, justifying the variable token trade-off.

------------------------------
If you want to refine this model further, let me know if we should:

* Adjust the average meetings per month slider to see the margin breaking point.
* Map out the specific open-weights architecture needed to replace the OpenAI/Anthropic APIs.
* Draft the financial scenario for shifting entirely to an outcome-based pricing model.

Which lever should we stress-test next?

