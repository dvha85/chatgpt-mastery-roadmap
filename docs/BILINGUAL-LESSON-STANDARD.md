# Bilingual Lesson Standard — Tiêu chuẩn bài học song ngữ

> Áp dụng cho mọi lesson trong repository.  
> Quy tắc ngôn ngữ vận hành chi tiết: [Vietnamese-first Usage](VIETNAMESE-FIRST-USAGE.md).

## 1. Goal — Mục tiêu

Mỗi bài học đồng thời xây hai năng lực:

1. **ChatGPT / AI capability** — hiểu và sử dụng đúng tính năng hoặc khái niệm.
2. **Practical English** — trước hết nhận diện và hiểu thuật ngữ tiếng Anh thường gặp trong tài liệu AI.

The English track supports reading official documentation. It does **not** require the learner to operate ChatGPT in English.

English track giúp đọc tài liệu chính thức. Nó **không yêu cầu** người học phải giao việc cho ChatGPT bằng tiếng Anh.

### Current learner mode — Vocabulary-first / Chế độ hiện tại: ưu tiên từ vựng

Ở giai đoạn hiện tại, English track chỉ bắt buộc hai mức:

1. **Recognize** — nhận ra thuật ngữ tiếng Anh chính.
2. **Understand** — giải thích được nghĩa bằng tiếng Việt và hiểu nghĩa trong ngữ cảnh AI/ChatGPT.

Mức **Use** — tự viết prompt/instruction bằng tiếng Anh — được **DEFERRED** cho giai đoạn sau và **không chặn PASS** của lesson hiện tại.

Các English pattern vẫn có thể xuất hiện như tài liệu tham khảo để làm quen mắt, nhưng người học không phải tự viết prompt tiếng Anh trừ khi chủ động muốn luyện thêm.

## 2. Vietnamese-first operating rule — Quy tắc vận hành tiếng Việt trước

Đây là quy tắc bắt buộc cho mọi lesson mới và mọi lesson được cập nhật:

- Prompt để copy/paste vào ChatGPT: **tiếng Việt trước**.
- Task brief / bản giao việc: **tiếng Việt trước**.
- Ví dụ hội thoại và follow-up của người dùng: **tiếng Việt trước**.
- Verification prompt / yêu cầu kiểm chứng: **tiếng Việt trước**.
- ChatGPT exercise: dùng tiếng Việt, trừ khi chính mục tiêu bài là xử lý nội dung tiếng Anh.
- Kết quả mong đợi mặc định: `Trả lời bằng tiếng Việt.`
- Nếu cần bản tiếng Anh, đặt **sau** bản tiếng Việt và ghi `English reference / Tham khảo tiếng Anh` hoặc đặt trong English exercise.
- Không dùng nhãn `English prompt` cho prompt chính của ví dụ.

Tên sản phẩm, code, command, API field, tên file và thuật ngữ kỹ thuật chuẩn như `prompt`, `context`, `tool`, `model`, `token`, `repository`, `commit`, `API` được giữ nguyên khi dịch sẽ làm sai nghĩa hoặc sai thao tác.

## 3. Required lesson structure — Cấu trúc bắt buộc

### A. Lesson title — Tên bài

Giữ thuật ngữ tiếng Anh chính thức khi cần, sau đó có diễn giải tiếng Việt tự nhiên.

Ví dụ: `M00.2 — How ChatGPT Works / ChatGPT tạo câu trả lời như thế nào`.

### B. Learning objectives — Mục tiêu học tập

Viết mục tiêu bằng cả English và Tiếng Việt. Mục tiêu ChatGPT track phải có thể hoàn thành hoàn toàn bằng tiếng Việt.

### C. Key vocabulary — Từ vựng trọng tâm

Với thuật ngữ kỹ thuật quan trọng, ưu tiên các trường:

| Field | Requirement |
|---|---|
| **Term** | tên tiếng Anh chuẩn |
| **Pronunciation** | IPA hoặc gợi ý phát âm khi hữu ích |
| **Vietnamese** | nghĩa/giải thích tự nhiên bằng tiếng Việt |
| **Plain English** | định nghĩa tiếng Anh đơn giản |
| **In ChatGPT / AI** | nghĩa trong ngữ cảnh ChatGPT/AI |
| **Common confusion** | điểm dễ nhầm khi cần |

