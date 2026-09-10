# Prompt Lab — Phòng thực hành Prompt

> **Purpose / Mục tiêu:** chuyển prompting từ “thử câu chữ” thành experiment có baseline, thay đổi có chủ đích, output contract và verification.

## 1. Terms first — Thuật ngữ cần hiểu

- **experiment / thí nghiệm:** một lần thử có task, thay đổi và tiêu chí đánh giá rõ.
- **baseline / mốc ban đầu:** prompt hoặc kết quả trước khi cải thiện.
- **task specification / bản đặc tả tác vụ:** goal + context + output + boundaries + verification phù hợp.
- **variable / biến thay đổi:** điều bạn chủ động thay trong một vòng thử, ví dụ thêm output contract.
- **rubric / thang chấm:** tiêu chí chấm cố định để so sánh kết quả.
- **ground truth / dữ kiện đối chiếu:** thông tin được coi là đúng cho bài test cố định.

## 2. Core loop — Vòng lặp cốt lõi

```text
TASK
  ↓
BASELINE PROMPT
  ↓
RUN / INSPECT
  ↓
DIAGNOSE ONE OR TWO FAILURES
  ↓
CHANGE THE TASK SPEC
  ↓
RUN AGAIN
  ↓
VERIFY WITH RUBRIC / GROUND TRUTH
  ↓
SAVE THE REUSABLE LESSON
```

Không thay 10 thứ cùng lúc rồi kết luận “prompt dài hơn tốt hơn”. Hãy biết thay đổi nào giải quyết lỗi nào.

## 3. Three guided labs — 3 lab mẫu

| Lab | Main skill | Data |
|---|---|---|
| [P-001 — Summary](examples/P-001-summary.md) | grounding + output contract | Dataset A |
| [P-002 — Planning](examples/P-002-planning.md) | constraints + decomposition + arithmetic | Dataset B |
| [P-003 — Comparison](examples/P-003-comparison.md) | unknown handling + evidence-based recommendation | Dataset C |

Dữ liệu cố định: [labs/data/sample-brief.md](data/sample-brief.md).

## 4. How to run a lab — Cách làm một lab

1. Đọc task và dataset, chưa xem reference result nếu muốn tự kiểm tra thật.
2. Viết **baseline prompt** ngắn như bạn thường viết.
3. Chạy prompt hoặc dùng supplied weak output khi bài yêu cầu chẩn đoán lỗi tái lập.
4. Đánh dấu lỗi theo rubric: task hiểu sai, thiếu context, format khó kiểm, unsupported claim, arithmetic, boundary, v.v.
5. Viết **improved task spec**. Chỉ thêm chi tiết có vai trò rõ.
6. Chạy lại.
7. Verify bằng ground truth, phép tính, source hoặc checklist phù hợp.
8. Chấm `0 / 1 / 2` từng criterion.
9. Ghi thay đổi nào cải thiện chất lượng nhiều nhất.
10. Lưu evidence đã làm sạch.

## 5. Experiment template — Mẫu experiment

### Experiment ID

`P-YYYYMMDD-XX`

### Task / Tác vụ

- Outcome:
- Why it matters:

### Input / Đầu vào

- File/data/source:
- Ground truth or check method:

### Baseline prompt

```text
...
```

### Baseline result

- What worked:
- What failed:

### Diagnosis / Chẩn đoán

| Failure | Evidence | Likely prompt/task-spec gap |
|---|---|---|
| | | |

### Change hypothesis / Giả thuyết thay đổi

```text
If I add/change ..., then ... should improve because ...
```

### Improved task spec

- Goal:
- Context:
- Output:
- Boundaries:
- Tools/sources:
- Verification:

### Improved result

- Summary:
- Remaining failure:

### Verification

- [ ] Ground truth/source checked
- [ ] Calculations/tests checked if relevant
- [ ] Boundaries checked
- [ ] Unsupported claims marked

### Rubric score

| Criterion | Baseline 0–2 | Improved 0–2 | Evidence |
|---|---:|---:|---|
| | | | |

### What changed quality most?

- ...

### Reusable lesson

- ...

## 6. Rules for fair comparison — Quy tắc so sánh công bằng

- Giữ cùng task/input khi so baseline và improved prompt.
- Không chấm “hay” bằng cảm giác; dùng rubric/checklist.
- Nếu output thay đổi vì dữ liệu mới hoặc web mới, ghi rõ biến đó.
- Không yêu cầu model phải tạo đúng cùng câu chữ để PASS.
- Không coi model tự nói “I verified it” là verification evidence.
- Với fact hiện tại, dùng nguồn hiện tại; với dữ liệu đóng, không cần web.

## 7. What counts as improvement? — Khi nào gọi là cải thiện?

Improvement nên quan sát được, ví dụ:

- ít unsupported claims hơn;
- đủ field bắt buộc hơn;
- đúng constraint hơn;
- giảm số follow-up cần thiết;
- phép tính/test đúng;
- output dễ review hơn;
- unknown được giữ thay vì bịa.

“Prompt dài hơn” không tự động là improvement.

## 8. Evidence standard — Chuẩn evidence

Lưu tối thiểu:

- task + input;
- baseline prompt/result;
- diagnosis;
- improved prompt/result;
- rubric trước/sau;
- verification evidence;
- reflection.

Không lưu secret hoặc dữ liệu riêng tư lên repo. Xem [Evidence Template](../evidence/TEMPLATE.md).

## 9. Official sources — Nguồn chính thức

- [Prompt engineering best practices for ChatGPT — OpenAI Help Center](https://help.openai.com/en/articles/10032626)
- [How do I create a good prompt for an AI model? — OpenAI Help Center](https://help.openai.com/en/articles/4936848)
- [Does ChatGPT tell the truth? — OpenAI Help Center](https://help.openai.com/en/articles/8313428)

## 10. Next — Tiếp theo

Sau khi hoàn thành ba guided labs, dùng [Evaluation Lab](EVALUATION-LAB.md) để chấm theo cùng hệ thống `0 / 1 / 2`, rồi làm [M01 Check](../assessments/M01-CHECK.md).
