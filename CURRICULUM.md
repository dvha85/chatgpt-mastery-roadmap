# Curriculum

> **Publication status:** lesson ID không đồng nghĩa bài đã phát hành. Xem [Content Status](docs/CONTENT-STATUS.md) và [Start Here](START-HERE.md).

> **Language format / Định dạng ngôn ngữ:** all lessons are bilingual English–Vietnamese. Technical terms use their canonical English names, with plain-English definitions, contextual Vietnamese explanations, examples, and a cumulative glossary. English exposure increases gradually across the three stages.

## Stage 0 — Getting started / Khởi động

> **Status:** READY. Bốn lesson BOOT đã được phát hành trong U02.

**[BOOT.1 — First chat / Cuộc chat đầu tiên](modules/BOOT-getting-started/BOOT.1-first-chat.md)**  
Mở ChatGPT, gửi yêu cầu đầu tiên và nhận biết prompt/response.

**[BOOT.2 — Conversation basics / Thao tác hội thoại cơ bản](modules/BOOT-getting-started/BOOT.2-conversation-basics.md)**  
Sửa, rút gọn, đổi format và nhận biết context của chat hiện tại.

**[BOOT.3 — Safe use & verification / Dùng an toàn và kiểm chứng](modules/BOOT-getting-started/BOOT.3-safe-use-and-verification.md)**  
Hiểu câu trả lời có thể sai, kiểm tra một claim và dùng dữ liệu giả lập.

**[BOOT.4 — Save evidence / Lưu bằng chứng học tập](modules/BOOT-getting-started/BOOT.4-save-evidence.md)**  
Lưu prompt, kết quả, verification và reflection mà không đưa secret/dữ liệu riêng tư lên repo.

**PASS BOOT:** hoàn thành 4 bài, đạt BOOT Check và nộp evidence đã làm sạch.

---
## Stage A — ChatGPT Operator

### M00 — Mental model & choosing the right surface

> **Status:** READY. Ba lesson M00 và bộ M00 Check đã được phát hành trong U03.

**[M00.1 — Chat vs ChatGPT Work vs Codex](modules/M00-mental-model/M00.1-chat-work-codex.md)**  
Hiểu ba bề mặt, khi nào dùng từng loại, khi nào không nên dùng; phân biệt surface với tool.

**[M00.2 — How ChatGPT works / ChatGPT tạo câu trả lời như thế nào](modules/M00-mental-model/M00.2-how-chatgpt-works.md)**  
Hiểu model, context, tools, uncertainty, hallucination và giới hạn; biết vì sao câu trả lời tự tin vẫn cần kiểm chứng.

**[M00.3 — Task Brief and Verification / Giao việc và kiểm chứng](modules/M00-mental-model/M00.3-task-and-verification.md)**  
Dùng mental model `Outcome → Context → Tools → Verification`, thêm boundaries và acceptance criteria khi cần.

**[M00 Check — 10 tình huống thực hành](assessments/M00-CHECK.md)**  
Chọn surface/tool, viết task brief, xác định điểm cần verification và so với đáp án giải thích.

**PASS M00:** đạt ít nhất 16/20 ở M00 Check; giải thích đúng Chat, Work, Codex, model, context, tool và surface; viết được ít nhất một task brief O-C-T-V hoàn chỉnh; kiểm chứng được ít nhất một claim bằng nguồn, phép tính, test hoặc human review phù hợp.

### M01 — Prompting as task specification

> **Status:** READY. Bốn lesson M01 và M01 Check đã được phát hành trong U04; P2 content scope hoàn tất.

**[M01.1 — Prompt Foundations / Nền tảng viết yêu cầu](modules/M01-prompting/M01.1-prompt-foundations.md)**  
Goal + Context + Output + Boundaries; prompt ngắn vẫn tốt nếu đủ thông tin và chỉ thêm context có ích.

