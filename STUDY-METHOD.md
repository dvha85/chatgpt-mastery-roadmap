# Study Method

> **Bilingual learning rule:** every lesson teaches ChatGPT/AI and practical English together. See [docs/BILINGUAL-LESSON-STANDARD.md](docs/BILINGUAL-LESSON-STANDARD.md).

## 0. Hai track học song song

Mỗi lesson có hai track:

- **ChatGPT track:** hiểu khái niệm → thực hiện → chẩn đoán lỗi → kiểm chứng → áp dụng sang tình huống khác.
- **English track:** nhận diện thuật ngữ → hiểu nghĩa trong ngữ cảnh → dùng được thuật ngữ/mẫu câu khi làm việc với AI.

Không học tiếng Anh như một môn tách rời. Từ vựng, mẫu câu và bài luyện đều lấy trực tiếp từ công việc ChatGPT/AI.

## 1. Học theo năng lực, không theo số trang đã đọc

Tài liệu chính thức là source of truth về tính năng hiện tại. Nhưng mục tiêu khóa học là năng lực sử dụng.

Mỗi lesson dùng vòng:

1. **READ** — đọc nguồn chính thức.
2. **EXPLAIN** — tự giải thích lại không nhìn tài liệu.
3. **PRACTICE** — làm một bài nhỏ.
4. **VERIFY** — kiểm tra đầu ra, nguồn, giả định hoặc test.
5. **BUILD** — áp dụng vào một việc thật.
6. **REFLECT** — ghi 3 dòng: điều gì hiệu quả, điều gì sai, lần sau thay đổi gì.

## 2. Tỷ lệ học khuyến nghị

- 20% đọc tài liệu.
- 60% thực hành trực tiếp trong ChatGPT/Codex.
- 20% review, ghi evidence và sửa mental model.

## 3. PASS model

ChatGPT track chỉ PASS khi đạt cả 5:

- **Explain:** giải thích bằng lời của mình.
- **Execute:** tự thực hiện được.
- **Diagnose:** nhận ra failure mode phổ biến.
- **Verify:** có cách kiểm tra kết quả.
- **Transfer:** áp dụng được vào tình huống khác.

English track cần đạt 3 mức:

- **Recognize:** nhận ra thuật ngữ và mẫu câu chính.
- **Understand:** giải thích được ý nghĩa trong ngữ cảnh AI.
- **Use:** tự dùng được một số thuật ngữ/mẫu câu trong prompt hoặc workflow.

English track ưu tiên khả năng sử dụng thực tế, không yêu cầu ngữ pháp hoàn hảo.

## 4. Evidence

Evidence có thể là:

- prompt + kết quả + critique;
- screenshot;
- research memo;
- file tạo ra;
- issue/commit/PR;
- skill/workflow spec;
- automation spec;
- eval cases.

Không lưu secret, token, password hoặc dữ liệu riêng tư không cần thiết vào repo.

## 5. Một session học mẫu

- 5 phút: recall bài trước.
- 10 phút: đọc mục tiêu và nguồn.
- 15 phút: guided exercise.
- 10 phút: real-world exercise.
- 5 phút: verification/critique.
- 5 phút: update PROGRESS + notes.

Có thể rút ngắn hoặc kéo dài, nhưng không bỏ bước verify.

## 6. Beginner mode — Chế độ người mới
Nếu đây là lần đầu dùng ChatGPT, làm theo [START-HERE.md](START-HERE.md) và chỉ mở lesson READY. Một buổi học nên có một mục tiêu nhỏ, input không nhạy cảm và kết quả quan sát được.

Nếu bị kẹt, ghi bước và lỗi trước khi hỏi lại. Nếu tính năng không có, làm fallback và ghi rõ giới hạn; fallback không chứng minh bạn đã dùng tính năng thật.

## 7. Evidence và quyền riêng tư
Evidence là đầu ra của người học. Dùng [evidence checklist](evidence/README.md), thay dữ liệu thật bằng dữ liệu giả lập và xóa secret. Có thể dùng private notes hoặc private repository độc lập.

## 8. Ôn tập khi chưa PASS
Chấm từng năng lực Explain, Execute, Diagnose, Verify, Transfer và English. Ôn đúng tiêu chí thiếu, làm input khác và ghi lần đánh giá lại.

Một session mục tiêu là 50 phút; có thể rút còn 30 phút bằng cách gộp recall với đọc docs hoặc làm một bài transfer ngắn hơn. Không bỏ verification.