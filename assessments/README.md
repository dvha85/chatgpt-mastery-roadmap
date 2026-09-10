# Assessments — Hướng dẫn làm bài kiểm tra

> Assessment đo năng lực người học. `READY` của tài liệu không tự động làm người học `PASS`.

## Available checkpoints — Các checkpoint hiện có

- [BOOT Check](BOOT-CHECK.md) — thao tác nền tảng, safe use và evidence.
- [M00 Check](M00-CHECK.md) — mental model, surface/tool, task brief và verification.
- [M01 Check](M01-CHECK.md) — viết 5 task specifications có thể thực hiện và kiểm.
- [Answer Key & Remediation Map](ANSWER-KEY.md) — cách dùng đáp án, lỗi thường gặp và bài cần ôn.

## How to take an assessment — Cách làm

1. Học các lesson prerequisite.
2. Mở checkpoint nhưng **không xem phần answer guide trước**.
3. Tự làm bài bằng dữ liệu giả lập hoặc dữ liệu bạn có quyền sử dụng.
4. Với phần yêu cầu chạy thật, lưu prompt + output + verification evidence.
5. Chấm bằng rubric được ghi trong checkpoint.
6. Đọc answer guide để chẩn đoán chênh lệch, không chép lại câu mẫu.
7. Nếu FAIL, chỉ học lại skill còn thiếu và làm một case tương đương mới.
8. Chỉ cập nhật [PROGRESS.md](../PROGRESS.md) khi evidence của chính bạn đạt gate.

## General 0–2 scale — Thang điểm chung

| Score | Meaning |
|---:|---|
| 0 | Chưa chứng minh hoặc sai cốt lõi |
| 1 | Làm được một phần / cần gợi ý đáng kể |
| 2 | Tự làm đúng và có evidence phù hợp |

Checkpoint riêng có thể thêm điều kiện bắt buộc, ví dụ một câu critical không được `0`.

## Five-capability lens — 5 năng lực

Khi review tổng hợp, hỏi:

- **Explain** — giải thích được khái niệm?
- **Execute** — tự làm task?
- **Diagnose** — tìm được lỗi?
- **Verify** — kiểm bằng evidence độc lập?
- **Transfer** — áp dụng sang task mới?

Thang tổng hợp P3: >=8/10, không năng lực nào 0, Execute = 2 và Verify = 2.

## English track — Nhánh tiếng Anh

Mục tiêu là hiểu và dùng thuật ngữ, không phải thi ngữ pháp:

- Recognize: nhận ra thuật ngữ.
- Understand: giải thích đúng bằng tiếng Việt.
- Use: dùng trong instruction/prompt có nghĩa đúng.

Lỗi ngữ pháp nhỏ không đổi intent không phải lý do để đánh trượt năng lực ChatGPT.

## Evidence rules — Quy tắc bằng chứng

Evidence tốt gồm:

- task/input;
- prompt hoặc task spec;
- output;
- verification;
- rubric score;
- reflection/retest nếu cần.

Không công khai password, API key, token, payment data, thông tin khách hàng hoặc dữ liệu riêng tư. Xem [Evidence Guide](../evidence/README.md).

## If you fail — Nếu chưa đạt

Không học lại toàn bộ từ đầu. Dùng vòng:

```text
missing criterion
→ matching lesson/example
→ one focused practice
→ new equivalent case
→ verification
→ retest evidence
```

Xem [ANSWER-KEY.md](ANSWER-KEY.md) để map lỗi về bài cần ôn.