**[M01.2 — Iterate and Decompose / Lặp lại và chia nhỏ tác vụ](modules/M01-prompting/M01.2-iterate-and-decompose.md)**  
Bổ sung thông tin bằng follow-up có mục tiêu, chia task tại verification boundaries, dùng checkpoints và biết khi nào mở chat mới.

**[M01.3 — Output Contracts / Hợp đồng đầu ra](modules/M01-prompting/M01.3-output-contracts.md)**  
Format, required fields, missing-data rules, checklist và acceptance criteria; schema kỹ thuật được để dành cho builder track.

**[M01.4 — Verify Answers / Kiểm chứng câu trả lời](modules/M01-prompting/M01.4-verify-answers.md)**  
Claim → Evidence → Conclusion; kiểm source, calculation, test, assumptions và dùng correction prompt khi phát hiện unsupported claim.

**[M01 Check — 5 task specifications](assessments/M01-CHECK.md)**  
Viết lại 5 yêu cầu mơ hồ thành task spec có thể chạy và kiểm; ít nhất một task phải có response + verification evidence thật.

**PASS M01:** nộp đủ 5/5 task spec; ít nhất 4/5 đạt mức 2 theo rubric, task còn lại ít nhất mức 1; chạy và kiểm ít nhất một spec; không dùng lời tự xác nhận của AI thay cho evidence.

### M02 — Models & reasoning

**M02.1 — Model selection**  
Không phải model mạnh nhất luôn là lựa chọn tốt nhất.

**M02.2 — Reasoning effort**  
Khi nào cần suy luận sâu; trade-off chất lượng, tốc độ và chi phí/quota.

**M02.3 — Build your own task benchmark**  
Đánh giá model bằng tác vụ của chính mình thay vì cảm giác.

**PASS M02:** tạo mini benchmark 5 tác vụ và ghi quyết định model/reasoning cho từng loại.

### M03 — Context, personalization, Projects & Memory

**M03.1 — Context architecture**  
Phân biệt nội dung chat hiện tại, file, project context và connected data.

**M03.2 — Personalization & instructions**  
Đưa preference bền vững vào đúng tầng.

**M03.3 — Projects & chats**  
Tổ chức công việc dài hạn, tách project, giữ context sạch.

**M03.4 — Memory: khi nào hữu ích, khi nào không**  
Không dùng memory như database hay source of truth.

**M03.5 — Files as source context**  
Upload, hỏi đúng phạm vi, trích dẫn và kiểm chứng nội dung file.

**PASS M03:** thiết kế một Project thật với instructions, files và quy tắc context rõ ràng.

### M04 — Web Search & Deep Research

**M04.1 — Web Search**  
Khi nào cần web, freshness, query formulation, citations.

**M04.2 — Source quality**  
Primary vs secondary sources, recency, conflicts, provenance.

**M04.3 — Deep Research**  
Khi nào search thường chưa đủ; scope, plan, source selection, review.

**M04.4 — Research workflow**  
Question → source plan → evidence → synthesis → verification → decision.

**PASS M04:** hoàn thành một research memo có nguồn, claim-evidence mapping và phần uncertainty.

---

## Stage B — ChatGPT Power User

### M05 — Files & multimodal work

**M05.1 — Image inputs**  
Phân tích screenshot, diagram, photo và visual evidence.

**M05.2 — Image generation & editing**  
Viết visual brief, iterative editing, consistency.

**M05.3 — Documents, spreadsheets, presentations & PDFs**  
Source data, output spec, review criteria và render/verify mindset.

**M05.4 — Voice**  
Khi voice tốt hơn text; capture, synthesis và follow-up.

**PASS M05:** hoàn thành một tác vụ có ít nhất 2 modality và vòng review.

### M06 — ChatGPT Work, Browser & Computer Use

**M06.1 — ChatGPT Work**  
Giao outcome thay vì từng câu hỏi nhỏ; reviewable deliverables.

**M06.2 — Long-running work**  
Definition of done, constraints, checkpoints, steering.

