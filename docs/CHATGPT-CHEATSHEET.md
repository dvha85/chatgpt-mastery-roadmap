# ChatGPT Cheat Sheet — Cẩm nang sử dụng nhanh

> **Mục tiêu:** mở ra là dùng ngay khi làm việc với ChatGPT.  
> **Ngôn ngữ vận hành:** tiếng Việt. Thuật ngữ kỹ thuật chuẩn giữ tiếng Anh và được giải thích theo ngữ cảnh.  
> **Source snapshot:** 2026-09-11  
> Xem thêm: [Vietnamese-first Usage](VIETNAMESE-FIRST-USAGE.md)

## 1. Chọn đúng cách sử dụng

| Tôi cần làm gì? | Nên dùng |
|---|---|
| Hỏi nhanh, giải thích, brainstorm, viết lại | **Chat** |
| Phân tích, so sánh, lập kế hoạch | **Chat** |
| Công việc lớn, nhiều bước, nhiều file, cần deliverable hoàn chỉnh | **Work** |
| Sửa code, làm việc với repository, chạy test | **Codex** |
| Tìm thông tin mới nhất | **Web Search** |
| Nghiên cứu nhiều nguồn, tổng hợp sâu | **Deep Research** |
| Làm việc với PDF, bảng tính, ảnh, tài liệu | **Upload file + Chat/Work** |

Quy tắc nhanh:

```text
Việc nhỏ → Chat
Việc lớn → Work
Việc code → Codex
Thông tin mới → Search
Nghiên cứu sâu → Deep Research
```

## 2. Công thức prompt chuẩn

```text
Kết quả cần đạt:
...

Ngữ cảnh:
...

Nguồn hoặc dữ liệu cần dùng:
...

Dạng đầu ra:
...

Ranh giới:
...

Tiêu chí chấp nhận:
...

Cách kiểm chứng:
...

Ngôn ngữ đầu ra:
Tiếng Việt.
```

Không cần dùng đủ tất cả mục cho task đơn giản.

## 3. Prompt dùng cho hầu hết công việc

```text
Tôi cần đạt kết quả sau:
[ĐIỀN KẾT QUẢ]

Ngữ cảnh:
[ĐIỀN THÔNG TIN CẦN THIẾT]

Hãy:
1. phân tích yêu cầu;
2. thực hiện nhiệm vụ;
3. trình bày kết quả rõ ràng;
4. nêu các giả định bạn đã sử dụng;
5. đánh dấu những thông tin chưa chắc chắn;
6. đề xuất cách kiểm chứng các kết luận quan trọng.

Không tự bịa dữ liệu còn thiếu.
Trả lời bằng tiếng Việt.
```

## 4. Prompt ngắn theo loại việc

### Giải thích

```text
Giải thích [KHÁI NIỆM] cho người mới.
Dùng ngôn ngữ đơn giản.
Cho 2 ví dụ thực tế.
Giải thích các thuật ngữ tiếng Anh khi xuất hiện.
```

### Tóm tắt

```text
Tóm tắt nội dung dưới đây.
Chỉ sử dụng thông tin có trong nguồn.
Trình bày:
- ý chính;
- quyết định;
- rủi ro;
- việc cần làm tiếp theo.
Không tự bổ sung dữ kiện.
```

### So sánh

```text
So sánh các lựa chọn sau theo:
- chi phí;
- ưu điểm;
- nhược điểm;
- độ khó;
- rủi ro;
- phù hợp với ai.

Trình bày thành bảng.
Nếu thiếu dữ liệu, ghi “Chưa xác định” thay vì suy đoán.
```

### Lập kế hoạch

```text
Lập kế hoạch để tôi đạt mục tiêu:
[MỤC TIÊU]

Điều kiện:
[THỜI GIAN / NGÂN SÁCH / GIỚI HẠN]

Chia thành các bước nhỏ.
Cho mỗi bước:
- việc cần làm;
- thời gian;
- kết quả cần đạt;
- cách kiểm tra hoàn thành.
```

