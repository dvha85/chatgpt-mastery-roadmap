# Vietnamese-first Usage — Quy ước dùng ChatGPT bằng tiếng Việt

> Áp dụng cho prompt, task brief, ví dụ hội thoại, bài thực hành và đáp án trong roadmap này.

## Nguyên tắc chính

Repo vẫn **song ngữ English–Tiếng Việt** để học thuật ngữ và đọc tài liệu AI, nhưng **ngôn ngữ vận hành mặc định là tiếng Việt**.

- Prompt để copy/paste vào ChatGPT: **tiếng Việt trước**.
- Task brief / bản giao việc: **tiếng Việt trước**.
- Ví dụ câu hỏi của người dùng và yêu cầu kiểm chứng: **tiếng Việt trước**.
- Kết quả mong đợi từ ChatGPT: mặc định **trả lời bằng tiếng Việt**.
- Bản tiếng Anh nếu hữu ích được đặt ở phần **English reference / Tham khảo tiếng Anh**; không bắt buộc phải dùng tiếng Anh để hoàn thành ChatGPT track.
- Tên sản phẩm và thuật ngữ kỹ thuật chuẩn như `prompt`, `context`, `tool`, `model`, `token`, `API`, `repository`, `commit` vẫn giữ tiếng Anh và phải được giải thích bằng tiếng Việt khi xuất hiện lần đầu.
- Không dịch tên file, lệnh terminal, code identifier, API field hoặc cú pháp kỹ thuật nếu việc dịch làm sai thao tác.

## Current English mode — Vocabulary-first

Hiện tại người học chỉ tập trung vào **từ vựng tiếng Anh trong ngữ cảnh AI/ChatGPT**.

English track bắt buộc:

- nhận diện thuật ngữ (`Recognize`);
- hiểu và giải thích nghĩa bằng tiếng Việt (`Understand`);
- nhận biết cách thuật ngữ được dùng trong câu mẫu hoặc tài liệu (`Understand in context`).

English track **chưa yêu cầu**:

- tự viết prompt tiếng Anh;
- tự viết instruction tiếng Anh;
- dịch prompt tiếng Việt sang tiếng Anh;
- dùng tiếng Anh để vận hành ChatGPT.

Mức `Use` được **DEFERRED** cho phase học tiếng Anh sau và không chặn PASS của lesson hiện tại.

## Mẫu prompt vận hành mặc định

```text
Kết quả cần đạt: ...
Ngữ cảnh: ...
Công cụ hoặc nguồn cần dùng: ...
Dạng đầu ra: ...
Ranh giới: ...
Tiêu chí chấp nhận: ...
Cách kiểm chứng: ...
Ngôn ngữ đầu ra: Tiếng Việt.
```

Không cần điền tất cả dòng cho task đơn giản. Mục tiêu là rõ việc, rõ dữ kiện, rõ giới hạn và rõ cách kiểm.

## Tách hai track học

### ChatGPT track

Người học được phép dùng **100% tiếng Việt** để giao việc, phân tích, kiểm chứng và tạo sản phẩm. PASS dựa trên khả năng dùng ChatGPT đúng, không dựa trên khả năng viết prompt tiếng Anh.

### English track

Trong Vocabulary-first mode, tiếng Anh được học thông qua:

- key vocabulary / từ vựng trọng tâm;
- nghĩa tiếng Việt và meaning-in-context;
- phát âm khi hữu ích;
- phân biệt các thuật ngữ dễ nhầm;
- nhận diện từ trong English patterns hoặc đoạn tài liệu ngắn.

English patterns là **reference để đọc và làm quen**, không phải bài bắt buộc tự viết lại.

## Quy tắc cho lesson mới hoặc lesson được cập nhật

1. Mọi prompt thực hành phải có bản tiếng Việt hoàn chỉnh và dùng được ngay.
2. Nếu thêm bản tiếng Anh, đặt sau bản tiếng Việt và ghi rõ đó là tham khảo.
3. Không đặt `English prompt` làm prompt chính của ví dụ.
4. Bài ChatGPT exercise dùng tiếng Việt.
5. English exercise trong Vocabulary-first mode chỉ kiểm tra nhận diện và hiểu từ vựng; không yêu cầu tự viết prompt tiếng Anh.
6. Khi prompt có code, command hoặc tên kỹ thuật, giữ nguyên phần kỹ thuật và viết phần hướng dẫn xung quanh bằng tiếng Việt.
7. QA phải kiểm tra người mới có thể hoàn thành lesson mà không cần tự dịch hoặc tự viết prompt tiếng Anh.

## PASS rule hiện tại

- **ChatGPT track:** Explain → Execute → Diagnose → Verify → Transfer.
- **English track:** Recognize → Understand.
- **English Use:** DEFERRED, không chặn PASS.

Nếu một lesson cũ còn yêu cầu viết prompt/instruction tiếng Anh, bỏ qua yêu cầu đó trong mode hiện tại cho tới khi lesson được cập nhật.
