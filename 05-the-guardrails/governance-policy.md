## Governance Policy

**Scope:** 
* This policy covers AI features that capture meeting audio/transcripts, generate private meeting notes, extract decisions and action items, answer questions across authorized meeting history, apply user/team note templates, and send approved meeting outputs into downstream tools such as CRM, project management, Slack, email, or docs. Excludes: 
* This policy excludes internal employee use of general-purpose AI tools, non-product analytics dashboards, model vendor infrastructure controls, and company-wide security policy outside the meeting-intelligence product.

**Autonomy boundaries:** Generate private notes from meetings the user intentionally captures. 
* auto. Summarize meetings, extract decisions, identify action items, and apply user-selected templates. 
* auto. Answer questions using only meetings, folders, and notes the requesting user is authorized to access. 
* auto. Suggest follow-up emails, CRM updates, task tickets, and project summaries as drafts. 
* auto. Share notes with another person, team, customer, or external domain. 
* human approval required. Send follow-up emails or messages. 
* human approval required. Create or update CRM records, support tickets, project tickets, or customer-facing documents. 
* human approval required. Use meeting content for durable personalization, team memory, or model-improvement loops. 
* human approval required. Export content containing customer data, confidential business data, regulated data, or sensitive employee information. 
* human approval required. Capture, record, or summarize a meeting without user intent and required participant notice/consent. 
* never auto. Send messages as the user. 
* never auto. Make pricing, legal, HR, medical, financial, security, contractual, or policy commitments. — never auto. Expose private notes, transcripts, or summaries to unauthorized users. 
* never auto. Train on customer content unless explicitly permitted by user setting, tenant policy, and contract. 
* never auto. Delete, merge, or permanently alter meeting records without explicit user action. 
* never auto.

**Escalation triggers:** 
* Confidence is below 70%. 
* The output includes a quote, commitment, decision, or action item without source support. 
* The meeting contains legal, HR, medical, financial, security, incident-response, acquisition, board, compensation, or customer-confidential content. 
* The action would share, export, send, create, update, or delete content outside Granola. The recipient is outside the user’s organization. 
* The user asks the AI to “send,” “commit,” “promise,” “approve,” “file,” “escalate,” “refund,” “price,” “terminate,” or “notify.” 
* Permission checks fail or the requested answer crosses folders, teams, customers, or private notes. 
* A user disputes an AI-generated note, action item, quote, or decision.

**Audit cadence:** 
* Real-time — permission checks, sharing events, external tool calls, export attempts, failed access attempts, and blocked actions (Security Engineering).
* Daily — eview blocked external shares, failed permission checks, anomalous exports, and high-risk escalation events (Product Operations).
* Weekly — run evals against the golden dataset for note accuracy, decision extraction, action-item precision, quote fidelity, privacy redaction, and cross-meeting answer grounding (AI Product Manager).
* Monthly — review sampled user-approved outputs, escalation queues, correction patterns, template failures, and downstream workflow errors (Product + Legal + Security).
* Quarterly — review model/vendor changes, retention policy, consent language, enterprise admin controls, regulatory exposure, SOC 2 evidence, and customer-facing governance artifacts (CTO or Head of Product Security).

**Regulatory exposure (EU AI Act / other):** 
* GDPR / UK GDPR for personal data in meetings, transcripts, notes, and user identity.
* CCPA/CPRA for applicable US consumer and employee data.
* Call-recording and consent rules by jurisdiction.
* SOC 2 / enterprise security commitments for access control, logging, retention, and vendor oversight.
* EU AI Act: likely limited-risk for general meeting-assistant use; may become high-risk if positioned for employment, performance evaluation, legal, credit, healthcare, or education decisions.. Risk tier: limited. Controls: User-initiated capture only.
* Clear meeting notice and consent flow.
* Role-based access control by user, folder, team, and workspace.
* Private-by-default notes.
* Explicit approval for external sharing and tool writes.
* Tenant-level controls for retention, training opt-out, sharing, exports, and integrations.
* Encryption in transit and at rest.
* Audit logs for access, sharing, exports, model calls, and tool calls.
* Data minimization in prompts.
* Vendor DPAs and subprocessors reviewed quarterly.
* Customer content excluded from model training unless explicitly opted in and contractually permitted..

## Agent Topology

Notes Agent:
* Can transcribe, summarize, extract decisions, and generate action items from authorized meetings.
* Cannot share, send, export, or update external systems. Approval owner: user.

Memory Agent:
* Can answer questions across meetings, folders, and workspace content the user is authorized to access.
* Cannot cross private folders, infer missing facts, or answer without source grounding. Approval owner: Product + Security.

Workflow Agent:
* Can draft CRM updates, task tickets, follow-up emails, handoff summaries, and project notes.
* Cannot write to external systems or send messages without user approval. Approval owner: user; enterprise admins may restrict tools.

Governance Agent:
* Can block risky outputs, enforce permission checks, log tool calls, flag low-confidence answers, and route escalations.
* Cannot override user/admin policy or silently approve external actions. Approval owner: Security Engineering.
