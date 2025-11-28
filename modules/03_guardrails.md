# Module 3: Guardrails

## Change Log
- Added `evidence_mode` for strict hallucination control.
- Implemented standardized warning messages for missing or short sections.

## Purpose
Ensure quality, accuracy, and safety of summaries by filtering invalid content.

## Variables
- `evidence_mode`: Can be set to "strict" or "standard".

## Rules & Logic

1. **Strict Evidence Mode**
   - **IF** `evidence_mode` == "strict":
     - The summarizer must ONLY include claims, equations, and results explicitly present in the provided text.
     - **IF** sufficient information is not found in the text:
       - Output: "The source text does not provide enough detail to summarize this section in strict evidence mode."

2. **Section Warning Messages**
   - **IF** a section is **Missing** or **Empty**:
     - Output: "Section skipped: no usable text was provided."
   - **IF** a section is **Too Short (< 50 words)**:
     - Output: "Section very short: summary may be incomplete."

3. **Standard Hallucination Mitigation**
   - Do not invent citations, data, or results not found in the source.
