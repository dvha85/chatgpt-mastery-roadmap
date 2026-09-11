# P-001 — Summary Lab / Lab tóm tắt

> **Skills / Kỹ năng:** task specification, output contract, grounding, verification  
> **Input:** [Dataset A in sample-brief.md](../data/sample-brief.md#dataset-a--meeting-notes-for-summary--ghi-chú-họp-để-tóm-tắt)  
> **Expected time / Thời lượng:** 25–40 minutes  
> **Data:** synthetic / giả lập

> **Ngôn ngữ vận hành:** prompt và output tham chiếu dùng tiếng Việt. Thuật ngữ kỹ thuật tiếng Anh được giữ khi hữu ích.

## Goal / Mục tiêu
Biến một prompt tóm tắt mơ hồ thành prompt có thể kiểm được, sau đó đối chiếu output với ground truth thay vì chỉ đánh giá “nghe có vẻ đúng”.

## 1. Baseline prompt — Prompt ban đầu

```text
Hãy tóm tắt ghi chú cuộc họp này bằng tiếng Việt.
```

### Why it is weak — Vì sao còn yếu
Prompt chưa nói ai sẽ đọc summary, thông tin nào cần ưu tiên, format mong muốn và có được thêm suy luận hay không.

## 2. Supplied weak output — Output yếu được cung cấp sẵn

```text
Nhóm đang chuẩn bị một website freelancer song ngữ gồm bốn trang và dự định ra mắt vào thứ Sáu tuần tới. Home và About đã được duyệt. Form Contact đã sẵn sàng để ra mắt. Nhóm sẽ mua một trong ba domain còn trống trong tuần này và có thể thêm blog sau khi ra mắt.
```

## 3. Diagnose — Chẩn đoán

| Claim | Ground truth | Result |
|---|---|---|
| website bốn trang | four pages confirmed | SUPPORTED |
| ra mắt thứ Sáu tuần tới | no date approved | UNSUPPORTED |
| Home đã duyệt | Home approved | SUPPORTED |
| About đã duyệt | About not reviewed | WRONG |
| Contact sẵn sàng ra mắt | mobile test not done | WRONG / OVERSTATED |
| ba domain còn trống | only shortlist three names is planned | UNSUPPORTED |
| có thể thêm blog sau launch | no blog in v1; future blog not stated | UNSUPPORTED |

## 4. Improved task specification — Task spec cải thiện

```text
Mục tiêu: Tóm tắt ghi chú cuộc họp cho chủ dự án.
Ngữ cảnh: Người đọc cần quyết định, trạng thái hiện tại, rủi ro và việc tiếp theo.
Đầu ra: Dùng đúng bốn phần: Quyết định, Trạng thái, Rủi ro, Việc tiếp theo. Dùng bullet ngắn gọn.
Ranh giới: Chỉ dùng thông tin xuất hiện rõ trong ghi chú. Không tự tạo ngày, trạng thái phê duyệt, owner hoặc kế hoạch tương lai. Khi thông tin quan trọng còn thiếu, ghi “Chưa xác định”.
Kiểm chứng: Sau phần tóm tắt, thêm checklist ngắn xác nhận mỗi bullet đều có thể truy ngược về ghi chú nguồn.
Ngôn ngữ đầu ra: Tiếng Việt.
```

## 5. Reference result — Kết quả tham chiếu

```text
Quyết định
- Version 1 gồm Home, Services, About và Contact.
- Tiếng Việt là ngôn ngữ chính; Home có một phần tóm tắt tiếng Anh ngắn.
- Version 1 không có blog.

Trạng thái
- Bản nháp Home đã được duyệt.
- Services cần viết lại ví dụ về giá.
- About có bản nháp đầu tiên nhưng chưa được review.
- Contact đã có nhưng chưa test trên mobile.
- Chưa mua domain và chưa có ngày launch được duyệt.

Rủi ro
- Domain ưu tiên có thể không còn khả dụng.
- Contact form có thể được publish trước khi test mobile.

Việc tiếp theo
- Sửa ví dụ pricing của Services.
- Review About.
- Lập shortlist ba domain.
- Test Contact trên mobile trước launch.
```

## 6. Verification — Kiểm chứng
- [ ] Bốn trang v1 đúng.
- [ ] Quyết định ngôn ngữ đúng.
- [ ] Quyết định không có blog được giữ nguyên.
- [ ] Trạng thái Home/About/Contact không bị nói quá.
- [ ] Không tự tạo launch date.
- [ ] Không tự tạo domain availability/purchase.
- [ ] Đủ bốn next steps.
- [ ] Đủ hai risks.

## 7. Guided variation — Biến thể có hướng dẫn
Giữ Dataset A nhưng viết prompt **bằng tiếng Việt** cho một team member thay vì project owner. Output chỉ có: `Việc tôi cần làm`, `Quyết định tôi cần biết`, `Câu hỏi còn mở`. Không tự gán owner nếu notes không nêu.

## 8. Self practice — Bài tự làm
Không nhìn prompt tham chiếu. Viết prompt tiếng Việt mới có Goal, Context, Output, Boundaries và Verification. Chạy prompt rồi chấm bằng checklist mục 6.

## 9. Rubric — Chấm điểm 0–2
| Criterion | 0 | 1 | 2 |
|---|---|---|---|
| Goal & audience | mơ hồ | có task nhưng audience/priority chưa rõ | task, audience và priority rõ |
| Output contract | không có | format chung | section/structure kiểm được |
| Grounding boundary | cho phép đoán | cảnh báo chung | chỉ source data + xử lý unknown rõ |
| Verification | không kiểm | “double-check” chung | checklist/ground-truth comparison cụ thể |
| Result quality | lỗi nghiêm trọng | cơ bản đúng | facts đúng, đủ trọng tâm, không bịa |

**PASS lab:** ít nhất 8/10, không criterion nào 0.

## 10. Evidence to save — Evidence cần lưu
Baseline prompt, lỗi tìm thấy, improved prompt tiếng Việt, output của bạn, checklist verification, score và reflection.

## Reusable lesson — Bài học tái sử dụng
> Với tóm tắt dựa trên nguồn, hãy nêu thông tin ưu tiên, định dạng, cấm thêm dữ kiện không có nguồn và kiểm lại với nguồn gốc.
