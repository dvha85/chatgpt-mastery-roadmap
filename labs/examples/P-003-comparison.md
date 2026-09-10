# P-003 — Comparison Lab / Lab so sánh

> **Skills / Kỹ năng:** output contract, unknown handling, decision criteria, evidence-based recommendation  
> **Input:** [Dataset C in sample-brief.md](../data/sample-brief.md#dataset-c--fictional-website-options--bảng-lựa-chọn-giả-lập)  
> **Expected time / Thời lượng:** 30–45 minutes  
> **Data:** synthetic / giả lập

## Goal / Mục tiêu

So sánh nhiều lựa chọn từ một bảng dữ liệu đóng, xử lý dữ kiện thiếu đúng cách và đưa ra recommendation dựa trên criteria thay vì tự điền phần Unknown.

## 1. Baseline prompt — Prompt ban đầu

```text
Which website option is best?
```

### Why it is weak — Vì sao còn yếu

Prompt chưa nêu:

- “best” theo tiêu chí nào;
- dữ liệu nào được phép dùng;
- cách xử lý Unknown;
- output structure;
- cách chứng minh recommendation.

## 2. Supplied weak output — Output yếu được cung cấp sẵn

```text
Cedar is the best choice. It costs about $10/month, supports a contact form, and has low setup and maintenance. Pine is cheaper but less flexible, while Maple is too expensive for the budget.
```

## 3. Diagnose — Chẩn đoán

Đối chiếu Dataset C:

- Cedar cost = **Unknown**, không phải $10.
- Cedar contact form = **Unknown**, không thể nói supports.
- Pine “less flexible” không có trong dataset.
- Maple = $14/month, vẫn **<= $15 budget**, nên nói “too expensive for the budget” là sai.

Output đã biến unknown thành facts và thêm một criteria không có trong dữ liệu.

## 4. Improved task specification — Task spec cải thiện

```text
Goal: Compare Pine, Maple, and Cedar for the freelancer website requirements in the supplied table.
Context: Monthly cost must be <= $15, custom domain and contact form are required, and lower setup difficulty and maintenance are preferred.
Output: Return a table with Option, Budget fit, Custom domain, Contact form, Setup difficulty, Maintenance, Eligibility status, and Evidence note. Then recommend one option in no more than four bullets.
Boundaries: Use only the supplied dataset. Do not infer or estimate Unknown values. If a required field is Unknown, mark the option as Not yet confirmed rather than Pass.
Verification: For the recommendation, cite the exact dataset fields that satisfy each required criterion and list any unresolved unknowns.
```

## 5. Reference result — Kết quả tham chiếu

| Option | Budget fit | Custom domain | Contact form | Setup | Maintenance | Eligibility | Evidence note |
|---|---|---|---|---|---|---|---|
| Pine | Yes ($9) | Yes | Yes | Low | Low | PASS | All required fields confirmed |
| Maple | Yes ($14) | Yes | Yes | Medium | Medium | PASS | Meets requirements, less preferred on setup/maintenance |
| Cedar | Unknown | Yes | Unknown | Low | Low | NOT YET CONFIRMED | Required cost/contact-form evidence missing |

### Recommendation / Khuyến nghị

- **Pine** is the strongest choice from the supplied data.
- It is within budget at $9/month.
- Custom domain and contact form are both confirmed.
- Setup and maintenance are both Low; Cedar cannot be fairly selected until its Unknown required fields are resolved.

## 6. Verification — Kiểm chứng

### Evidence map

| Criterion | Pine | Maple | Cedar |
|---|---|---|---|
| <= $15/month | PASS | PASS | UNKNOWN |
| Custom domain | PASS | PASS | PASS |
| Contact form | PASS | PASS | UNKNOWN |
| Low setup preferred | PASS | Medium | PASS |
| Low maintenance preferred | PASS | Medium | PASS |

### Checks

- [ ] No Unknown field became a numeric or Yes/No fact.
- [ ] Maple is not rejected for budget because $14 <= $15.
- [ ] Recommendation uses only stated criteria.
- [ ] Eligibility and preference are kept separate.
- [ ] Missing evidence is visible instead of hidden.

## 7. Key distinction — Phân biệt quan trọng

**Eligibility / đủ điều kiện** khác **preference / mức ưu tiên**.

Ví dụ:

- Maple **eligible** vì đáp ứng requirement bắt buộc.
- Pine **preferred** vì setup/maintenance thấp hơn theo criteria đã cho.
- Cedar chưa thể xác nhận eligible vì thiếu hai required fields.

Nếu không tách hai khái niệm này, model dễ biến “không tối ưu” thành “không hợp lệ”.

## 8. Guided practice — Bài có hướng dẫn

Thay criteria ưu tiên thành:

```text
Among eligible options, lower monthly cost is the only preference. Ignore setup and maintenance when ranking eligible options.
```

Hãy dự đoán recommendation có thay đổi không và vì sao.

## 9. Self practice — Bài tự làm

Viết prompt riêng để:

1. so sánh ba option;
2. đánh dấu PASS / FAIL / UNKNOWN từng requirement;
3. recommend một option;
4. tạo danh sách câu hỏi cần trả lời trước khi Cedar có thể được xem xét công bằng.

Sau đó kiểm lại với Dataset C.

## 10. Rubric — Chấm điểm 0–2

| Criterion | 0 | 1 | 2 |
|---|---|---|---|
| Criteria clarity | “best” mơ hồ | có vài criteria | mandatory vs preferred rõ |
| Unknown handling | tự bịa | đánh dấu thiếu nhưng vẫn suy đoán | Unknown giữ nguyên và ảnh hưởng eligibility đúng |
| Output contract | narrative khó kiểm | có bảng nhưng thiếu status | bảng cho phép đối chiếu từng criterion |
| Evidence mapping | recommendation không có evidence | giải thích chung | map từng requirement về dataset |
| Recommendation | sai/unsupported | hợp lý nhưng thiếu nuance | đúng dữ liệu, nêu trade-off/unknown rõ |

**PASS lab:** >=8/10 và Unknown handling không được 0.

## 11. Evidence to save — Evidence cần lưu

- baseline prompt;
- ít nhất ba lỗi tìm được trong supplied weak output;
- improved prompt;
- comparison table của bạn;
- evidence map;
- recommendation + unresolved unknowns;
- score và reflection.

## Reusable lesson — Bài học tái sử dụng

> Missing data is information. Do not replace it with a guess just to make the comparison look complete.  
> Dữ liệu bị thiếu chính là một thông tin cần giữ lại; đừng biến nó thành suy đoán chỉ để bảng trông đầy đủ.
