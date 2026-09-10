# Capstone — ChatGPT Agentic Workflow

## Mục tiêu

Thiết kế một workflow thực tế kết hợp những gì đã học, ưu tiên bài toán có giá trị thật thay vì demo.

Gợi ý mặc định: một workflow hỗ trợ **nghiên cứu, ra quyết định hoặc vận hành bot/affiliate project**.

## Bắt buộc có

1. Outcome và Definition of Done.
2. Source map: web/files/connected systems.
3. Tool selection: Chat / Work / Codex / plugins / browser / computer use.
4. Context architecture.
5. Ít nhất một reusable skill hoặc workflow spec.
6. Automation chỉ sau khi manual workflow PASS.
7. Human review tại hành động có rủi ro/cost cao hoặc khó hoàn tác.
8. Logging/evidence.
9. Tối thiểu 10 eval cases.
10. Retrospective và backlog cải tiến.

## Design review

Trước khi build, trả lời:

- Vì sao cần agent/tool use?
- Phần nào nên deterministic?
- State nằm ở đâu?
- Source of truth là gì?
- Tool nào có quyền ghi?
- Hành động nào cần approval?
- Nếu source thiếu/sai/stale thì sao?
- Nếu tool fail thì fallback gì?
- Làm sao biết workflow đang tốt lên?

## PASS

Capstone PASS khi:

- chạy được end-to-end;
- có evidence cho các bước quan trọng;
- không phụ thuộc vào “model tự đoán” ở nơi cần source of truth;
- có verification trước output/action quan trọng;
- đạt rubric đã định nghĩa trên tập eval;
- có tài liệu để người khác hiểu và chạy lại workflow.
