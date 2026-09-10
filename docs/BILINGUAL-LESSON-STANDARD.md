# Bilingual Lesson Standard — Tiêu chuẩn bài học song ngữ

> Applies to every lesson in this repository from v0.1.1 onward.  
> Áp dụng cho mọi bài học trong repository từ phiên bản v0.1.1 trở đi.

## 1. Goal — Mục tiêu

Every lesson teaches two things at the same time:

1. **ChatGPT / AI capability** — understand and use the feature or concept correctly.
2. **Practical English** — understand the English terms and sentence patterns that appear in real AI documentation and workflows.

Mỗi bài học đồng thời dạy hai năng lực:

1. **Năng lực ChatGPT / AI** — hiểu và sử dụng đúng tính năng hoặc khái niệm.
2. **Tiếng Anh thực dụng** — hiểu thuật ngữ và mẫu câu thực tế xuất hiện trong tài liệu AI và workflow.

The English goal is not academic translation. The goal is to make official English documentation progressively easier to read without translation.

Mục tiêu tiếng Anh không phải là dịch thuật hàn lâm. Mục tiêu là giúp người học dần có thể đọc tài liệu chính thức bằng tiếng Anh mà không cần phụ thuộc vào bản dịch.

## 2. Required lesson structure — Cấu trúc bắt buộc của mỗi bài

Every lesson MUST contain the following sections.

Mỗi bài MUST có các phần sau.

### A. Lesson title — Tên bài

Use the official English term first, followed by a natural Vietnamese explanation.

Đặt thuật ngữ tiếng Anh chính thức trước, sau đó là cách diễn giải tiếng Việt tự nhiên.

Example:

`M00.2 — Context, Tools & Hallucination / Ngữ cảnh, công cụ và hiện tượng bịa thông tin`

### B. Learning objectives — Mục tiêu học tập

Write objectives in English and Vietnamese.

Viết mục tiêu bằng cả tiếng Anh và tiếng Việt.

### C. Key vocabulary — Từ vựng trọng tâm

For every important technical term, explain:

| Field | Requirement |
|---|---|
| **Term** | Official English term |
| **Pronunciation** | IPA or an easy pronunciation hint when useful |
| **Vietnamese** | Natural Vietnamese meaning |
| **Plain English** | Simple English explanation |
| **In ChatGPT** | What the term specifically means in a ChatGPT/AI context |
| **Example** | One short English example plus Vietnamese meaning |
| **Common confusion** | Similar term or common misunderstanding when relevant |

Do not translate technical terminology mechanically. Prefer the English term as the canonical name and use Vietnamese to explain the concept.

Không dịch máy móc thuật ngữ kỹ thuật. Giữ thuật ngữ tiếng Anh là tên chuẩn và dùng tiếng Việt để giải thích bản chất.

### D. Core concept — Khái niệm cốt lõi

Use paired explanations:

**English** — concise explanation written in natural, accessible English.  
**Tiếng Việt** — explanation of the same idea, with extra clarification when necessary.

The Vietnamese paragraph does not need to be a literal sentence-by-sentence translation. It should optimize understanding.

Phần tiếng Việt không cần dịch từng chữ; ưu tiên giúp hiểu đúng bản chất.

### E. Why it matters — Vì sao quan trọng

Explain both the practical benefit and the failure caused by misunderstanding the concept.

Giải thích cả lợi ích khi hiểu đúng và lỗi có thể xảy ra khi hiểu sai.

### F. Examples — Ví dụ

Include realistic examples. Prompts should normally be shown in English first, then Vietnamese explanation/translation.

Ví dụ phải sát tình huống thực tế. Prompt nên ưu tiên viết bằng tiếng Anh trước, sau đó giải thích/dịch tiếng Việt.

### G. English patterns for AI work — Mẫu câu tiếng Anh dùng với AI

Each lesson introduces 3–8 reusable sentence patterns, for example:

- `Use the attached file as the primary source.` — Dùng file đính kèm làm nguồn chính.
- `State your assumptions explicitly.` — Nêu rõ các giả định của bạn.
- `Cite the evidence for each claim.` — Trích dẫn bằng chứng cho từng nhận định.
- `Ask only if a missing detail materially changes the answer.` — Chỉ hỏi lại nếu thông tin thiếu làm thay đổi đáng kể câu trả lời.

These are functional expressions the learner can reuse directly with ChatGPT.

Đây là các mẫu câu thực dụng có thể dùng trực tiếp khi làm việc với ChatGPT.

### H. Practice — Thực hành

Every lesson includes:

1. a comprehension check;
2. a ChatGPT exercise;
3. an English exercise;
4. a real-world transfer exercise.

