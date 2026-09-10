# Roadmap Design Decisions

## D1 — Không học prompt engineering như một môn độc lập

Prompt chỉ là một phần của task specification. Chất lượng còn phụ thuộc context, tool choice, source quality, permissions và verification.

## D2 — Học product trước, builder sau

Người học cần sử dụng tốt ChatGPT trước khi xây agent bằng API. Điều này giúp tránh tự code lại những capability sản phẩm đã có và giúp hiểu rõ UX của agent tốt.

## D3 — Automation ở sau manual reliability

Workflow phải chạy thủ công ổn định và có eval trước khi schedule/trigger tự động.

## D4 — Official-source-first

ChatGPT thay đổi nhanh. Docs, Help Center, Academy và developer docs của OpenAI là nguồn chính; community content là bổ sung.

## D5 — PASS dựa trên evidence

Đọc xong không tương đương hiểu. Mỗi module có output và tiêu chí PASS.

## D6 — Capstone gắn với công việc thật

Capstone nên dùng một project có giá trị thực để kiểm tra khả năng chuyển giao kiến thức.
