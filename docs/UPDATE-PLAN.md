# Repository Update Plan — Kế hoạch hoàn thiện khóa học ChatGPT

> **Plan version:** 1.1  
> **Updated:** 2026-09-10  
> **Baseline review commit:** `9d70449b6309c3ce6c3e1289fae15bbbd4b9f20c`  
> **Current state:** U01–U05 DONE; U06 is NEXT  
> **Release state:** v0.2.0 preview — not yet validated by a real beginner pilot

## 1. Goal — Mục tiêu

Biến repo thành khóa học ChatGPT song ngữ English–Tiếng Việt mà một người mới có thể:

1. biết bắt đầu ở đâu;
2. hiểu thuật ngữ trước khi bị yêu cầu sử dụng;
3. học bằng ví dụ + thực hành thay vì chỉ đọc lý thuyết;
4. kiểm chứng output thay vì tin vì câu trả lời nghe tự tin;
5. tự chấm bằng rubric;
6. lưu evidence an toàn;
7. tiến từ Operator → Power User → Builder theo các gate rõ ràng.

Khóa học giữ thuật ngữ tiếng Anh chuẩn nhưng giải thích plain English + tiếng Việt theo ngữ cảnh. Không yêu cầu biết lập trình để hoàn thành phần Foundation.

## 2. Current snapshot — Hiện trạng

- Planned total: **56 lessons** = 4 BOOT + 52 lessons M00–M11.
- READY: **11 lessons** = BOOT.1–BOOT.4 + M00.1–M00.3 + M01.1–M01.4.
- PLANNED: **45 lessons** = M02–M11.
- P0 infrastructure: complete.
- P1 BOOT: complete.
- P2 M00 + M01 content: complete.
- U05 pre-pilot P3 work: complete.
- U06 real beginner pilot: not run yet.
- v0.2.0 release gate: not yet pass.

Content state is tracked in [CONTENT-STATUS.md](CONTENT-STATUS.md). Learner competence is tracked separately in [PROGRESS.md](../PROGRESS.md).

## 3. Release milestones — Mốc phát hành

| Milestone | Scope | Release condition |
|---|---|---|
| v0.2.0 | BOOT + M00 + M01, 11 lessons | P3 pass: labs/assessment ready + real beginner pilot + blocker fixes/retest |
| v0.3.0 | Foundation through M05, 27 lessons + Foundation capstone | P4 pass + real capstone/pilot evidence |
| v0.4.0 | Add M06–M08 Power User modules | P5 pass; permissions/automation workflows verified |
| v1.0.0 | Add M09–M11 + Builder capstone | P6–P7 pass; all 56 lessons accounted for and final QA complete |

A milestone name is a target until its release gate has evidence. Do not use version labels alone as proof that the course has been validated.

---

# 4. P0 — Learning infrastructure / Hạ tầng học

**Status:** COMPLETED in U01.

Delivered:

- `START-HERE.md`
- `docs/LEARNING-PATHS.md`
- `docs/CONTENT-STATUS.md`
- `docs/FEATURE-AVAILABILITY.md`
- `docs/TROUBLESHOOTING.md`
- improved `LESSON-TEMPLATE.md`
- improved `STUDY-METHOD.md`
- bilingual standard
- official-source registry
- evidence guide/template
- navigation and publication-state rules

**Gate P0:** from the repository entry point, a new learner can identify the first lesson, where to save evidence, how PASS works, and which content is READY.

---

# 5. P1 — BOOT / Khởi động

**Status:** COMPLETED in U02.

Delivered:

| Lesson | Skill |
|---|---|
| BOOT.1 | first prompt/response and basic interaction |
| BOOT.2 | follow-up, format changes and conversation context |
| BOOT.3 | safe use, claim checking and redaction |
| BOOT.4 | save evidence without exposing sensitive data |

Also delivered:

- BOOT module README
- `assessments/BOOT-CHECK.md`
- synthetic BOOT data
- evidence example
- BOOT QA evidence

