# Data Flywheel Map

The network loop is the weakest part of the strategy. Competitors can attack here first.

## Flywheel Loops

| Loop | What It Measures | Score 1 | Score 5 | Score |
|------|------------------|---------|---------|-------|
| **Correction** | Do users fix AI outputs? Is that signal captured and reused? | No capture | Automated retraining | 3/5 |
| **Preference** | Does the product learn individual / team preferences over time? | Stateless | Deep personalization | 3/5 |
| **Domain Context** | Does usage in one area improve quality in adjacent areas? | Siloed | Cross-domain transfer | 2/5 |
| **Network** | Does each new user / team make the product better for everyone? | Isolated | Strong network effects | 1/5 |

### Correction Loop - 3/5
Granola records text edits when a user changes generated bullet points or writes over a PRD summary. These edits fix the current file and change prompt examples for the next meeting. Granola does not train core models due to privacy contracts, so the information stays in a local prompt loop.

### Preference Loop - 3/5
The tool saves custom formats like Jira templates and team shorthand vocabulary. This builds a personalized writing setup. Teams are unlikely to leave for a generic recorder because they would have to recreate these templates.

### Domain Context Loop - 2/5
Granola searches past notes inside a single project folder. Users can find historical context from a meeting three weeks ago. The tool fails to share insights automatically between different teams, so engineering data stays separated from product data.

### Network Loop - 1/5
Shared folders and text comments do not create network effects. Adding a new user to the software does not make the application smarter for existing users. Value grows line by line as the team expands.

**Total Flywheel Score: 9/20**

**Weakest Loop:** Network loop

**Fix for weakest loop:** Change Granola from a passive notebook into an internal map of product knowledge. The software must parse notes and link related items automatically. For example, it should connect a feature request from a sales call to an engineering bug report. Opening an organizational Model Context Protocol server creates this data connection, so every new user increases the context available to the whole team.

## Encroachment Threat Assessment

### 1. Platform Encroachment
- **Attacker:** Apple and Microsoft
- **Vector:** Building audio recording straight into macOS and Windows systems to capture loopback sound without software bots.
- **Time-to-threat:** 6 to 12 months
- **% of value at risk:** 65%

### 2. Vertical Competitor
- **Attacker:** Productboard and Dovetail
- **Vector:** Shipping a desktop app that records audio and sends meeting text directly into existing roadmaps and dashboards.
- **Time-to-threat:** 3 to 6 months
- **% of value at risk:** 45%

### 3. Adjacent Expansion
- **Attacker:** Notion and Slack
- **Vector:** Adding native huddle recorders that expand text notes instantly inside team wikis.
- **Time-to-threat:** 6 months
- **% of value at risk:** 50%

## 90-Day Encroachment Plan

**Attacker:** Microsoft Teams and Copilot Studio

**Attack vector:** Destroys the network loop by linking Teams audio capture with Outlook emails, DevOps records, and Word documents.

**Weeks 1-4 - what they ship:**
Microsoft updates Teams to record background desktop audio without a bot joining the call. They add a text window called Copilot Scratchpad that copies Granola's interface, allowing users to type short notes that expand using meeting text.

**Weeks 5-8 - how they poach users:**
Microsoft connects this audio data directly to Azure DevOps and Outlook. When a manager types a short note during a call, Copilot creates a DevOps ticket and drafts a release update email. Microsoft includes this tool for free in enterprise E5 contracts.

**Weeks 9-12 - why users don't come back:**
The Microsoft database holds information across sales, engineering, and support teams. Managers cannot return to Granola because Granola only knows what the manager typed. Microsoft knows what the client told sales and what engineering wrote in the code tracker.

**Your defense:**
Stop trying to compete as a text editor and become an open data layer for AI developers. Open-source a Model Context Protocol server framework. This allows users to stream clean, human-guided meeting data straight into engineering tools like Cursor and Claude Code.
