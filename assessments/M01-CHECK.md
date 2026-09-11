# M01 Check — Prompting as Task Specification / Bài kiểm tra M01

> Làm sau M01.4. Hãy tự làm đủ 5 task spec trước khi xem đáp án mẫu và rubric. **Toàn bộ ChatGPT track dùng tiếng Việt.**

## Instructions / Hướng dẫn

Với mỗi yêu cầu mơ hồ:
1. Viết lại thành task specification rõ bằng tiếng Việt.
2. Ghi ít nhất Goal, Context, Output và Boundaries nếu cần.
3. Nêu một verification step.
4. Với ít nhất một câu, chạy prompt thật và lưu evidence.

Không cần prompt dài. Prompt tốt là prompt đủ rõ để làm và kiểm.

---

## Five vague requests / 5 yêu cầu mơ hồ

### 1. `Hãy làm nội dung này tốt hơn.`
Context giả lập: đây là email cập nhật tiến độ cho khách hàng. Có ngày giao dự kiến chưa được xác nhận.

**Bản giao việc của bạn:** Goal / Context / Output / Boundaries / Verification

### 2. `Hãy tóm tắt báo cáo này.`
Context giả lập: report dự án 3 trang cho quản lý; họ cần decisions, risks và next steps trước.

**Bản giao việc của bạn:** Goal / Context / Output / Boundaries / Verification

### 3. `Hãy lập kế hoạch tuần cho tôi.`
Context giả lập: có 9 giờ học; fundamentals phải học trước automation; Chủ nhật dành cho review; không học quá 2 giờ liên tục.

**Bản giao việc của bạn:** Goal / Context / Output / Boundaries / Verification

### 4. `Công cụ làm website nào tốt nhất?`
Context giả lập: freelancer Việt Nam, không chuyên kỹ thuật, budget dưới $15/tháng, cần custom domain và maintenance thấp. Giá/feature hiện tại phải được kiểm chứng.

**Bản giao việc của bạn:** Goal / Context / Output / Boundaries / Tools/sources / Verification

### 5. `Hãy giải thích dữ liệu này.`

| Month | Revenue |
|---|---:|
| Jan | 1000 |
| Feb | 1250 |
| Mar | 1100 |
| Apr | 1500 |

Audience không chuyên data. Bạn muốn trend và anomaly nhưng không muốn AI bịa nguyên nhân.

**Bản giao việc của bạn:** Goal / Context / Output / Boundaries / Verification

---

# Answer guide / Gợi ý đáp án

> Có nhiều đáp án hợp lệ. Trọng tâm là task spec đủ rõ, không phải câu chữ giống mẫu.

## 1. Email update

```text
Hãy viết lại email cập nhật trạng thái dự án này cho khách hàng. Giữ nguyên mọi fact và ngày đã được xác nhận. Dùng giọng bình tĩnh, chuyên nghiệp và giới hạn dưới 150 từ. Không hứa ngày giao nếu email gốc chưa xác nhận rõ. Sau khi viết lại, liệt kê riêng câu nào bạn đã bỏ vì thiếu bằng chứng. Viết bằng tiếng Việt.
```

**Verification:** đối chiếu facts/dates với email gốc.

## 2. Report summary

```text
Hãy tóm tắt báo cáo dự án 3 trang này cho quản lý. Đưa quyết định lên trước, sau đó là rủi ro và việc tiếp theo. Dùng tối đa 8 bullet. Chỉ dùng thông tin trong báo cáo; nếu thiếu owner hoặc due date, ghi “Chưa xác định” thay vì tự tạo. Trả lời bằng tiếng Việt.
```

**Verification:** đối chiếu từng bullet với report, đặc biệt decisions và dates.

## 3. Weekly plan

