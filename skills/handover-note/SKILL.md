---
name: handover-note
description: Use at the end of a working session or before opening a pull request. Writes an honest note of what changed, what was verified, and what is left.
---

# Handover note

1. Read the actual diff and the commands that were run in this session. Do not rely on memory of what was intended.
2. Write the note in this order, keeping each section short:
   - **Changed**: files and the behaviour change, in plain language.
   - **Verified**: only checks that were actually run, with the command and the result. A command that was proposed but not run goes under Unknown.
   - **Not verified / unknown**: what has not been tested or is assumed.
   - **Risks**: what could break and who would notice.
   - **Next**: the next concrete step, and any decision needed from a human.
3. Keep it under one page. Link files rather than pasting code.

Rules: never write "should work". State what ran and what happened.
