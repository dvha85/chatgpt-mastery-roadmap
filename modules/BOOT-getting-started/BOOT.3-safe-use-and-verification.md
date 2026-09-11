# BOOT.3 — Safe Use & Verification / Dùng an toàn và kiểm chứng

> **Stage:** 0 — Getting started  
> **Module:** BOOT  
> **Source snapshot:** 2026-09-10  
> **Prerequisite:** BOOT.2  
> **Estimated time:** 30–40 minutes  
> **Environment tested:** ChatGPT web hoặc mobile; trình duyệt để mở nguồn  
> **Account or plan assumption:** không cần tool trả phí; dùng dữ liệu giả lập  
> **Feature status:** available  
> **Status:** READY  
> **Learner status:** NOT STARTED / IN PROGRESS / PASS / REVIEW

> **Ngôn ngữ vận hành:** thực hành ChatGPT bằng tiếng Việt; tiếng Anh chỉ dùng cho từ vựng và English track.

## 0. Access and setup — Điều kiện truy cập
Đọc [boot-sample-brief](../../labs/data/boot-sample-brief.md). Bài này dùng claim giả lập để luyện kiểm tra, không dùng quyết định y tế, pháp lý, tài chính hoặc dữ liệu cá nhân thật. Nếu ChatGPT không có web search, mở nguồn được cung cấp bằng trình duyệt và ghi rõ cách làm.

## 1. Learning objectives — Mục tiêu học tập

### English
- identify a claim that needs verification
- separate source evidence from an AI guess
- remove sensitive data before sending an input

### Tiếng Việt
- nhận diện một claim cần kiểm chứng
- phân biệt bằng chứng nguồn với suy đoán của AI
- loại bỏ dữ liệu nhạy cảm trước khi gửi input

## 2. Key vocabulary — Từ vựng trọng tâm

| Term | Pronunciation | Nghĩa tiếng Việt | Plain English | In ChatGPT / AI |
|---|---|---|---|---|
| `claim` | /kleɪm/ | nhận định có thể kiểm tra | A statement that can be supported or contradicted. | Một mệnh đề cần bằng chứng, không chỉ cảm giác. |
| `evidence` | /ˈevɪdəns/ | bằng chứng | Information that supports or challenges a claim. | Nguồn, trích đoạn, phép tính hoặc test dùng để kiểm tra. |
| `uncertainty` | /ʌnˈsɜːtənti/ | độ không chắc chắn | What is not known or not sufficiently supported. | Phần còn thiếu nguồn, dữ liệu hoặc confidence phù hợp. |
| `redact` | /rɪˈdækt/ | che/xóa thông tin nhạy cảm | Remove sensitive details before sharing. | Thay tên, email, số tiền hoặc ID thật bằng placeholder. |

### Vocabulary notes — Giải thích thuật ngữ

#### `claim`
**Plain English:** A statement that could be true or false.  
**Tiếng Việt:** Claim quan trọng cần evidence tương ứng.  
**Common confusion:** Chi tiết do AI viết không phải evidence.

#### `redact`
**Plain English:** Remove or replace sensitive information.  
**Tiếng Việt:** Làm sạch dữ liệu trước khi gửi hoặc lưu.

## 3. Core concept — Khái niệm cốt lõi

### English
ChatGPT can produce a confident-looking answer that still needs checking. Verification connects each important claim to evidence, a calculation, a test, or a reliable source. Privacy starts before you send the prompt.

### Tiếng Việt
ChatGPT có thể trả lời rất tự tin nhưng vẫn cần kiểm tra. Verification nối từng claim quan trọng với evidence, phép tính, test hoặc nguồn đáng tin. Bảo vệ riêng tư bắt đầu trước khi gửi prompt.

## 4. Why it matters — Vì sao quan trọng

### English
Verification reduces avoidable mistakes and helps you know when an answer is still uncertain.

### Tiếng Việt
Kiểm chứng giảm lỗi có thể tránh được và giúp bạn biết phần nào của câu trả lời vẫn chưa chắc chắn.

## 5. Mental model — Mô hình tư duy
Claim → Evidence → Check → Conclusion + Uncertainty

## 6. Examples — Ví dụ

### Example — Ask for grounded output / Yêu cầu đầu ra bám nguồn

**Prompt tiếng Việt — dùng trực tiếp**

```text
Chỉ dùng brief đính kèm. Hãy liệt kê ba claim, trích câu trong brief hỗ trợ cho từng claim và đánh dấu những mục không có bằng chứng là CHƯA CHẮC CHẮN. Không tự tạo thêm dữ kiện. Trả lời bằng tiếng Việt.
```

**English reference — Tham khảo tiếng Anh**

```text
Use only the attached brief. List three claims, quote the supporting sentence for each claim, and mark unsupported items as UNCERTAIN. Do not invent facts.
```

**Giải thích:** Prompt yêu cầu nguồn, giới hạn và nhãn uncertainty.

### Example — Redact before sending / Làm sạch trước khi gửi

Input trước khi làm sạch: `Khách hàng Nguyễn Văn A, email a@example.com, ngân sách 18.000.000đ`.

