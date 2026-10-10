# Copilot skills to steal

Six small, plain-English skills for GitHub Copilot, from the "Six things to hold in mind before you start" workshop. Take what is useful, change the rest.

A skill is a folder with a `SKILL.md` file. Copilot loads it when your request matches its `description`. Skills use the open Agent Skills format.

## The skills

| Skill | Use it when | What you get |
|---|---|---|
| [`characterise-first`](skills/characterise-first/SKILL.md) | You are about to change or migrate code that has few tests | Tests that pin down what the code does today |
| [`one-slice-at-a-time`](skills/one-slice-at-a-time/SKILL.md) | A migration or big feature must be split up | An ordered slice plan, then only slice 1 |
| [`change-evidence`](skills/change-evidence/SKILL.md) | You want the facts gathered before any edit | A short evidence card: task, scope, invariants, checks, unknowns |
| [`diagram-it`](skills/diagram-it/SKILL.md) | You need to explain how code works | A small Mermaid diagram grounded in real files |
| [`security-triage`](skills/security-triage/SKILL.md) | You are reviewing a change or a list of scanner alerts | Findings ranked by whether an attacker can really reach them |
| [`handover-note`](skills/handover-note/SKILL.md) | You are finishing a session or opening a pull request | An honest note: changed, verified, unknown, risks, next |

The two I would start with are `characterise-first` and `one-slice-at-a-time`. They fit any migration.

## Install

Copy the folder you want into your repository:

```
.github/skills/<skill-name>/SKILL.md
```

For example, to take `characterise-first`, copy `skills/characterise-first` to `.github/skills/characterise-first` in your own repo, commit it, and ask Copilot to characterise the module you are about to change.

## Read before you install

Skills are instructions that an agent follows. They are not verified by GitHub. Read any skill, including these, before you add it to a repository. Every skill here is a short text file, so this takes a minute.

## Check your own setup

Which Copilot surfaces and features are available to you is decided by your administrators. If a skill does not appear to load, check with them first.

## Docs and more skills

- GitHub Docs, adding agent skills: https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills
- The Agent Skills standard: https://agentskills.io
- Community collection: https://github.com/github/awesome-copilot

## Licence

MIT. See [LICENSE](LICENSE).
