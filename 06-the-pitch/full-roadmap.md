# Sorted Backlog (Full Roadmap)

### Horizon 1 — Ship (0–4 weeks)

| Initiative | Strategy Component | Why it ships now | Confidence |
| --- | --- | --- | --- |
| **GRAN-001** Bot-free local system audio capture | Bet | Foundations for non-invasive capturing are vital before any other feature functions. | H |
| **GRAN-002** Meeting transcript ingestion and cleanup | Bet | Downstream value relies on clean transcripts; core data foundation must exist now. | H |
| **GRAN-003** Live shorthand note capture | Bet | Validates the primary proprietary text-editor interaction mode immediately. | H |
| **GRAN-004** Shorthand-to-audio timestamp map | Bet | Crucial architecture choice to link user intent directly to the captured source. | H |
| **GRAN-005** Post-meeting Enhance flow | Bet | Validates the core Automator utility loop for early adopters within days. | H |
| **GRAN-006** Structured meeting note editor | Bet | The sticky text workspace must be live to house the generated summaries. | H |
| **GRAN-007** Default summary and next-step generation | Bet | Necessary baseline value fallback when users do not provide explicit shorthand. | H |
| **GRAN-011** Transcript source viewer | Contract | Drives foundational user trust by exposing the evidence behind generated points. | H |
| **GRAN-012** Speaker attribution support | Contract | Addressed failure mode explicitly mentioned in the Contract strategy. | H |
| **GRAN-024** Action item extraction with owner/due date | Guardrails | Addresses the missing workflow loop by pulling explicit downstream metrics out. | H |
| **GRAN-032** Workflow review inbox | Contract | Delivers the critical desktop inbox review queue for human-in-the-loop (HITL). | H |
| **GRAN-034** External tool approval orchestration | Guardrails | Powers the Governance Posture requirement for human approval on external sharing/writes. | H |
| **GRAN-035** Integration permission scopes | Guardrails | Foundational constraint needed to fulfill regulatory and security posture mandates. | H |
| **GRAN-039** Structured edit telemetry capture | Guardrails | Essential to fix the broken recursive learning loop by collecting user edits. | H |
| **GRAN-040** Learn-from-this-edit control | Guardrails | Immediate user-facing mechanism to start capturing durable formatting preferences. | M |
| **GRAN-041** User and team preference profile | Guardrails | Database layer required to house the style/format rules captured from user edits. | H |
| **GRAN-046** Golden dataset expansion to 100+ cases | Contract | Critical engineering fix to stabilize verification testing beyond the current 5 rows. | H |
| **GRAN-047** Automated formatting regression tests | Contract | Ensures prompt and model optimizations do not alter the sticky text editor layout. | H |
| **GRAN-048** LLM and rule-based judge harness | Contract | Powers automated validation of summaries, speaker tags, and acronyms. | H |
| **GRAN-049** Reliability metrics dashboard | Contract | Essential telemetry platform to monitor hallucination rates and accuracy. | H |
| **GRAN-050** Hallucination and grounding detector | Contract | Guardrail engine to surface low-confidence outputs before they reach the user. | H |
| **GRAN-053** Confidence scoring pipeline | Contract | Generates the raw scores required to drive the Tiered Confidence UX layout. | H |
| **GRAN-054** Tiered confidence highlighting | Contract | Delivers the user-facing visibility architecture for uncertainty. | H |
| **GRAN-055** Low-confidence export blocker | Guardrails | Security policy layer to stop raw ungrounded facts from shifting out of the application. | H |
| **GRAN-056** Capture consent and notice flow | Guardrails | Non-negotiable feature required for regulatory compliance under CPRA/GDPR. | H |
| **GRAN-057** Sensitive-content detection | Guardrails | Immediate trigger mechanism to route HR/Legal/Financial logs to human review. | H |
| **GRAN-058** Permission-grounded Q&A | Guardrails | Enforces information containment bounds for localized data search actions. | H |
| **GRAN-059** External sharing approval gate | Guardrails | Core security mechanism to ensure data never leaves local boundaries automatically. | H |
| **GRAN-060** External write/send approval gate | Guardrails | Core security mechanism for CRM, email, and messaging task creation. | H |
| **GRAN-061** Escalation trigger engine Engine | Guardrails | Infrastructure to shift actions to human review if confidence falls below 70%. | H |
| **GRAN-062** Audit log for AI actions | Guardrails | Enterprise compliance foundation to record data processing and user actions. | H |
| **GRAN-063** Enterprise training opt-out policy | Guardrails | Closes risk vector for corporate tenants concerned about model exposure. | H |
| **GRAN-065** Redaction before external share | Guardrails | Protects information privacy constraints when compiling final notes. | H |
| **GRAN-067** Commitment/regulated-advice blocker | Guardrails | Direct agent safety policy layer to prevent autonomous company liability. | H |
| **GRAN-068** Usage metering by hours & actions | Margin | Essential data logging mechanism required to track model costs and bill outcomes. | H |
| **GRAN-070** Model cascading router | Margin | Immediately delivers the 80% triage / 20% frontier economic architecture. | H |
| **GRAN-073** Unified model provider abstraction | Margin | Isolates application logic from model dependencies to allow flexible switching. | H |
| **GRAN-074** Provider failover and cost balancing | Margin | Protects core margins from platform rate shifts or third-party outages. | H |
| **GRAN-080** Two-week PM cohort trial instrumentation | Bet | Validates core customer behavior parameters via the Lovable shell prototype. | H |
| **GRAN-081** Native OS audio layer assessment | Bet | High-priority technical spike addressing the absolute existential platform risk. | H |

