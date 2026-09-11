# Prompt Lab — Phòng thực hành Prompt

> **Purpose / Mục tiêu:** chuyển prompting từ “thử câu chữ” thành experiment có baseline, thay đổi có chủ đích, output contract và verification.  
> **Ngôn ngữ vận hành:** baseline prompt, improved task spec, diagnosis và evidence dùng tiếng Việt làm mặc định. English chỉ dùng trong English track hoặc khi task bắt buộc.

## 1. Terms first — Thuật ngữ cần hiểu
- **experiment / thí nghiệm:** một lần thử có task, thay đổi và tiêu chí đánh giá rõ.
- **baseline / mốc ban đầu:** prompt hoặc kết quả trước khi cải thiện.
- **task specification / bản đặc tả tác vụ:** goal + context + output + boundaries + verification phù hợp.
- **variable / biến thay đổi:** điều bạn chủ động thay trong một vòng thử.
- **rubric / thang chấm:** tiêu chí chấm cố định để so sánh kết quả.
- **ground truth / dữ kiện đối chiếu:** thông tin được coi là đúng cho bài test cố định.

## 2. Core loop — Vòng lặp cốt lõi

```text
TASK / TÁC VỤ
  ↓
BASELINE PROMPT / PROMPT BAN ĐẦU
  ↓
CHẠY VÀ KIỂM OUTPUT
  ↓
CHẨN ĐOÁN 1–2 LỖI
  ↓
SỬA TASK SPEC
  ↓
CHẠY LẠI
  ↓
KIỂM BẰNG RUBRIC / GROUND TRUTH
  ↓
LƯU BÀI HỌC TÁI SỬ DỤNG
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
1. Đọc task và dataset, chưa xem reference result.
2. Viết **baseline prompt bằng tiếng Việt** như bạn thường viết.
3. Chạy prompt hoặc dùng supplied weak output khi bài yêu cầu chẩn đoán lỗi tái lập.
4. Đánh dấu lỗi theo rubric.
5. Viết **improved task spec bằng tiếng Việt**.
6. Chạy lại và yêu cầu output tiếng Việt.
7. Verify bằng ground truth, phép tính, source hoặc checklist.
8. Chấm `0 / 1 / 2` từng criterion.
9. Ghi thay đổi nào cải thiện chất lượng nhiều nhất.
10. Lưu evidence đã làm sạch.

## 5. Experiment template — Mẫu experiment

### Experiment ID
`P-YYYYMMDD-XX`

### Task / Tác vụ
- Kết quả cần đạt:
- Vì sao quan trọng:

### Input / Đầu vào
- File/data/source:
- Ground truth hoặc cách kiểm:

### Baseline prompt — Prompt ban đầu
```text
...
Trả lời bằng tiếng Việt.
```

### Baseline result — Kết quả ban đầu
- Điều làm tốt:
- Điều chưa đạt:

### Diagnosis / Chẩn đoán
| Lỗi | Evidence | Khoảng trống trong prompt/task spec |
|---|---|---|
| | | |

### Change hypothesis / Giả thuyết thay đổi
```text
Nếu tôi thêm/thay đổi ..., thì ... sẽ cải thiện vì ...
```

### Improved task spec — Bản giao việc cải thiện
- Mục tiêu:
- Ngữ cảnh:
- Đầu ra:
- Ranh giới:
- Công cụ/nguồn:
- Kiểm chứng:
- Ngôn ngữ đầu ra: Tiếng Việt.

### Improved result — Kết quả cải thiện
- Tóm tắt:
- Lỗi còn lại:

### Verification
- [ ] Ground truth/source đã kiểm
- [ ] Phép tính/test đã kiểm nếu liên quan
- [ ] Boundary đã kiểm
- [ ] Unsupported claims được đánh dấu

### Rubric score
| Criterion | Baseline 0–2 | Improved 0–2 | Evidence |
|---|---:|---:|---|
| | | | |

### Điều gì cải thiện chất lượng nhiều nhất?
- ...

### Reusable lesson — Bài học tái sử dụng
- ...

## 6. Rules for fair comparison — Quy tắc so sánh công bằng
- Giữ cùng task/input khi so baseline và improved prompt.
- Không chấm “hay” bằng cảm giác; dùng rubric/checklist.
- Nếu output thay đổi vì dữ liệu/web mới, ghi rõ biến đó.
- Không yêu cầu model tạo đúng cùng câu chữ để PASS.
- Không coi model tự nói “đã kiểm chứng” là verification evidence.
- Với fact hiện tại, dùng nguồn hiện tại; với dữ liệu đóng, không cần web.

## 7. What counts as improvement? — Khi nào gọi là cải thiện?
- ít unsupported claims hơn;
- đủ field bắt buộc hơn;
- đúng constraint hơn;
- giảm follow-up cần thiết;
- phép tính/test đúng;
- output dễ review hơn;
- unknown được giữ thay vì bịa.

“Prompt dài hơn” không tự động là improvement.

## 8. Evidence standard — Chuẩn evidence
Lưu task + input; baseline prompt/result; diagnosis; improved prompt/result; rubric trước/sau; verification evidence; reflection. Không lưu secret hoặc dữ liệu riêng tư lên repo.

## 9. Official sources — Nguồn chính thức
- [Prompt engineering best practices for ChatGPT — OpenAI Help Center](https://help.openai.com/en/articles/10032626)
- [How do I create a good prompt for an AI model? — OpenAI Help Center](https://help.openai.com/en/articles/4936848)
- [Does ChatGPT tell the truth? — OpenAI Help Center](https://help.openai.com/en/articles/8313428)

## 10. Next — Tiếp theo
Sau ba guided labs, dùng [Evaluation Lab](EVALUATION-LAB.md), rồi làm [M01 Check](../assessments/M01-CHECK.md).
