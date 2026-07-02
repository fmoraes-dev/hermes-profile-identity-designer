---
name: hermes-profile-identity-designer
description: "Use when creating, grading, or standardizing Hermes SOUL.md profile identity files; triggers include SOUL.md generation, profile identity design, SOUL.md review/audit/grading, and preservation-aware SOUL.md rewrites."
version: 1.2.0
author: M.I.N.E.R.V.A.
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [hermes-agent, soul-md, agent-identity, profile-design, prompt-engineering]
    related_skills: [hermes-agent, writing-great-skills]
---

# Hermes Profile Identity Designer

## Purpose

Create, grade, or standardize a Hermes profile `SOUL.md`: the profile's durable operating identity. Keep `SOUL.md` focused on identity, voice, values, boundaries, memory policy, and action posture — not project conventions, live facts, workflows, secrets, or config.

## Reference Files

- `references/lightweight-hermes-soul-template.md` — raw copy-ready lightweight `SOUL.md` baseline. Contains only Markdown content.
- `references/section-guide.md` — section meanings, good/bad examples, final skeleton, checklist, and common mistakes. Load before Generate Mode section iteration, before final assembly, or when a section-specific question arises.
- `references/grading-rubric.md` — full Grade Mode workflow, scoring rubric, letter mapping, and report format. Load before grading an existing `SOUL.md`.
- `references/update-workflow.md` — full Standardize / Update workflow and preservation rules. Load before rewriting an existing `SOUL.md`.

## Source Principles

- `SOUL.md` = identity, voice, values, restrictions, action posture.
- `AGENTS.md`, `.hermes.md`, `CLAUDE.md`, `.cursorrules` = project instructions.
- `MEMORY.md`, `USER.md`, memory backend = learned facts and stable preferences.
- Skills = reusable procedures.
- `config.yaml` / `.env` = tool, provider, and secret configuration.
- Target 50–80 lines unless the profile's role justifies more. Every line must change behavior.

## Mode Selection

Identify the operator's requested mode:

1. **Generate** — create a new `SOUL.md` from a high-level profile overview.
2. **Grade** — evaluate an existing `SOUL.md`; load `references/grading-rubric.md`.
3. **Standardize / Update** — rewrite existing content toward the standard while preserving useful identity; load `references/update-workflow.md`.

If unclear, ask which mode they want. Do not rewrite when the operator only asked for a grade.

## Generate Mode Steps

1. **Purpose first.** Ask for the profile's high-level purpose: what work it should do, who/what it serves, and important constraints. Do not ask for the name yet.
   - Completion criterion: you can state the intended role and success criteria in 1–3 sentences.
2. **Seed the draft.** Load `references/lightweight-hermes-soul-template.md` and create a provisional draft of all sections: Title / Identity, Mission, Core Truths, Worldview, Communication Style, Expertise, Boundaries, Tool and Action Posture, Memory Policy, Escalation and Clarification, Pet Peeves, Session Discipline.
   - Completion criterion: every section has a provisional role-specific draft or a marked decision point.
3. **Name the profile.** Ask what the profile should be called for the H1 title. If given both codename and display name, use the display name for H1.
   - Completion criterion: the H1 title is known.
4. **Iterate section by section.** Load `references/section-guide.md`. For each section: explain what it controls, ask one focused question, provide 2–4 options based on the overview and prior approvals, allow freeform input, craft the section, then ask for explicit approval. Do not move on until approved.
   - Completion criterion: every included section has operator approval.
5. **Session Discipline gate.** Before Section 12, ask whether review/closing behavior should exist. If declined, remove the section entirely.
   - Completion criterion: Section 12 is either approved or absent.
6. **Assemble final Markdown.** Present one complete copy-ready `SOUL.md` fenced as Markdown. Do not write it to disk unless explicitly asked.
   - Completion criterion: final file matches the approved sections and contains no unresolved placeholders.

## Grade Mode Summary

Load `references/grading-rubric.md`, inspect the actual file/content, score every rubric category from 0–5, and return the prescribed grade report. Do not rewrite unless asked.

## Standardize / Update Mode Summary

Load `references/update-workflow.md`, preserve existing useful identity and voice, remove/move content outside SOUL scope, add missing safety/tool/memory posture, and return an update summary plus complete rewritten Markdown. Ask at most three focused questions only when identity, mission, or boundaries are underdetermined.

## Non-Negotiables

- Use actual file content when a path is provided; never grade from a vague description if the source is accessible.
- Preserve strong existing identity language during updates.
- Keep section directions and rubric details in references; keep this file step-focused.
- Do not leave `## Session Discipline` as an empty heading after it is declined.
- Do not embed secrets, live task status, workflow recipes, or config values in generated or updated SOUL content.
