# Content Status — Trạng thái biên soạn

> Tài liệu khóa học được theo dõi ở đây; [PROGRESS.md](../PROGRESS.md) theo dõi năng lực người học. Cập nhật đề cương không tự tạo bài giảng hay PASS.

| Status | Ý nghĩa | Chuyển bài được? |
|---|---|---|
| `PLANNED` | Có đề cương, chưa có bài hoàn chỉnh | Không |
| `DRAFT` | Có bản thảo, chưa đủ kiểm tra | Không |
| `IN REVIEW` | Đang kiểm nguồn, bài tập, ngôn ngữ hoặc pilot | Không |
| `READY` | Đủ tiêu chuẩn bài, QA evidence và link hợp lệ | Có |
| `NEEDS UPDATE` | Bài READY cần rà lại vì nguồn/UI/nội dung đổi | Không |

## Snapshot

- **Curriculum/source-map sync:** 2026-10-22, xem [Learn Sync](LEARN-SYNC-2026-10-22.md).
- **Lesson QA/source dates:** giữ nguyên từng hàng bên dưới; không đánh dấu toàn bộ bài đã QA lại ngày 2026-10-22.
- **Core scope:** 56 lesson (4 BOOT + 52 bài M00–M11); **11 READY / 45 PLANNED**.
- **Optional scope:** 4 chuyên đề X01–X04 đều PLANNED; ngoài số 56 bài cốt lõi, chưa có lesson hoàn chỉnh.
- P2 content scope đã hoàn tất. U05 pre-pilot P3 work đã hoàn tất.
- U06 pilot đã bắt đầu theo PROGRESS: BOOT.1–BOOT.2 PASS, BOOT.3 IN PROGRESS. Chưa hoàn thành pilot đầu-cuối BOOT → M00 → M01.
- **P3 release gate: NOT YET PASS**; vẫn cần hoàn thành pilot, sửa blocker, retest và quyết định release.

## Lesson registry — Giữ nguyên mã bài cốt lõi

