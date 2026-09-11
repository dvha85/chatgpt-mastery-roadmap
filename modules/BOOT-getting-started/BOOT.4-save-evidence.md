# BOOT.4 — Save Evidence / Lưu bằng chứng học tập

> **Stage:** 0 — Getting started  
> **Module:** BOOT  
> **Source snapshot:** 2026-09-10  
> **Prerequisite:** BOOT.3  
> **Previous lesson:** [BOOT.3 — Safe Use & Verification](BOOT.3-safe-use-and-verification.md)  
> **Next lesson:** [M00.1 — Chat vs ChatGPT Work vs Codex](../M00-mental-model/M00.1-chat-work-codex.md)  
> **Estimated time:** 25–35 minutes  
> **Environment tested:** ChatGPT + trình duyệt GitHub hoặc ghi chú riêng  
> **Account or plan assumption:** không cần Git, CLI hay API key  
> **Feature status:** available  
> **Status:** READY  
> **Learner status:** NOT STARTED / IN PROGRESS / PASS / REVIEW

> **Ngôn ngữ vận hành:** evidence, prompt mẫu và hướng dẫn thực hành dùng tiếng Việt; English track được tách riêng.

## 0. Access and setup — Điều kiện truy cập
Chuẩn bị một prompt và response đã làm sạch từ BOOT.1–BOOT.3. Bạn có thể lưu trong ghi chú riêng hoặc repo riêng. Repo này là public; không dùng fork public để lưu dữ liệu riêng tư. Nếu muốn dùng GitHub cho evidence riêng tư, tạo một private repository độc lập hoặc dùng notes cá nhân.

## 1. Learning objectives — Mục tiêu học tập

### English
- capture a reproducible record of a learning task
- separate learner evidence from the course author’s example
- choose a safe place to store cleaned evidence

### Tiếng Việt
- ghi lại một hồ sơ có thể tái hiện của bài học
- phân biệt evidence của người học với ví dụ của tác giả
- chọn nơi lưu evidence đã làm sạch một cách an toàn

## 2. Key vocabulary — Từ vựng trọng tâm

| Term | Pronunciation | Nghĩa tiếng Việt | Plain English | In ChatGPT / AI |
|---|---|---|---|---|
| `evidence` | /ˈevɪdəns/ | bằng chứng | A record that supports what you did and checked. | Prompt, kết quả, verification và reflection của bạn. |
| `reproducible` | /ˌriːprəˈdjuːsəbl/ | có thể tái hiện | Someone can repeat the steps and understand the result. | Người khác có thể làm lại với input tương đương. |
| `reflection` | /rɪˈflekʃən/ | tự tổng kết | A short note about what worked and what to change. | Ghi điều hiệu quả, điều sai và bước tiếp theo. |
| `status` | /ˈsteɪtəs/ | trạng thái | A label such as IN PROGRESS, REVIEW, or PASS. | Trạng thái tiến độ của người học, tách khỏi trạng thái tài liệu. |

### Vocabulary notes — Giải thích thuật ngữ

#### `reproducible`
**Plain English:** A task can be repeated from recorded steps.  
**Tiếng Việt:** Evidence tốt không cần response giống từng chữ; cần đủ input, prompt và cách kiểm tra.

#### `status`
**Plain English:** A label that describes current progress.  
**Tiếng Việt:** `IN PROGRESS` và `REVIEW` được dùng trước `PASS`; không nhảy trạng thái vì đã đọc.

## 3. Core concept — Khái niệm cốt lõi

### English
Evidence is a compact record of an actual attempt: task, prompt, result, verification, failure mode, score, and reflection. It should be clean enough to share and detailed enough to repeat.

### Tiếng Việt
Evidence là hồ sơ ngắn của một lần làm thật: task, prompt, kết quả, verification, failure mode, điểm và reflection. Hồ sơ phải đủ sạch để chia sẻ và đủ rõ để làm lại.

## 4. Why it matters — Vì sao quan trọng

### English
Saving evidence turns learning into a visible process and prevents confusing a course example with your own ability.

### Tiếng Việt
Lưu evidence biến việc học thành quá trình có thể nhìn lại và tránh nhầm ví dụ của khóa học với năng lực của chính bạn.

## 5. Mental model — Mô hình tư duy
Attempt → Record → Clean → Verify → Score → Reflect

## 6. Examples — Ví dụ

### Example — Minimal evidence / Evidence tối thiểu

```text
Bài học: BOOT.1
Prompt: Hãy giải thích “prompt” là gì bằng ba câu đơn giản và cho một ví dụ. Trả lời bằng tiếng Việt.
Kết quả: [response đã làm sạch]
Kiểm chứng: Response dùng đúng ba câu và có một ví dụ.
Lỗi phát hiện: Response giả định tôi đã biết từ “model”.
Tự tổng kết: Lần sau tôi sẽ yêu cầu giải thích thuật ngữ kỹ thuật bằng tiếng Việt trước khi dùng.
```

**Giải thích:** Hồ sơ ghi những gì đã làm và đã kiểm tra, không chỉ ghi “đã học”.

### Example — Safe GitHub storage / Lưu an toàn trên GitHub