Không dịch máy móc thuật ngữ kỹ thuật. Giữ tên chuẩn tiếng Anh và giải thích bản chất bằng tiếng Việt.

### D. Core concept — Khái niệm cốt lõi

Có thể dùng cặp giải thích:

- **English:** ngắn, tự nhiên, hỗ trợ đọc hiểu.
- **Tiếng Việt:** bản giải thích chính để người học hiểu sâu; không cần dịch từng chữ.

### E. Why it matters — Vì sao quan trọng

Nêu lợi ích khi hiểu đúng và lỗi/rủi ro khi hiểu sai.

### F. Examples — Ví dụ

Ví dụ phải sát tình huống thực tế và theo thứ tự:

1. nhiệm vụ / tình huống bằng tiếng Việt;
2. **Prompt tiếng Việt — dùng trực tiếp**;
3. kết quả/điểm cần quan sát;
4. cách kiểm chứng;
5. `English reference` chỉ khi hữu ích cho English track.

Ví dụ chuẩn:

```text
Hãy dùng file đính kèm làm nguồn chính. Tách các dữ kiện được hỗ trợ khỏi phần chưa chắc chắn. Không đoán khi thiếu bằng chứng. Trả lời bằng tiếng Việt.
```

English reference tùy chọn:

```text
Use the attached file as the primary source. Separate supported facts from uncertain items. Do not guess when evidence is missing.
```

### G. Vietnamese operational patterns + English patterns

Mỗi bài nên có 3–8 mẫu lệnh tiếng Việt dùng trực tiếp, sau đó mới tới mẫu tiếng Anh để **nhận diện và học từ vựng**.

Ví dụ:

| Mẫu tiếng Việt | English reference |
|---|---|
| `Dùng file đính kèm làm nguồn chính.` | `Use the attached file as the primary source.` |
| `Nêu rõ các giả định của bạn.` | `State your assumptions explicitly.` |
| `Trích dẫn bằng chứng cho từng nhận định.` | `Cite the evidence for each claim.` |

Trong Vocabulary-first mode, người học **không phải tự tạo câu tiếng Anh từ các pattern này**.

### H. Practice — Thực hành

Mỗi bài gồm:

1. comprehension check / kiểm tra hiểu bài;
2. ChatGPT exercise / bài thực hành ChatGPT **bằng tiếng Việt**;
3. English vocabulary exercise / bài luyện **nhận diện + hiểu từ vựng tiếng Anh**;
4. real-world transfer / bài áp dụng thực tế.

Trong Vocabulary-first mode, English exercise ưu tiên: ghép thuật ngữ với nghĩa, giải thích bằng tiếng Việt, phân biệt hai thuật ngữ gần nghĩa, hoặc nhận diện thuật ngữ trong một câu mẫu. Không bắt buộc viết prompt/instruction tiếng Anh.

### I. Verification & failure modes — Kiểm chứng và lỗi thường gặp

Hướng dẫn cách kiểm output và ít nhất một failure mode. Verification prompt dùng trong ChatGPT track phải có bản tiếng Việt dùng trực tiếp.

### J. Language checkpoint — Kiểm tra tiếng Anh

Trước PASS trong Vocabulary-first mode, người học cần:

- nhận diện các thuật ngữ tiếng Anh chính;
- giải thích 3–5 thuật ngữ bằng tiếng Việt;
- hiểu nghĩa của thuật ngữ trong ngữ cảnh AI/ChatGPT;
- phân biệt được các thuật ngữ dễ nhầm khi lesson có yêu cầu.

**Không yêu cầu viết prompt tiếng Anh ở giai đoạn hiện tại.** Khả năng viết prompt tiếng Anh sẽ được mở lại ở một phase riêng sau này.

### K. PASS criteria — Tiêu chí PASS

**ChatGPT track:** Explain → Execute → Diagnose → Verify → Transfer.  
**English track hiện tại:** Recognize → Understand.  
**English Use:** DEFERRED — không chặn PASS.

