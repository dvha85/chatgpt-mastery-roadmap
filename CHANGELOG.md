# Changelog

## Unreleased — Learn delta sync — 2026-11-05

- Kiểm nguồn mới nhất ChatGPT Learn (What's New tuần 2026-10-26–30, Changelog tới 2026-10-29, Models, Model Selection, Meet dots); ghi riêng [báo cáo có nguồn](docs/LEARN-SYNC-2026-11-05.md).
- Bổ sung GPT-6.1 Terra vào nhánh M02/M06, giới hạn Work/Codex (không phải Chat); cập nhật dots iMessage/RCS beta cho Pro tại Mỹ ở X01, Codex CLI 0.164–0.166 ở M09 và media trên iOS ở M05.
- Cập nhật bản đồ chương trình, nguồn, điều kiện tính năng và README; giữ ngày QA cũ. Không kiểm thử tính năng, không tạo lesson READY giả.
- Giữ PROGRESS.md, 56 bài cốt lõi (11 READY/45 PLANNED), 4 chuyên đề tùy chọn PLANNED và chính sách Vocabulary-first, không yêu cầu viết prompt tiếng Anh.

## Unreleased — Learn curriculum sync — 2026-10-22

- Đối chiếu ChatGPT Learn, các trang nền tảng/tính năng, What's new, changelog và Help Center; thêm `docs/LEARN-SYNC-2026-10-22.md` với nguồn và phạm vi xác minh.
- Cập nhật `CURRICULUM.md` cho 56 bài cốt lõi, giữ nguyên ID, thứ tự nền tảng và tiêu chí PASS chính; làm rõ model benchmark, Project/local context, file review, Work local/cloud, permissions, plugins/skills/tasks và nhánh Builder.
- Thêm bốn chuyên đề tùy chọn PLANNED: dots, Space, Sites, workspace administration; có prerequisite, lab dự kiến, evidence và fallback; không cộng vào 56 bài cốt lõi.
- Cập nhật `OFFICIAL-SOURCES.md`, tách nguồn đã đọc khỏi trang chỉ định tuyến; ngày rà soát đề cương không thay ngày QA từng bài.
- Cập nhật `docs/FEATURE-AVAILABILITY.md`: không lấy tài liệu làm bằng chứng tài khoản có quyền; phân biệt đọc tài liệu, kiểm tính năng, READY và PASS.
- Đồng bộ README, START-HERE và CONTENT-STATUS; sửa cách mô tả pilot: đã bắt đầu ở BOOT nhưng chưa hoàn thành đầu-cuối, P3 release gate vẫn pending.
- Giữ Vocabulary-first; không bắt viết câu/prompt tiếng Anh. Không sửa PROGRESS hoặc evidence người học; không tự nâng PLANNED thành READY.
- Đây là cập nhật chương trình và định tuyến nội dung, không phải phát hành đầy đủ M02–M11 hoặc xác nhận đã kiểm thử các tính năng mới.

## Unreleased — v0.2.0 preview — 2026-09-11

- Chuyển ngôn ngữ vận hành của khóa học sang **Vietnamese-first**: prompt, task brief, follow-up, verification prompt, ví dụ thực hành và ChatGPT exercise dùng tiếng Việt làm bản chính.
- Thêm `docs/VIETNAMESE-FIRST-USAGE.md` và `modules/M00-mental-model/M00-VI-PROMPT-PACK.md`.
- Cập nhật `LESSON-TEMPLATE.md` và `docs/BILINGUAL-LESSON-STANDARD.md`: English vẫn dùng cho thuật ngữ, đọc hiểu và English track nhưng không còn là ngôn ngữ bắt buộc của ChatGPT track.
- Việt hóa phần vận hành của toàn bộ **11 lesson READY**: BOOT.1–BOOT.4, M00.1–M00.3 và M01.1–M01.4.
- Việt hóa ví dụ/task spec trong `M00-CHECK.md`, `M01-CHECK.md`, `ANSWER-KEY.md`, Prompt Lab, Evaluation Lab và ba guided labs P-001/P-002/P-003.
- Giữ nguyên tên sản phẩm, thuật ngữ kỹ thuật chuẩn, code identifier, command và API field khi dịch sẽ làm sai nghĩa hoặc thao tác.
- README và module overview đã được cập nhật để nêu rõ ChatGPT track có thể hoàn thành hoàn toàn bằng tiếng Việt.

## Unreleased — v0.2.0 preview — 2026-09-10

- Hoàn thiện U01/P0: sửa hướng dẫn lưu private repository, đồng bộ tên lesson, rubric, metadata tính năng, thời lượng session và điều hướng.
- Triển khai U02/P1: thêm BOOT.1–BOOT.4 song ngữ, module README, dữ liệu mẫu, BOOT Check, evidence mẫu và QA checklist.
- Triển khai U03: thêm M00.1–M00.3, M00 Check 10 tình huống, đáp án giải thích và M00 QA evidence.
- Triển khai U04: thêm M01.1–M01.4, M01 Check 5 task specifications, supplied broken-output verification exercise và M01 QA evidence.
- Triển khai U05: nâng cấp Prompt Lab/Evaluation Lab; thêm P-001 Summary, P-002 Planning, P-003 Comparison; thêm fixed synthetic dataset + ground truth; Assessment Guide, Answer Key/Remediation Map và U05 Pre-Pilot QA.
- Chuẩn bị `docs/BEGINNER-PILOT.md` cho U06 với trạng thái `PREPARED — NOT RUN`; self-QA không được tính là pilot với người mới thật.
- Đánh dấu **11 lesson BOOT–M01 READY**; 45 lesson M02–M11 tiếp tục PLANNED.
- Hoàn tất P2 và phần pre-pilot của P3 trong U05; **P3 release gate vẫn pending U06 beginner pilot, blocker fixes, retest và release decision**.
- Mở rộng `GLOSSARY.md`, cập nhật README/START-HERE/CURRICULUM/CONTENT-STATUS/UPDATE-PLAN theo từng gói và nối navigation M00 → M01 → Labs/Assessments.

## v0.1.3 — 2026-09-10
- Triển khai U01/P0: thêm Start Here, learning paths, content status, feature availability, troubleshooting và evidence workflow.
- Mở rộng curriculum với 4 bài BOOT ở trạng thái PLANNED; chưa phát hành bài giảng mới.
- Chuẩn hóa lesson metadata về prerequisite, môi trường, điều kiện tài khoản và trạng thái biên soạn.

## v0.1.2 — 2026-09-10
- Thêm `docs/UPDATE-PLAN.md`: kế hoạch hoàn thiện khóa học cho người mới, gồm 8 giai đoạn P0–P7 và 14 gói công việc U01–U14.
- Đặc tả 4 bài BOOT và 7 bài M00–M01; lập kế hoạch cho tổng 56 bài, labs, checkpoints và 3 capstone theo trình độ.
- Bổ sung tiêu chuẩn READY, rubric PASS, thử học thực tế, điều kiện truy cập tính năng và ước lượng công sức biên soạn.
- README liên kết kế hoạch và ghi rõ repo hiện mới có đề cương, chưa có bài giảng chi tiết.
- Đây là bản cập nhật kế hoạch; chưa triển khai các lesson mới và chưa thay đổi tiến độ học.

## v0.1.1 — 2026-09-10
- Chuyển toàn bộ roadmap sang chuẩn bài học song ngữ English–Tiếng Việt.
- Thêm `LESSON-TEMPLATE.md` cho cấu trúc bài học thống nhất.
- Thêm `GLOSSARY.md` để tích lũy thuật ngữ ChatGPT/AI.
- Bổ sung English track: Recognize → Understand → Use.
- Quy định English exposure tăng dần Stage A → B → C nhưng luôn giữ hỗ trợ tiếng Việt.

## v0.1.0 — 2026-09-10
- Khởi tạo roadmap 3 stage: Operator → Power User → Builder.
- Thêm 12 module M00–M11.
- Thêm PASS model và progress tracker.
- Thêm curated official sources.
- Thêm Prompt Lab, Evaluation Lab và Capstone.
