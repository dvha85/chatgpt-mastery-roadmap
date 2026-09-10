# Evaluation Lab — Phòng đánh giá

> **Purpose / Mục tiêu:** chuyển từ “cảm giác câu trả lời tốt” sang đánh giá có tiêu chí, evidence và đường học lại rõ ràng.

## 1. Terms first — Thuật ngữ cần hiểu

- **evaluation / đánh giá:** kiểm một output hoặc workflow bằng tiêu chí định trước.
- **criterion / tiêu chí:** một điều cụ thể cần đạt.
- **rubric / thang chấm:** mô tả thế nào là 0, 1 và 2 điểm.
- **ground truth / dữ kiện đối chiếu:** dữ liệu chuẩn để kiểm đúng/sai khi có thể.
- **failure mode / kiểu lỗi:** cách output có thể thất bại lặp lại.
- **evidence / bằng chứng:** dữ liệu, source, calculation, test hoặc artifact chứng minh score.

## 2. Core scoring scale — Thang điểm 0–2

| Score | Meaning / Ý nghĩa | Observable behavior / Dấu hiệu quan sát được |
|---:|---|---|
| 0 | Not demonstrated / Chưa chứng minh | sai cốt lõi, thiếu hoàn toàn hoặc phải đoán thay người học |
| 1 | Partial / Một phần | làm được một phần nhưng còn thiếu tiêu chí hoặc cần gợi ý đáng kể |
| 2 | Independent pass / Tự làm đạt | làm đúng, giải thích được và có evidence phù hợp |

Không cho `2` chỉ vì output trông chuyên nghiệp.

## 3. Five learning capabilities — 5 năng lực cần đo

Áp dụng cho checkpoint BOOT–M01 và các lab nền tảng:

| Capability | Câu hỏi đánh giá |
|---|---|
| **Explain** | Người học có giải thích khái niệm bằng lời mình không? |
| **Execute** | Có tự thực hiện task đúng yêu cầu không? |
| **Diagnose** | Có tìm ra lỗi/nguyên nhân khi output kém không? |
| **Verify** | Có kiểm kết quả bằng evidence độc lập phù hợp không? |
| **Transfer** | Có áp dụng cùng nguyên tắc sang task khác không? |

### PASS capability gate

- tổng >= **8/10**;
- không capability nào bằng `0`;
- **Execute = 2**;
- **Verify = 2**.

Đây là gate năng lực tổng hợp. Checkpoint module vẫn có rubric riêng chi tiết hơn.

## 4. English track — Nhánh tiếng Anh

English không được dùng để làm khó người mới. Kiểm ba mức:

1. **Recognize / nhận ra** — biết thuật ngữ đang nói tới gì.
2. **Understand / hiểu** — giải thích đúng bằng tiếng Việt.
3. **Use / sử dụng** — dùng thuật ngữ trong một instruction/prompt có nghĩa đúng.

### Foundation checkpoint

- nhận ra ít nhất 4/5 từ được kiểm;
- giải thích đúng ít nhất 3 từ trọng tâm bằng tiếng Việt;
- viết một instruction tiếng Anh có ý nghĩa đúng;
- lỗi ngữ pháp nhỏ không đổi ý định **không làm trượt**.

## 5. Eval case template — Mẫu một case đánh giá

| Field | Value |
|---|---|
| Eval ID | E-001 |
| Task | |
| Input / source | |
| Expected properties | |
| Must-not-do | |
| Ground truth / verification method | |
| Model/settings/environment | |
| Result | |
| Score by criterion | |
| Failure notes | |
| Retest action | |

## 6. Output-quality criteria — Tiêu chí chất lượng output

Dùng khi phù hợp với task, không bắt buộc mọi case có đủ tất cả:

- Correctness / đúng dữ kiện hoặc logic
- Completeness / đủ phần cần thiết
- Instruction following / làm đúng instruction
- Format compliance / đúng format
- Grounding / bám input/source
- Unknown handling / xử lý dữ liệu thiếu
- Calculation or test correctness / phép tính hoặc test
- Safety/risk handling / boundary và hành động rủi ro
- Efficiency / không thêm thủ tục không cần thiết

## 7. Example: a failing evaluation — Ví dụ bài chưa đạt

Dùng supplied weak output của [P-003 Comparison](examples/P-003-comparison.md):

