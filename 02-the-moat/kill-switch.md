# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | Highly Concentrated: Granola relies on OpenAI (GPT-4o) and Anthropic (Claude 3.5 Sonnet) via standard developer APIs for its heavy-lifting synthesis and custom "Recipe" execution. | High | Freeze non-essential feature development and immediately switch default system prompt routing to open-weight models via an alternative inference provider. |
| **Abstraction** | Proprietary/Hardcoded: Prompts, few-shot examples, and user "Recipes" are heavily tailored to the specific context window behaviors, instruction-following quirks, and system-prompt sensitivities of Anthropic and OpenAI.| Medium | Re-map core product management templates to a unified LLM wrapper framework (e.g., LangChain or an open-source gateway) to decouple application code from specific provider SDKs.|
| **Routing** | Static/Hardcoded: Requests are statically routed based on the complexity of the "Recipe" or summary requested (e.g., standard summaries to a faster model, complex cross-meeting synthesis to a smarter model). No real-time dynamic failure fallback or cost-optimizing router.| Medium | |
| **Eval** | Ad-Hoc/User-Driven: Quality control relies primarily on real-time human correction (the PM editing the output). Granola lacks an automated, programmatic internal evaluation harness to test output consistency across different model swaps.| High | Stand up a continuous integration evaluation suite running automated assertions on a golden dataset of past meeting transcripts to ensure formatting and structured data output don't break during an emergency swap.|

## Portability Score
<!-- Ready / Partial / Locked -->
**Partial**
**Rationale:** While Granola is an installed desktop application that captures audio and manages text files locally (which makes client data highly portable), its cognitive synthesis layer is tightly bound to commercial APIs. Moving the text files is trivial; moving the specialized processing logic without losing output quality is not.

## If [primary vendor] doubles pricing tomorrow:
<!-- What's your 48-hour response? -->
**Deploy Alternative Inference Providers:** Immediately shift the application backend to run through alternative infrastructure providers (such as DeepSeek, Groq, or Together AI) using high-performance open-weight models like Llama 3.1 70B/405B.
**On-Device Offloading:** Lean heavily into Granola's existing local-first desktop footprint. Offload basic transcription formatting and initial shorthand note-cleansing to a compact, local on-device model (such as a quantized Llama 3 8B or Mistral 7B) running directly on the user's local hardware (e.g., leveraging Apple Silicon's Neural Engine), saving premium cloud API calls exclusively for complex multi-meeting cross-referencing.

## If [primary vendor] ships a competing product:
<!-- What's defensible that they can't replicate? -->
**The "Write-Then-Enhance" Interaction Loop:** Foundation model providers offer passive chat interfaces or brute-force transcripts. They do not own the intentional UX interaction where a PM intentionally types minimalist context during a meeting to shape the final output.
**The Local Context and Shorthand Mapping:** The core defensible asset is Granola's precise metadata map—linking sparse, human-typed keywords to specific temporal chunks of local system audio. A foundation model provider only sees the final raw text block fed into an API. They lack the local system hook that captures the exact micro-moments of human focus and interest as the conversation is happening.