**Gate P1:** all four tasks can be completed without CLI/API key/programming; exercises use safe data and include fallbacks for UI differences.

---

# 6. P2 — Mental model + prompting / M00 + M01

**Status:** COMPLETED in U03–U04.

## M00 — Mental Model

Delivered:

- `M00.1-chat-work-codex.md`
- `M00.2-how-chatgpt-works.md`
- `M00.3-task-and-verification.md`
- `assessments/M00-CHECK.md`
- M00 QA evidence

Core model:

```text
Choose surface
      ↓
Outcome → Context → Tools → Verification
```

Learner must distinguish:

- Chat / Work / Codex;
- surface vs tool;
- model vs product;
- context vs memory/source of truth;
- confident output vs verified evidence.

## M01 — Prompting as Task Specification

Delivered:

- `M01.1-prompt-foundations.md`
- `M01.2-iterate-and-decompose.md`
- `M01.3-output-contracts.md`
- `M01.4-verify-answers.md`
- `assessments/M01-CHECK.md`
- M01 QA evidence

Core loop:

```text
Specify → Generate → Inspect → Diagnose → Revise → Verify
```

Learner practices:

- Goal + Context + Output + Boundaries;
- deliberate iteration instead of random rewriting;
- decomposition/checkpoints for complex tasks;
- output contracts and missing-data rules;
- Claim → Evidence → Conclusion;
- source/calculation/test/human-review verification.

**Gate P2:** seven M00–M01 lessons meet lesson template, bilingual terminology rules, practice/rubric requirements and QA checks.

---

# 7. P3 — Labs, PASS framework, beginner pilot, v0.2.0

**Status:** IN PROGRESS. U05 pre-pilot work is complete; U06 pilot/release work remains.

## U05 — Pre-pilot system

**Status:** DONE.

Delivered:

### Prompt labs

- `labs/PROMPT-LAB.md` — repeatable experiment workflow.
- `labs/examples/P-001-summary.md`
- `labs/examples/P-002-planning.md`
- `labs/examples/P-003-comparison.md`

### Fixed data

- `labs/data/README.md`
- `labs/data/sample-brief.md`

The sample brief contains:

- Dataset A: fixed meeting notes + summary ground truth;
- Dataset B: fixed 8-hour plan + arithmetic/dependency checks;
- Dataset C: fictional comparison table + explicit Unknown values.

The labs do not depend on a model randomly generating the expected mistake. Each lab includes a supplied weak output, reference result, verification method and 0–2 rubric.

### Evaluation and assessment integration

- `labs/EVALUATION-LAB.md`
- `assessments/README.md`
- `assessments/ANSWER-KEY.md`
- `labs/examples/U05-qa-check.md`

Evaluation capabilities:

- Explain
- Execute
- Diagnose
- Verify
- Transfer

Aggregate P3 capability rule:

- score >= 8/10;
- no capability = 0;
- Execute = 2;
- Verify = 2.

English track:

- Recognize terminology;
- Understand meaning in Vietnamese;
- Use at least one instruction correctly;
- minor grammar errors that preserve intent do not fail the learner.

### Known PASS and FAIL rubric evidence

U05 QA applies the rubric to:

- a fixed P-003 FAIL result that invents Unknown fields and misreads the budget;
- a reference P-003 PASS result that preserves Unknowns, maps criteria to evidence and makes a supported recommendation.

This proves the rubric is usable for pre-pilot QA; it does **not** prove a real beginner can self-study the course.

## U06 — Real beginner pilot + release decision

**Status:** NEXT — NOT RUN.

Protocol prepared in `docs/BEGINNER-PILOT.md`.

U06 must:

1. select at least one real beginner or novice learner;
2. have them start from README/START-HERE without author explanation;
3. record time, confusion points and help required;
4. have them complete relevant lessons/labs/checkpoints;
5. classify blockers S0–S3;
6. fix all S2/S3 blockers;
7. retest fixed blocker paths;
8. record assessment/evidence quality;
9. verify no privacy/safety workflow pushes the learner to expose sensitive data;
10. make the explicit v0.2.0 release decision.