## 5. Khi câu trả lời chưa tốt — dùng follow-up

| Muốn làm gì | Follow-up |
|---|---|
| Giữ phần đúng | `Giữ nguyên phần đang đúng. Chỉ sửa...` |
| Ngắn hơn | `Rút gọn còn khoảng 150 từ.` |
| Dễ hiểu hơn | `Giải thích lại cho người mới.` |
| Chuyển thành bảng | `Giữ nguyên nội dung, chuyển thành bảng.` |
| Không thêm dữ liệu | `Không thêm bất kỳ thông tin nào ngoài nguồn.` |
| Kiểm lỗi | `Kiểm tra lại câu trả lời và chỉ ra các phần có thể sai.` |
| Tìm giả định | `Bạn đã sử dụng những giả định nào mà tôi chưa cung cấp?` |
| Tăng khả năng kiểm chứng | `Gắn mỗi kết luận quan trọng với nguồn hoặc cách kiểm chứng.` |

Mẫu follow-up mạnh:

```text
Giữ nguyên cấu trúc và các dữ kiện đã đúng.

Chỉ sửa phần sau:
[PHẦN CẦN SỬA]

Không thay đổi:
[PHẦN PHẢI GIỮ]

Sau khi sửa, cho biết bạn đã thay đổi những gì.
```

## 6. Khi task lớn — chia nhỏ

```text
Bước 1: Xác định tiêu chí.
Dừng lại để kiểm tra.

Bước 2: Thu thập dữ kiện.

Bước 3: Kiểm chứng dữ kiện.

Bước 4: So sánh hoặc phân tích.

Bước 5: Đề xuất phương án.

Bước 6: Lập kế hoạch triển khai.
```

Mental model:

```text
TASK
 ↓
CHIA NHỎ
 ↓
LÀM
 ↓
KIỂM
 ↓
SỬA
 ↓
LÀM TIẾP
```

## 7. Kiểm chứng câu trả lời

Đừng chỉ hỏi:

```text
Bạn chắc không?
```

Hãy hỏi:

```text
Tách câu trả lời vừa rồi thành:
1. Dữ kiện có thể kiểm chứng
2. Giả định
3. Suy luận
4. Khuyến nghị

Với mỗi dữ kiện quan trọng:
- nêu nguồn hoặc cách kiểm;
- nếu chưa đủ bằng chứng, ghi “Chưa được kiểm chứng”;
- không bảo vệ kết luận nếu dữ liệu không hỗ trợ.
```

Mental model:

```text
CLAIM / NHẬN ĐỊNH
        ↓
EVIDENCE / BẰNG CHỨNG
        ↓
CHECK / KIỂM TRA
        ↓
CONCLUSION / KẾT LUẬN
```

## 8. Khi dùng Web Search

```text
Tìm thông tin mới nhất về [CHỦ ĐỀ].

Ưu tiên:
1. nguồn chính thức;
2. nguồn gốc / primary source;
3. nguồn mới nhất.

Với mỗi thông tin quan trọng:
- ghi nguồn;
- ghi ngày;
- phân biệt fact với nhận định.

Nếu các nguồn mâu thuẫn, hãy chỉ ra sự khác biệt.
```

## 9. Khi upload file

```text
Chỉ sử dụng file tôi cung cấp làm nguồn chính.

Hãy:
1. tóm tắt nội dung;
2. trích các dữ kiện quan trọng;
3. nêu những điểm chưa rõ;
4. không bổ sung thông tin ngoài file.

Với mỗi kết luận quan trọng, cho biết nó dựa trên phần nào của file.
```

## 10. Khi học một chủ đề mới

