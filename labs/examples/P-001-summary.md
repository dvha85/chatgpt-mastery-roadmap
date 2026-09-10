# P-001 — Summary Lab / Lab tóm tắt

> **Skills / Kỹ năng:** task specification, output contract, grounding, verification  
> **Input:** [Dataset A in sample-brief.md](../data/sample-brief.md#dataset-a--meeting-notes-for-summary--ghi-chú-họp-để-tóm-tắt)  
> **Expected time / Thời lượng:** 25–40 minutes  
> **Data:** synthetic / giả lập

## Goal / Mục tiêu

Biến một prompt tóm tắt mơ hồ thành prompt có thể kiểm được, sau đó đối chiếu output với ground truth thay vì chỉ đánh giá “nghe có vẻ đúng”.

## 1. Baseline prompt — Prompt ban đầu

```text
Summarize these meeting notes.
```

### Why it is weak — Vì sao còn yếu

Prompt chưa nói:

- ai sẽ đọc summary;
- thông tin nào cần ưu tiên;
- format mong muốn;
- có được thêm suy luận hay không.

## 2. Supplied weak output — Output yếu được cung cấp sẵn

> Dùng output cố định này để bài tập tái lập được. Không cần chờ model tự sinh đúng lỗi.

```text
The team is preparing a four-page bilingual freelancer website and plans to launch next Friday. Home and About are approved. The Contact form is ready for launch. The team will buy one of three available domains this week and may add a blog after launch.
```

## 3. Diagnose — Chẩn đoán

Đối chiếu với Dataset A:

| Claim | Ground truth | Result |
|---|---|---|
| four-page website | four pages confirmed | SUPPORTED |
| launch next Friday | no date approved | UNSUPPORTED |
| Home approved | Home approved | SUPPORTED |
| About approved | About not reviewed | WRONG |
| Contact ready for launch | mobile test not done | WRONG / OVERSTATED |
| three available domains | only shortlist three names is planned | UNSUPPORTED |
| may add a blog after launch | no blog in v1; future blog not stated | UNSUPPORTED |

**Lesson / Bài học:** summary ngắn vẫn có thể chứa hallucination hoặc overstatement nếu prompt không bảo vệ source boundaries và người dùng không verify.

## 4. Improved task specification — Task spec cải thiện

```text
Goal: Summarize the meeting notes for the project owner.
Context: The owner needs decisions, current status, risks, and next steps.
Output: Use exactly four sections: Decisions, Status, Risks, Next steps. Use concise bullets.
Boundaries: Use only information explicitly present in the notes. Do not invent dates, approvals, owners, or future plans. Mark missing information as Unknown when relevant.
Verification: After the summary, provide a short checklist confirming that every bullet can be traced to the source notes.
```

## 5. Reference result — Kết quả tham chiếu

```text
Decisions
- Version 1 will include Home, Services, About and Contact.
- Vietnamese is the main language; Home will include a short English summary.
- Version 1 will not include a blog.

Status
- Home draft is approved.
- Services needs its pricing example rewritten.
- About has a first draft but has not been reviewed.
- Contact exists but has not been tested on mobile.
- No domain has been purchased and no launch date is approved.

Risks
- A preferred domain may be unavailable.
- The Contact form could be published without mobile testing.

Next steps
- Revise the Services pricing example.
- Review About.
- Shortlist three domain names.
- Test Contact on mobile before launch.
```

## 6. Verification — Kiểm chứng

Use the ground-truth block in Dataset A.

### Checklist

- [ ] Four v1 pages are correct.
- [ ] Language decision is correct.
- [ ] No-blog decision is preserved.
- [ ] Home/About/Contact statuses are not overstated.
- [ ] No launch date is invented.
- [ ] No domain purchase/availability is invented.
- [ ] All four next steps are represented.
- [ ] Both listed risks are represented.

## 7. What changed quality most? — Điều gì cải thiện chất lượng nhiều nhất?

1. **Priority / ưu tiên:** decisions/status/risks/next steps thay vì “summarize everything”.
2. **Output contract / hợp đồng đầu ra:** bốn section cố định.
3. **Boundary / ranh giới:** chỉ dùng source notes, không bịa missing facts.
4. **Verification:** checklist ánh xạ về ground truth.

## 8. Guided variation — Biến thể có hướng dẫn

Giữ Dataset A nhưng viết prompt cho một **team member** thay vì project owner. Output phải chỉ có:

- My next actions
- Decisions I should know
- Open questions

Không được tự gán owner cho task nếu notes không nêu owner.

## 9. Self practice — Bài tự làm

Không nhìn reference prompt. Viết lại một prompt mới có:

- Goal
- Context
- Output
- Boundaries
- Verification

Sau đó chạy prompt và chấm output theo checklist ở mục 6.

## 10. Rubric — Chấm điểm 0–2

| Criterion | 0 | 1 | 2 |
|---|---|---|---|
| Goal & audience | mơ hồ | có task nhưng audience/priority chưa rõ | task, audience và priority rõ |
| Output contract | không có | có format chung | section/structure kiểm được |
| Grounding boundary | cho phép đoán | cảnh báo chung | chỉ source data + xử lý Unknown rõ |
| Verification | không kiểm | “double-check” chung | checklist/ground-truth comparison cụ thể |
| Result quality | có lỗi nghiêm trọng | cơ bản đúng nhưng thiếu/overstate | facts đúng, đủ trọng tâm, không bịa |

**PASS lab:** ít nhất 8/10, không criterion nào 0.

## 11. Evidence to save — Evidence cần lưu

- baseline prompt;
- lỗi tìm thấy trong supplied weak output;
- improved prompt;
- output của bạn;
- checklist verification;
- score và một reflection: `What instruction reduced the biggest error?`

## Reusable lesson — Bài học tái sử dụng

> For source-bound summaries, specify what matters, define the output shape, forbid unsupported additions, and verify against the source.  
> Với tóm tắt dựa trên nguồn, hãy nêu thông tin ưu tiên, định dạng, cấm thêm dữ kiện không có nguồn và kiểm lại với nguồn gốc.
