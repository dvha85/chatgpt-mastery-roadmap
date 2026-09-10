# Sample Brief — Dữ liệu giả lập cho Prompt Labs

> **Synthetic data / Dữ liệu giả lập.** File này không mô tả người, công ty hay sản phẩm thật. Dùng cho P-001, P-002 và P-003 để bài lab có thể làm lại và chấm theo cùng ground truth.

## Scenario / Bối cảnh

Một freelancer đang chuẩn bị website giới thiệu dịch vụ. Website v1 cần nhỏ, dễ bảo trì và đủ để khách hiểu dịch vụ rồi gửi inquiry.

### Confirmed requirements / Yêu cầu đã xác nhận

- Audience: khách hàng tiềm năng của một freelancer tại Việt Nam.
- Pages: Home, Services, About, Contact.
- Language: Vietnamese main copy; English summary on Home only.
- Must support: custom domain và contact form.
- Monthly operating budget: tối đa **$15/month**.
- Setup priority: càng đơn giản càng tốt cho người không chuyên kỹ thuật.
- Version 1: **không có blog**.

### Unknowns / Chưa biết

- Chưa chọn domain.
- Chưa có ngày launch cuối cùng được duyệt.
- Chưa biết traffic thực tế.
- Chưa có dữ liệu conversion.

---

## Dataset A — Meeting notes for summary / Ghi chú họp để tóm tắt

```text
The team agreed that version 1 will contain Home, Services, About and Contact pages. Vietnamese will be the main language, with a short English summary on Home. The Home draft is approved. The Services draft still needs one pricing example to be rewritten because the current wording could be interpreted as a fixed quote. The About page has a first draft but has not been reviewed. The Contact page exists, but the form has not been tested on mobile. The team decided not to add a blog in version 1. No domain has been purchased. A launch date was discussed, but no date was approved. The main risks are choosing an unavailable domain and publishing the contact form without testing it. Next steps are: revise the Services example, review About, shortlist three domain names, and test the Contact form on mobile before launch.
```

### Ground truth for Dataset A / Dữ kiện đối chiếu

**Decisions**
- Four pages in v1: Home, Services, About, Contact.
- Vietnamese main copy + short English Home summary.
- No blog in v1.

**Confirmed status**
- Home draft approved.
- About has a first draft but is not reviewed.
- Contact form exists but is not mobile-tested.
- No domain purchased.
- No launch date approved.

**Next steps**
- Revise Services pricing example.
- Review About.
- Shortlist three domain names.
- Test Contact form on mobile before launch.

**Risks**
- Domain availability.
- Untested mobile contact form.

Anything else is unsupported unless explicitly labeled as an assumption.

---

## Dataset B — Planning tasks / Dữ liệu lập kế hoạch

Capacity for one week: **8 hours**.

| Task | Required? | Estimate | Dependency / Ghi chú |
|---|---|---:|---|
| Revise Services pricing example | Yes | 1.0 h | none |
| Review About draft | Yes | 1.5 h | first draft already exists |
| Draft three domain candidates | Yes | 1.0 h | none |
| Check domain availability | Yes | 0.5 h | after candidates exist |
| Test Contact form on mobile | Yes | 1.5 h | form already exists |
| Fix Contact form issues | Conditional | 1.5 h | only if test finds issues |
| Polish English Home summary | Nice-to-have | 1.0 h | Home draft already approved |
| Add analytics dashboard | Nice-to-have | 2.0 h | not required for v1 |

### Planning rules / Quy tắc lập kế hoạch

- Do not exceed 8 planned hours.
- Required work has priority over nice-to-have work.
- Conditional work must not be treated as definitely required before the test result exists.
- `Check domain availability` must happen after `Draft three domain candidates`.
- Do not invent a launch deadline.
- If all useful work cannot fit, show what is deferred and why.

### Checkable facts / Dữ kiện có thể kiểm

- All definitely required tasks excluding conditional fixes total **5.5 hours**.
- Adding `Polish English Home summary` produces **6.5 hours**.
- Adding `Add analytics dashboard` as well produces **8.5 hours**, which exceeds capacity.

---

## Dataset C — Fictional website options / Bảng lựa chọn giả lập

> Các option dưới đây là hư cấu. Không dùng bảng này để đưa ra quyết định mua sản phẩm thật.

| Field | Pine | Maple | Cedar |
|---|---|---|---|
| Monthly cost | $9 | $14 | Unknown |
| Custom domain | Yes | Yes | Yes |
| Contact form | Yes | Yes | Unknown |
| Setup difficulty | Low | Medium | Low |
| Maintenance | Low | Medium | Low |
| Vietnamese content | Manual content entry | Manual content entry | Manual content entry |
| English Home summary | Supported as normal page content | Supported as normal page content | Supported as normal page content |
| Blog required for v1 | No | No | No |

### Comparison rules / Quy tắc so sánh

The decision criteria are:

1. monthly cost must be at or below $15;
2. custom domain is required;
3. contact form is required;
4. lower setup difficulty is preferred;
5. lower maintenance is preferred.

### Ground truth / Dữ kiện đối chiếu

- Pine satisfies every confirmed requirement in the table and costs $9/month.
- Maple satisfies every confirmed requirement in the table and costs $14/month, but setup and maintenance are Medium.
- Cedar cannot be confirmed as eligible because monthly cost and contact-form support are Unknown.
- It is incorrect to invent Cedar's missing values.

---

## Safety and evidence rule — Quy tắc an toàn và evidence

When saving learner evidence:

- copy only this synthetic data or other data you are allowed to share;
- do not add real email addresses, passwords, tokens, payment details or client information;
- mark unsupported claims as `UNKNOWN`, `UNSUPPORTED` or `ASSUMPTION` instead of filling the gap by guessing.
