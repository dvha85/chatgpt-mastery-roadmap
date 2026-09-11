# M01 — Prompting as Task Specification / Viết yêu cầu như bản giao việc

> **Content status:** READY  
> **Source snapshot:** 2026-09-10  
> **Operating language / Ngôn ngữ vận hành:** **Vietnamese-first**

## Outcome / Kết quả
Sau module này, người học có thể biến yêu cầu mơ hồ thành task specification rõ, cải thiện response theo vòng lặp, định nghĩa output có thể kiểm và xác minh các claim quan trọng trước khi sử dụng.

After this module, the learner can turn vague requests into clear task specifications, iterate deliberately, define reviewable outputs, and verify important claims before use.

> **Quy tắc:** Prompt, task brief, follow-up, output contract, verification prompt và bài ChatGPT exercise đều dùng **tiếng Việt làm bản chính**. Mẫu tiếng Anh chỉ nằm trong English track hoặc `English reference`. Xem [Vietnamese-first Usage](../../docs/VIETNAMESE-FIRST-USAGE.md).

## Lessons / Bài học
1. [M01.1 — Prompt Foundations / Nền tảng viết yêu cầu](M01.1-prompt-foundations.md) — Goal + Context + Output + Boundaries.
2. [M01.2 — Iterate and Decompose / Lặp lại và chia nhỏ tác vụ](M01.2-iterate-and-decompose.md) — follow-up có mục tiêu, decomposition, checkpoints.
3. [M01.3 — Output Contracts / Hợp đồng đầu ra](M01.3-output-contracts.md) — format, fields, checklist, unknown handling, acceptance criteria.
4. [M01.4 — Verify Answers / Kiểm chứng câu trả lời](M01.4-verify-answers.md) — Claim → Evidence → Conclusion, assumptions và correction prompts.

## Module mental model — Mô hình tư duy

```text
Đặc tả → Tạo → Kiểm tra → Chẩn đoán → Sửa → Kiểm chứng
Specify → Generate → Inspect → Diagnose → Revise → Verify
```

M01 không dạy “prompt thần kỳ”. Trọng tâm là giao việc đủ rõ và xây vòng review có thể lặp lại.

## Study rule — Quy tắc học
- Học theo thứ tự M01.1 → M01.4.
- Thực hành ChatGPT bằng tiếng Việt.
- Giữ thuật ngữ kỹ thuật tiếng Anh và học nghĩa qua English track.
- Dùng dữ liệu giả lập hoặc dữ liệu bạn có quyền sử dụng.
- Mỗi bài phải có evidence riêng; ví dụ khóa học không thay cho bài làm của người học.
- Không đánh dấu PASS chỉ vì response nghe hay; phải kiểm theo rubric/evidence.

## Guided practice path — Đường thực hành
Sau M01.4:
1. [P-001 — Summary Lab](../../labs/examples/P-001-summary.md) — grounding + output contract.
2. [P-002 — Planning Lab](../../labs/examples/P-002-planning.md) — decomposition + constraints + arithmetic.
3. [P-003 — Comparison Lab](../../labs/examples/P-003-comparison.md) — unknown handling + evidence-based recommendation.

Dữ liệu: [Sample Brief](../../labs/data/sample-brief.md).  
Experiment: [Prompt Lab](../../labs/PROMPT-LAB.md).  
Cách chấm/retest: [Evaluation Lab](../../labs/EVALUATION-LAB.md).

## Module assessment — Bài kiểm tra module
Hoàn thành [M01 Check — 5 task specifications](../../assessments/M01-CHECK.md). Chỉ mở [Answer Key](../../assessments/ANSWER-KEY.md) sau khi tự làm.

**PASS M01 khi:**
- nộp đủ 5/5 task spec bằng tiếng Việt;
- ít nhất 4/5 đạt mức 2;
- task còn lại ít nhất mức 1;
- ít nhất một task chạy thật và có response + verification evidence;
- giải thích được thuật ngữ trọng tâm bằng tiếng Việt.

**English track:** nhận diện/hiểu/dùng một số thuật ngữ và instruction tiếng Anh. Không bắt buộc dùng prompt tiếng Anh để PASS ChatGPT track.

## QA evidence — Bằng chứng QA nội dung
Tình trạng `READY` được kiểm tại [M01 QA Check](../../labs/examples/M01-qa-check.md); hệ thống lab/rubric trước pilot tại [U05 Pre-Pilot QA](../../labs/examples/U05-qa-check.md). QA khóa học không thay thế PASS của người học hoặc beginner pilot thật.

## Navigation — Điều hướng
← [M00 — Mental Model](../M00-mental-model/README.md) · [Start M01.1](M01.1-prompt-foundations.md) · [P-001 Summary Lab](../../labs/examples/P-001-summary.md) · [M01 Check](../../assessments/M01-CHECK.md) · [M02 — Models & Reasoning](../M02-models-reasoning/README.md) →
