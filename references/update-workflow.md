## Required Workflow — Standardize / Update Mode

Use this mode when the operator provides existing `SOUL.md` content and asks to improve, update, standardize, normalize, convert, or bring it to the desired structure.

### Update Step 1 — Preserve Before Changing

Read the provided content carefully and extract:

- existing profile name / title,
- durable identity claims,
- mission or role statements,
- distinctive voice preferences,
- domain expertise,
- hard boundaries,
- memory rules,
- review/closing behavior,
- unique phrases or principles worth preserving,
- content that belongs elsewhere.

Do not discard useful existing identity just because it uses different headings.

### Update Step 2 — Diagnose Against the Rubric

Run a compact grading pass internally using the Grade Mode rubric. In the response, summarize only:

- what will be preserved,
- what will be tightened,
- what will be moved or removed,
- what is missing and must be added.

### Update Step 3 — Ask for Missing Intent Only When Needed

If the file lacks enough context to safely rewrite identity, mission, or boundaries, ask up to three focused questions before rewriting.

Do not ask questions for information already present in the file. If the existing content is sufficient, proceed directly to a draft.

### Update Step 4 — Rewrite to Standard Structure

Rewrite the file into the standard section order. Use `references/lightweight-hermes-soul-template.md` as the compact target shape unless the existing file has a justified reason to be more specialized:

1. Title / Identity
2. Mission
3. Core Truths
4. Worldview
5. Communication Style
6. Expertise
7. Boundaries
8. Tool and Action Posture
9. Memory Policy
10. Escalation and Clarification
11. Pet Peeves
12. Session Discipline (only if useful or already present)

Preservation rules:

- Preserve the profile's existing purpose and personality unless clearly harmful or generic.
- Preserve strong original phrases where they improve distinctiveness.
- Convert long prose into enforceable bullets where appropriate.
- Merge duplicate rules.
- Move project-specific instructions out of the SOUL.md rewrite and list them separately as `Should move elsewhere`.
- Remove secrets, live task status, temporary facts, tool config, and implementation recipes.
- Add missing Hermes-specific safety defaults: confirmation for destructive/external actions, no secrets, no fabricated evidence, verification before success claims.
- Add tool/action posture and memory policy if missing.
- Keep the result compact; if longer than 80 lines, explain why the length is justified or tighten it.

### Update Step 5 — Present Diff-Style Rationale and Final Markdown

Return this structure:

````text
Update summary:
- Preserved: <key existing elements retained>
- Strengthened: <weak areas improved>
- Removed or moved elsewhere: <items removed from SOUL.md scope>
- Added: <new standard sections / safety defaults>

Updated SOUL.md:
```md
<complete rewritten SOUL.md>
```
````

If the operator requested an interactive update, instead use the Generate Mode section-by-section approval loop, seeded with the existing file content.

