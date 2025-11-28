# Module 3: Guardrails

## Purpose
Ensure quality, accuracy, and safety of summaries.

## Rules
- **Missing/Empty Sections** → Output "No content available".
- **Short Sections (<50 words)** → Expand minimally with context, but do not invent content.
- **Hallucination Mitigation** → Summaries must only reflect actual text.
- **Long-Paper Chunking** → If section exceeds context window, split into chunks, summarize each, then merge into ≤100 words.
