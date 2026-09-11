# Evaluation Lab — Phòng đánh giá

> **Purpose / Mục tiêu:** chuyển từ “cảm giác câu trả lời tốt” sang đánh giá có tiêu chí, evidence và đường học lại rõ ràng.  
> **Ngôn ngữ vận hành:** eval case, prompt, output ví dụ và retest dùng tiếng Việt làm mặc định. English track được chấm riêng.

## 1. Terms first — Thuật ngữ cần hiểu
- **evaluation / đánh giá:** kiểm một output hoặc workflow bằng tiêu chí định trước.
- **criterion / tiêu chí:** một điều cụ thể cần đạt.
- **rubric / thang chấm:** mô tả thế nào là 0, 1 và 2 điểm.
- **ground truth / dữ kiện đối chiếu:** dữ liệu chuẩn để kiểm đúng/sai khi có thể.
- **failure mode / kiểu lỗi:** cách output có thể thất bại lặp lại.
- **evidence / bằng chứng:** dữ liệu, source, calculation, test hoặc artifact chứng minh score.

## 2. Core scoring scale — Thang điểm 0–2
| Score | Meaning / Ý nghĩa | Dấu hiệu quan sát được |
|---:|---|---|
| 0 | Not demonstrated / Chưa chứng minh | sai cốt lõi, thiếu hoàn toàn hoặc phải đoán thay người học |
| 1 | Partial / Một phần | làm được một phần nhưng thiếu tiêu chí hoặc cần gợi ý đáng kể |
| 2 | Independent pass / Tự làm đạt | làm đúng, giải thích được và có evidence phù hợp |

Không cho `2` chỉ vì output trông chuyên nghiệp.

## 3. Five learning capabilities — 5 năng lực cần đo
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

## 4. English track — Nhánh tiếng Anh
English không được dùng để làm khó người mới. Kiểm ba mức: Recognize, Understand, Use. Người học có thể giải thích bằng tiếng Việt; lỗi grammar nhỏ không đổi intent không làm trượt. **Không yêu cầu dùng tiếng Anh trong ChatGPT track.**

## 5. Eval case template — Mẫu một case đánh giá

| Field | Value |
|---|---|
| Eval ID | E-001 |
| Tác vụ | |
| Đầu vào / nguồn | |
| Thuộc tính mong đợi | |
| Điều không được làm | |
| Ground truth / cách kiểm | |
| Model/settings/environment | |
| Kết quả | |
| Điểm theo tiêu chí | |
| Ghi chú lỗi | |
| Hành động retest | |

## 6. Output-quality criteria — Tiêu chí chất lượng output
Dùng khi phù hợp: Correctness, Completeness, Instruction following, Format compliance, Grounding, Unknown handling, Calculation/test correctness, Safety/risk handling, Efficiency.

## 7. Example: a failing evaluation — Ví dụ bài chưa đạt

Dùng weak output của [P-003 Comparison](examples/P-003-comparison.md):

```text
Cedar là lựa chọn tốt nhất. Nó có giá khoảng $10/tháng, hỗ trợ contact form và có setup/maintenance thấp. Pine rẻ hơn nhưng kém linh hoạt hơn, còn Maple quá đắt so với ngân sách.
```

### Score
| Criterion | Score | Evidence |
|---|---:|---|
| Correctness | 0 | Cedar cost/contact form là Unknown; Maple $14 vẫn trong budget $15 |
| Grounding | 0 | thêm “Pine kém linh hoạt” không có trong data |
| Unknown handling | 0 | biến Unknown thành fact tự tạo |
| Format compliance | 1 | có recommendation nhưng thiếu cấu trúc comparison |
| Verification | 0 | không map về dataset |

**Result:** FAIL.

Đây là execution/verification error, không phải English error. Học lại M01.3 + M01.4 rồi làm case tương đương mới.

## 8. Example: a passing evaluation — Ví dụ bài đạt
Một result đạt cho Dataset C phải tối thiểu:
- giữ Cedar cost/contact form là `Unknown`;
- xác nhận Pine và Maple đều trong budget;
- tách mandatory criteria khỏi preference;
- recommend Pine bằng evidence trong bảng;
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

## 9. Diagnose the type of failure — Phân loại lỗi
| Failure type | Ví dụ | Học/sửa ở đâu |
|---|---|---|
| Knowledge | nghĩ confidence = evidence | M00.2, M00.3 |
| Task-spec | goal/context/output mơ hồ | M01.1 |
| Iteration | sửa lan man, không checkpoint | M01.2 |
| Output contract | thiếu field, format khó kiểm | M01.3 |
| Verification | không kiểm source/calculation/unknown | M01.4 |
| English expression | câu tiếng Anh chưa tự nhiên nhưng intent đúng | sửa ngôn ngữ, không học lại concept nếu concept đúng |

## 10. Retest loop — Vòng học lại

```text
TIÊU CHÍ FAIL
  ↓
TÌM LESSON / VÍ DỤ LIÊN QUAN
  ↓
SỬA MỘT KHOẢNG TRỐNG KỸ NĂNG
  ↓
LÀM CASE TƯƠNG ĐƯƠNG MỚI BẰNG TIẾNG VIỆT
  ↓
KIỂM CHỨNG LẠI
  ↓
LƯU EVIDENCE RETEST
```

Không yêu cầu học lại toàn module nếu chỉ vướng một criterion.

## 11. Reliability rule — Quy tắc độ tin cậy
Không dùng một eval case duy nhất để kết luận model, prompt hay workflow “tốt”. Một case chỉ chứng minh hệ thống làm tốt case đó trong môi trường đã ghi.

## 12. Evidence to save — Evidence cần lưu
Eval case, input/ground truth, output, rubric score, evidence cho score quan trọng, failure classification và retest nếu có.

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
6. Lưu evidence và chỉ cập nhật `PROGRESS.md` khi bài làm của người học đạt gate.
