# BOOT.2 — Conversation Basics / Thao tác hội thoại cơ bản

> **Stage:** 0 — Getting started  
> **Module:** BOOT  
> **Source snapshot:** 2026-09-10  
> **Prerequisite:** BOOT.1  
> **Estimated time:** 25–35 minutes  
> **Environment tested:** ChatGPT web hoặc mobile  
> **Account or plan assumption:** tài khoản có thể mở ChatGPT; không cần tính năng trả phí  
> **Feature status:** available  
> **Status:** READY  
> **Learner status:** NOT STARTED / IN PROGRESS / PASS / REVIEW

## 0. Access and setup — Điều kiện truy cập
Dùng cùng một chat với BOOT.1 và một chat mới. Chuẩn bị một đoạn ghi chú giả lập từ [boot-sample-brief](../../labs/data/boot-sample-brief.md). Không dùng chat có dữ liệu công việc thật.

## 1. Learning objectives — Mục tiêu học tập

### English
- use follow-up requests to refine content and format
- explain what context is in the current conversation
- choose a new chat when the goal or source context changes

### Tiếng Việt
- dùng yêu cầu tiếp nối để sửa nội dung và định dạng
- giải thích context trong cuộc chat hiện tại
- mở chat mới khi mục tiêu hoặc nguồn context thay đổi

## 2. Key vocabulary — Từ vựng trọng tâm

| Term | Pronunciation | Nghĩa tiếng Việt | Plain English | In ChatGPT / AI |
|---|---|---|---|---|
| `context` | /ˈkɒntekst/ | ngữ cảnh | Information available for the current task. | Thông tin ChatGPT có thể dùng từ các lượt trước và input hiện tại. |
| `refine` | /rɪˈfaɪn/ | tinh chỉnh | Improve something by making targeted changes. | Sửa một phần cụ thể thay vì yêu cầu lại toàn bộ. |
| `format` | /ˈfɔːmæt/ | định dạng | The structure or presentation of an output. | Bảng, bullet, tiêu đề, số lượng và thứ tự của đầu ra. |
| `new chat` | /njuː tʃæt/ | chat mới | A separate conversation with separate immediate context. | Cuộc chat tách context hiện tại khỏi nhiệm vụ khác. |

### Vocabulary notes — Giải thích thuật ngữ

#### `context`

**Plain English:** Information available while ChatGPT answers.  
**Tiếng Việt:** Context giúp giữ liên tục, nhưng không phải database chính xác hay trí nhớ vô hạn.  
**Common confusion:** Chat mới không mang toàn bộ context chat cũ sang.

#### `refine`

**Plain English:** Improve one part with a precise follow-up.  
**Tiếng Việt:** Tinh chỉnh giúp giảm việc phải viết lại từ đầu.


## 3. Core concept — Khái niệm cốt lõi

### English
A conversation has working context. Follow-ups can refine the previous result, while a new chat gives you a clean context for a different task. State the part you want changed.

### Tiếng Việt
Một cuộc chat có context làm việc. Follow-up giúp tinh chỉnh response trước; chat mới tạo context sạch cho nhiệm vụ khác. Hãy nói rõ phần cần thay đổi.

## 4. Why it matters — Vì sao quan trọng

### English
Knowing when to continue and when to start over prevents accidental mixing of instructions and sources.

### Tiếng Việt
Biết khi nào tiếp tục và khi nào mở chat mới giúp tránh trộn nhầm hướng dẫn hoặc nguồn.

## 5. Mental model — Mô hình tư duy
Same goal → continue and refine; New goal/source → new chat

## 6. Examples — Ví dụ
### Example — Refine in the same chat

**English prompt**

```text
Turn the three ideas above into a two-column table: Action and First step. Do not add new ideas.
```

**Giải thích tiếng Việt:** Vẫn giữ context nhưng đặt output format và boundary rõ.

### Example — Start a new chat

```text
New task: create a packing checklist for a two-day trip. Ask me only for details that change the checklist.
```

**Giải thích tiếng Việt:** Mục tiêu mới nên tách khỏi context cũ.

