---
name: characterise-first
description: Use before changing, migrating or rewriting existing code that has few or no tests. Writes tests that pin down what the code does today, so any later change can prove it kept the behaviour.
---

# Characterise first

Goal: capture what the code **does now**, not what it should do. A characterisation test
is a snapshot of real behaviour, including awkward behaviour.

1. Ask for the unit of code to be changed (a page, module or function). If it is vague, stop and ask.
2. Find the existing test command and framework from the repo (package.json, composer.json, CI file). Never assume one. If there is none, say so and propose the smallest option.
3. List the observable behaviours of the unit: inputs, outputs, side effects, error and empty cases. Read the code; do not guess.
4. For each behaviour write one test that asserts the **current** result. Use real values from the code or from running it. If current behaviour looks like a bug, still pin it and mark it `// KNOWN ODDITY`. Do not fix it here.
5. Run the tests against the **unchanged** code. All must pass. A test that fails on unchanged code is wrong, not the code.
6. Return a short report: behaviours covered, behaviours not covered and why, the exact command run, and the result.

Do not: change production code, refactor, or add tests for behaviour you have not observed.