```text
Hãy tạo kế hoạch học ChatGPT trong một tuần với tổng thời gian đúng 9 giờ. Học nền tảng trước automation, dành Chủ nhật để review và mỗi block học tối đa 2 giờ. Trả kết quả bằng bảng: Ngày | Chủ đề | Thời lượng | Tiêu chí hoàn thành; sau đó ghi tổng thời gian tuần. Trả lời bằng tiếng Việt.
```

**Verification:** cộng tổng giờ, kiểm thứ tự và block-duration constraint.

## 4. Website tool

```text
Hãy so sánh ít nhất 4 lựa chọn website hiện tại cho freelancer Việt Nam không chuyên kỹ thuật. Ngân sách dưới $15/tháng; custom domain là bắt buộc; ưu tiên maintenance thấp. Dùng nguồn sản phẩm chính thức hiện tại cho claim về giá và tính năng. Trả bảng: Lựa chọn | Chi phí định kỳ | Custom domain | Độ khó thiết lập | Maintenance | Trade-off chính | Trạng thái bằng chứng. Ghi “Chưa xác minh” cho fact còn thiếu. Khuyến nghị một lựa chọn và giải thích 2 trade-off. Không mua, tạo tài khoản hoặc nhập thông tin thanh toán. Trả lời bằng tiếng Việt.
```

**Verification:** mở nguồn chính thức, đối chiếu current price/custom-domain claim và tính recurring cost.

## 5. Revenue data

```text
Chỉ dùng bảng doanh thu theo tháng tôi cung cấp. Hãy mô tả xu hướng tổng thể và xác định mức tăng và giảm lớn nhất giữa hai tháng liên tiếp. Hiển thị phép tính cho các thay đổi đó. Giải thích cho người không chuyên dữ liệu trong dưới 150 từ. Không suy luận nguyên nhân nếu tôi chưa cung cấp evidence về nguyên nhân. Trả lời bằng tiếng Việt.
```

**Verification:** tính lại từng chênh lệch tháng; kiểm narrative không biến correlation thành cause.

---

## Quality examples / Ví dụ mức chất lượng

### Level 0 — Chưa đạt
```text
Hãy làm email chuyên nghiệp và tốt hơn nhiều.
```
Thiếu mục tiêu cụ thể, facts cần giữ và boundary về ngày giao.

### Level 1 — Một phần
```text
Hãy viết lại email chuyên nghiệp cho khách hàng trong dưới 150 từ.
```
Goal/output/audience rõ hơn nhưng chưa bảo vệ facts hoặc ngày giao chưa xác nhận.

### Level 2 — Đạt
```text
Hãy viết lại email cập nhật tiến độ này cho khách hàng bằng giọng bình tĩnh, chuyên nghiệp, dưới 150 từ. Giữ nguyên fact và ngày đã xác nhận. Không hứa ngày giao trừ khi email gốc xác nhận rõ. Viết bằng tiếng Việt.
```

## Rubric / Cách chấm

Mỗi task spec tối đa 2 điểm:
- `0`: vẫn mơ hồ hoặc thiếu thành phần cốt lõi khiến hệ thống phải đoán.
- `1`: làm được nhưng thiếu context/output/boundary/verification quan trọng.
- `2`: goal rõ, context liên quan, output kiểm được, boundaries phù hợp và verification có ý nghĩa.

### PASS M01
- nộp đủ **5/5** task spec;
- ít nhất **4/5** đạt `2`;
- task còn lại ít nhất `1`;
- ít nhất một task chạy thật và có response + verification evidence;
- không có lỗi nghiêm trọng như yêu cầu AI tự xác nhận sự thật bằng lời của chính nó, bịa missing data hoặc bỏ boundary cho hành động khó hoàn tác.

## English checkpoint / Kiểm tra tiếng Anh
English track riêng: nhận ra `goal`, `context`, `boundary`, `iteration`, `verification`; giải thích ít nhất 3 từ bằng tiếng Việt và tự viết một instruction tiếng Anh có nghĩa đúng. Không cần dùng prompt tiếng Anh để PASS ChatGPT track.
