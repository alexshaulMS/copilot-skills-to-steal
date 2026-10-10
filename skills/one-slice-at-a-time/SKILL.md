---
name: one-slice-at-a-time
description: Use when a migration, rewrite or large feature must be split into small reviewable pull requests. Produces an ordered slice plan, then delivers only the next slice.
---

# One slice at a time

A slice is the smallest change that can be reviewed, tested and merged on its own while the
system keeps working.

1. Restate the end goal in one sentence and name what is out of scope.
2. Check that a characterisation baseline exists (see `characterise-first`). If it does not, the first slice is to create it.
3. Break the work into slices. Each slice must have: a title, the files it touches (aim for 5 or fewer), how a reviewer verifies it, and how to roll it back.
4. Order slices so that every one leaves the app working. Prefer adding the new beside the old, switching over, then deleting the old.
5. Output the plan as a table. Mark slice 1 as the only one to do now.
6. Implement slice 1 only. Run the checks. Stop and report. Do not start slice 2 until asked.

Rules: no slice mixes a refactor with a behaviour change. If a slice grows past its file budget, split it again.
