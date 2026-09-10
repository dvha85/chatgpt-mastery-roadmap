# M01 Check — Prompting as Task Specification / Bài kiểm tra M01

> Làm sau M01.4. Hãy tự làm đủ 5 task spec trước khi xem phần đáp án mẫu và rubric.

## Instructions / Hướng dẫn

Với mỗi yêu cầu mơ hồ:

1. Viết lại thành task specification rõ.
2. Ghi ít nhất Goal, Context, Output và Boundaries nếu cần.
3. Nêu một verification step.
4. Với ít nhất một câu, chạy prompt thật và lưu evidence.

Không cần prompt dài. Prompt tốt là prompt đủ rõ để làm và kiểm.

---

## Five vague requests / 5 yêu cầu mơ hồ

### 1. `Make this better.`

Context giả lập: đây là email cập nhật tiến độ cho khách hàng. Có ngày giao dự kiến chưa được xác nhận.

**Your task spec / Bản giao việc của bạn:**

- Goal:
- Context:
- Output:
- Boundaries:
- Verification:

### 2. `Summarize this report.`

Context giả lập: report dự án 3 trang cho quản lý; họ cần decisions, risks và next steps trước.

**Your task spec:**

- Goal:
- Context:
- Output:
- Boundaries:
- Verification:

### 3. `Plan my week.`

Context giả lập: có 9 giờ học; fundamentals phải học trước automation; Sunday dành cho review; không học quá 2 giờ liên tục.

**Your task spec:**

- Goal:
- Context:
- Output:
- Boundaries:
- Verification:

### 4. `Which website tool is best?`

Context giả lập: freelancer Việt Nam, không chuyên kỹ thuật, budget dưới $15/tháng, cần custom domain và maintenance thấp. Giá/feature hiện tại phải được kiểm chứng.

**Your task spec:**

- Goal:
- Context:
- Output:
- Boundaries:
- Tools/sources:
- Verification:

### 5. `Explain this data.`

Context giả lập:

| Month | Revenue |
|---|---:|
| Jan | 1000 |
| Feb | 1250 |
| Mar | 1100 |
| Apr | 1500 |

Audience không chuyên data. Bạn muốn trend và anomaly nhưng không muốn AI bịa nguyên nhân.

**Your task spec:**

- Goal:
- Context:
- Output:
- Boundaries:
- Verification:

---

# Answer guide / Gợi ý đáp án

> Có nhiều đáp án hợp lệ. Trọng tâm là task spec đủ rõ, không phải câu chữ giống mẫu.

## 1. Email update

```text
Rewrite this project-status email for a client. Keep every confirmed fact and date unchanged. Use a calm, professional tone and keep it under 150 words. Do not promise a delivery date unless it is explicitly confirmed in the original email. After rewriting, list any statement you removed because it was unsupported.
```

**Why / Vì sao:** goal, audience, output và boundary đều quan sát được. Verification là đối chiếu facts/dates với email gốc.

## 2. Report summary

```text
Summarize this three-page project report for a manager. Put decisions first, then risks, then next steps. Use no more than eight bullets. Use only information in the report; label missing owner or due-date information as Unknown instead of inventing it.
```

**Verification:** đối chiếu từng bullet với report, đặc biệt decisions và dates.

## 3. Weekly plan

```text
Create a one-week ChatGPT study plan using exactly 9 hours total. Teach fundamentals before automation, reserve Sunday for review, and keep each study block at 2 hours or less. Return a table with Day, Topic, Duration, and Completion criterion, then show the weekly total.
```

**Verification:** cộng tổng giờ, kiểm thứ tự và block-duration constraint.

## 4. Website tool

```text
Compare at least four current website options for a non-technical Vietnamese freelancer. Budget is under $15/month; custom domain is required; low maintenance is preferred. Use current official product sources for price and feature claims. Return a table with Option, Recurring cost, Custom domain, Setup difficulty, Maintenance, Main trade-off, and Evidence status. Mark missing facts Unknown. Recommend one option and explain two trade-offs. Do not purchase, create accounts, or enter payment information.
```

**Verification:** mở source chính thức, đối chiếu current price/custom-domain claim và tính recurring cost.

## 5. Revenue data

```text
Using only the monthly revenue table I provide, describe the overall trend and identify the largest month-to-month increase and decrease. Show the arithmetic for those changes. Explain the result for a non-technical reader in under 150 words. Do not infer causes for the changes unless evidence about causes is provided.
```

**Verification:** tính lại từng month-to-month difference; kiểm narrative không biến correlation thành cause.

---

## Quality examples / Ví dụ các mức chất lượng

### Level 0 — Chưa đạt

```text
Make the email much better and professional.
```

Vẫn thiếu mục tiêu cụ thể, facts cần giữ và boundary về ngày giao.

### Level 1 — Một phần

```text
Rewrite the email professionally in under 150 words for a client.
```

Goal/output/audience rõ hơn nhưng chưa bảo vệ facts hoặc xử lý delivery date chưa xác nhận.

### Level 2 — Đạt

```text
Rewrite this project-status email for a client in a calm, professional tone under 150 words. Keep confirmed facts and dates unchanged. Do not promise a delivery date unless the source email explicitly confirms it.
```

Có thể thực hiện và kiểm được.

---

## Rubric / Cách chấm

Mỗi task spec tối đa 2 điểm:

- `0`: vẫn mơ hồ hoặc thiếu thành phần cốt lõi khiến hệ thống phải đoán.
- `1`: làm được nhưng thiếu context/output/boundary/verification quan trọng.
- `2`: goal rõ, context liên quan, output kiểm được, boundaries phù hợp và verification có ý nghĩa.

### PASS M01

- nộp đủ **5/5** task spec;
- ít nhất **4/5** đạt `2`;
- task còn lại ít nhất `1`;
- ít nhất một task đã được chạy thật và có response + verification evidence;
- không có lỗi nghiêm trọng như yêu cầu AI tự xác nhận sự thật bằng lời của chính nó, bịa missing data hoặc bỏ boundary cho hành động khó hoàn tác.

Nếu chưa PASS: xác định đúng criterion thiếu, quay lại bài M01 tương ứng, làm một task tương đương mới và lưu lần đánh giá lại.

## English checkpoint / Kiểm tra tiếng Anh

Bạn cần:

- nhận ra ít nhất 4/5 từ: `goal`, `context`, `boundary`, `iteration`, `verification`;
- giải thích đúng ít nhất 3 từ bằng tiếng Việt;
- tự viết ít nhất một instruction tiếng Anh có nghĩa đúng, ví dụ `Do not invent missing information.`
