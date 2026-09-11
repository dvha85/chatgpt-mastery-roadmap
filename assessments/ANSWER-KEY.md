# Answer Key & Remediation Map — Đáp án và đường ôn tập

> **Rule / Quy tắc:** chỉ mở file này sau khi đã tự làm checkpoint. Đáp án mẫu không phải chuỗi câu bắt buộc phải giống; hãy chấm theo reasoning, boundaries và verification. **Ví dụ vận hành dùng tiếng Việt; English track được chấm riêng.**

## 1. BOOT Check — Hướng đáp án

| # | Cần chứng minh | Review lesson |
|---:|---|---|
| 1 | prompt tiếng Việt nêu task rõ; output phù hợp người mới | BOOT.1 |
| 2 | follow-up yêu cầu đúng bảng/2 cột và kiểm format | BOOT.2 |
| 3 | new chat khi task không liên quan hoặc giải thích được vì sao tiếp tục | BOOT.2 |
| 4 | con số không có nguồn phải là unsupported/uncertain | BOOT.3 |
| 5 | redact tên/email trước khi dùng/lưu nếu không cần | BOOT.3 |
| 6 | instruction nêu phần được sửa và phần phải giữ nguyên | BOOT.2 |
| 7 | lưu prompt + response + task/evidence reference | BOOT.4 |
| 8 | nêu verification step độc lập phù hợp claim | BOOT.3 |
| 9 | chọn nơi lưu phù hợp privacy | BOOT.4 |
| 10 | áp dụng cùng loop vào input/task mới | BOOT.1–BOOT.4 |

### BOOT common failures — Lỗi thường gặp
- Dùng `ChatGPT nói vậy` như evidence → ôn BOOT.3.
- Không lưu prompt tạo output → ôn BOOT.4.
- Sửa text nhưng làm đổi số/fact gốc → ôn BOOT.2 + BOOT.3.
- Đưa dữ liệu riêng tư vào repo → ôn BOOT.3 + BOOT.4.

## 2. M00 Check — Hướng đáp án

- **Chat** cho hỏi/viết/phân tích ngắn.
- **Work** cho task nhiều bước/nhiều nguồn/deliverable dài khi phù hợp và có sẵn.
- **Codex** cho repository, code changes, commands và tests.
- **Tool ≠ surface**.
- **Model ≠ product**: output còn phụ thuộc context, tools và verification.
- Claim không có evidence phải đánh dấu uncertain/unsupported.
- Task brief cần Outcome → Context → Tools → Verification, thêm boundary/acceptance criteria khi cần.
- External action cần boundary/human review theo rủi ro.

### M00 remediation map
| Failure | Review |
|---|---|
| nhầm Chat/Work/Codex | M00.1 |
| nhầm model/context/tool | M00.2 |
| tin confidence là proof | M00.2 + M00.3 |
| task brief mơ hồ | M00.3 |
| verification chỉ là “kiểm lại” | M00.3 |
| không đặt boundary cho external action | M00.3 |

## 3. M01 Check — Hướng đáp án

Một task spec đạt thường có:
1. **Goal** rõ.
2. **Context** liên quan.
3. **Output** kiểm được.
4. **Boundaries** phù hợp.
5. **Verification** độc lập.

### M01 remediation map
| Failure | Review lesson / lab |
|---|---|
| task vẫn mơ hồ | M01.1 |
| prompt sửa lan man | M01.2 |
| task phức tạp không chia bước | M01.2 + P-002 |
| output thiếu field/khó chấm | M01.3 + P-001/P-003 |
| Unknown bị biến thành fact | M01.3 + M01.4 + P-003 |
| tính tổng sai | M01.4 + P-002 |
| summary thêm fact ngoài nguồn | M01.4 + P-001 |
| recommendation không map criteria | M01.3 + P-003 |

## 4. PASS vs FAIL examples — Ví dụ cách chấm

### Example A — FAIL

```text
Prompt: Hãy so sánh các lựa chọn và chọn lựa chọn tốt nhất.
Output: Cedar tốt nhất vì giá khoảng $10 và hỗ trợ contact form.
```

Nếu dataset ghi Cedar cost/contact form là `Unknown`, bài này FAIL vì `best` mơ hồ, output bịa missing facts và không có verification.

### Example B — PASS

```text
Chỉ dùng bảng đã cung cấp. Với từng tiêu chí bắt buộc, đánh dấu PASS/FAIL/UNKNOWN. Không suy luận giá trị Unknown. Chỉ khuyến nghị một lựa chọn sau khi map khuyến nghị về các tiêu chí đã nêu. Trả lời bằng tiếng Việt.
```

Nếu output giữ Unknown nguyên trạng và recommendation bám đúng criteria, task spec có thể PASS dù wording khác mẫu.

## 5. How to retest — Cách thi lại

1. xác định criterion bị thiếu;
2. học lại lesson/example tương ứng;
3. chọn case tương đương khác;
4. chạy task bằng prompt tiếng Việt;
5. verify;
6. lưu score/evidence mới.

`PASS` phải phản ánh năng lực chuyển giao, không phải khả năng chép reference answer.

## 6. Scoring principle — Nguyên tắc chấm

Tự hỏi:

```text
Câu trả lời có giữ đúng ý định của task không?
Có tôn trọng facts và boundaries đã biết không?
Kết quả có thể kiểm chứng được không?
Người học có biết phần nào vẫn chưa chắc chắn không?
```

Nếu bốn câu được đáp ứng bằng evidence phù hợp, khác câu chữ mẫu không phải lỗi.

## English track
English track chỉ kiểm nhận diện/hiểu/dùng thuật ngữ. Không yêu cầu chuyển các prompt vận hành ở trên sang tiếng Anh để PASS ChatGPT track.
