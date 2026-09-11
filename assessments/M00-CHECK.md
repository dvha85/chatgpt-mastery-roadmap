# M00 Check — Mental Model Practice / Bài thực hành Mental Model

> Làm sau M00.3. Bộ này gồm 10 tình huống thực hành, có đáp án và giải thích. Hãy tự làm trước, sau đó mới mở phần đáp án. **ChatGPT track dùng tiếng Việt.**

## Instructions / Hướng dẫn

Với mỗi tình huống, ghi:
1. `Surface / Bề mặt`: Chat, Work hoặc Codex.
2. `Tools / Công cụ`: tool nào cần, nếu có.
3. `Task brief / Bản giao việc`: ít nhất Kết quả + Ngữ cảnh + Kiểm chứng.
4. `Verification / Kiểm chứng`: cách xác nhận kết quả.

Nếu tính năng không có trên tài khoản, ghi fallback thay vì coi đó là lỗi.

---

## Ten situations / 10 tình huống

### 1. Giải thích nhanh một khái niệm
Bạn muốn giải thích “domain khác hosting thế nào” cho một freelancer mới bắt đầu.

### 2. So sánh giá hiện tại
Bạn cần biết giá hiện tại của ba website builder và muốn so sánh gói phù hợp cho freelancer.

### 3. Báo cáo nhiều nguồn
Bạn có một brief và năm nguồn web, muốn tạo báo cáo quyết định một trang có bảng so sánh và khuyến nghị.

### 4. Sửa bug trong repository
Một repo có test parser đang fail. Bạn muốn tìm nguyên nhân, sửa tối thiểu và chạy test.

### 5. Response có con số không có trong brief
ChatGPT nói “70% khách hàng thích lựa chọn A”, nhưng brief không có số này và response không có nguồn.

### 6. Yêu cầu quá mơ hồ
Bạn viết: `Hãy tìm công cụ làm website tốt nhất cho tôi.`

Hãy nêu Outcome còn thiếu, Context còn thiếu, Tools cần và Verification phù hợp.

### 7. File đầu vào quan trọng
Bạn upload một CSV doanh thu và muốn ChatGPT tính doanh thu theo tháng rồi mô tả trend.

### 8. Hành động khó hoàn tác
Bạn muốn hệ thống nghiên cứu 20 lead, soạn email và tự gửi tất cả email phù hợp.

Hãy nêu surface, boundary, human review point và verification.

### 9. Không thấy Work trên tài khoản
Bạn học M00.1 nhưng tài khoản hiện tại không có Work.

Hãy nêu liệu vẫn PASS khái niệm được không, fallback thực hành và evidence nên lưu.

### 10. Task tổng hợp
Bạn cần chọn một stack website cho freelancer Việt Nam: ngân sách dưới $15/tháng, ưu tiên dễ setup, custom domain và bảo trì thấp. Bạn muốn khuyến nghị dựa trên dữ liệu hiện tại nhưng không muốn hệ thống mua dịch vụ hay tạo tài khoản.

Hãy nêu surface, tools, task brief, boundaries, acceptance criteria và verification.

---

# Answer key / Đáp án và giải thích

> Đáp án không cần giống hệt câu chữ mẫu. PASS khi lựa chọn đúng bản chất task và verification tương xứng với rủi ro.

## 1. Giải thích nhanh
- Surface: **Chat**.
- Tools: không cần tool đặc biệt.
- Task brief mẫu:

```text
Kết quả cần đạt: Giải thích domain khác hosting thế nào cho freelancer mới trong dưới 200 từ, có một phép so sánh và một ví dụ.
Ngữ cảnh: Người đọc chưa có kiến thức kỹ thuật.
Kiểm chứng: Kiểm cả hai khái niệm được giải thích và không có thuật ngữ chưa định nghĩa.
Ngôn ngữ đầu ra: Tiếng Việt.
```

## 2. So sánh giá hiện tại
- Surface: **Chat** cho so sánh ngắn; **Work** nếu cần deliverable nhiều bước.
- Tools: web search/nguồn hiện tại.
- Verification: ưu tiên nguồn chính thức, ghi ngày kiểm tra, đối chiếu từng mức giá/feature quan trọng.

## 3. Báo cáo nhiều nguồn
- Surface: **Work**.
- Tools: web search + file/brief input.
- Task brief mẫu:

