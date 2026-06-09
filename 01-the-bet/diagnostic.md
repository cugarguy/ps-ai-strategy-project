# Three-Axis Vulnerability Diagnostic

## Product
**Product:**
- Granola AI records computer audio locally without visible bots. It turns quick, human-typed keywords into formatted roadmaps, user pain points, and PRDs for product teams.

**Your Role:**
- Chief Product Officer and AI Strategist

---

## Scores

### Contextual Moat
*Workflow depth × switching cost. Would users leave in a weekend if a competitor showed up?*

**Score** 
- 3/5

**Score rationale:**
- Users must type keywords during calls to guide the notes. This active writing loop creates a strong daily habit.
- Moving notes out of the app is easy. The tool relies on exporting data to tools like Notion, Jira, and Linear. If a competitor offers cleaner integration with those platforms, users can switch quickly.

**Named attacker (from partner challenge):**
- Dovetail and Productboard are adding local audio capture directly into their established product research software.

---

### Data Advantage
*Proprietary signal that compounds with usage. What do you see that OpenAI doesn't?*

**Score**
- 2/5

**Score rationale:**
- Granola uses standard public APIs from OpenAI and Anthropic. Privacy rules prevent the company from training models on user transcripts, so the software does not build a unique core model edge.
- The only data advantage is linking a user's typed shorthand notes to specific timestamps in the audio recording. This maps meeting context in a way a generic LLM window cannot access.

**Named attacker (from partner challenge):**
- The ChatGPT Desktop App can hold local, cross-session memory if OpenAI adapts it for workspace templates.

---

### Platform Exposure
*Encroachment risk × pivot speed. If Apple/Google/OpenAI ships your hero feature native — then what?*

**Score**
- 4/5

**Score rationale:**
- Granola relies entirely on operating system permissions to record loopback audio without a bot. This leaves it vulnerable to system updates.
- Apple, Microsoft, and Google are building free, bot-free transcription directly into macOS, Windows, and Teams. When transcription becomes a free operating system feature, standalone notetakers lose their core value.

**Named attacker (from partner challenge):**
- Microsoft Teams and Zoom Workplace are launching hidden, local audio recording that places structured notes directly inside corporate wikis.

---

## Top Vulnerability
- Free, built-in operating system audio recording will commoditize standalone transcription utilities, forcing Granola to move from a text notebook to an enterprise infrastructure layer.

## Confidence Level
- M. The platform risk is high, but Granola can defend its position by opening an server framework via the Model Context Protocol to feed clean data into external AI tools like Cursor.
