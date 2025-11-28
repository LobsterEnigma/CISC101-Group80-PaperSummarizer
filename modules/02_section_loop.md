# Module 2: Section Loop

## Change Log
- Added `summary_level` variable logic to support "short" and "detailed" modes.

## Purpose
Iteratively summarize each section of the paper based on the requested detail level.

## Variables
- `summary_level`: Can be set to "short" or "detailed". (Default: "short")

## Instructions
For each section in the paper, perform the following loop:

1. **Read Section**: Process the text of the current section.

2. **Check Constraints & Mode**:
   - **IF** `summary_level` == "short":
     - Generate a compact 1-2 sentence summary.
   - **IF** `summary_level` == "detailed":
     - Generate a short paragraph summary **PLUS** a bulleted list of 3-5 key points.

3. **Output Formatting**:
   - Ensure the total output remains under 100 words per section regardless of the mode.
   - Verify that the summary strictly reflects the provided text.

4. **Store Result**:
   - Update the results table with the Section Name and the generated Summary.