**M06.3 — Browser vs Web Search**  
Đọc/tương tác website so với chỉ lấy thông tin.

**M06.4 — Computer Use**  
Khi cần GUI interaction; confirmation points và rủi ro.

**M06.5 — Permissions & sandboxing mindset**  
Least privilege, destructive actions, review before commit/send/publish.

**PASS M06:** viết task brief cho một công việc nhiều bước có tool choice, permissions và checkpoints.

### M07 — Plugins & connected data

**M07.1 — Built-in tool vs Plugin**  
Chọn đúng nguồn năng lực.

**M07.2 — Permissions & data boundaries**  
Đọc/ghi, scope, connected accounts và nguyên tắc least privilege.

**M07.3 — Connected workflow design**  
Ví dụ: Gmail/Calendar/Drive/GitHub hoặc hệ thống tương đương.

**M07.4 — Human-in-the-loop actions**  
Phân biệt read, draft, modify, send/publish và hành động khó hoàn tác.

**PASS M07:** thiết kế một workflow qua ít nhất 2 connected systems, nêu rõ quyền và điểm cần human review.

### M08 — Skills & Scheduled Tasks

**M08.1 — Skill vs Plugin**  
Reusable instructions so với installable workflow + connected services.

**M08.2 — Designing a reusable Skill**  
Trigger, instructions, resources, scripts, verification.

**M08.3 — Scheduled Tasks**  
One-time, recurring và condition/event-driven workflows.

**M08.4 — Automation reliability**  
Idempotency, state, alert fatigue, retry, stop conditions, failure reporting.

**M08.5 — Evaluate before automate**  
Test thủ công trước, automation sau.

**PASS M08:** biến một workflow thủ công đã test thành reusable workflow và automation spec.

---

## Stage C — Builder

### M09 — Codex & GitHub

**M09.1 — Codex surfaces**  
ChatGPT/Codex app, CLI, IDE/cloud và lựa chọn theo tác vụ.

**M09.2 — Repository context**  
README, AGENTS.md, tests, conventions, scope.

**M09.3 — Coding task specification**  
Bugfix, feature, refactor, migration và acceptance tests.

**M09.4 — GitHub workflow**  
Issues, branches, commits, PR review, CI evidence.

**M09.5 — Safe autonomous coding**  
Sandbox, permissions, tests, diff review, rollback.

**PASS M09:** hoàn thành một thay đổi repo nhỏ có test + commit/PR evidence.

### M10 — API, MCP & Agents

**M10.1 — ChatGPT vs API mental model**  
Product workflow và programmable system khác nhau thế nào.

**M10.2 — Responses API & tools**  
Conversation state, tool calling, structured outputs.

**M10.3 — MCP & connectors**  
Chuẩn kết nối model với tools/data.

**M10.4 — Agents SDK**  
Agent definitions, orchestration, guardrails, state, observability.

**M10.5 — Evals**  
Đánh giá chất lượng workflow thay vì demo một lần.

**PASS M10:** vẽ architecture của một agent và định nghĩa ít nhất 5 eval cases.

### M11 — Agentic system design

**M11.1 — Workflow before agent**  
Không dùng agent khi deterministic workflow đủ tốt.

**M11.2 — State, tools & boundaries**  
Ai sở hữu state, tool contract, permission boundary.

**M11.3 — Human review architecture**  
Checkpoint dựa trên risk/cost/reversibility.

**M11.4 — Observability & improvement loop**  
Logs, traces, errors, evals, feedback và versioning.

**M11.5 — Production readiness**  
Reliability, security, cost, compliance, fallback.

**PASS M11:** system design review cho capstone trước khi build.

---

## Capstone — Real workflow

Capstone mặc định: thiết kế một workflow hỗ trợ **nghiên cứu, quyết định hoặc vận hành bot/affiliate project** bằng ChatGPT + nguồn dữ liệu + tool + automation, nhưng giữ human review ở các hành động có rủi ro.

Xem [capstone/README.md](capstone/README.md).
