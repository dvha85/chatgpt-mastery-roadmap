# M01 QA Check — Author evidence

> QA snapshot: 2026-09-10  
> Scope: M01.1–M01.4 + `assessments/M01-CHECK.md`  
> Purpose: evidence for changing M01 lessons from PLANNED to READY. This is author QA, not learner PASS evidence.

## Template and language

- [x] Four M01 lesson files exist and follow the lesson structure used by the repository.
- [x] Lessons are bilingual English–Vietnamese.
- [x] Core English terms are defined before learners are required to use them.
- [x] Technical English is kept in canonical form with contextual Vietnamese explanation.
- [x] Each lesson includes learning objectives, vocabulary, concept, examples, practice, verification, failure modes, PASS criteria, evidence, sources and navigation.

## Practice reproducibility

- [x] M01.1 includes five vague requests and a repeatable rewrite exercise.
- [x] M01.2 requires at least two targeted follow-ups and explains same-chat vs new-chat decisions.
- [x] M01.3 includes a fixed sample table, output contract, checklist and 0–2 rubric.
- [x] M01.4 includes a supplied broken output so detecting a hallucination does not depend on a live model spontaneously making the expected error.
- [x] M01 Check contains five task specifications, answer guidance, quality levels and PASS threshold.
- [x] No exercise requires CLI, API key or paid-only access.
- [x] No exercise requires private or production data.

## Gate P2 coverage

- [x] Prompt foundation covers Goal + Context + Output + Boundaries.
- [x] Iteration covers targeted feedback, decomposition, checkpoints and context reset.
- [x] Output contracts cover tables, fields, unknown handling, checklist and acceptance criteria; technical schema is explicitly deferred.
- [x] Verification covers claim → evidence → conclusion, assumptions, source checks, calculation/test checks and correction prompts.
- [x] Learners can distinguish course examples from evidence they must produce themselves.
- [x] Every referenced input is inline or points to an existing repository file.

## Source review

Official-source claims were checked against current OpenAI materials on 2026-09-10:

- `https://learn.chatgpt.com/docs/prompting`
- `https://learn.chatgpt.com/docs/use-chatgpt`
- `https://help.openai.com/en/articles/10032626`
- `https://help.openai.com/en/articles/8313428-accuracy-and-reliability`

Durable principles are taught separately from account/UI-specific behavior.

## Navigation and link review

- [x] M00.3 → M01 boundary identified for direct navigation update.
- [x] M01.1 → M01.2 → M01.3 → M01.4 sequence exists.
- [x] M01.4 links to `assessments/M01-CHECK.md` and M02 overview rather than a nonexistent M02 lesson.
- [x] Internal paths used by M01 lessons were reviewed against repository structure.

## QA result

**PASS for content READY.**

This QA result means the material can be published as READY. It does not mark any learner as PASS and it does not satisfy P3 beginner-pilot requirements.
