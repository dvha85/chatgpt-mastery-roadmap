# M00 Check — Mental Model Practice / Bài thực hành Mental Model

> Làm sau M00.3. Bộ này gồm 10 tình huống thực hành, có đáp án và giải thích. Hãy tự làm trước, sau đó mới mở phần đáp án.

## Instructions / Hướng dẫn

Với mỗi tình huống, ghi 4 phần:

1. `Surface / Bề mặt`: Chat, Work hoặc Codex.
2. `Tools / Công cụ`: tool nào cần, nếu có.
3. `Task brief / Bản giao việc`: ít nhất Outcome + Context + Verification.
4. `Verification / Kiểm chứng`: cách bạn xác nhận kết quả.

Nếu tính năng không có trên tài khoản, ghi fallback thay vì coi đó là lỗi.

---

## Ten situations / 10 tình huống

### 1. Giải thích nhanh một khái niệm
Bạn muốn giải thích “domain khác hosting thế nào” cho một freelancer mới bắt đầu.

**Your answer / Câu trả lời của bạn:**

- Surface:
- Tools:
- Task brief:
- Verification:

### 2. So sánh giá hiện tại
Bạn cần biết giá hiện tại của ba website builder và muốn so sánh gói phù hợp cho freelancer.

**Your answer / Câu trả lời của bạn:**

- Surface:
- Tools:
- Task brief:
- Verification:

### 3. Báo cáo nhiều nguồn
Bạn có một brief và năm nguồn web, muốn tạo báo cáo quyết định một trang có bảng so sánh và khuyến nghị.

**Your answer / Câu trả lời của bạn:**

- Surface:
- Tools:
- Task brief:
- Verification:

### 4. Sửa bug trong repository
Một repo có test parser đang fail. Bạn muốn tìm nguyên nhân, sửa tối thiểu và chạy test.

**Your answer / Câu trả lời của bạn:**

- Surface:
- Tools:
- Task brief:
- Verification:

### 5. Response có con số không có trong brief
ChatGPT nói “70% khách hàng thích lựa chọn A”, nhưng brief bạn đưa không có số này và response không có nguồn.

**Your answer / Câu trả lời của bạn:**

- Problem category: model, context, tool hay verification?
- Action:
- Verification:

### 6. Yêu cầu quá mơ hồ
Bạn viết: `Find the best website tool for me.`

**Your answer / Câu trả lời của bạn:**

- Thiếu Outcome gì?
- Thiếu Context gì?
- Cần Tools nào?
- Verification nên là gì?

### 7. File đầu vào quan trọng
Bạn upload một CSV doanh thu và muốn ChatGPT tính doanh thu theo tháng rồi mô tả trend.

**Your answer / Câu trả lời của bạn:**

- Surface:
- Tools:
- Task brief:
- Verification:

### 8. Hành động khó hoàn tác
Bạn muốn hệ thống nghiên cứu 20 lead, soạn email và tự gửi tất cả email phù hợp.

**Your answer / Câu trả lời của bạn:**

- Surface:
- Boundary:
- Human review point:
- Verification:

### 9. Không thấy Work trên tài khoản
Bạn học bài M00.1 nhưng tài khoản hiện tại không có surface Work.

**Your answer / Câu trả lời của bạn:**

- Có thể PASS khái niệm Work không?
- Fallback thực hành là gì?
- Evidence nào nên lưu?

### 10. Task tổng hợp
Bạn cần chọn một stack website cho freelancer Việt Nam: ngân sách dưới $15/tháng, ưu tiên dễ setup, custom domain và bảo trì thấp. Bạn muốn một khuyến nghị dựa trên dữ liệu hiện tại, nhưng không muốn hệ thống mua dịch vụ hay tạo tài khoản.

**Your answer / Câu trả lời của bạn:**

- Surface:
- Tools:
- Task brief:
- Boundaries:
- Acceptance criteria:
- Verification:

---

# Answer key / Đáp án và giải thích

> Đáp án không yêu cầu câu chữ giống hệt. PASS khi lựa chọn đúng bản chất task, lý do hợp lý và verification đủ mạnh so với rủi ro.

## 1. Giải thích nhanh một khái niệm

**Đáp án mẫu:**

- Surface: **Chat**.
- Tools: không cần tool đặc biệt.
- Task brief: `Outcome: explain domain vs hosting for a beginner freelancer in under 200 words, with one analogy and one example.`
- Verification: kiểm xem có giải thích cả hai khái niệm, không có thuật ngữ kỹ thuật chưa giải thích và không thêm claim hiện tại không cần thiết.

**Giải thích:** task ngắn, ổn định, đầu ra đơn giản. Work hoặc Codex sẽ tạo thêm độ phức tạp không cần thiết.

## 2. So sánh giá hiện tại

**Đáp án mẫu:**

- Surface: **Chat** nếu chỉ cần so sánh ngắn; **Work** nếu cần deliverable nhiều bước, nhiều nguồn hoặc bảng quyết định hoàn chỉnh.
- Tools: **web search** hoặc nguồn web hiện tại.
- Task brief: nêu ba sản phẩm, audience, budget và tiêu chí.
- Verification: ưu tiên nguồn chính thức; ghi ngày kiểm tra; mở nguồn và đối chiếu từng mức giá/feature quan trọng.

**Giải thích:** “giá hiện tại” là claim có thể thay đổi. Model alone không đủ.

## 3. Báo cáo nhiều nguồn

**Đáp án mẫu:**

- Surface: **Work**.
- Tools: web search + file/brief input.
- Task brief: `Outcome: one-page decision memo comparing the options and recommending one.`
- Verification: cite claim hiện tại, tách facts khỏi recommendation, gắn unknowns và kiểm tiêu chí đầu ra.

