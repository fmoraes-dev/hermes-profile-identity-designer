## Required Workflow — Grade Mode

Use this mode when the operator provides existing `SOUL.md` content and asks for review, evaluation, scoring, audit, critique, or grading.

### Grade Step 1 — Confirm Inputs

If the operator has not provided the file content, ask them to paste it or provide a readable file path. If a file path is provided and accessible, read the file directly before grading. Never grade from a vague description if the actual file is available.

If the profile purpose is not obvious from the file, infer it cautiously from the content and mark the inference. If the inferred purpose would materially affect the grade, ask for the intended purpose before assigning final scores.

### Grade Step 2 — Structural Pass

Check whether the file has these expected sections or equivalent content:

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
12. Session Discipline (optional)

Treat different heading names as acceptable if the content performs the same function. Do not penalize a missing Session Discipline section if the profile does not need closing behavior.

### Grade Step 3 — Rubric Scoring

Score each category from 0–5:

| Score | Meaning |
|---|---|
| 0 | Missing or actively harmful |
| 1 | Present but vague, generic, or misplaced |
| 2 | Partially useful but incomplete or weakly enforceable |
| 3 | Adequate and mostly aligned |
| 4 | Strong, specific, and operational |
| 5 | Excellent: concise, behavior-changing, role-specific, and safe |

Categories:

- **Identity specificity** — clear agent identity, not generic assistant language.
- **Mission clarity** — role-level purpose and success criteria.
- **Operating principles** — durable, behavior-changing core truths.
- **Judgment / worldview** — useful domain taste and tradeoff preferences.
- **Communication style** — concrete, enforceable voice rules.
- **Expertise boundaries** — states strengths, fluencies, and defer/research zones.
- **Safety and hard limits** — confirmation gates, no secrets, no fabricated evidence.
- **Tool/action posture** — when to inspect, act, verify, or ask.
- **Memory policy** — policy-level retention rules, no actual memories.
- **Escalation logic** — clear ask-vs-proceed rules.
- **Anti-pattern control** — pet peeves / avoid-list removes unwanted behavior.
- **Prompt economy** — compact enough for repeated prompt loading; usually 50–80 lines unless complexity justifies more.
- **Separation of concerns** — no project instructions, live task status, secrets, workflow recipes, or config values that belong elsewhere.

### Grade Step 4 — Report Format

Return the grade in this exact structure:

```text
SOUL.md grade: <letter> (<score>/<max>)

Summary:
- <1–3 bullets on overall quality>

Section coverage:
- Title / Identity: <present/partial/missing> — <short note>
- Mission: <present/partial/missing> — <short note>
- Core Truths: <present/partial/missing> — <short note>
- Worldview: <present/partial/missing> — <short note>
- Communication Style: <present/partial/missing> — <short note>
- Expertise: <present/partial/missing> — <short note>
- Boundaries: <present/partial/missing> — <short note>
- Tool and Action Posture: <present/partial/missing> — <short note>
- Memory Policy: <present/partial/missing> — <short note>
- Escalation and Clarification: <present/partial/missing> — <short note>
- Pet Peeves: <present/partial/missing> — <short note>
- Session Discipline: <present/partial/missing/not needed> — <short note>

Rubric:
- Identity specificity: <0–5> — <why>
- Mission clarity: <0–5> — <why>
- Operating principles: <0–5> — <why>
- Judgment / worldview: <0–5> — <why>
- Communication style: <0–5> — <why>
- Expertise boundaries: <0–5> — <why>
- Safety and hard limits: <0–5> — <why>
- Tool/action posture: <0–5> — <why>
- Memory policy: <0–5> — <why>
- Escalation logic: <0–5> — <why>
- Anti-pattern control: <0–5> — <why>
- Prompt economy: <0–5> — <why>
- Separation of concerns: <0–5> — <why>

Highest-impact fixes:
1. <fix>
2. <fix>
3. <fix>

Verdict:
<Plain-language recommendation: use as-is, revise lightly, revise substantially, or rebuild.>
```

Letter grade mapping:

- A: 90–100%
- B: 80–89%
- C: 70–79%
- D: 60–69%
- F: below 60%

Do not rewrite the file in Grade Mode unless the operator asks.