Mỗi bài gồm kiểm tra hiểu bài, bài thực hành ChatGPT, bài luyện tiếng Anh và bài áp dụng thực tế.

### I. Verification & failure modes — Kiểm chứng và lỗi thường gặp

Teach how to verify the result and identify at least one failure mode.

Hướng dẫn cách kiểm tra kết quả và nhận diện ít nhất một failure mode.

### J. Language checkpoint — Kiểm tra tiếng Anh

Before PASS, the learner should be able to:

- recognize the lesson's key English terms;
- explain 3–5 important terms in simple Vietnamese;
- understand several common English instructions without translation;
- write at least one useful ChatGPT instruction in English.

Trước khi PASS, người học cần nhận diện được thuật ngữ chính, giải thích được bản chất bằng tiếng Việt, đọc hiểu một số chỉ dẫn tiếng Anh phổ biến và tự viết ít nhất một câu lệnh ChatGPT bằng tiếng Anh.

### K. PASS criteria — Tiêu chí PASS

A lesson passes only when both tracks are satisfied:

**ChatGPT track:** Explain → Execute → Diagnose → Verify → Transfer.  
**English track:** Recognize → Understand → Use.

Không yêu cầu tiếng Anh hoàn hảo. Chấm khả năng hiểu và sử dụng đúng trong ngữ cảnh AI, không chấm theo chuẩn thi học thuật.

## 3. Progressive English exposure — Tăng dần tỷ lệ tiếng Anh

The repository remains bilingual at every stage, but English exposure increases gradually.

Repo luôn song ngữ ở mọi stage, nhưng tỷ lệ tiếp xúc tiếng Anh tăng dần:

| Stage | Suggested balance | Goal |
|---|---:|---|
| Stage A — Operator | ~50% EN / 50% VI | Build confidence and core vocabulary |
| Stage B — Power User | ~60% EN / 40% VI | Read product docs more independently |
| Stage C — Builder | ~70% EN / 30% VI | Work comfortably with developer documentation |

Vietnamese explanations remain available for difficult concepts even in Stage C.

Ở Stage C vẫn giữ phần giải thích tiếng Việt cho các khái niệm khó.

## 4. Vocabulary policy — Quy tắc thuật ngữ

- Keep canonical product and engineering terms in English: `prompt`, `context`, `token`, `agent`, `tool`, `workflow`, `plugin`, `skill`, `grounding`, `retrieval`, etc.
- Give a Vietnamese explanation on first use.
- Prefer meaning-in-context over dictionary translation.
- Distinguish closely related terms explicitly.
- Add important terms to the cumulative [GLOSSARY.md](../GLOSSARY.md).
- Mark terms that are OpenAI product names separately from general AI terms.

## 5. What NOT to do — Những điều không làm

- Do not create two disconnected lessons, one English and one Vietnamese.
- Do not produce word-for-word Vietnamese translations that sound unnatural.
- Do not overload a lesson with every possible English word.
- Do not hide key technical terms behind Vietnamese-only translations.
- Do not require perfect grammar before the learner can PASS an AI skill.
- Do not teach obsolete terminology when official OpenAI terminology has changed.

## 6. Source-first rule — Ưu tiên nguồn chính thức

When terminology is product-specific, check the latest official OpenAI documentation before finalizing a lesson.

Nếu thuật ngữ liên quan đến sản phẩm/tính năng cụ thể, phải kiểm tra tài liệu OpenAI mới nhất trước khi hoàn thiện bài học.

## 7. Beginner accessibility — Khả năng tiếp cận cho người mới
- Giải thích bước thao tác trước khi dùng từ viết tắt hoặc tên tính năng.
- Mỗi ví dụ chỉ rõ input, hành động, kết quả minh họa và cách kiểm tra.
- Không viết “hãy thực hành” nếu chưa có dữ liệu, prompt mẫu hoặc tiêu chí quan sát.
- Ghi rõ nguyên lý bền vững và chi tiết giao diện có thể đổi.
- Tính năng không có trên mọi tài khoản phải có fallback và nhãn `not tested`.

## 7. Beginner accessibility — Khả năng tiếp cận cho người mới

- Lesson phải giải thích bước thao tác trước khi dùng từ viết tắt hoặc tên tính năng.
- Mỗi bài nên giới hạn khoảng 3–7 thuật ngữ mới và nhắc lại thuật ngữ cũ trước khi thêm từ mới.
- Mỗi ví dụ chỉ rõ input, hành động, kết quả minh họa và cách kiểm tra.
- Không viết “hãy thực hành” nếu chưa có dữ liệu, prompt mẫu hoặc tiêu chí quan sát.
- Tính năng không có trên mọi tài khoản phải có fallback và nhãn `not tested`.