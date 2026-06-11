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



--- 
## Source Data

Based on Granola's current [Business plan pricing ($14/user/month)](https://www.granola.ai/pricing), its target demographic of executive power users, and baseline SaaS infrastructure metrics, here is a unit economics estimation for the platform. [1, 2, 3, 4] 
## 1. Average AI Requests Being Made
Granola operates via a unique "no-bot" architecture where a user manually clicks "Enhance" after a meeting to process a locally recorded transcript. [1] 

* Meetings per User: As established, the blended average across free and paid accounts sits at roughly 10 meetings per user per week.
* Monthly Base Requests: 10 meetings × 4.35 weeks = ~43.5 core transcription/summary requests per user per month.
* Downstream Requests: Users frequently make secondary requests (e.g., querying the meeting notes using Granola's chat interface, syncing customized templates to CRMs like HubSpot/Attio, or pushing action items to Slack). Assuming 1.5 follow-up prompts per meeting, this adds ~65 micro-requests.
* Total Estimated AI Requests: ~108 requests per user per month. [3, 4] 

## 2. Blended Cost Per Request
Granola utilizes a multi-model approach, routing heavy text formatting and synthesis to advanced LLMs (like Anthropic's Claude or OpenAI's GPT-4o) while processing the raw audio-to-text locally or through highly optimized Whisper-based endpoints. [3, 5, 6] 

* Audio Transcription Cost: A standard 45-minute meeting processed via high-quality API endpoints averages $0.015 to $0.03. [7] 
* LLM Reasoning & Summary Cost: For a ~6,000-word transcript tokenized into an LLM prompt, input and output tokens for a dense summary call cost roughly $0.02 to $0.04.
* Blended Cost per Core Request: ~$0.05 per meeting session.
* If counting downstream chat micro-requests (which use far fewer output tokens), the macro-blended cost drops to ~$0.02 to $0.03 per individual API call.

## 3. Revenue Per User / Month [4] 
Granola operates a freemium model with distinct tiers: [2, 8] 

* Basic Tier: $0 (Free, but caps your searchable meeting history to 25 notes).
* Business Tier: $14 per user / month (Paid monthly) or $10–$12 if billed annually.
* Enterprise Tier: [$35+ per user / month](https://www.granola.ai/blog/granola-pricing-teams-per-user-enterprise) (Includes dedicated features like advanced SSO, organization-wide AI training opt-outs, and priority support). [2, 3, 4, 9] 

Considering a standard B2B SaaS freemium funnel with a high executive mix (~15% to 20% conversion to paid seats):

* Blended Average Revenue Per User (ARPU): ~$2.50 to $3.50 per month across all active workspace users.
* Paid ARPU: ~$14.00 per month for the standard core cohort. [2, 9] 

## 4. Non-AI COGS / User / Month [4] 
Because Granola does not utilize heavy cloud-based cloud-bots (like Fireflies or Otter) to dial into virtual meetings as an active video participant, their non-AI server overhead is remarkably lean. They don't have to pay for the massive video/audio streaming compute required to keep a web-bot sitting inside a 60-minute Zoom call. [1, 7] 

* Database & Hosting (AWS/Vercel): Storing clean markdown text summaries, meeting metadata, and basic calendar sync vectors costs roughly $0.05 to $0.10 per user / month. [3, 10] 
* Authentication, Integrations, & APIs: Managing integrations with platforms like Notion, Slack, and Salesforce via tools like Zapier or internal webhooks averages $0.05 per user / month. [3] 
* Total Non-AI COGS: ~$0.10 to $0.15 per active user / month.

[1] [https://zackproser.com](https://zackproser.com/blog/granola-ai-review)
[2] [https://www.granola.ai](https://www.granola.ai/blog/granola-pricing-teams-per-user-enterprise)
[3] [https://www.granola.ai](https://www.granola.ai/pricing)
[4] [https://www.granola.ai](https://www.granola.ai/blog/granola-pricing-plans-features-roi)
[5] [https://docs.granola.ai](https://docs.granola.ai/help-center/consent-security-privacy/model-training)
[6] [https://www.instagram.com](https://www.instagram.com/reel/DQekWrHEong/)
[7] [https://www.granola.ai](https://www.granola.ai/blog/ai-meeting-notes-pricing-granola-costs-less-alternatives)
[8] [https://www.brex.com](https://www.brex.com/tools/charge-finder/granola)
[9] [https://get-alfred.ai](https://get-alfred.ai/blog/granola-pricing)
[10] [https://docs.granola.ai](https://docs.granola.ai/help-center/getting-started/syncing-your-calendars)


