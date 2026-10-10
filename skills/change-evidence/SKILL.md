---
name: change-evidence
description: Prepare an evidence card before a scoped code change by reading the task, repo conventions, relevant implementation and tests; no edits or execution.
---

# Change evidence

This skill is a preparation procedure, not a tool permission grant.

1. Read the task/guide the user named. If it is missing or ambiguous, stop and ask
   for the approved task; do not invent a replacement.
2. Read applicable repository instructions and relevant source/test configuration.
   Cite files rather than relying on assumed language/framework conventions.
3. Identify invariants and distinguish preserved behaviour from intended changes.
4. Identify exact baseline and acceptance commands from repository evidence.
   Missing commands remain unknown. Do not claim to execute them.
5. List only relevant existing skills/tools; do not install or enable anything.
   A task may need no external MCP server.
6. Return an evidence card with: Task; Scope; Invariants; Baseline check; Acceptance
   check; Unknowns. Keep it short and cite the sources.
7. Stop before planning implementation in detail, editing files, running commands
   or accessing external systems. Human approval is a separate step.

Follow the repository's actual task and conventions.