```text
Tôi là người mới về [CHỦ ĐỀ].

Hãy dạy tôi theo thứ tự:
1. Khái niệm cốt lõi
2. Mental model
3. Thuật ngữ quan trọng
4. Ví dụ đơn giản
5. Ví dụ thực tế
6. Lỗi người mới thường gặp
7. Bài tập
8. Cách kiểm tra tôi đã hiểu

Giữ thuật ngữ tiếng Anh chuyên ngành nhưng giải thích nghĩa tiếng Việt khi xuất hiện lần đầu.
```

## 11. Khi muốn ChatGPT làm tutor

```text
Hãy làm gia sư cho tôi về [CHỦ ĐỀ].

Không đưa toàn bộ đáp án ngay.
Mỗi vòng:
1. giải thích một phần;
2. hỏi tôi 1–3 câu để kiểm tra;
3. đánh giá câu trả lời;
4. sửa phần tôi hiểu sai;
5. chỉ chuyển sang phần tiếp theo khi tôi đã hiểu phần hiện tại.

Trả lời bằng tiếng Việt.
```

## 12. Khi cần đưa ra quyết định

```text
Tôi cần quyết định giữa:
[A]
[B]
[C]

Tiêu chí:
[TIÊU CHÍ]

Ràng buộc:
[NGÂN SÁCH / THỜI GIAN / ĐIỀU KIỆN]

Hãy:
1. lập bảng so sánh;
2. phân biệt tiêu chí bắt buộc và tiêu chí ưu tiên;
3. đánh dấu dữ liệu còn thiếu;
4. loại các phương án vi phạm điều kiện bắt buộc;
5. đề xuất phương án tốt nhất;
6. nêu trade-off lớn nhất;
7. giải thích điều gì có thể khiến lựa chọn thay đổi.
```

## 13. Khi muốn ChatGPT phản biện chính nó

```text
Hãy phản biện câu trả lời vừa rồi.

Tìm:
- giả định yếu;
- dữ liệu thiếu;
- lỗi logic;
- kết luận quá mạnh;
- rủi ro bị bỏ sót.

Sau đó đề xuất phiên bản kết luận thận trọng hơn.
```

## 14. Những câu cực hữu ích

```text
Không tự bịa dữ liệu còn thiếu.
Nếu chưa biết, hãy nói rõ là chưa biết.
Nêu các giả định bạn đang sử dụng.
Chỉ sử dụng nguồn tôi cung cấp.
Phân biệt fact với suy luận.
Giữ nguyên phần đúng, chỉ sửa phần này.
Hãy chỉ ra cách tôi có thể kiểm chứng kết quả.
Nếu thiếu dữ liệu, ghi “Chưa xác định”.
Đừng thực hiện hành động bên ngoài trước khi tôi duyệt.
```

## 15. Checklist trước khi dùng kết quả

```text
□ ChatGPT có hiểu đúng mục tiêu không?
□ Context quan trọng đã được cung cấp chưa?
□ Output có đúng format không?
□ Có dữ kiện nào được tự suy đoán không?
□ Số liệu đã được tính lại chưa?
□ Giá/ngày/tính năng hiện tại đã kiểm nguồn chưa?
□ Citation/source có thực sự tồn tại không?
□ Assumption đã được nêu rõ chưa?
□ Unknown có bị biến thành fact không?
□ Recommendation có dựa trên criteria không?
□ Hành động rủi ro có cần tôi duyệt trước không?
```

## 16. Công thức nên thuộc lòng

```text
KẾT QUẢ
+
NGỮ CẢNH
+
ĐẦU RA
+
RANH GIỚI
+
KIỂM CHỨNG
```

Hoặc tự hỏi 5 câu:

```text
Tôi muốn gì?
ChatGPT cần biết gì?
Tôi muốn nhận lại cái gì?
Điều gì không được làm?
Làm sao biết kết quả đúng?
```

## Golden rule

> **ChatGPT không phải “máy trả lời đúng”. ChatGPT là công cụ giúp tạo, phân tích và giải quyết công việc nhanh hơn — với điều kiện bạn giao việc rõ và kiểm những gì quan trọng.**