---

### Horizon 2 — Validate (1–3 months)

| Initiative | Strategy Component | Hypothesis | Kill Criteria | Confidence |
| --- | --- | --- | --- | --- |
| **GRAN-008** PM artifact template library | Bet | PMs will convert meetings into specialized roadmaps/PRDs if templates are built-in. | If fewer than 30% of trials generate a formal PRD or roadmap by week 4, we stop template expansions. | M |
| **GRAN-009** Custom team templates | Bet | Allowing custom configurations decreases seat churn and cements workspace stickiness. | If teams do not build at least one custom template within 30 days of onboarding, we pause team features. | M |
| **GRAN-010** AI recipe selector | Bet | Users need upfront control to select the output layout shape prior to compilation. | If the selector is left on default settings by 85% of power users by week 6, we remove the UI step. | M |
| **GRAN-013** Domain acronym expansion | Contract | Custom vocabulary handling raises contextual note reliability past the 95% target. | If acronym overrides do not drop total user editing time by 15% by week 4, we freeze the expansion model. | M |
| **GRAN-014** Cross-language translation flag | Contract | Multilingual teams need explicit flags to prevent translation errors in notes. | If the translation flag is triggered on less than 2% of total logged hours by week 6, we drop the flagging engine. | M |
| **GRAN-015** Authorized meeting history search | Guardrails | localized history query adds cross-domain context without breaking data lines. | If users run fewer than 2 history searches per week by month 2, we deprecate the custom history tool. | M |
| **GRAN-016** Prior decision Q&A | Guardrails | Context-bounded retrieval answers prevent ungrounded hallucinations about history. | If accuracy score on decision lookups stays under 90% during internal evals by week 6, we kill the tool. | M |
| **GRAN-018** Pre-meeting brief generator | Guardrails | Combining cross-domain data creates a compounding asset users read before calls. | If fewer than 20% of generated briefs are opened by users before scheduled meetings, we kill the builder. | M |
| **GRAN-020** Unresolved action item carryover | Guardrails | Tracking action chains across calls bridges the broken workflow completion loop. | If carried-over action items are deleted or ignored by users 70% of the time, we drop the tracker loop. | M |
| **GRAN-025** Follow-up email drafter | Guardrails | Providing a secure email draft workspace improves the speed of downstream workflows. | If fewer than 40% of generated email drafts are exported or sent by week 4, we stop integration expansion. | M |
| **GRAN-026** External recap mode | Guardrails | Regulated tone/redaction controls allow secure external distribution without leaks. | If users manually rewrite over 50% of external recaps before sharing, we halt the feature for redesign. | M |
| **GRAN-027** CRM update generator | Margin | Monetizing outcome-based CRM field writes unlocks the hybrid revenue model strategy. | If less than 10% of active seats connect CRM credentials within 45 days, we reconsider the pricing structure. | M |
| **GRAN-028** Project task draft generator | Guardrails | Automated ticket drafts turn passive note storage into active workflow items. | If fewer than 25% of generated task drafts are pushed into Jira/Linear, we freeze ticket integrations. | M |
| **GRAN-029** Knowledge-base export workflow | Guardrails | Exporting notes directly into tools like Notion enhances daily usage stickiness. | If fewer than 15% of daily active users leverage the wiki export button by week 6, we stop native connections. | M |
| **GRAN-030** Slack/message draft workflow | Guardrails | Safe messaging drafts reduce time-to-broadcast for core product choices. | If Slack draft edits take longer than writing the message manually, we remove the messaging pipeline. | M |
| **GRAN-031** Formal PRD/roadmap generation | Guardrails | Aggregating insights from multiple meetings changes artifact generation velocity. | If multi-meeting synthesis fails to score 4/5 on usefulness in user trials by week 8, we kill the feature. | M |
| **GRAN-036** Local files and vector index sync | Moat | Local vector index isolation maintains partial portability while powering search. | If local index size compromises application performance on standard setups by week 6, we shift strategies. | M |
| **GRAN-042** Weekly eval dataset update | Contract | Automated correction pipelines scale the evaluation dataset without privacy issues. | If the pipeline fails to catch at least 3 prompt regressions during evals by month 2, we kill the automation. | M |
| **GRAN-044** Team vocabulary dictionary | Guardrails | A shared team glossary prevents acronym failure modes during synthesis. | If team dictionary entries are updated less than once a month per group, we retire the team glossary UI. | L |
| **GRAN-045** Prompt example updater | Guardrails | Few-shot update patterns can adjust style layouts without training costs. | If dynamically injected prompt examples cause latency drift over p95 targets, we kill the updater. | M |
| **GRAN-051** Latency p95 instrumentation | Contract | Tracking per-stage bottlenecks identifies whether cascading model routers slow usage. | If optimizing latency from data points fails to lower p95 under 5 seconds, we scrap the tracking framework. | M |
| **GRAN-052** Drift velocity monitor | Contract | Tracking quality shifts across model changes protects baseline reliability scores. | If the drift monitor generates false alarms on 80% of minor prompt shifts, we stop monitor development. | M |
| **GRAN-064** Data retention/explicit delete | Guardrails | Direct retention management tools are required to close enterprise sales cycles. | If enterprise buyers do not require automated retention configs during sales calls, we shelve the panel. | M |
| **GRAN-069** Fair-use cap and upgrade trigger | Margin | Applying soft caps safely shifts intensive users into profitable usage tiers. | If less than 5% of users hit the soft cap within 60 days, we adjust the fair-use threshold limits. | M |
| **GRAN-071** Semantic compression layer Layer | Margin | Compressing transcript texts lowers token overhead and protects gross margins. | If semantic compression introduces more than a 2% degradation in evaluation accuracy, we cut it. | M |
| **GRAN-075** Provider cost monitor | Margin | granular tracking isolates AI COGS by user to prevent margin bleeding. | If monitoring infrastructure cost exceeds 1% of total monthly infrastructure spend, we kill the tool. | M |
| **GRAN-076** Outcome-based CRM billing event | Margin | Emitting billable events anchors pricing directly to high-value product outcomes. | If transactional billing logic generates balance disputes from over 2% of users, we drop the model. | M |
| **GRAN-077** Enterprise admin console | Guardrails | Centralized policy controls are necessary to pass corporate information audits. | If zero enterprise pilots activate centralized policy gates within 60 days, we pause console features. | M |
| **GRAN-079** Modern prototype shell/onboarding | Bet | A highly polished frontend workspace drives early retention for trials. | If 1-week user retention does not rise by 15% after deploying the shell, we pivot onboarding patterns. | M |
| **GRAN-082** Formal 3-horizon roadmap setup | Bet | Populating explicit CAD frameworks aligns ongoing priorities against risks. | If the roadmap is not integrated into monthly review cadences by week 4, we abandon the layout style. | H |

