# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | | |
| Inference (cascading/triage) | | |
| Infrastructure | | |
| Data/storage | | |
| Human-in-the-loop | | |
| **Total AI COGS** | | |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:**
**Frontier model:**
**Routing rule:**
**Expected cascade ratio:**

## Pricing Model

**Current pricing:**
**Proposed AI pricing:**
**Model:** seat-based / usage-based / outcome-based / hybrid

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | | |
| Heaviest segment doubles | | |
| Model provider raises prices 50% | | |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
**After (AI-enabled):**
**Net margin shift:**








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

