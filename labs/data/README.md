# Lab Data — Dữ liệu thực hành

> Tất cả dữ liệu trong thư mục này phải là dữ liệu giả lập hoặc dữ liệu người học có quyền chia sẻ.

## Files

- [boot-sample-brief.md](boot-sample-brief.md) — dữ liệu nhỏ cho BOOT.2–BOOT.3.
- [sample-brief.md](sample-brief.md) — bộ dữ liệu chuẩn cho P-001, P-002 và P-003.

## Why fixed data matters — Vì sao cần dữ liệu cố định

Các Prompt Lab dùng cùng input và ground truth để người học có thể:

1. chạy lại cùng task;
2. so sánh prompt trước/sau;
3. biết lỗi nằm ở prompt, output hay verification;
4. chấm bằng rubric thay vì cảm giác.

## Rules / Quy tắc

- Không thay dữ kiện thiếu bằng suy đoán.
- Dùng `UNKNOWN`, `UNSUPPORTED` hoặc `ASSUMPTION` khi chưa có evidence.
- Không đưa secret, token, password, payment data hoặc thông tin khách hàng thật vào evidence công khai.
- Nếu thay dataset bằng dữ liệu thật, ghi nguồn/quyền sử dụng và tạo ground truth/checklist riêng.

## Lab mapping

| Lab | Dataset | Skill |
|---|---|---|
| P-001 | Dataset A | summary + instruction following + grounding |
| P-002 | Dataset B | planning + constraints + arithmetic verification |
| P-003 | Dataset C | comparison + unknown handling + recommendation |