```text
Kết quả cần đạt: Tạo memo ra quyết định dài một trang, so sánh các lựa chọn và khuyến nghị một lựa chọn.
Ngữ cảnh: Dùng brief và năm nguồn đã cung cấp.
Kiểm chứng: Trích nguồn cho claim hiện tại, tách fact khỏi recommendation và đánh dấu unknown.
Ngôn ngữ đầu ra: Tiếng Việt.
```

## 4. Sửa bug trong repository
- Surface: **Codex**.
- Tools: repository inspection, command execution, test runner.

```text
Tìm bản sửa nhỏ nhất và an toàn cho các parser test đang fail. Không thay đổi file không liên quan. Chạy focused tests rồi relevant test suite. Báo cáo lệnh, kết quả test và file đã thay đổi bằng tiếng Việt; giữ nguyên code identifier và command.
```

## 5. Con số không có nguồn
- Problem category: verification phải xử lý; nguyên nhân có thể là hallucination/thiếu evidence.
- Action: hỏi nguồn; nếu không có, gỡ claim hoặc đánh dấu unsupported.
- Verification: tìm source/dữ liệu gốc thật sự chứa con số đó.

## 6. Yêu cầu quá mơ hồ
- Outcome thiếu: “best” để làm gì?
- Context thiếu: audience, budget, kỹ năng kỹ thuật, custom domain, maintenance, thị trường.
- Tools: web search nếu so current price/feature.
- Verification: source cho feature/price, unknown tách riêng, acceptance criteria rõ.

## 7. CSV doanh thu
- Surface: Chat cho phân tích đơn; Work nếu cần workflow/report nhiều bước.
- Tools: file/data analysis hoặc code tính toán.
- Task brief: nêu cột ngày, doanh thu, quy tắc grouping và output.
- Verification: tính lại 1–2 tháng, kiểm grand total và nhãn tháng trước khi tin narrative.

## 8. Hành động khó hoàn tác
- Surface: Work có thể phù hợp cho research + drafting.
- Boundary:

```text
Không gửi bất kỳ email nào nếu chưa có tôi review và chấp thuận rõ ràng.
```

- Human review point: sau lead list + draft, trước gửi.
- Verification: kiểm lead fit, recipient, personalization và factual claims.

## 9. Không thấy Work
- Vẫn có thể PASS khái niệm nếu giải thích đúng khi nào Work phù hợp.
- Fallback: mô phỏng workflow nhiều bước trong Chat bằng task brief + checkpoints + deliverable cuối.
- Evidence: bảng chọn surface, lý do và ghi chú availability thật; không giả vờ đã dùng Work.

## 10. Task tổng hợp
- Surface: **Work** nếu có; Chat + web search là fallback hợp lệ.
- Tools: current web search, ưu tiên official product sources.

```text
Kết quả cần đạt: Khuyến nghị một website stack cho portfolio của freelancer Việt Nam.
Ngữ cảnh: Ngân sách dưới $15/tháng. Ưu tiên dễ thiết lập, custom domain và ít bảo trì.
Công cụ/nguồn: Dùng trang sản phẩm chính thức hiện tại và nguồn web mới.
Ranh giới: Không mua, đăng ký, tạo tài khoản, nhập payment hoặc thay đổi dữ liệu bên ngoài.
Tiêu chí chấp nhận: So sánh ít nhất 4 option hợp lệ; recurring cost rõ; custom domain được xác nhận; có một khuyến nghị và ít nhất 2 trade-off.
Kiểm chứng: Trích dẫn claim về giá/tính năng hiện tại, gắn nhãn unknown và kiểm tổng chi phí hàng tháng.
Ngôn ngữ đầu ra: Tiếng Việt.
```

---

## Scoring / Cách chấm
Mỗi tình huống tối đa 2 điểm:
- `0`: sai bản chất hoặc không có verification.
- `1`: lựa chọn chấp nhận được nhưng thiếu context/tool/verification quan trọng.
- `2`: lựa chọn phù hợp, lý do rõ và cách kiểm tương xứng rủi ro.

**PASS M00:**
- tổng ít nhất **16/20**;
- câu 4, 5, 8, 10 không được 0;
- giải thích đúng `model`, `context`, `tool`, `surface` bằng tiếng Việt;
- viết được ít nhất một task brief O-C-T-V hoàn chỉnh bằng tiếng Việt;
- không dùng thuật ngữ tiếng Anh trọng tâm mà không giải thích được nghĩa.

## English checkpoint
English track riêng: nhận diện thuật ngữ và viết một vài câu tiếng Anh ngắn. Không cần dùng prompt tiếng Anh để PASS ChatGPT track.