- Public repo: chỉ dùng dữ liệu giả lập hoặc dữ liệu được phép công khai.
- Private repository độc lập: dùng khi evidence chứa nội dung công việc không thể công khai.
- Private notes: lựa chọn mặc định cho dữ liệu nhạy cảm.

**Giải thích:** Repo public và fork của repo public không phải nơi an toàn cho dữ liệu riêng tư.

## 7. Vietnamese operational patterns — Mẫu lệnh tiếng Việt dùng trực tiếp

| Mẫu tiếng Việt | Nghĩa / cách dùng |
|---|---|
| `Ghi lại prompt và kết quả quan sát được.` | Lưu đầu vào/đầu ra. |
| `Nêu rõ cách bạn đã kiểm chứng kết quả.` | Gắn evidence với verification. |
| `Xóa dữ liệu riêng tư trước khi lưu.` | Bảo vệ thông tin nhạy cảm. |
| `Đánh dấu trạng thái là IN PROGRESS / REVIEW / PASS theo bằng chứng hiện có.` | Không tự nâng trạng thái. |

### English patterns for AI work — Mẫu câu tiếng Anh để học

| English pattern | Nghĩa / cách dùng |
|---|---|
| `Record the prompt and the observed result.` | Ghi prompt và kết quả quan sát được. |
| `State how you verified it.` | Nêu cách bạn kiểm chứng. |
| `Remove private data before saving.` | Làm sạch dữ liệu trước khi lưu. |
| `Mark this as IN PROGRESS / REVIEW / PASS.` | Gắn trạng thái đúng với bằng chứng. |

## 8. Practice — Thực hành

### A. Comprehension check — Kiểm tra hiểu bài
1. Liệt kê sáu phần tối thiểu của evidence.
2. Phân biệt `READY` của lesson với `PASS` của learner.

### B. ChatGPT exercise — Bài tập ChatGPT
Dùng một task đã làm ở BOOT.1–BOOT.3, điền [Evidence Template](../../evidence/TEMPLATE.md) bằng tiếng Việt. Xóa dữ liệu riêng tư và thêm một failure mode cụ thể.

### C. English exercise — Bài luyện tiếng Anh
Viết ba câu: `I used...`, `I verified...`, `Next time I will...`. Đối chiếu với evidence tiếng Việt.

### D. Real-world transfer — Áp dụng thực tế
Lưu một evidence tiếng Việt vào notes cá nhân hoặc private repository độc lập. Nếu dùng GitHub web, Preview trước khi commit và kiểm tra secret/link/file.

## 9. Verification — Kiểm chứng
- Người khác có biết task, input, prompt và expected result không?
- Kết quả có gắn với verification cụ thể không?
- Evidence có làm lộ secret hoặc dữ liệu riêng tư không?
- Status có đúng với mức bằng chứng hiện có không?

## 10. Failure modes — Lỗi thường gặp
- Lưu screenshot nhưng không ghi prompt hoặc cách kiểm tra.
- Đưa API key, token, password hoặc dữ liệu khách hàng vào repo.
- Dùng ví dụ của tác giả để đánh dấu PASS cho bản thân.
- Đánh dấu PASS khi mới đọc, chưa Execute và Verify.

## 11. Language checkpoint — Kiểm tra tiếng Anh
- [ ] I recognize evidence, reproducible, reflection and status.
- [ ] Tôi giải thích được sự khác nhau giữa READY và PASS.
- [ ] I can write a short reflection in English trong English track.

## 12. PASS criteria — Tiêu chí PASS

### ChatGPT track
- [ ] Explain: mô tả evidence tối thiểu.
- [ ] Execute: điền một evidence hoàn chỉnh bằng tiếng Việt.
- [ ] Diagnose: nhận ra một lỗ hổng tái hiện hoặc privacy.
- [ ] Verify: kiểm tra evidence trước khi lưu.
- [ ] Transfer: lưu evidence cho một task khác.

### English track
- [ ] Recognize ít nhất 4/4 thuật ngữ.
- [ ] Understand status labels in context.
- [ ] Use ba câu reflection tiếng Anh có nghĩa đúng.

## 13. Evidence to save — Evidence cần lưu
Lưu file evidence đã làm sạch hoặc ghi rõ vị trí private notes. Không cần public link chat. Dùng [evidence README](../../evidence/README.md) và [template](../../evidence/TEMPLATE.md).

## 14. Official sources — Nguồn chính thức
- [Getting started with ChatGPT — OpenAI Academy](https://openai.com/academy/getting-started/)
- [Forks: visibility and permissions — GitHub Docs](https://docs.github.com/en/pull-requests/reference/forks)

## 15. Reflection — Tự tổng kết
**What I learned / Tôi đã học được:** ...  
**What confused me / Điều còn chưa rõ:** ...  
**What I will use / Điều tôi sẽ áp dụng:** ...

## 16. Navigation — Điều hướng
← [BOOT.3 — Safe Use & Verification](BOOT.3-safe-use-and-verification.md) · [BOOT overview](README.md) · [M00.1 — Chat vs ChatGPT Work vs Codex](../M00-mental-model/M00.1-chat-work-codex.md) →