| ID | Path dự kiến | Status | Source checked | QA evidence |
|---|---|---|---|---|
| BOOT.1 | `modules/BOOT-getting-started/BOOT.1-first-chat.md` | READY | 2026-09-10 | `labs/examples/BOOT-qa-check.md` |
| BOOT.2 | `modules/BOOT-getting-started/BOOT.2-conversation-basics.md` | READY | 2026-09-10 | `labs/examples/BOOT-qa-check.md` |
| BOOT.3 | `modules/BOOT-getting-started/BOOT.3-safe-use-and-verification.md` | READY | 2026-09-10 | `labs/examples/BOOT-qa-check.md` |
| BOOT.4 | `modules/BOOT-getting-started/BOOT.4-save-evidence.md` | READY | 2026-09-10 | `labs/examples/BOOT-qa-check.md` |
| M00.1 | `modules/M00-mental-model/M00.1-chat-work-codex.md` | READY | 2026-09-10 | `labs/examples/M00-qa-check.md` |
| M00.2 | `modules/M00-mental-model/M00.2-how-chatgpt-works.md` | READY | 2026-09-10 | `labs/examples/M00-qa-check.md` |
| M00.3 | `modules/M00-mental-model/M00.3-task-and-verification.md` | READY | 2026-09-10 | `labs/examples/M00-qa-check.md` |
| M01.1 | `modules/M01-prompting/M01.1-prompt-foundations.md` | READY | 2026-09-10 | `labs/examples/M01-qa-check.md` |
| M01.2 | `modules/M01-prompting/M01.2-iterate-and-decompose.md` | READY | 2026-09-10 | `labs/examples/M01-qa-check.md` |
| M01.3 | `modules/M01-prompting/M01.3-output-contracts.md` | READY | 2026-09-10 | `labs/examples/M01-qa-check.md` |
| M01.4 | `modules/M01-prompting/M01.4-verify-answers.md` | READY | 2026-09-10 | `labs/examples/M01-qa-check.md` |
| M02.1 | `modules/M02-models-reasoning/M02.1-model-selection.md` | PLANNED | — | — |
| M02.2 | `modules/M02-models-reasoning/M02.2-reasoning-effort.md` | PLANNED | — | — |
| M02.3 | `modules/M02-models-reasoning/M02.3-personal-benchmark.md` | PLANNED | — | — |
| M03.1 | `modules/M03-context-projects-memory/M03.1-context-architecture.md` | PLANNED | — | — |
| M03.2 | `modules/M03-context-projects-memory/M03.2-personalization.md` | PLANNED | — | — |
| M03.3 | `modules/M03-context-projects-memory/M03.3-projects-and-chats.md` | PLANNED | — | — |
| M03.4 | `modules/M03-context-projects-memory/M03.4-memory.md` | PLANNED | — | — |
| M03.5 | `modules/M03-context-projects-memory/M03.5-files-as-context.md` | PLANNED | — | — |
| M04.1 | `modules/M04-search-research/M04.1-web-search.md` | PLANNED | — | — |
| M04.2 | `modules/M04-search-research/M04.2-source-quality.md` | PLANNED | — | — |
| M04.3 | `modules/M04-search-research/M04.3-deep-research.md` | PLANNED | — | — |
| M04.4 | `modules/M04-search-research/M04.4-research-workflow.md` | PLANNED | — | — |
| M05.1 | `modules/M05-files-multimodal/M05.1-image-inputs.md` | PLANNED | — | — |
| M05.2 | `modules/M05-files-multimodal/M05.2-image-generation.md` | PLANNED | — | — |
| M05.3 | `modules/M05-files-multimodal/M05.3-files-and-artifacts.md` | PLANNED | — | — |
| M05.4 | `modules/M05-files-multimodal/M05.4-voice.md` | PLANNED | — | — |
| M06.1 | `modules/M06-work-browser-computer/M06.1-chatgpt-work.md` | PLANNED | — | — |
| M06.2 | `modules/M06-work-browser-computer/M06.2-long-running-work.md` | PLANNED | — | — |
| M06.3 | `modules/M06-work-browser-computer/M06.3-browser-vs-search.md` | PLANNED | — | — |
| M06.4 | `modules/M06-work-browser-computer/M06.4-computer-use.md` | PLANNED | — | — |
| M06.5 | `modules/M06-work-browser-computer/M06.5-permissions.md` | PLANNED | — | — |
| M07.1 | `modules/M07-plugins-connected-data/M07.1-built-in-vs-plugin.md` | PLANNED | — | — |
| M07.2 | `modules/M07-plugins-connected-data/M07.2-data-boundaries.md` | PLANNED | — | — |
| M07.3 | `modules/M07-plugins-connected-data/M07.3-connected-workflows.md` | PLANNED | — | — |
| M07.4 | `modules/M07-plugins-connected-data/M07.4-human-in-the-loop.md` | PLANNED | — | — |
| M08.1 | `modules/M08-skills-automation/M08.1-skill-vs-plugin.md` | PLANNED | — | — |
| M08.2 | `modules/M08-skills-automation/M08.2-reusable-skill.md` | PLANNED | — | — |
| M08.3 | `modules/M08-skills-automation/M08.3-scheduled-tasks.md` | PLANNED | — | — |
| M08.4 | `modules/M08-skills-automation/M08.4-automation-reliability.md` | PLANNED | — | — |
| M08.5 | `modules/M08-skills-automation/M08.5-evaluate-before-automate.md` | PLANNED | — | — |
| M09.1 | `modules/M09-codex-github/M09.1-codex-surfaces.md` | PLANNED | — | — |
| M09.2 | `modules/M09-codex-github/M09.2-repository-context.md` | PLANNED | — | — |
| M09.3 | `modules/M09-codex-github/M09.3-coding-task-specification.md` | PLANNED | — | — |
| M09.4 | `modules/M09-codex-github/M09.4-github-workflow.md` | PLANNED | — | — |
| M09.5 | `modules/M09-codex-github/M09.5-safe-coding.md` | PLANNED | — | — |
| M10.1 | `modules/M10-api-mcp-agents/M10.1-chatgpt-vs-api.md` | PLANNED | — | — |
| M10.2 | `modules/M10-api-mcp-agents/M10.2-responses-and-tools.md` | PLANNED | — | — |
| M10.3 | `modules/M10-api-mcp-agents/M10.3-mcp-and-connectors.md` | PLANNED | — | — |
| M10.4 | `modules/M10-api-mcp-agents/M10.4-agents-sdk.md` | PLANNED | — | — |
| M10.5 | `modules/M10-api-mcp-agents/M10.5-evals.md` | PLANNED | — | — |
| M11.1 | `modules/M11-agentic-system-design/M11.1-workflow-before-agent.md` | PLANNED | — | — |
| M11.2 | `modules/M11-agentic-system-design/M11.2-state-tools-boundaries.md` | PLANNED | — | — |
| M11.3 | `modules/M11-agentic-system-design/M11.3-human-review.md` | PLANNED | — | — |
| M11.4 | `modules/M11-agentic-system-design/M11.4-observability.md` | PLANNED | — | — |
| M11.5 | `modules/M11-agentic-system-design/M11.5-production-readiness.md` | PLANNED | — | — |

## Optional registry — Chưa phải lesson phát hành

| Mã | Chuyên đề | Trạng thái | Đặc tả hiện có |
|---|---|---|---|
| X01 | dots | PLANNED | [Learn Sync](LEARN-SYNC-2026-10-22.md) |
| X02 | Space / Pages / collaboration | PLANNED | [Learn Sync](LEARN-SYNC-2026-10-22.md) |
| X03 | Sites | PLANNED | [Learn Sync](LEARN-SYNC-2026-10-22.md) |
| X04 | Workspace administration | PLANNED | [Learn Sync](LEARN-SYNC-2026-10-22.md) |

Chưa tạo đường dẫn lesson giả cho X01–X04. Chỉ thêm bảng tiến độ chuyên đề khi người học chọn và có bài READY; không sửa các hàng hiện có của PROGRESS trong đợt đồng bộ.

## QA và cách đổi trạng thái

BOOT: [QA](../labs/examples/BOOT-qa-check.md). M00: [QA](../labs/examples/M00-qa-check.md). M01: [QA](../labs/examples/M01-qa-check.md). U05: [Pre-Pilot QA](../labs/examples/U05-qa-check.md).

Viết theo [Lesson Template](../LESSON-TEMPLATE.md); ghi nguồn, môi trường, dữ liệu, fallback và rubric. Kiểm ví dụ, bài tự làm, đáp án, ngôn ngữ, link và privacy; lưu QA evidence trước khi chuyển READY. Nếu thay đổi sản phẩm làm hướng dẫn sai, đánh dấu NEEDS UPDATE và sửa đúng bài; không mặc định mọi bài cũ hỏng chỉ vì thêm một tính năng mới.

Release gate yêu cầu pilot thật theo [Beginner Pilot](BEGINNER-PILOT.md). Self-QA và cập nhật nguồn không thay thế pilot. `READY` của bài không biến `PROGRESS` thành `PASS`.
