# Answer Key & Remediation Map — Đáp án và đường ôn tập

> **Rule / Quy tắc:** chỉ mở file này sau khi đã tự làm checkpoint. Đáp án mẫu không phải chuỗi câu bắt buộc phải giống; hãy chấm theo reasoning, boundaries và verification.

## 1. BOOT Check — Hướng đáp án

| # | What a passing answer should show / Cần chứng minh | Review lesson |
|---:|---|---|
| 1 | prompt nêu task rõ; output phù hợp người mới | BOOT.1 |
| 2 | follow-up yêu cầu đúng table/2 columns và kiểm format | BOOT.2 |
| 3 | new chat khi task không liên quan hoặc giải thích được vì sao tiếp tục | BOOT.2 |
| 4 | con số không có nguồn phải là unsupported/uncertain, không biến thành fact | BOOT.3 |
| 5 | redact tên/email trước khi dùng/lưu nếu không cần cho task | BOOT.3 |
| 6 | instruction nêu phần được sửa và phần phải giữ nguyên | BOOT.2 |
| 7 | lưu prompt + response + task/evidence reference | BOOT.4 |
| 8 | nêu verification step độc lập phù hợp claim | BOOT.3 |
| 9 | chọn nơi lưu phù hợp privacy; không public dữ liệu nhạy cảm | BOOT.4 |
| 10 | áp dụng cùng loop vào input/task mới, không chép ví dụ | BOOT.1–BOOT.4 |

### BOOT common failures — Lỗi thường gặp

- `ChatGPT said so` được dùng như evidence → ôn BOOT.3.
- Không lưu prompt tạo ra output → ôn BOOT.4.
- Sửa text nhưng làm đổi số liệu/fact gốc → ôn BOOT.2 + BOOT.3.
- Đưa dữ liệu riêng tư vào repo để chứng minh bài → ôn BOOT.3 + BOOT.4.

---

## 2. M00 Check — Hướng đáp án

Đáp án giải thích chi tiết đã được đặt **sau phần tự làm** trong [M00-CHECK.md](M00-CHECK.md). Khi chấm, ưu tiên các nguyên tắc sau:

- **Chat** cho hỏi/viết/phân tích ngắn và tương tác qua lại.
- **Work** cho task nhiều bước/nhiều nguồn/deliverable dài khi surface này phù hợp và có sẵn.
- **Codex** cho repository, code changes, commands và tests.
- **Tool ≠ surface**: search, data analysis, code execution, v.v. là capability phục vụ task.
- **Model ≠ product**: output còn phụ thuộc context, tools và verification.
- Claim không có evidence phải được đánh dấu uncertain/unsupported.
- Task brief cần có Outcome → Context → Tools → Verification, thêm boundaries/acceptance criteria khi cần.
- Hành động gửi/publish/mua/xóa/sửa bên ngoài cần boundary/human review theo rủi ro.

### M00 remediation map — Map ôn tập

| Failure | Review |
|---|---|
| nhầm Chat/Work/Codex | M00.1 |
| nhầm model/context/tool | M00.2 |
| tin confidence là proof | M00.2 + M00.3 |
| task brief mơ hồ | M00.3 |
| verification chỉ là “check again” | M00.3 |
| không đặt boundary cho external action | M00.3 |

---

## 3. M01 Check — Hướng đáp án

Đáp án mẫu Level 0/1/2 đã được đặt sau bài tự làm trong [M01-CHECK.md](M01-CHECK.md). Một task spec đạt thường có:

1. **Goal** rõ — kết quả cần tạo.
2. **Context** liên quan — audience, input, facts, constraints.
3. **Output** kiểm được — dạng, fields, length hoặc structure nếu cần.
4. **Boundaries** phù hợp — điều không được bịa/thay đổi/thực hiện.
5. **Verification** độc lập — source, calculation, test, ground truth hoặc human review.

### M01 remediation map — Map ôn tập

| Failure | Review lesson / lab |
|---|---|
| task vẫn mơ hồ | M01.1 |
| prompt sửa lan man, không biết thay gì | M01.2 |
| task phức tạp nhưng không chia bước | M01.2 + P-002 |
| output thiếu field/khó chấm | M01.3 + P-001/P-003 |
| Unknown bị biến thành fact | M01.3 + M01.4 + P-003 |
| tính tổng sai nhưng narrative nghe hợp lý | M01.4 + P-002 |
| summary thêm fact ngoài nguồn | M01.4 + P-001 |
| recommendation không map về criteria | M01.3 + P-003 |

---

## 4. PASS vs FAIL examples — Ví dụ cách chấm

### Example A — FAIL

```text
Prompt: Compare the options and choose the best one.
Output: Cedar is best because it costs around $10 and supports a contact form.
```

Nếu dataset ghi Cedar cost/contact form là `Unknown`, bài này **FAIL** vì:

- criteria `best` mơ hồ;
- output bịa hai missing facts;
- không có verification.

Review: M01.1, M01.3, M01.4, [P-003](../labs/examples/P-003-comparison.md).

### Example B — PASS

```text
Use only the supplied table. Mark every required criterion PASS/FAIL/UNKNOWN. Do not infer Unknown values. Recommend one option only after mapping the recommendation to the stated criteria.
```

Nếu output giữ Unknown nguyên trạng và recommendation bám đúng criteria, đây là task spec có thể đạt dù wording khác mẫu.

---

## 5. How to retest — Cách thi lại

Không dùng chính case vừa xem đáp án làm evidence mới. Hãy:

1. xác định criterion bị thiếu;
2. học lại lesson/example tương ứng;
3. tạo hoặc chọn một case tương đương khác;
4. chạy task;
5. verify;
6. lưu score/evidence mới.

`PASS` phải phản ánh năng lực chuyển giao, không phải khả năng chép reference answer.

## 6. Scoring principle — Nguyên tắc chấm

Nếu có nhiều đáp án hợp lệ, chấm theo:

```text
Does the answer preserve the task's intent?
Does it respect known facts and boundaries?
Can the result be checked?
Does the learner know what remains uncertain?
```

Nếu bốn câu này được đáp ứng bằng evidence phù hợp, khác câu chữ mẫu không phải lỗi.
