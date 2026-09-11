# M00 Vietnamese Prompt Pack — Bộ prompt tiếng Việt dùng trực tiếp

> Dùng kèm M00.1–M00.3. Đây là bản vận hành tiếng Việt để copy/paste trực tiếp vào ChatGPT. Thuật ngữ tiếng Anh vẫn được giữ khi cần học khái niệm chuẩn.

## 1. Chat — giải thích nhanh

```text
Hãy giải thích sự khác nhau giữa tên miền (domain) và hosting cho một freelancer mới bắt đầu.

Yêu cầu:
- dùng một phép so sánh dễ hiểu;
- có bảng hai cột;
- giới hạn dưới 250 từ;
- giải thích thuật ngữ kỹ thuật trước khi dùng;
- trả lời bằng tiếng Việt.
```

## 2. Chat + web search — thông tin hiện tại

```text
Hãy tìm thông tin hiện tại về chủ đề tôi yêu cầu.

Yêu cầu:
- dùng web search cho các fact có thể thay đổi theo thời gian;
- ưu tiên nguồn chính thức hoặc nguồn có thẩm quyền;
- trích dẫn nguồn cho từng claim quan trọng;
- ghi rõ ngày kiểm tra;
- nếu nguồn mâu thuẫn, nêu rõ thay vì tự chọn một kết luận;
- trả lời bằng tiếng Việt.
```

## 3. Work — báo cáo nhiều bước

```text
Kết quả cần đạt:
Tạo một báo cáo so sánh đủ rõ để ra quyết định.

Ngữ cảnh:
Đối tượng là người mới, không chuyên kỹ thuật.

Đầu vào:
Dùng các file, brief và link tôi cung cấp.

Công cụ/nguồn:
Dùng nguồn web hiện tại khi cần kiểm tra fact có thể thay đổi.

Dạng đầu ra:
- tóm tắt kết luận trước;
- bảng so sánh;
- khuyến nghị cuối;
- các trade-off chính.

Kiểm chứng:
- trích dẫn các fact quan trọng;
- tách dữ kiện khỏi khuyến nghị;
- đánh dấu phần chưa chắc chắn;
- không đoán khi thiếu bằng chứng.

Ngôn ngữ đầu ra: Tiếng Việt.
```

## 4. Codex — sửa code an toàn

```text
Hãy kiểm tra các test đang thất bại và xác định nguyên nhân.

Yêu cầu:
- tìm bản sửa nhỏ nhất và an toàn;
- không thay đổi hành vi ngoài phạm vi lỗi nếu không cần thiết;
- không sửa file hoặc dependency không liên quan;
- chạy focused tests trước, sau đó chạy test suite liên quan;
- tóm tắt các file đã thay đổi;
- hiển thị lệnh test và kết quả kiểm chứng;
- báo cáo bằng tiếng Việt nhưng giữ nguyên tên file, command và code identifier.
```

## 5. Prompt khi thiếu context

```text
Đừng trả lời ngay nếu thông tin hiện có chưa đủ để đưa ra kết luận đáng tin cậy.

Trước tiên hãy:
1. chỉ ra những thông tin còn thiếu;
2. giải thích vì sao từng thông tin có thể làm thay đổi câu trả lời;
3. tách rõ điều đã biết, điều đang giả định và điều chưa biết;
4. không tự bịa dữ kiện còn thiếu.

Trả lời bằng tiếng Việt.
```

## 6. O-C-T-V — bản giao việc ngắn

```text
Kết quả cần đạt:
...

Ngữ cảnh:
...

Công cụ hoặc nguồn cần dùng:
...

Cách kiểm chứng:
...

Ngôn ngữ đầu ra: Tiếng Việt.
```

## 7. O-C-T-V — bản thực dụng

```text
Kết quả cần đạt:
...

Đối tượng sử dụng:
...

Ngữ cảnh và đầu vào:
...

Ranh giới:
...

Công cụ hoặc nguồn:
...

Dạng đầu ra:
...

Tiêu chí chấp nhận:
...

Cách kiểm chứng:
...

Ngôn ngữ đầu ra: Tiếng Việt.
```

## 8. Verification — kiểm chứng câu trả lời

```text
Hãy kiểm chứng câu trả lời vừa tạo.

Thực hiện theo thứ tự:
1. liệt kê các claim quan trọng;
2. đánh dấu claim nào là fact, suy luận hay khuyến nghị;
3. với fact có thể thay đổi, kiểm tra bằng nguồn hiện tại;
4. với số liệu, tính lại hoặc chỉ ra phép tính;
5. với code, nêu test nào chứng minh kết quả;
6. đánh dấu PASS / FAIL / UNKNOWN cho từng tiêu chí;
7. nếu thiếu evidence, ghi UNKNOWN thay vì đoán.

Trả lời bằng tiếng Việt.
```

## 9. Boundary — dừng trước hành động bên ngoài

```text
Bạn có thể nghiên cứu, phân tích và chuẩn bị bản nháp, nhưng phải dừng trước mọi hành động bên ngoài có hậu quả.

Không được tự:
- gửi email hoặc tin nhắn;
- đăng nội dung;
- mua hàng hoặc thanh toán;
- tạo tài khoản;
- xóa dữ liệu;
- thay đổi dữ liệu bên ngoài.

Trước các bước đó, hãy trình bày kế hoạch và chờ tôi review.
```

## 10. Prompt tổng hợp chọn website stack

```text
Kết quả cần đạt:
Khuyến nghị một website stack phù hợp cho portfolio của freelancer Việt Nam.

Ngữ cảnh:
- ngân sách dưới $15/tháng;
- người dùng không chuyên kỹ thuật;
- ưu tiên dễ thiết lập;
- bắt buộc hỗ trợ custom domain;
- ưu tiên ít phải bảo trì.

Công cụ/nguồn:
Dùng các trang sản phẩm chính thức hiện tại và web search cho thông tin mới.

Ranh giới:
Không mua dịch vụ, không nhập thông tin thanh toán và không tạo tài khoản.

Tiêu chí chấp nhận:
- so sánh ít nhất 4 lựa chọn khả thi;
- nêu rõ chi phí định kỳ;
- xác nhận hỗ trợ custom domain;
- đưa ra 1 khuyến nghị cuối;
- giải thích ít nhất 2 trade-off.

Kiểm chứng:
- trích dẫn giá và tính năng hiện tại;
- ghi ngày kiểm tra;
- đánh dấu unknowns;
- tách facts khỏi recommendation;
- kiểm lại tổng chi phí hàng tháng.

Ngôn ngữ đầu ra: Tiếng Việt.
```

## Cách dùng trong khóa học

- **ChatGPT track:** ưu tiên dùng các prompt tiếng Việt ở file này.
- **English track:** quay lại từng lesson để học vocabulary và English patterns tương ứng.
- Nếu prompt trong lesson cũ còn viết tiếng Anh trước, coi file này là bản vận hành ưu tiên theo [Vietnamese-first Usage](../../docs/VIETNAMESE-FIRST-USAGE.md).
