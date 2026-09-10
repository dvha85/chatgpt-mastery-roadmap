# U05 Pre-Pilot QA — Labs, Rubrics & Assessment Integration

> **Checked:** 2026-09-10  
> **Scope:** U05 only  
> **Decision:** U05 SELF-QA PASS — U06 beginner pilot still required  
> **Not evidence of:** a real beginner successfully completing the course

## 1. Required files

- [x] `labs/PROMPT-LAB.md` expanded from template to repeatable workflow.
- [x] `labs/EVALUATION-LAB.md` includes 0/1/2 scale and capability rubric.
- [x] `labs/examples/P-001-summary.md` exists.
- [x] `labs/examples/P-002-planning.md` exists.
- [x] `labs/examples/P-003-comparison.md` exists.
- [x] `labs/data/README.md` exists.
- [x] `labs/data/sample-brief.md` exists.
- [x] `assessments/README.md` exists.
- [x] `assessments/ANSWER-KEY.md` exists.
- [x] `docs/BEGINNER-PILOT.md` exists with status `PREPARED — NOT RUN`.

## 2. Reproducibility gate — Gate tái lập

- [x] P-001 uses a fixed meeting-note dataset and fixed supplied weak output.
- [x] P-002 uses a fixed 8-hour task dataset and checkable arithmetic.
- [x] P-003 uses a fixed fictional comparison table with explicit Unknown values.
- [x] Labs do not depend on the model generating a particular mistake by chance.
- [x] Reference results are examples, not exact-string requirements.
- [x] Every lab states how to verify independently from response confidence.

## 3. PASS/FAIL rubric evidence

### Known FAIL case

P-003 supplied weak output claims:

- Cedar costs about $10/month;
- Cedar supports a contact form;
- Maple is over budget.

Dataset C says:

- Cedar cost = Unknown;
- Cedar contact form = Unknown;
- Maple cost = $14 and budget limit = $15.

Therefore the fixed weak output scores `0` on correctness/grounding/unknown handling and is an observable FAIL.

### Known PASS reference

A P-003 answer that:

- preserves Cedar's Unknown values;
- marks Pine and Maple within budget;
- separates eligibility from preference;
- recommends Pine using only the stated criteria;
- maps requirements back to dataset fields;

meets the five lab criteria at Level 2 and is a reference PASS (10/10). Exact wording is not required.

## 4. Capability rubric gate

`labs/EVALUATION-LAB.md` defines:

- Explain
- Execute
- Diagnose
- Verify
- Transfer

P3 aggregate rule:

- >=8/10;
- no capability = 0;
- Execute = 2;
- Verify = 2.

English track separately measures Recognize → Understand → Use and does not fail a learner for minor grammar errors that preserve intent.

## 5. Assessment integration

- [x] BOOT Check remains the BOOT checkpoint.
- [x] M00 Check remains the M00 checkpoint.
- [x] M01 Check remains the M01 checkpoint.
- [x] `assessments/README.md` explains how to take, score, save evidence and retest.
- [x] `assessments/ANSWER-KEY.md` maps common failures to lessons/labs.
- [x] Learners are told not to use the reference answer itself as retest evidence.
- [x] Content READY remains separate from learner PASS.

## 6. Data and privacy gate

- [x] Lab dataset is explicitly synthetic.
- [x] Real product purchasing decisions must not use the fictional Dataset C.
- [x] Missing values remain Unknown/Unsupported/Assumption.
- [x] Evidence instructions exclude password, API key, token, payment data and client/private information.

## 7. Source check

Official-source principles used by the labs were checked on 2026-09-10:

- OpenAI Help Center — Prompt engineering best practices for ChatGPT
- OpenAI Help Center — How do I create a good prompt for an AI model?
- OpenAI Help Center — Does ChatGPT tell the truth?

The relevant stable principles remain:

- prompts should be clear and specific;
- iterative refinement is expected;
- complex tasks can be broken into smaller focused prompts;
- model confidence is not evidence;
- important facts should be verified with reliable sources or another appropriate verification method.

## 8. Internal navigation review

Expected paths checked by construction and repository structure:

- `labs/PROMPT-LAB.md` → P-001/P-002/P-003 + sample data + Evaluation Lab.
- each P-00x lab → `../data/sample-brief.md`.
- `labs/EVALUATION-LAB.md` → all three labs + M00/M01 Check.
- `assessments/README.md` → BOOT/M00/M01 Check + Answer Key + Evidence Guide.
- `assessments/ANSWER-KEY.md` → M00/M01 checkpoints and P-001/P-002/P-003.
- `docs/BEGINNER-PILOT.md` remains a protocol, not a completed pilot record.

## 9. U05 decision

```text
U05 / pre-pilot P3 work: PASS
P3 release gate: NOT YET PASS
Reason: real beginner pilot U06 has not been run.
```

Next work package: **U06 — run beginner pilot, fix S2/S3 blockers, retest and make the v0.2.0 release decision.**