---

### Horizon 3 — Explore (3–6 months)

| Initiative | Strategy Component | What must be true first | Confidence |
| --- | --- | --- | --- |
| **GRAN-017** Product knowledge graph | Moat | Core single-meeting notes and artifact pipelines must achieve stable 95% accuracy scores first. | L |
| **GRAN-019** Related item linker | Guardrails | Downstream connectors (Jira/HubSpot) must show high organic activation across early cohorts. | M |
| **GRAN-021** Customer-insight synthesis | Moat | Multi-meeting analysis pipelines must prove highly accurate without contextual hallucinations. | M |
| **GRAN-022** Executive weekly memory query | Moat | Permissions checking and context-grounded retrieval filters must work flawlessly. | M |
| **GRAN-023** Meeting-type classifier | Bet | Template libraries must expand enough to justify automated style routing rules. | L |
| **GRAN-037** Meeting intelligence webhook/API | Moat | Enterprise security parameters and programmatic authentication systems must be fully built. | M |
| **GRAN-043** Privacy-gated network intelligence | Moat | Compliance frameworks must confirm anonymized aggregation rules clear strict GDPR bounds. | L |
| **GRAN-066** HR/performance summary blocklist | Guardrails | The core sensitive content monitoring engine must maintain a 0% false-negative rate. | L |
| **GRAN-072** On-device basic cleanup model | Margin | On-device hardware capabilities (like Apple Silicon) must offer reliable local small model speeds. | L |

