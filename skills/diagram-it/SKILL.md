---
name: diagram-it
description: Use to explain how code works or what a change does. Produces a small Mermaid diagram, grounded in the actual files, for a README or pull request.
---

# Diagram it

1. Ask what the diagram is for (onboarding, a pull request, a design decision) and the one question it must answer.
2. Read the relevant files. Only draw components, calls and data flows you found in code. Cite the file for each box in a legend beneath the diagram.
3. Pick the type that fits the question:
   - `flowchart` for how data moves.
   - `sequenceDiagram` for who calls whom, in order.
   - `stateDiagram-v2` for lifecycles.
4. Keep it to 12 nodes or fewer. If more are needed, split into two diagrams.
5. Output a fenced `mermaid` block, then a legend of file references, then one sentence on what to notice.
6. Check the syntax by rendering it, or by re-reading each line. A diagram that does not render is not finished.

Rules: no invented components. Mark anything uncertain with a `?` label instead of guessing.
