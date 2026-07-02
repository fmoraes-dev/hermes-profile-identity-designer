# Hermes Profile Identity Designer

A Hermes skill for designing `SOUL.md` files.

`SOUL.md` is the identity file for a Hermes profile. It tells the agent who it is, what it protects, how it talks, when it uses tools, what it may remember, and when it should stop and ask.

This skill helps you create, review, or clean up those files without turning them into project docs, config notes, or memory dumps.

## What it does

The skill has three modes:

- **Generate:** builds a new `SOUL.md` from a short profile brief, then walks through each section with approval gates.
- **Grade:** reviews an existing `SOUL.md` against a rubric and returns a score with specific fixes.
- **Standardize / Update:** rewrites an existing `SOUL.md` into a cleaner structure while preserving useful identity, voice, boundaries, and intent.

The generated file is meant to be copied into a Hermes profile directory, usually as:

```text
~/.hermes/profiles/<profile-name>/SOUL.md
```

## Why this exists

Hermes profiles work better when their identity is stable and scoped.

A good `SOUL.md` should answer questions like:

- What kind of agent is this?
- What work should it optimize for?
- What should it refuse to do?
- When should it inspect sources, use tools, or ask the operator?
- What should it remember, and what should it leave out?

It should not contain live task status, secrets, one-off facts, shell recipes, or project rules. Those belong in memory, skills, config, or project files.

## Skill layout

```text
hermes-profile-identity-designer/
├── SKILL.md
└── references/
    ├── grading-rubric.md
    ├── lightweight-hermes-soul-template.md
    ├── section-guide.md
    └── update-workflow.md
```

`SKILL.md` holds the main workflow. The reference files keep the longer rubrics, examples, and templates out of the primary prompt path until they are needed.

## When to use it

Use this skill when you want to:

- create a new Hermes profile identity
- audit an existing `SOUL.md`
- convert a long profile prompt into a tighter identity file
- separate profile identity from project instructions
- add missing boundaries, memory policy, or tool-use rules

## How to use it

In Hermes, load the skill and describe the task:

```text
/skill hermes-profile-identity-designer
```

Examples:

```text
Create a SOUL.md for a research analyst profile.
```

```text
Grade this SOUL.md and tell me what to fix.
```

```text
Standardize this existing SOUL.md, but preserve the voice and hard limits.
```

For generation, the skill asks for the profile purpose first. It asks for the profile name later, after the first draft exists. This keeps the design focused on behavior instead of branding.

## What the generated SOUL.md covers

The default structure includes:

1. Identity
2. Mission
3. Core truths
4. Worldview
5. Communication style
6. Expertise
7. Boundaries
8. Tool and action posture
9. Memory policy
10. Escalation and clarification
11. Pet peeves
12. Session discipline, if the profile needs closing behavior

Session discipline is optional. If you do not want closing reviews, the skill removes that section instead of leaving an empty heading.

## Design principles

The skill follows a few rules:

- Keep identity separate from procedure.
- Keep project rules out of `SOUL.md`.
- Use approval gates for interactive generation.
- Preserve strong existing language during rewrites.
- Add safety defaults when they are missing.
- Keep the final file short enough to load often.

The companion `writing-great-skills` skill was used to split long reference material out of `SKILL.md`, leaving the main workflow short and easier to run.

## Compatibility

This skill is written for Hermes Agent and the `SKILL.md` format. It should also be readable by other agent systems that support Markdown-based skills, but the interaction flow assumes Hermes tools such as `skill_view` and `clarify`.