---

### Unmapped (cut or rethink)

| Initiative | Why it's unmapped | Recommendation |
| --- | --- | --- |
| **GRAN-038** Meeting-library partner integration | Dilutes the primary value proposition of being a private, lightweight, local-first note application. | **Cut.** Revisit only if enterprise clients present it as a mandatory procurement blocker. |

---

### Mapping Disagreements

| Initiative | I mapped to | You'd map to | Why |
| --- | --- | --- | --- |
| **GRAN-033** Model Context Protocol server framework | Moat | **Unmapped** | The Moat strategy states building an open-source MCP framework protects against encroachment, but spending early resources creating independent developer frameworks is a major distraction from fixing the core application's existential OS risk. |
| **GRAN-078** SSO and organization management | Bet | **Guardrails** | Enterprise administration tools do not change the underlying validation of what the product is or who it is for; they are standard governance and access-control primitives. |

---

* **(a)** The roadmap is heavily **over-indexed on Horizon 1 (Ship)**, packing it with 40 infrastructure and compliance tasks that will bottle-neck early velocity while Horizon 3 remains starved of scalable data loops.
* **(b)** Protect **GRAN-021 (Customer-insight synthesis)** above all other H3 choices, as multi-meeting cross-account analysis is the only path to building a true, defensible product data moat that generic operating systems cannot replicate.
* **(c)** Kill **GRAN-033 (Model Context Protocol server framework)** today; building open-source developer architecture is expensive engineering theater that does absolutely nothing to protect an early-stage PM notebook from being crushed by native OS audio recording.