**Giải thích:** đây là công việc nhiều bước, nhiều nguồn và cần deliverable reviewable.

## 4. Sửa bug trong repository

**Đáp án mẫu:**

- Surface: **Codex**.
- Tools: repository inspection, command execution, test runner.
- Task brief: `Find the smallest safe fix for the failing parser tests. Do not change unrelated files.`
- Verification: chạy focused tests, rồi relevant test suite; review diff và changed files.

**Giải thích:** code, repo và test là việc chính, nên Codex là surface phù hợp.

## 5. Response có con số không có trong brief

**Đáp án mẫu:**

- Problem category: **verification** là lỗi bạn phải xử lý; nguyên nhân có thể là hallucination do thiếu evidence/context.
- Action: hỏi nguồn của con số; nếu không có, yêu cầu gỡ claim hoặc đánh dấu unsupported.
- Verification: tìm nguồn gốc đáng tin cậy hoặc dữ liệu đầu vào có con số đó.

**Giải thích:** câu trả lời nghe tự tin không phải bằng chứng.

## 6. Yêu cầu quá mơ hồ

**Đáp án mẫu:**

- Outcome thiếu: “best” để làm gì — chọn một tool cho portfolio, e-commerce hay landing page?
- Context thiếu: audience, ngân sách, kỹ năng kỹ thuật, custom domain, maintenance, ngôn ngữ/thị trường.
- Tools: web search nếu so tính năng/giá hiện tại.
- Verification: source cho feature/price, unknowns tách riêng, acceptance criteria rõ.

**Giải thích:** đây là bài tập điển hình về task brief. Mục tiêu không phải prompt dài mà là giảm những phần buộc model phải đoán.

## 7. File đầu vào quan trọng

**Đáp án mẫu:**

- Surface: Chat nếu phân tích đơn; Work nếu cần workflow nhiều bước và báo cáo hoàn chỉnh.
- Tools: file/data analysis hoặc code tính toán phù hợp.
- Task brief: nêu cột ngày, cột doanh thu, quy tắc grouping và định dạng đầu ra.
- Verification: kiểm một số dòng mẫu, tính lại 1–2 tháng, kiểm grand total và nhãn tháng trước khi tin narrative.

**Giải thích:** tool có thể tính đúng nhưng phần diễn giải vẫn cần review.

## 8. Hành động khó hoàn tác

**Đáp án mẫu:**

- Surface: Work có thể phù hợp cho nghiên cứu + soạn thảo nhiều bước.
- Boundary: `Do not send any email without my explicit review.`
- Human review point: sau khi lead list và draft đã hoàn tất, trước bước gửi.
- Verification: kiểm lead fit, nội dung cá nhân hóa, recipient, factual claims và danh sách email trước hành động.

**Giải thích:** gửi email là hành động bên ngoài có hậu quả. Human-in-the-loop phải được xác định trước.

## 9. Không thấy Work trên tài khoản

**Đáp án mẫu:**

- Có thể PASS khái niệm: **có**, nếu người học giải thích đúng khi nào Work phù hợp và biết sự khác biệt surface/tool.
- Fallback: mô phỏng task nhiều bước trong Chat bằng task brief rõ, checkpoints và deliverable cuối; ghi rằng Work chưa khả dụng.
- Evidence: decision table về surface + lý do + screenshot/ghi chú availability nếu muốn, không cần giả vờ đã dùng Work.

**Giải thích:** gate kiểm mental model, không bắt buộc mọi tài khoản có cùng feature.

## 10. Task tổng hợp

**Đáp án mẫu:**

- Surface: **Work** là lựa chọn mạnh nếu cần research nhiều bước và memo hoàn chỉnh; Chat + web search vẫn là fallback hợp lệ nếu Work không khả dụng.
- Tools: current web search, ưu tiên official product sources.
- Task brief:

```text
Outcome: Recommend one website stack for a Vietnamese freelancer portfolio site.
Context: Budget under $15/month. Priorities: easy setup, custom domain, low maintenance.
Tools: Use current official product pages and current web sources.
Verification: Cite current pricing and feature claims, label unknowns, and explain the main trade-off of the recommendation.
```

- Boundaries: không mua, không đăng ký, không nhập payment, không tạo tài khoản.
- Acceptance criteria: ít nhất bốn option hợp lệ; recurring cost rõ; custom domain được xác nhận; có một khuyến nghị và ít nhất hai trade-off.
- Verification: mở nguồn chính thức, đối chiếu giá/feature, kiểm tổng monthly cost, review recommendation so với criteria.

**Giải thích:** tình huống này kiểm toàn bộ M00: surface, model/context/tool mental model, task brief, boundaries và verification.

---

## Scoring / Cách chấm

Mỗi tình huống tối đa 2 điểm:

- `0`: sai bản chất hoặc không có lý do/verification.
- `1`: lựa chọn chấp nhận được nhưng thiếu context, tool hoặc verification quan trọng.
- `2`: lựa chọn phù hợp, lý do rõ và cách kiểm chứng tương xứng với rủi ro.

**PASS M00:**

- tổng ít nhất **16/20**;
- câu 4, 5, 8, 10 không được 0;
- giải thích đúng `model`, `context`, `tool`, `surface` bằng tiếng Việt;
- viết được ít nhất một task brief O-C-T-V hoàn chỉnh;
- không dùng thuật ngữ tiếng Anh trọng tâm mà không thể giải thích nghĩa.

Nếu chưa PASS, quay lại đúng lesson liên quan, làm một tình huống tương đương bằng input khác và lưu evidence lần làm lại.
