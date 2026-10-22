# Feature Availability — Kiểm điều kiện tính năng

> **Rà soát tài liệu:** 2026-10-22. **Kiểm thử trên tài khoản người học:** chưa thực hiện trong đợt cập nhật này.
> Không suy ra quyền truy cập từ việc một tính năng xuất hiện trong Learn hoặc từ tên gói tài khoản.

## Ba câu hỏi khác nhau

**Có tài liệu không?** Kiểm nguồn chính thức. **Tài khoản có dùng được không?** Kiểm surface, phiên bản ứng dụng, workspace, rollout, quyền và giới hạn. **Bài học đã READY chưa?** Kiểm [Content Status](CONTENT-STATUS.md). Ba câu trả lời có thể khác nhau.

## Ma trận kiểm trước khi học

| Năng lực | Cần kiểm trực tiếp | Tình trạng trong đợt này | Phương án thay thế |
|---|---|---|---|
| Chat / prompting | Mở chat và gửi yêu cầu văn bản | Có evidence học BOOT.1–BOOT.2 trước đây; không thử lại UI hôm nay | Yêu cầu văn bản và ghi chú riêng |
| Model / reasoning | Tên model đang có, mức suy luận, giới hạn theo surface | Đã đọc Models/Model selection; chưa thử bộ chọn của người học | Một model, nhiều cách giao việc; ghi đúng phạm vi benchmark |
| Projects / memory | Project sources, instructions, các lựa chọn memory | Đã đọc Projects/Personalize; quyền tài khoản chưa xác minh | Context pack với file giả lập |
| Search / Deep Research | Công cụ có sẵn, phạm vi nguồn, quota, quyền đọc app | Đã đọc Deep Research; chưa chạy trên tài khoản | Mở nguồn chính thức, nghiên cứu thủ công và ghi nguồn |
| Files / images / voice | Định dạng, dung lượng, preview, thiết bị và quyền | Đã đọc Work with files; các khả năng khác cần kiểm theo bài | Text, ảnh mẫu hoặc transcript |
| Work / local / cloud | Nơi chạy, nguồn file, quyền local, kết nối máy và trạng thái tác vụ | Đã đọc Work; không khẳng định mọi tài khoản có sync | Task brief nhiều bước và mô phỏng có nhãn |
| Browser / Computer Use | Công cụ, phiên đăng nhập, quyền website/ứng dụng, điểm duyệt | Chưa thử; phải kiểm trước lab | Screenshot hoặc thao tác thủ công do người học thực hiện |
| Plugins / skills | Plugin được phép cài, tài khoản kết nối, hành động đọc/ghi | Đã đọc định nghĩa; không tự cài hoặc cấp quyền trong đợt này | Quy trình và dữ liệu giả lập |
| Scheduled Tasks | Loại lịch/sự kiện được hỗ trợ, múi giờ, nguồn, trạng thái run, nơi chạy | Đã đọc Tasks; không tạo lịch tự động trong đợt này | Automation spec; không nhận đã có run thật |
| dots | Quyền truy cập, rollout, workspace và điều khiển dừng | Learn ghi đang triển khai dần; tài khoản chưa xác minh | Bản giao trách nhiệm; X01 không bắt buộc |
| Space | Trang/space có sẵn, người được xem, nguồn liên kết và nội dung sao chép | Đã đọc Space; chưa thử chia sẻ | File riêng hoặc trang Markdown với ma trận quyền |
| Sites | Quyền tạo, host, chia sẻ, mức dùng và người truy cập | Đã đọc Sites; chưa xuất bản gì | Bản mẫu riêng với dữ liệu giả lập |
| Codex / API / MCP | Client/runtime, repo, sandbox, key/quota hoặc phương thức xác thực | Chưa kiểm thử thực thi; tra nguồn đúng surface trước bài | Kiến trúc và eval cases; không thay evidence triển khai thật |
| Workspace administration | Vai trò admin, chính sách tổ chức và kết nối được phép | Chỉ là chuyên đề tùy chọn PLANNED | Thiết kế ma trận quyền, không đổi thiết lập thật |

## Maturity không đồng nghĩa availability

Theo [Feature Maturity](https://learn.chatgpt.com/docs/feature-maturity), tài liệu phân biệt Under development, Experimental, Beta, Stable và Deprecated. Đọc nhãn của tính năng cụ thể; không tự gán Stable khi trang không nói. Không dùng tính năng Under development; tránh bắt đầu mới trên hướng Deprecated; tính năng thử nghiệm phải có giới hạn và phương án quay lui.

## Những ranh giới cần nhớ

[Work](https://learn.chatgpt.com/docs/get-started-with-work): local/cloud và khả năng tiếp tục qua thiết bị tùy môi trường. Bước cần tài nguyên máy cá nhân có thể cần máy đó online; không suy “cloud” thành truy cập mọi file local.

[Tasks](https://learn.chatgpt.com/docs/automations): tác vụ web không mặc nhiên làm việc trong thư mục máy cá nhân. Khi lịch cần file local, phải đáp ứng điều kiện chạy local. Không suy mọi sự kiện của mọi plugin đều tạo được trigger.

[Permissions](https://learn.chatgpt.com/docs/permission-modes): phạm vi sandbox và cơ chế duyệt hành động là hai việc khác nhau. Tự động review không đồng nghĩa mở rộng quyền hoặc đảm bảo an toàn tuyệt đối.

[Space](https://learn.chatgpt.com/docs/space): link nguồn giữ quyền gốc, nhưng nội dung chép/tóm tắt vào trang được nhìn thấy bởi người có quyền xem trang. Luôn kiểm đối tượng nhận trước khi chia sẻ.

## Mẫu ghi evidence môi trường

```text
Ngày kiểm tra:
Surface: web / desktop / mobile / CLI / IDE / cloud
Ứng dụng và phiên bản nếu biết:
Workspace: cá nhân / tổ chức (không ghi định danh nhạy cảm)
Tính năng cần dùng:
Quan sát thực tế:
Nguồn chính thức và ngày đọc:
Quyền đọc/ghi; giới hạn tác vụ:
Kết quả: VERIFIED IN THIS ENVIRONMENT / NOT AVAILABLE / NOT VERIFIED
Phương án thay thế: LIVE / SIMULATED / DESIGN ONLY
Bằng chứng đã làm sạch:
```

Không nâng bài yêu cầu vận hành thật thành PASS khi chỉ mô phỏng. Có thể ghi nhận riêng năng lực thiết kế. Không yêu cầu mua gói hoặc xin quyền admin để qua BOOT–M01. Không lưu secret, cookie, dữ liệu tài khoản hoặc ảnh chưa làm sạch lên repo.
