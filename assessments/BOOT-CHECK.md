# BOOT Check — Bài kiểm tra khởi động

> Làm sau BOOT.4. Không xem rubric chi tiết cho đến khi hoàn thành 10 tình huống.

## Instructions / Hướng dẫn

- Dùng dữ liệu giả lập hoặc [boot-sample-brief](../labs/data/boot-sample-brief.md).
- Ghi prompt, response, verification và reflection vào evidence.
- Với mỗi tình huống, ghi surface/chat choice, action và lý do.
- Không cần response giống đáp án; cần lý do và cách kiểm tra phù hợp.

## Ten situations / Mười tình huống

| # | Situation | Your output |
|---:|---|---|
| 1 | Bạn muốn giải thích một khái niệm AI cho người mới | Prompt + expected output |
| 2 | Bạn muốn response thành bảng hai cột | Follow-up + format check |
| 3 | Bạn đổi sang một nhiệm vụ không liên quan | Continue hay new chat + lý do |
| 4 | Response đưa ra một con số không có trong brief | Claim/evidence/uncertainty |
| 5 | Brief chứa tên và email khách hàng | Redacted input |
| 6 | Bạn muốn sửa một đoạn nhưng giữ nguyên dữ liệu | Refinement instruction |
| 7 | Bạn cần biết prompt nào đã tạo response | Evidence record |
| 8 | Bạn chưa kiểm tra một claim quan trọng | Verification step |
| 9 | Bạn muốn lưu evidence có dữ liệu công việc | Storage choice + privacy reason |
| 10 | Bạn áp dụng quy trình cho một task mới | Transfer evidence |

## Self-score / Tự chấm

Chấm 0–2 cho mỗi năng lực:
- `0`: chưa thực hiện hoặc sai cốt lõi.
- `1`: làm được một phần hoặc cần gợi ý.
- `2`: tự làm đúng, có lý do và evidence.

| Skill | Score 0–2 | Evidence location |
|---|---:|---|
| Explain | | |
| Execute | | |
| Diagnose | | |
| Verify | | |
| Transfer | | |
| English: Recognize | | |
| English: Understand | | |
| English: Use | | |

## BOOT PASS

PASS khi: ChatGPT track đạt ít nhất 8/10, không năng lực nào 0, Execute và Verify đạt 2; English track nhận ra 4/4 thuật ngữ kiểm tra, giải thích đúng 3 thuật ngữ và viết được một instruction tiếng Anh có nghĩa.

Nếu chưa PASS: đọc lại đúng bài liên quan, làm một tình huống tương đương với input khác và ghi lần đánh giá lại. Không dùng ví dụ của khóa học làm evidence của bạn.