Input an toàn: `Khách hàng [CLIENT], email [REDACTED], ngân sách [BUDGET]`.

**Giải thích:** Giữ cấu trúc cần cho bài nhưng loại thông tin nhận diện.

## 7. Vietnamese operational patterns — Mẫu lệnh tiếng Việt dùng trực tiếp

| Mẫu tiếng Việt | Nghĩa / cách dùng |
|---|---|
| `Chỉ dùng nguồn đính kèm.` | Giới hạn nguồn. |
| `Trích dẫn bằng chứng cho từng claim.` | Gắn evidence cho claim. |
| `Đánh dấu phần không có bằng chứng là chưa chắc chắn.` | Không lấp phần thiếu bằng suy đoán. |
| `Xóa hoặc thay dữ liệu nhạy cảm trước khi xử lý.` | Bảo vệ riêng tư. |

### English patterns for AI work — Mẫu câu tiếng Anh để học

| English pattern | Nghĩa / cách dùng |
|---|---|
| `Use only the attached source.` | Chỉ dùng nguồn được cung cấp. |
| `Cite the evidence for each claim.` | Gắn bằng chứng cho từng nhận định. |
| `Mark unsupported items as uncertain.` | Đánh dấu phần chưa có hỗ trợ. |
| `Remove or replace sensitive details.` | Xóa hoặc thay dữ liệu nhạy cảm. |

## 8. Practice — Thực hành

### A. Comprehension check — Kiểm tra hiểu bài
1. Chọn ba câu trong một response và đánh dấu câu nào là claim.
2. Nói evidence nào đủ mạnh hơn: “AI nói vậy” hay một câu trong brief? Vì sao?

### B. ChatGPT exercise — Bài tập ChatGPT
Dùng sample brief với prompt tiếng Việt ở mục 6. Tạo bảng `Claim → Evidence → Trạng thái`. Sau đó tự kiểm tra một claim bằng cách đối chiếu đúng câu trong brief.

### C. English exercise — Bài luyện tiếng Anh
Viết một instruction có `uncertain` và `evidence`. Đọc thành tiếng, rồi giải thích bằng tiếng Việt.

### D. Real-world transfer — Áp dụng thực tế
Lấy một đoạn text không nhạy cảm bạn có quyền sử dụng. Redact tên/email/số nhận diện, yêu cầu ChatGPT tóm tắt **bằng tiếng Việt**, rồi kiểm tra hai claim quan trọng.

## 9. Verification — Kiểm chứng
- Mỗi claim có câu nguồn, phép tính, test hoặc URL cụ thể chưa?
- Claim nào không được support phải mang nhãn `CHƯA CHẮC CHẮN` hoặc `UNSUPPORTED`.
- Có dữ liệu riêng tư nào còn sót trong prompt, screenshot hoặc evidence không?
- Nếu nguồn thiếu hoặc cũ, bạn đã ghi uncertainty chưa?

## 10. Failure modes — Lỗi thường gặp
- Dùng câu trả lời của AI làm nguồn duy nhất.
- Không phân biệt claim, evidence và conclusion.
- Gửi dữ liệu nhận diện vì nghĩ bài tập nhỏ thì không sao.
- Trích nguồn nhưng trích sai phạm vi hoặc nguồn không hỗ trợ claim.

## 11. Language checkpoint — Kiểm tra tiếng Anh
- [ ] I recognize claim, evidence, uncertainty and redact.
- [ ] Tôi giải thích được vì sao AI output không tự là evidence.
- [ ] I can ask ChatGPT to cite evidence and mark uncertainty trong English track.

## 12. PASS criteria — Tiêu chí PASS

### ChatGPT track
- [ ] Explain: mô tả chuỗi Claim → Evidence → Check.
- [ ] Execute: tạo bảng claim/evidence từ sample brief bằng prompt tiếng Việt.
- [ ] Diagnose: phát hiện ít nhất một claim unsupported.
- [ ] Verify: đối chiếu claim với câu nguồn hoặc phép kiểm tra.
- [ ] Transfer: làm sạch và kiểm tra một input khác.

### English track
- [ ] Recognize ít nhất 4/4 thuật ngữ.
- [ ] Understand `unsupported` và `uncertain` trong ngữ cảnh.
- [ ] Use một prompt tiếng Anh yêu cầu evidence rõ.

## 13. Evidence to save — Evidence cần lưu
Lưu input đã redact, prompt tiếng Việt, bảng claim/evidence/status, một lỗi phát hiện được và reflection theo [evidence template](../../evidence/TEMPLATE.md).

## 14. Official sources — Nguồn chính thức
- [Getting started with ChatGPT — OpenAI Academy](https://openai.com/academy/getting-started/)
- [Prompting — ChatGPT Learn](https://learn.chatgpt.com/docs/prompting)

## 15. Reflection — Tự tổng kết
**What I learned / Tôi đã học được:** ...  
**What confused me / Điều còn chưa rõ:** ...  
**What I will use / Điều tôi sẽ áp dụng:** ...
