# P-002 — Planning Lab / Lab lập kế hoạch

> **Skills / Kỹ năng:** decomposition, constraints, arithmetic verification, prioritization  
> **Input:** [Dataset B in sample-brief.md](../data/sample-brief.md#dataset-b--planning-tasks--dữ-liệu-lập-kế-hoạch)  
> **Expected time / Thời lượng:** 30–45 minutes  
> **Data:** synthetic / giả lập

## Goal / Mục tiêu

Học cách giao một bài toán lập kế hoạch có giới hạn thời gian, dependency và task conditional; sau đó kiểm tổng thời lượng bằng phép cộng thay vì tin vào narrative.

## 1. Baseline prompt — Prompt ban đầu

```text
Plan my website work for this week.
```

### Why it is weak — Vì sao còn yếu

Prompt không cho biết:

- tổng capacity;
- task nào bắt buộc;
- dependency;
- conditional work;
- cách xử lý khi không đủ thời gian;
- cách kiểm tổng giờ.

## 2. Supplied weak output — Output yếu được cung cấp sẵn

```text
This week:
1. Revise Services pricing example — 1h
2. Review About draft — 1.5h
3. Draft domain candidates — 1h
4. Check domain availability — 0.5h
5. Test Contact form on mobile — 1.5h
6. Fix Contact form issues — 1.5h
7. Polish English Home summary — 1h
8. Add analytics dashboard — 2h
Total: 8 hours
```

## 3. Diagnose — Chẩn đoán

Tính lại:

```text
1 + 1.5 + 1 + 0.5 + 1.5 + 1.5 + 1 + 2 = 10 hours
```

Output có ba lỗi chính:

1. ghi tổng **8h** nhưng thực tế **10h**;
2. đưa `Fix Contact form issues` thành task chắc chắn dù nó chỉ conditional sau khi test;
3. ưu tiên analytics nice-to-have dù capacity không đủ.

## 4. Improved task specification — Task spec cải thiện

```text
Goal: Create a one-week execution plan using the task table I provide.
Context: Total capacity is 8 hours. Required work has priority over nice-to-have work. Some tasks have dependencies or are conditional.
Output: Return a table with Order, Task, Planned hours, Why now, Dependency, and Status (Required / Conditional / Nice-to-have). Then show Total planned hours and Deferred work.
Boundaries: Do not exceed 8 planned hours. Do not treat conditional work as definitely required before its trigger happens. Do not invent a launch deadline.
Verification: Show the arithmetic for total planned hours and check that every dependency is respected.
```

## 5. Reference result — Kết quả tham chiếu

Một đáp án hợp lệ:

| Order | Task | Hours | Why now | Dependency | Status |
|---:|---|---:|---|---|---|
| 1 | Revise Services pricing example | 1.0 | required | none | Required |
| 2 | Review About draft | 1.5 | required | draft exists | Required |
| 3 | Draft three domain candidates | 1.0 | required | none | Required |
| 4 | Check domain availability | 0.5 | required | after domain candidates | Required |
| 5 | Test Contact form on mobile | 1.5 | required | form exists | Required |
| 6 | Polish English Home summary | 1.0 | fits remaining capacity | Home exists | Nice-to-have |

```text
Total planned = 1 + 1.5 + 1 + 0.5 + 1.5 + 1 = 6.5 hours
Remaining capacity = 1.5 hours
```

**Deferred / Chưa xếp chắc chắn**

- Fix Contact form issues — conditional, only if testing finds issues; reserve up to 1.5h if needed.
- Add analytics dashboard — nice-to-have, 2h; defer because it is not required for v1 and would exceed the remaining confirmed capacity.

### Important nuance — Điểm cần hiểu

Có nhiều plan hợp lệ. Ví dụ có thể giữ **1.5h buffer** cho conditional fixes thay vì dùng 1h để polish English. Rubric đánh giá logic và constraints, không bắt người học giống reference result từng dòng.

## 6. Verification — Kiểm chứng

### Constraint checks

- [ ] Planned definite work <= 8h.
- [ ] Required tasks are included before optional work.
- [ ] Domain availability comes after domain candidates.
- [ ] Conditional fix is not presented as guaranteed work before testing.
- [ ] No launch deadline is invented.
- [ ] Total hours are shown with arithmetic.

### Ground-truth arithmetic

- Definitely required work = **5.5h**.
- Required + English polish = **6.5h**.
- Required + English polish + analytics = **8.5h**, so that combination violates capacity.

## 7. Decomposition lesson — Bài học về chia việc

Planning tasks thường thất bại khi model phải cùng lúc:

1. hiểu task table;
2. xác định dependencies;
3. phân loại required/conditional/optional;
4. ưu tiên;
5. tính tổng giờ;
6. viết narrative.

Bạn có thể chia thành hai lượt:

```text
Step 1: Check the task table for dependencies, conditional tasks, and total hours. Do not make a schedule yet.
```

Sau khi kiểm đúng:

```text
Step 2: Using that checked task inventory, create the 8-hour plan and show what is deferred.
```

Đây là **decomposition / chia tác vụ**: tách việc phức tạp thành bước dễ kiểm hơn.

## 8. Guided practice — Bài có hướng dẫn

Tạo một plan khác với chiến lược:

```text
Keep 1.5 hours unallocated as a risk buffer for possible Contact-form fixes.
```

Sau đó kiểm:

- required tasks có đủ không;
- tổng giờ planned chắc chắn là bao nhiêu;
- buffer có bị model bí mật dùng cho việc khác không.

## 9. Self practice — Bài tự làm

Không xem reference result, hãy viết prompt riêng rồi yêu cầu ChatGPT tạo plan từ Dataset B.

Sau response:

1. cộng lại từng giờ bằng tay hoặc calculator;
2. đánh dấu mọi dependency;
3. đánh dấu `Required / Conditional / Nice-to-have`;
4. ghi ít nhất một lỗi hoặc một điểm tốt trong reasoning/output.

## 10. Rubric — Chấm điểm 0–2

| Criterion | 0 | 1 | 2 |
|---|---|---|---|
| Goal & constraints | thiếu capacity/priority | có nhưng chưa đủ | capacity, priority và rule rõ |
| Dependency handling | vi phạm | có nhận biết nhưng chưa chắc | dependency đúng và kiểm được |
| Conditional work | coi là chắc chắn | có ghi conditional nhưng plan mơ hồ | xử lý trigger/buffer đúng |
| Arithmetic verification | không tính / tính sai | có total nhưng không show check | phép cộng rõ và đúng |
| Plan quality | vượt 8h / bỏ required | cơ bản dùng được | hợp lý, <=8h, deferred rõ |

**PASS lab:** >=8/10 và Arithmetic verification không được 0.

## 11. Evidence to save — Evidence cần lưu

- baseline prompt;
- lỗi trong supplied weak output;
- improved prompt;
- plan của bạn;
- phép cộng kiểm chứng;
- dependency/conditional check;
- score và reflection.

## Reusable lesson — Bài học tái sử dụng

> A plan is not verified until its constraints and arithmetic are checked separately from the prose.  
> Một kế hoạch chưa được kiểm chứng nếu constraints và phép tính chưa được kiểm riêng khỏi phần diễn giải.
