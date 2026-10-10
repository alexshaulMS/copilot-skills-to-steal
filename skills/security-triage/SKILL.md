---
name: security-triage
description: Use to review a code change or a list of scanner alerts for exploitable weaknesses. Ranks findings by whether an attacker can really reach them, and rejects noise.
---

# Security triage

Goal: a short list of findings that matter, each with evidence, not a long list of maybes.

1. Identify the change or alerts to review. List the entry points touched: user input, files, URLs, queries, exports, headers.
2. For each entry point trace where the data goes (sinks): database, shell, HTML, file, CSV or spreadsheet, redirect, log.
3. For each candidate weakness, answer three questions and cite file and line:
   - Can an attacker control the input?
   - Does it reach the sink without validation or encoding?
   - What is the impact if it does?
4. Classify: **Exploitable**, **Needs a condition** (state it), or **Not reachable** (state why).
5. Rate Exploitable and conditional items High, Medium or Low by impact and ease.
6. For each High and Medium item give the smallest fix and a test that would fail before the fix and pass after.
7. Return a table: finding, file and line, class, rating, fix. Put rejected items in a separate list with one-line reasons.

Rules: do not change code. Do not report a pattern match as a vulnerability without a traced path. Say "no exploitable findings" if that is the truth.