## 7. English patterns for AI work — Mẫu câu tiếng Anh dùng với AI

| English pattern | Nghĩa / cách dùng |
|---|---|
| `Use the previous answer, but change only ...` | Giữ phần còn lại và sửa một phần. |
| `Do not add new information.` | Không tự bổ sung dữ liệu ngoài input. |
| `Start a new chat for this task.` | Tách context cho nhiệm vụ mới. |
| `Ask only if a missing detail changes the answer.` | Chỉ hỏi khi thiếu thông tin quan trọng. |

## 8. Practice — Thực hành

### A. Comprehension check — Kiểm tra hiểu bài

1. Nêu hai thông tin mà follow-up có thể lấy từ context trước.
2. Cho hai ví dụ: một trường hợp tiếp tục chat, một trường hợp mở chat mới.

### B. ChatGPT exercise — Bài tập ChatGPT

1. Trong chat hiện tại, dùng `boot-sample-brief` và yêu cầu tóm tắt 3 bullet.
2. Follow-up yêu cầu đổi thành bảng hai cột, không thêm thông tin.
3. Mở chat mới, hỏi một nhiệm vụ khác và so sánh xem thông tin cũ còn được dùng không.

### C. English exercise — Bài luyện tiếng Anh

Viết hai instruction: một instruction tinh chỉnh format và một instruction yêu cầu không thêm dữ liệu. Đọc lại xem động từ và boundary đã rõ chưa.

### D. Real-world transfer — Áp dụng thực tế

Chọn một nhiệm vụ bạn thường lặp lại. Tạo một chat cho nhiệm vụ đó, ghi instruction ổn định, rồi mở chat mới cho một mục tiêu không liên quan.

## 9. Verification — Kiểm chứng
- Output sau follow-up chỉ thay đổi phần được yêu cầu chưa?
- Có thông tin mới nào không có trong input không?
- Chat mới có còn dựa vào context cũ không?
- Bạn có thể chỉ ra câu nào trong output được grounding bởi sample brief không?

## 10. Failure modes — Lỗi thường gặp
- Mỗi follow-up lại đổi mục tiêu khiến context khó kiểm soát.
- Yêu cầu đổi format nhưng không nói giữ nguyên nội dung.
- Nghĩ rằng chat mới chắc chắn xóa mọi dữ liệu ở cấp tài khoản.
- Dùng memory hoặc history như source of truth mà không kiểm tra.

## 11. Language checkpoint — Kiểm tra tiếng Anh
- [ ] I recognize context, refine, format and new chat.
- [ ] Tôi giải thích được khi nào dùng continue và khi nào start over.
- [ ] I can write a boundary instruction in English.

## 12. PASS criteria — Tiêu chí PASS

### ChatGPT track
- [ ] Explain: mô tả context của chat hiện tại.
- [ ] Execute: tinh chỉnh response ít nhất hai lần.
- [ ] Diagnose: phát hiện một thay đổi ngoài yêu cầu.
- [ ] Verify: so sánh chat tiếp tục với chat mới.
- [ ] Transfer: áp dụng quy tắc vào một nhiệm vụ khác.

### English track
- [ ] Recognize ít nhất 4/4 thuật ngữ.
- [ ] Understand sự khác nhau giữa refine và rewrite.
- [ ] Use một instruction có boundary rõ.

## 13. Evidence to save — Evidence cần lưu
Lưu prompt tóm tắt, hai follow-up, kết quả trước/sau và so sánh chat mới theo [evidence template](../../evidence/TEMPLATE.md).

## 14. Official sources — Nguồn chính thức
- [Getting started with ChatGPT — OpenAI Academy](https://openai.com/academy/getting-started/)
- [Prompting — ChatGPT Learn](https://learn.chatgpt.com/docs/prompting)

## 15. Reflection — Tự tổng kết
**What I learned / Tôi đã học được:** ...  
**What confused me / Điều còn chưa rõ:** ...  
**What I will use / Điều tôi sẽ áp dụng:** ...