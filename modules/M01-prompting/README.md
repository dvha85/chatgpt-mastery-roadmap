# M01 — Prompting as Task Specification / Viết yêu cầu như bản giao việc

> **Content status:** READY  
> **Source snapshot:** 2026-09-10

## Outcome / Kết quả

Sau module này, người học có thể biến yêu cầu mơ hồ thành task specification rõ, cải thiện response theo vòng lặp, định nghĩa output có thể kiểm và xác minh các claim quan trọng trước khi sử dụng.

After this module, the learner can turn vague requests into clear task specifications, iterate deliberately, define reviewable outputs, and verify important claims before use.

## Lessons / Bài học

1. [M01.1 — Prompt Foundations / Nền tảng viết yêu cầu](M01.1-prompt-foundations.md)  
   Goal + Context + Output + Boundaries; prompt ngắn vẫn tốt nếu đủ thông tin.
2. [M01.2 — Iterate and Decompose / Lặp lại và chia nhỏ tác vụ](M01.2-iterate-and-decompose.md)  
   Follow-up có mục tiêu, decomposition, checkpoints và same chat vs new chat.
3. [M01.3 — Output Contracts / Hợp đồng đầu ra](M01.3-output-contracts.md)  
   Format, fields, checklist, missing-data rules và acceptance criteria.
4. [M01.4 — Verify Answers / Kiểm chứng câu trả lời](M01.4-verify-answers.md)  
   Claim → Evidence → Conclusion, assumptions, source/calculation/test checks và correction prompts.

## Module mental model — Mô hình tư duy

```text
Specify → Generate → Inspect → Diagnose → Revise → Verify
Đặc tả → Tạo → Kiểm tra → Chẩn đoán → Sửa → Kiểm chứng
```

M01 không dạy “prompt thần kỳ”. Trọng tâm là giao việc đủ rõ và xây một vòng review có thể lặp lại.

## Study rule — Quy tắc học

- Học theo thứ tự M01.1 → M01.4.
- Dùng dữ liệu giả lập hoặc dữ liệu bạn có quyền sử dụng.
- Mỗi bài phải có evidence riêng; ví dụ của khóa học không được dùng thay cho bài làm của người học.
- Nếu feature/tool không có, dùng fallback trong bài và chỉ ghi năng lực thực sự đã chứng minh.
- Không đánh dấu PASS chỉ vì response nghe hay; phải kiểm theo rubric hoặc evidence.

## Guided practice path — Đường thực hành có hướng dẫn

Sau M01.4, làm ba lab với cùng dữ liệu cố định để luyện cách chẩn đoán và kiểm chứng:

1. [P-001 — Summary Lab](../../labs/examples/P-001-summary.md) — grounding và output contract.
2. [P-002 — Planning Lab](../../labs/examples/P-002-planning.md) — decomposition, constraints và arithmetic verification.
3. [P-003 — Comparison Lab](../../labs/examples/P-003-comparison.md) — unknown handling, criteria và evidence-based recommendation.

Dữ liệu chung: [Sample Brief](../../labs/data/sample-brief.md).  
Quy trình experiment: [Prompt Lab](../../labs/PROMPT-LAB.md).  
Cách chấm 0–2 và retest: [Evaluation Lab](../../labs/EVALUATION-LAB.md).

## Module assessment — Bài kiểm tra module

Sau khi làm lab, hoàn thành [M01 Check — 5 task specifications](../../assessments/M01-CHECK.md). Xem [Assessment Guide](../../assessments/README.md) trước khi chấm; chỉ mở [Answer Key](../../assessments/ANSWER-KEY.md) sau khi đã tự làm.

**PASS M01 khi:**

- nộp đủ 5/5 task spec;
- ít nhất 4/5 đạt mức 2 theo rubric;
- task còn lại ít nhất mức 1;
- ít nhất một task được chạy thật và có response + verification evidence;
- giải thích được các thuật ngữ trọng tâm bằng tiếng Việt và viết được ít nhất một instruction tiếng Anh đúng nghĩa.

## QA evidence — Bằng chứng QA nội dung

Tình trạng `READY` của lesson được kiểm tra tại [M01 QA Check](../../labs/examples/M01-qa-check.md). Hệ thống lab/rubric trước pilot được kiểm tra tại [U05 Pre-Pilot QA](../../labs/examples/U05-qa-check.md). Đây là QA của khóa học, không phải PASS của người học và không thay thế beginner pilot thật.

## Navigation — Điều hướng

← [M00 — Mental Model](../M00-mental-model/README.md) · [Start M01.1](M01.1-prompt-foundations.md) · [P-001 Summary Lab](../../labs/examples/P-001-summary.md) · [M01 Check](../../assessments/M01-CHECK.md) · [M02 — Models & Reasoning](../M02-models-reasoning/README.md) →
