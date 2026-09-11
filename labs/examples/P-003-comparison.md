# P-003 — Comparison Lab / Lab so sánh

> **Skills / Kỹ năng:** output contract, unknown handling, decision criteria, evidence-based recommendation  
> **Input:** [Dataset C in sample-brief.md](../data/sample-brief.md#dataset-c--fictional-website-options--bảng-lựa-chọn-giả-lập)  
> **Expected time / Thời lượng:** 30–45 minutes  
> **Data:** synthetic / giả lập

> **Ngôn ngữ vận hành:** prompt và recommendation thực hành dùng tiếng Việt làm bản chính.

## Goal / Mục tiêu
So sánh nhiều lựa chọn từ bảng dữ liệu đóng, xử lý dữ kiện thiếu đúng cách và đưa ra recommendation dựa trên criteria thay vì tự điền phần Unknown.

## 1. Baseline prompt — Prompt ban đầu

```text
Lựa chọn website nào tốt nhất? Trả lời bằng tiếng Việt.
```

### Why it is weak — Vì sao còn yếu
Chưa nêu “best” theo tiêu chí nào, dữ liệu nào được dùng, cách xử lý Unknown, output structure và cách chứng minh recommendation.

## 2. Supplied weak output — Output yếu được cung cấp sẵn

```text
Cedar là lựa chọn tốt nhất. Nó có giá khoảng $10/tháng, hỗ trợ contact form và có mức thiết lập/bảo trì thấp. Pine rẻ hơn nhưng kém linh hoạt hơn, còn Maple quá đắt so với ngân sách.
```

## 3. Diagnose — Chẩn đoán
- Cedar cost = **Unknown**, không phải $10.
- Cedar contact form = **Unknown**, không thể nói supports.
- Pine “kém linh hoạt hơn” không có trong dataset.
- Maple = $14/month, vẫn **<= $15 budget**, nên nói “quá đắt” là sai.

## 4. Improved task specification — Task spec cải thiện

```text
Mục tiêu: So sánh Pine, Maple và Cedar theo yêu cầu website freelancer trong bảng dữ liệu đã cung cấp.
Ngữ cảnh: Chi phí hàng tháng phải <= $15; custom domain và contact form là bắt buộc; ưu tiên setup difficulty và maintenance thấp hơn.
Đầu ra: Trả bảng gồm Lựa chọn | Đạt ngân sách | Custom domain | Contact form | Độ khó thiết lập | Maintenance | Trạng thái đủ điều kiện | Ghi chú bằng chứng. Sau bảng, khuyến nghị một lựa chọn trong tối đa 4 bullet.
Ranh giới: Chỉ dùng dataset được cung cấp. Không suy luận hoặc ước tính giá trị Unknown. Nếu một trường bắt buộc là Unknown, đánh dấu “Chưa xác nhận” thay vì PASS.
Kiểm chứng: Với khuyến nghị, chỉ rõ field nào trong dataset đáp ứng từng tiêu chí bắt buộc và liệt kê unknown chưa giải quyết.
Ngôn ngữ đầu ra: Tiếng Việt.
```

## 5. Reference result — Kết quả tham chiếu

| Option | Budget fit | Custom domain | Contact form | Setup | Maintenance | Eligibility | Evidence note |
|---|---|---|---|---|---|---|---|
| Pine | Yes ($9) | Yes | Yes | Low | Low | PASS | All required fields confirmed |
| Maple | Yes ($14) | Yes | Yes | Medium | Medium | PASS | Meets requirements, lower preference on setup/maintenance |
| Cedar | Unknown | Yes | Unknown | Low | Low | NOT YET CONFIRMED | Required cost/contact-form evidence missing |

### Khuyến nghị
- **Pine** là lựa chọn mạnh nhất từ dữ liệu đã cung cấp.
- Giá $9/tháng nằm trong ngân sách.
- Custom domain và contact form đều được xác nhận.
- Setup và maintenance đều Low; chưa thể chọn Cedar công bằng cho đến khi giải quyết các trường bắt buộc còn Unknown.

## 6. Verification — Kiểm chứng

| Criterion | Pine | Maple | Cedar |
|---|---|---|---|
| <= $15/month | PASS | PASS | UNKNOWN |
| Custom domain | PASS | PASS | PASS |
| Contact form | PASS | PASS | UNKNOWN |
| Low setup preferred | PASS | Medium | PASS |
| Low maintenance preferred | PASS | Medium | PASS |

Checklist:
- [ ] Không có Unknown nào biến thành số hoặc Yes/No tự tạo.
- [ ] Maple không bị loại vì budget: $14 <= $15.
- [ ] Recommendation chỉ dùng criteria đã nêu.
- [ ] Eligibility và preference được tách riêng.
- [ ] Missing evidence được hiển thị rõ.

## 7. Key distinction — Phân biệt quan trọng
**Eligibility / đủ điều kiện** khác **preference / mức ưu tiên**.
- Maple eligible vì đáp ứng requirement bắt buộc.
- Pine preferred vì setup/maintenance thấp hơn.
- Cedar chưa xác nhận eligible vì thiếu hai required fields.

## 8. Guided practice — Bài có hướng dẫn

```text
Trong các lựa chọn đủ điều kiện, chỉ dùng chi phí hàng tháng thấp hơn làm tiêu chí ưu tiên. Bỏ qua setup và maintenance khi xếp hạng các lựa chọn đủ điều kiện. Trả lời bằng tiếng Việt và giải thích vì sao recommendation có hoặc không thay đổi.
```

## 9. Self practice — Bài tự làm
Viết prompt tiếng Việt để:
1. so sánh ba option;
2. đánh dấu PASS / FAIL / UNKNOWN từng requirement;
3. recommend một option;
4. tạo danh sách câu hỏi cần trả lời trước khi Cedar được xem xét công bằng.

Sau đó kiểm lại với Dataset C.

## 10. Rubric — Chấm điểm 0–2
| Criterion | 0 | 1 | 2 |
|---|---|---|---|
| Criteria clarity | “best” mơ hồ | có vài criteria | mandatory vs preferred rõ |
| Unknown handling | tự bịa | đánh dấu thiếu nhưng vẫn suy đoán | Unknown giữ nguyên và ảnh hưởng eligibility đúng |
| Output contract | narrative khó kiểm | bảng thiếu status | bảng cho phép đối chiếu từng criterion |
| Evidence mapping | recommendation không evidence | giải thích chung | map từng requirement về dataset |
| Recommendation | sai/unsupported | hợp lý nhưng thiếu nuance | đúng dữ liệu, nêu trade-off/unknown rõ |

**PASS lab:** >=8/10 và Unknown handling không được 0.

## 11. Evidence to save — Evidence cần lưu
Baseline prompt, ít nhất ba lỗi trong weak output, improved prompt tiếng Việt, comparison table, evidence map, recommendation + unresolved unknowns, score và reflection.

## Reusable lesson — Bài học tái sử dụng
> Dữ liệu bị thiếu chính là một thông tin cần giữ lại; đừng biến nó thành suy đoán chỉ để bảng trông đầy đủ.