Nếu lesson cũ còn ghi `Use` hoặc yêu cầu tự viết instruction/prompt tiếng Anh, áp dụng chuẩn này làm quy tắc ưu tiên cho tới khi lesson đó được cập nhật.

## 4. Progressive English exposure — Tăng dần tiếp xúc tiếng Anh

English exposure có thể tăng từ Stage A đến Stage C ở **phần đọc hiểu, từ vựng và tài liệu tham khảo** mà chưa cần tăng yêu cầu viết tiếng Anh.

| Stage | English-learning emphasis | Operating language |
|---|---|---|
| Stage 0 / Stage A | từ vựng + nghĩa trong ngữ cảnh | Vietnamese-first |
| Stage B — Power User | từ vựng + đọc product docs nhiều hơn | Vietnamese-first |
| Stage C — Builder | từ vựng kỹ thuật + đọc developer docs/code/API | Vietnamese-first; giữ nguyên code/technical syntax |

Khi người học chủ động chuyển sang phase luyện viết tiếng Anh, mới kích hoạt lại mức `Use`.

## 5. Vocabulary policy — Quy tắc thuật ngữ

- Giữ canonical terms: `prompt`, `context`, `token`, `agent`, `tool`, `workflow`, `plugin`, `skill`, `grounding`, `retrieval`, v.v.
- Giải thích tiếng Việt ở lần dùng đầu.
- Ưu tiên meaning-in-context hơn dịch từ điển.
- Phân biệt các thuật ngữ gần nghĩa.
- Bổ sung thuật ngữ quan trọng vào [GLOSSARY.md](../GLOSSARY.md).

## 6. What NOT to do — Những điều không làm

- Không tạo hai lesson tách rời EN và VI.
- Không dùng bản dịch từng chữ thiếu tự nhiên.
- Không giấu thuật ngữ chuẩn phía sau bản dịch tiếng Việt-only.
- Không bắt người học dùng prompt tiếng Anh trong ChatGPT track.
- Trong Vocabulary-first mode, không bắt người học tự viết prompt/instruction tiếng Anh để PASS.
- Không đặt English prompt trước rồi buộc người học tự dịch để thực hành.
- Không yêu cầu grammar hoàn hảo để PASS kỹ năng AI.
- Không dạy thuật ngữ/tính năng đã lỗi thời khi nguồn chính thức đã thay đổi.

## 7. Source-first rule — Ưu tiên nguồn chính thức

Khi nội dung liên quan trực tiếp sản phẩm/tính năng OpenAI, kiểm tra nguồn chính thức hiện tại trước khi hoàn thiện lesson và ghi source snapshot.

## 8. Beginner accessibility — Khả năng tiếp cận cho người mới

- Giải thích thao tác trước khi dùng viết tắt/tên tính năng khó.
- Mỗi bài nên giới hạn khoảng 3–7 thuật ngữ mới.
- Mỗi ví dụ phải có input/tình huống, prompt tiếng Việt, kết quả cần quan sát và cách kiểm.
- Không viết “hãy thực hành” nếu chưa có dữ liệu, prompt mẫu hoặc tiêu chí quan sát.
- Tính năng không có trên mọi tài khoản phải có fallback và nhãn phù hợp.
- Người mới phải hoàn thành được ChatGPT track mà **không cần tự dịch từ tiếng Anh sang tiếng Việt**.

## 9. QA gate — Gate kiểm tra Vietnamese-first

Một lesson chưa đạt READY nếu còn một trong các lỗi sau:

- prompt copy/paste chính chỉ có tiếng Anh;
- task brief chính chỉ có tiếng Anh;
- bài ChatGPT exercise bắt người học dùng prompt tiếng Anh;
- trong Vocabulary-first mode, English exercise bắt buộc tự viết prompt/instruction tiếng Anh để PASS;
- đáp án mẫu chỉ đưa prompt tiếng Anh;
- verification instruction chính chỉ có tiếng Anh;
- thuật ngữ tiếng Anh được dùng nhưng không có giải thích tiếng Việt phù hợp.
