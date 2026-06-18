## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Recursive Learning | User edits to AI-generated notes; deleted or rewritten bullets; corrected action items; speaker corrections; preferred templates by meeting type | Future notes match the user’s preferred structure, tone, level of detail, action-item format, and follow-up style | Y | broken |
| Cross-Domain Transfer | Prior meetings by customer, project, topic, team, and attendee; calendar context; folder-level meeting history; repeated decisions and unresolved action items | Pre-meeting briefs, better continuity across recurring meetings, surfaced patterns across customer calls, and stronger recall of prior decisions | Y | active |
| Network Intelligence | Privacy-gated aggregate patterns across meetings: common meeting types, accepted note structures, frequent edits, common action-item formats, anonymized correction trends | Better default templates, stronger summarization heuristics, better action-item detection, and improved meeting-type classification | Y | broken |
| Workflow Completion | Action items, owners, due dates, follow-up emails, project-plan requests, CRM/update destinations | Meetings turn into completed next steps, not just stored notes | Y | missing |




**Broken loop identified by partner:** Recursive Learning is leaking the most value. Users correct Granola’s notes, rewrite summaries, adjust formatting, and clean up action items, but those corrections are not yet reliably converted into durable user/team preferences or eval data.

**Fix plan:** Starting Monday, capture every user edit as structured feedback: deleted AI text, rewritten bullets, accepted/rejected action items, speaker corrections, and template changes. Convert those edits into a user/team preference profile and a weekly golden-dataset update. Use the profile to personalize future summaries by meeting type, customer, and team. Add a visible “learn from this edit” control so users can distinguish one-off cleanup from durable preference.


## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

**How knowledge flows:** Knowledge flows well inside a single note and partially across a folder of related meetings. 

**Where it silos:** It silos when meetings are split across private notes, personal folders, different teams, CRM systems, project tools, and unshared customer histories. The biggest compounding blocker is that meeting intelligence often stops at the note instead of flowing into CRM, product feedback, project plans, and follow-up workflows.