```text
Cedar is the best choice. It costs about $10/month, supports a contact form, and has low setup and maintenance. Pine is cheaper but less flexible, while Maple is too expensive for the budget.
```

### Score

| Criterion | Score | Evidence |
|---|---:|---|
| Correctness | 0 | Cedar cost/contact form are Unknown; Maple $14 is within $15 budget |
| Grounding | 0 | Adds “Pine less flexible” not present in data |
| Unknown handling | 0 | Converts Unknown to invented facts |
| Format compliance | 1 | Gives a recommendation but no requested comparison structure |
| Verification | 0 | No mapping back to dataset |

**Result:** FAIL.

### Diagnosis

Đây chủ yếu là **execution/verification error**, không phải English error. Học lại M01.3 + M01.4, rồi làm một comparison case tương đương mới.

## 8. Example: a passing evaluation — Ví dụ bài đạt

Một result đạt cho cùng Dataset C phải tối thiểu:

- giữ Cedar cost/contact form là `Unknown`;
- xác nhận Pine và Maple đều trong budget;
- tách mandatory criteria khỏi preference;
- recommend Pine bằng evidence có trong bảng;
- nêu Cedar chưa thể confirm eligible.

### Example score

| Criterion | Score | Evidence |
|---|---:|---|
| Correctness | 2 | mọi field khớp dataset |
| Grounding | 2 | không thêm criterion/fact ngoài input |
| Unknown handling | 2 | Unknown giữ nguyên và ảnh hưởng eligibility đúng |
| Format compliance | 2 | table + recommendation theo contract |
| Verification | 2 | requirement-to-evidence mapping đầy đủ |

**Result:** PASS 10/10.

Không cần câu chữ giống reference answer.

## 9. Diagnose the type of failure — Phân loại lỗi

| Failure type | Ví dụ | Học/sửa ở đâu |
|---|---|---|
| Knowledge / hiểu sai khái niệm | nghĩ confidence = evidence | M00.2, M00.3 |
| Task-spec / giao việc | goal/context/output mơ hồ | M01.1 |
| Iteration / chia việc | sửa lan man, không checkpoint | M01.2 |
| Output contract | thiếu field, format khó kiểm | M01.3 |
| Verification | không kiểm source/calculation/unknown | M01.4 |
| English expression | câu tiếng Anh chưa tự nhiên nhưng intent vẫn đúng | sửa ngôn ngữ, không học lại concept nếu concept đúng |

## 10. Retest loop — Vòng học lại

Khi FAIL:

```text
FAILED CRITERION
  ↓
FIND MATCHING LESSON / EXAMPLE
  ↓
FIX ONE SKILL GAP
  ↓
DO A NEW EQUIVALENT CASE
  ↓
VERIFY AGAIN
  ↓
SAVE RETEST EVIDENCE
```

Không yêu cầu học lại toàn module nếu chỉ vướng một criterion.

## 11. Reliability rule — Quy tắc độ tin cậy

Không dùng một eval case duy nhất để kết luận model, prompt hay workflow “tốt”. Một case chỉ chứng minh rằng hệ thống đã làm tốt case đó trong môi trường đã ghi.

Nếu mục tiêu sau này là so model/workflow, cần nhiều case đại diện và input cố định; nội dung này sẽ được mở rộng ở M02 và M10.

## 12. Evidence to save — Evidence cần lưu

- eval case;
- input/ground truth;
- output;
- rubric score;
- evidence cho từng score quan trọng;
- failure classification;
- retest nếu có.

## 13. Official sources — Nguồn chính thức

- [Prompt engineering best practices for ChatGPT — OpenAI Help Center](https://help.openai.com/en/articles/10032626)
- [How do I create a good prompt for an AI model? — OpenAI Help Center](https://help.openai.com/en/articles/4936848)
- [Does ChatGPT tell the truth? — OpenAI Help Center](https://help.openai.com/en/articles/8313428)

## 14. Practice path — Đường thực hành

1. [P-001 Summary](examples/P-001-summary.md)
2. [P-002 Planning](examples/P-002-planning.md)
3. [P-003 Comparison](examples/P-003-comparison.md)
4. [M00 Check](../assessments/M00-CHECK.md)
5. [M01 Check](../assessments/M01-CHECK.md)
6. Lưu evidence và chỉ cập nhật `PROGRESS.md` khi chính bài làm của người học đạt gate.
