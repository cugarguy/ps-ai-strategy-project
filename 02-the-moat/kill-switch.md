# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | Granola relies on OpenAI and Anthropic APIs for text synthesis and custom formats[cite: 5]. | High | Pause new features and shift prompt routing to open-weight models via a third-party inference host[cite: 5]. |
| **Abstraction** | Prompts and user formats are built for the specific window behaviors and system guidelines of Anthropic and OpenAI[cite: 5]. | Medium | Connect core product templates to a unified model wrapper framework to separate application code from specific provider tools[cite: 5]. |
| **Routing** | Traffic uses fixed routing based on text complexity[cite: 5]. There is no automatic backup engine or real-time cost balancing[cite: 5]. | Medium | Set up an open proxy layer like LiteLLM to route traffic to alternative providers instantly if a main API fails[cite: 5]. |
| **Eval** | Quality tracking relies entirely on live user edits[cite: 5]. Granola has no automated system to test layout errors during model changes[cite: 5]. | High | Build an automated test suite running code assertions on past transcript data to verify formatting stays intact[cite: 5]. |

## Portability Score
Partial[cite: 5]

**Rationale:** Granola runs as a desktop application that keeps text files and audio recordings locally on the computer[cite: 5]. This data is easy to extract[cite: 5]. However, the processing logic requires commercial cloud APIs[cite: 5]. Moving the files is simple, but moving the formatting logic alters output quality[cite: 5].

## If Anthropic or OpenAI doubles pricing tomorrow:
- **Move to alternative hosts:** Swap the application backend to alternative inference hosts using open-weight models like Llama[cite: 5].
- **Use local hardware:** Process baseline transcription text on the user's local computer using a smaller model running on the local device chip[cite: 5]. Save paid cloud API calls for multi-meeting lookups[cite: 5].

## If Deepgram and AssemblyAI ship a competing product:
- **The interactive loop:** Competitors offer passive audio transcripts[cite: 5]. They do not own the text setup where a manager types short notes during a call to change the output format[cite: 5].
- **The text-to-audio map:** Granola links typed keywords to precise time stamps in the local audio recording[cite: 5]. API providers only see final text strings[cite: 5]. They lack the local software layer that tracks what the user focuses on during the meeting[cite: 5].