### Gate P3

PASS only when:

- 11 lessons remain READY;
- no blocking internal navigation/link issue remains;
- P-001/P-002/P-003 are reproducible;
- rubric has PASS/FAIL evidence;
- real beginner pilot evidence exists;
- no unresolved S2/S3 blocker remains;
- required fixes are retested;
- the release decision is recorded.

If no real beginner pilot has been run, the repository stays **preview**, even if self-QA is green.

---

# 8. P4 — Foundation M02–M05

**Status:** PLANNED. Depends on P3 so beginner feedback can adjust lesson length and difficulty.

## U07 — M02 Models & Reasoning

Create:

- M02.1 Model selection
- M02.2 Reasoning effort
- M02.3 Personal benchmark
- M02 checkpoint + benchmark example

Output: five-task personal benchmark with fixed inputs/rubric and evidence-based model/reasoning choices.

## U08 — M03 Context, Projects & Memory

Create five lessons on:

- context architecture;
- personalization/instructions;
- Projects/chats;
- Memory limits;
- files as source context.

Output: a real Project or equivalent context package with instructions, clean files and update/verification rules.

## U09 — M04 Search & Research

Create four lessons on:

- Web Search;
- source quality;
- Deep Research;
- research workflow.

Output: research memo with at least three sources, claim-evidence mapping and uncertainty section.

## U10 — M05 Files & Multimodal

Create four lessons on:

- image inputs;
- image generation/editing;
- documents/spreadsheets/presentations/PDFs;
- voice.

M05.3 keeps one lesson ID but uses separate mini-labs to avoid overload.

## U11 — Foundation capstone + pilot

Create Foundation capstone and run/verify it before v0.3.0.

**Gate P4:** 27 BOOT–M05 lessons READY; Foundation capstone example + real pilot evidence; learner can stop at Foundation with a clearly defined endpoint.

---

# 9. P5 — Power User M06–M08

**Status:** PLANNED. Depends on P4.

## M06 — Work, Browser & Computer Use

Five lessons covering:

- ChatGPT Work;
- long-running work;
- browser vs search;
- computer use;
- permissions/sandboxing mindset.

## M07 — Plugins & Connected Data

Four lessons covering:

- built-in vs plugin;
- permissions/data boundaries;
- connected workflows;
- human-in-the-loop actions.

## M08 — Skills & Scheduled Tasks

Five lessons covering:

- Skill vs Plugin;
- reusable Skills;
- scheduled tasks;
- automation reliability;
- evaluate-before-automate.

Power User exercises must distinguish read/draft/modify/send/publish permissions and use safe fallbacks if connected tools are unavailable.

**Gate P5:** 14 new lessons READY; permission failures/tool failures handled; automation examples include stop conditions, review points and failure reporting.

---

# 10. P6 — Builder M09–M11

**Status:** PLANNED. Depends on P5.

Before Builder, create `docs/BUILDER-PREREQUISITES.md` covering:

- files/folders;
- Git/branch/commit basics;
- terminal basics;
- simple code reading;
- environments/authentication;
- API cost awareness.

## M09 — Codex & GitHub

Five lessons from Codex surfaces through repository context, coding task specification, GitHub workflow and safe autonomous coding.

Output: small repository change with reproduction, tests, diff review and commit/PR evidence.

## M10 — API, MCP & Agents

Five lessons covering:

- ChatGPT vs API;
- Responses/tools;
- MCP/connectors;
- Agents SDK;
- evals.

Output: agent/system architecture plus at least five eval cases before implementation.

## M11 — Agentic System Design

Five lessons covering:

- workflow before agent;
- state/tools/boundaries;
- human review;
- observability;
- production readiness.

Output: system-design review before capstone build.

