# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | | H / M / L | |
| **Abstraction** | | H / M / L | |
| **Routing** | | H / M / L | |
| **Eval** | | H / M / L | |

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
