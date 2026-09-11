# P-002 — Planning Lab / Lab lập kế hoạch

> **Skills / Kỹ năng:** decomposition, constraints, arithmetic verification, prioritization  
> **Input:** [Dataset B in sample-brief.md](../data/sample-brief.md#dataset-b--planning-tasks--dữ-liệu-lập-kế-hoạch)  
> **Expected time / Thời lượng:** 30–45 minutes  
> **Data:** synthetic / giả lập

> **Ngôn ngữ vận hành:** prompt và phần thực hành dùng tiếng Việt làm bản chính.

## Goal / Mục tiêu
Học cách giao một bài toán lập kế hoạch có giới hạn thời gian, dependency và task conditional; sau đó kiểm tổng thời lượng bằng phép cộng thay vì tin vào narrative.

## 1. Baseline prompt — Prompt ban đầu

```text
Hãy lập kế hoạch công việc website cho tuần này. Trả lời bằng tiếng Việt.
```

### Why it is weak — Vì sao còn yếu
Prompt không cho biết tổng capacity, task bắt buộc, dependency, conditional work, cách xử lý khi thiếu thời gian hoặc cách kiểm tổng giờ.

## 2. Supplied weak output — Output yếu được cung cấp sẵn

```text
Tuần này:
1. Sửa ví dụ pricing của Services — 1h
2. Review bản nháp About — 1.5h
3. Soạn danh sách domain — 1h
4. Kiểm tra domain availability — 0.5h
5. Test Contact form trên mobile — 1.5h
6. Sửa lỗi Contact form — 1.5h
7. Hoàn thiện English Home summary — 1h
8. Thêm analytics dashboard — 2h
Tổng: 8 giờ
```

Tính lại: `1 + 1.5 + 1 + 0.5 + 1.5 + 1.5 + 1 + 2 = 10 giờ`.

Ba lỗi chính: tổng sai; coi conditional fix là chắc chắn; ưu tiên nice-to-have dù capacity không đủ.

## 3. Improved task specification — Task spec cải thiện

```text
Mục tiêu: Tạo kế hoạch thực thi một tuần từ bảng task tôi cung cấp.
Ngữ cảnh: Tổng capacity là 8 giờ. Công việc bắt buộc ưu tiên hơn nice-to-have. Một số task có dependency hoặc chỉ thực hiện khi condition xảy ra.
Đầu ra: Bảng gồm Thứ tự | Task | Giờ dự kiến | Vì sao làm lúc này | Dependency | Trạng thái (Bắt buộc / Có điều kiện / Nice-to-have). Sau bảng, ghi Tổng giờ đã xếp và Công việc hoãn.
Ranh giới: Không vượt quá 8 giờ đã xếp chắc chắn. Không coi conditional work là bắt buộc trước khi trigger xảy ra. Không tự tạo launch deadline.
Kiểm chứng: Hiển thị phép cộng tổng giờ và kiểm từng dependency.
Ngôn ngữ đầu ra: Tiếng Việt.
```

## 4. Reference result — Kết quả tham chiếu

| Thứ tự | Task | Giờ | Vì sao lúc này | Dependency | Trạng thái |
|---:|---|---:|---|---|---|
| 1 | Sửa Services pricing example | 1.0 | bắt buộc | none | Bắt buộc |
| 2 | Review About draft | 1.5 | bắt buộc | draft exists | Bắt buộc |
| 3 | Soạn ba domain candidates | 1.0 | bắt buộc | none | Bắt buộc |
| 4 | Kiểm domain availability | 0.5 | bắt buộc | sau domain candidates | Bắt buộc |
| 5 | Test Contact trên mobile | 1.5 | bắt buộc | form exists | Bắt buộc |
| 6 | Hoàn thiện English Home summary | 1.0 | còn capacity | Home exists | Nice-to-have |

```text
Tổng đã xếp = 1 + 1.5 + 1 + 0.5 + 1.5 + 1 = 6.5 giờ
Capacity còn lại = 1.5 giờ
```

**Chưa xếp chắc chắn:**
- Fix Contact form — conditional, chỉ làm nếu test phát hiện lỗi; có thể giữ buffer tối đa 1.5h.
- Analytics dashboard — nice-to-have 2h; hoãn vì không bắt buộc cho v1.

## 5. Verification — Kiểm chứng
- [ ] Planned definite work <= 8h.
- [ ] Required tasks đứng trước optional work.
- [ ] Domain availability sau domain candidates.
- [ ] Conditional fix không bị coi là guaranteed.
- [ ] Không tự tạo launch deadline.
- [ ] Tổng giờ có phép cộng rõ.

Ground truth: required work = **5.5h**; required + English polish = **6.5h**; thêm analytics = **8.5h** nên vượt capacity.

## 6. Decomposition lesson — Bài học chia tác vụ

**Bước 1 — dùng trực tiếp**
```text
Trước tiên hãy kiểm bảng task để xác định dependency, conditional task và tổng giờ. Chưa lập lịch. Trả lời bằng tiếng Việt.
```

**Bước 2 — dùng trực tiếp**
```text
Dùng inventory đã kiểm ở bước trước để tạo kế hoạch trong giới hạn 8 giờ và ghi rõ phần bị hoãn. Hiển thị phép cộng tổng giờ. Trả lời bằng tiếng Việt.
```

## 7. Guided practice — Bài có hướng dẫn

```text
Hãy giữ lại 1.5 giờ chưa phân bổ làm risk buffer cho khả năng phải sửa Contact form. Không dùng buffer cho task khác nếu trigger chưa xảy ra. Trả lời bằng tiếng Việt.
```

Kiểm required tasks, tổng giờ chắc chắn và buffer.

## 8. Self practice — Bài tự làm
Viết prompt riêng bằng tiếng Việt rồi yêu cầu ChatGPT tạo plan từ Dataset B. Sau response: cộng lại giờ; kiểm dependency; đánh dấu `Bắt buộc / Có điều kiện / Nice-to-have`; ghi ít nhất một lỗi hoặc điểm tốt.

## 9. Rubric — Chấm điểm 0–2
| Criterion | 0 | 1 | 2 |
|---|---|---|---|
| Goal & constraints | thiếu capacity/priority | có nhưng chưa đủ | capacity, priority và rule rõ |
| Dependency handling | vi phạm | nhận biết một phần | dependency đúng và kiểm được |
| Conditional work | coi là chắc chắn | có ghi nhưng mơ hồ | xử lý trigger/buffer đúng |
| Arithmetic verification | không tính/tính sai | có total nhưng chưa show check | phép cộng rõ và đúng |
| Plan quality | vượt 8h/bỏ required | cơ bản dùng được | hợp lý, <=8h, deferred rõ |

**PASS lab:** >=8/10 và Arithmetic verification không được 0.

## 10. Evidence to save — Evidence cần lưu
Baseline prompt, lỗi output yếu, improved prompt tiếng Việt, plan, phép cộng kiểm chứng, dependency/conditional check, score và reflection.

## Reusable lesson — Bài học tái sử dụng
> Một kế hoạch chưa được kiểm chứng nếu constraints và phép tính chưa được kiểm riêng khỏi phần diễn giải.
