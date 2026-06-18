# Shadow AI Audit (user-side) — Module 5

## Discover — User-Side Workarounds
- Users copy Granola notes into ChatGPT or Claude to draft follow-up emails | source: User interview | signal: Workflow gap | freq: H | spend: $25/mo | decision: Build
- Sales users paste meeting notes into Salesforce / HubSpot to create CRM updates and next steps | source: Sales call | signal: Workflow gap | freq: H | spend: $50/mo | decision: Build
- Sales users paste meeting notes into Salesforce / HubSpot to create CRM updates and next steps | source: User interview | signal: Capability gap | freq: H | spend: $30/mo | decision: Build
- Teams export notes into Notion, Google Docs, or Confluence to create shared account/project memory | source: Support ticket | signal: Workflow gap | freq: M | spend: $20/mo | decision: Partner
- Managers use ChatGPT to convert multiple 1:1 or team meeting notes into performance summaries and coaching themes | source: User interview | signal: Trust gap | freq: M | spend: $25/mo | decision: Ignore
- Users use Zapier / Make / manual copy-paste to turn action items into Linear, Asana, Jira, or Todoist tasks | source: Other | signal: Workflow gap | freq: M | spend: $35/mo | decision: Partner
- Customer-facing teams use AI to rewrite notes into polished external recaps before sharing | source: User interview | signal: Trust gap | freq: H | spend: $20/mo | decision: Build
- Users compare Granola outputs against Fathom, Fireflies, or Otter when they need team-visible recordings, transcripts, or searchable meeting libraries | source: Other | signal: Capability gap | freq: M | spend: $40/mo | decision: Partner
- Executives ask ChatGPT questions across exported notes to identify commitments, risks, and decisions across a week or account | source: Other | signal: Capability gap | freq: M | spend: $30/mo | decision: Build
- Users manually redact sensitive details before sharing AI-generated notes externally | source: User interview | signal: Trust gap | freq: M | spend: $15/mo | decision: Build

## Pattern Assessment
- Workarounds found: 10
- Build candidates: 6
- Partner candidates: 3
- Ignore decisions: 1
- Adjacent spend: $290/mo
- Dominant signal: Workflow gap

## Action Plan
### Build
- Native follow-up email drafter from meeting notes.
- Native CRM update generator for Salesforce / HubSpot fields, next steps, risks, and account notes.
- Customer-insight synthesis across meetings, accounts, folders, and projects.
- External recap mode with tone, redaction, and approval controls.
- Executive weekly memory query: commitments, decisions, risks, blockers, and owner follow-ups.
- Sensitive-content detection before sharing or exporting notes.

### Partner
- Project/task tools: Linear, Jira, Asana, Todoist.
- Knowledge-base destinations: Notion, Google Docs, Confluence.
- Meeting-library / recording-heavy workflows where users need video, transcript archives, or compliance review.

### Ignore + Monitor
- HR/performance-summary use cases. Monitor because they create regulatory and trust exposure; do not build until governance, consent, and enterprise admin controls are stronger.

## Roadmap Brief
- Based on your audit: 10 user-side workarounds discovered.
- Decisions: 6 build · 3 partner · 1 ignore · 0 TBD.
- Estimated adjacent spend: $290/mo across surveyed users.
- Dominant signal: Workflow gap.

- Granola users are not just taking notes; they are moving meeting intelligence into follow-ups, CRM, product feedback, project tools, and executive memory. The dominant shadow-AI pattern is a workflow gap: users trust Granola to capture the meeting, then leave the product to turn notes into work. The highest-priority build opportunities are native follow-up drafting, CRM-ready updates, customer-insight synthesis, and share-safe external recaps. Partner opportunities should focus on task systems and knowledge-base destinations rather than rebuilding every downstream workflow. The main governance watchpoint is users applying meeting notes to HR, performance, or sensitive decision workflows without consent, policy, or audit trail.

- Recommended next step: Workflow gaps dominate — your users are stitching your product into multi-step pipelines. Strongest near-term move is partner integrations with the AI tools they already chain in.

- Sequence the Build column by frequency × strategic relevance. Confirm Partner candidates with the external tools' partnership teams. Re-run this audit each quarter — workarounds shift fast.