**Gate P6:** 15 Builder lessons READY; technical examples are actually runnable in documented environments; Builder capstone design has evaluation and cost boundaries.

---

# 11. P7 — Full-course QA & v1.0.0

**Status:** PLANNED.

Final QA must check:

- exactly 56 unique lesson IDs;
- each lesson has a file/status/source/prerequisite/exercise/rubric/navigation;
- README/CURRICULUM/CONTENT-STATUS/PROGRESS/module READMEs agree;
- bilingual terminology is explained at first use;
- no broken blocking internal links;
- current feature claims have current official sources;
- outdated UI/feature lessons are moved to NEEDS UPDATE;
- examples/evidence do not expose secrets/private data;
- capstones have rerunnable evidence and explicit limitations.

**Gate P7:** all v1.0.0 requirements have evidence and no release-blocking issue remains.

---

# 12. READY standard for a lesson — Chuẩn READY

| Area | Acceptance condition |
|---|---|
| Objectives | 2–4 observable outcomes aligned with prerequisite |
| Guidance | runnable steps/input/fallback; not merely “practice this” |
| Bilingual | technical English explained before required use; contextual Vietnamese support |
| Example | at least one complete example with verification |
| Practice | guided + self/transfer practice where appropriate |
| Sources | direct official links, source date and feature uncertainty when relevant |
| Access | environment/account requirements and fallback |
| Scoring | rubric + answer guidance + remediation path |
| Data | synthetic/authorized data; missing facts not invented |
| Evidence | exactly what learner should save; privacy rules |
| Navigation | previous/next existing path or clearly marked future lesson |

`READY` is a content-publication state. It is never proof that a learner has passed.

---

# 13. Work-package backlog — U01–U14

| ID | Work package | Dependency | Status / exit condition |
|---|---|---|---|
| U01 | Start path, infrastructure, templates | baseline | **DONE** — P0 pass |
| U02 | BOOT.1–BOOT.4 + BOOT Check | U01 | **DONE** — P1 pass |
| U03 | M00.1–M00.3 + 10 scenarios | U02 | **DONE** — M00 READY |
| U04 | M01.1–M01.4 + 5 task specs | U03 | **DONE** — P2 content pass |
| U05 | 3 labs + fixed data + eval/assessment framework | U04 | **DONE** — pre-pilot QA pass |
| U06 | real beginner pilot + fixes + v0.2.0 decision | U05 | **NEXT** — Gate P3 |
| U07 | M02 + personal benchmark | U06 | PLANNED |
| U08 | M03 + context/Project example | U07 | PLANNED |
| U09 | M04 + research memo example | U08 | PLANNED |
| U10 | M05 + multimodal mini-labs | U09 | PLANNED |
| U11 | Foundation capstone + pilot + v0.3.0 | U10 | PLANNED — Gate P4 |
| U12 | M06–M08 Power User | U11 | PLANNED — Gate P5 |
| U13 | Builder prerequisites + M09–M11 | U12 | PLANNED — Gate P6 |
| U14 | Builder capstone + full QA + release | U13 | PLANNED — Gate P7 / v1.0.0 |

**Current priority:** U06 only. Do not start M02 before deciding whether beginner feedback requires changes to BOOT–M01.

---

# 14. Verification and maintenance workflow — Quy trình cập nhật

For every Uxx package:

1. fetch current `main` state;
2. verify time-sensitive OpenAI product claims against current official sources;
3. implement one coherent package;
4. update content status/navigation/changelog;
5. keep learner PROGRESS untouched unless learner evidence exists;
6. inspect changed paths on GitHub after writing;
7. record QA evidence and limitations;
8. move affected lessons to NEEDS UPDATE when current product behavior invalidates their instructions.

## Immediate next action

Run **U06 Beginner Pilot** using [BEGINNER-PILOT.md](BEGINNER-PILOT.md). The preview must remain unreleased until that pilot and required retests are recorded.
