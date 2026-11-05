# Learn Sync — Bản rà soát ngày 2026-11-05

> **Phạm vi:** cập nhật thông tin mới kể từ [bản đồng bộ 2026-10-22](LEARN-SYNC-2026-10-22.md), không viết lại hoặc tái QA toàn bộ 56 bài học.
> **Tài liệu đã đọc:** ChatGPT Learn What's New, Changelog, Models, Model Selection và Meet dots vào ngày 2026-11-05.
> **Giới hạn:** Không kiểm thử khả năng truy cập trên tài khoản người học; tính năng có thể khác theo gói, khu vực, workspace và rollout.

## 1. Thông tin mới có căn cứ

| Mốc sự kiện | Thay đổi được nguồn xác nhận | Phạm vi / lưu ý |
|---|---|---|
| 2026-10-26 | **GPT-6.1 Terra** xuất hiện trong ChatGPT Work và Codex, tập trung vào xử lý hình ảnh, màn hình, viết rõ ràng và computer use. | Changelog nêu Plus, Pro, Business, Enterprise, Edu; **không có trong Chat**. Doanh nghiệp còn phụ thuộc workspace/admin. |
| 2026-10-26–30 | **Nhắn tin với dot** qua iMessage hoặc RCS trên Android, gồm văn bản, ảnh và tin nhắn thoại. | Beta đang triển khai cho **ChatGPT Pro tại Mỹ**. Không khẳng định hỗ trợ tại Việt Nam hoặc cho mọi tài khoản. |
| 2026-10-23 | **Codex CLI 0.164.0:** có /presets, chọn model và permission profile nhanh trong terminal. | Chỉ áp dụng Codex CLI tương ứng; không phải yêu cầu của BOOT. |
| 2026-10-27 | **Codex CLI 0.165.0:** cập nhật model catalog, thay đổi reasoning effort trong hội thoại khi model hỗ trợ, cùng sửa lỗi quyền/điều phối. | Tham chiếu CLI, không coi là thay đổi cách lưu Memory của ChatGPT Chat. |
| 2026-10-29 | **Codex CLI 0.166.0:** thêm Terra trong một số catalog, `codex queue --resume`, `codex doctor --network-only` và cải tiến giải thích safety block. | Thực hành khi M09 được phát hành và có CLI/môi trường phù hợp. |
| 2026-10-27 | **ChatGPT iOS 1.2026.293:** phát âm thanh/video trực tiếp trong câu trả lời và mở hội thoại subagent từ task activity. | Thông tin phiên bản iOS, không khẳng định đã có trên web/Android. |

**Mốc gần nhất quan sát:** What's New hiển thị tuần **2026-10-26–30**, Changelog bắt đầu bằng bản **2026-10-29** tại lần kiểm 2026-11-05. Không suy rằng OpenAI không có thông báo khác hoặc mọi tài khoản đã nhận tính năng.

## 2. Điều chỉnh lộ trình học

| Module / nhánh | Thay đổi áp dụng | Bài thực hành đề xuất khi viết lesson |
|---|---|---|
| M02 Models & reasoning | Thêm Terra là **ví dụ có ngày** trong Work/Codex, so sánh với Sol trên cùng bài đầu vào; giữ benchmark theo năng lực thật. | So hai model hiện có trên bài đọc biểu đồ hoặc tóm tắt ảnh; ghi chất lượng, thời gian, mức sử dụng, và model nào thực sự khả dụng. |
| M05 Files & multimodal | Nhắc âm thanh/video trong phản hồi iOS có điều kiện; không biến phiên bản ứng dụng thành kiến thức phải học thuộc. | Kiểm đối chiếu bản phiên âm/chú thích với clip mẫu nếu có tính năng, nếu không dùng văn bản. |
| M06 Work/Computer Use | Giải thích Terra cho tác vụ có màn hình và thao tác máy; không gộp Work với Chat; giữ quy trình duyệt quyền. | Đặt brief đọc screenshot, kiểm đầu ra trên dữ liệu giả và dừng trước thao tác chia sẻ/xuất bản. |
| M09 Codex & GitHub | Khi viết lesson CLI, cân nhắc `/presets`, đổi model/mức suy luận, `queue --resume` và kiểm lỗi mạng. | Thử trên môi trường có CLI phù hợp; lưu output command và quyền của sandbox; không nhận đã chạy nếu chỉ đọc. |
| X01 dots | Bổ sung kênh iMessage/RCS **Beta tại Mỹ**; không yêu cầu người học Việt Nam có quyền hoặc dùng iMessage. | Thiết kế kênh báo cáo trong ChatGPT, ghi lựa chọn thay thế khi SMS chưa khả dụng. |

**Giữ nguyên:** BOOT.1/BOOT.2 đã PASS, BOOT.3 IN PROGRESS; thứ tự BOOT → M00 → M01; 56 core lessons (11 READY / 45 PLANNED), 4 optional topics X01–X04 đều PLANNED; hướng học English Vocabulary-first (Recognize + Understand), English prompt writing DEFERRED.

## 3. Nguồn trực tiếp

- [What's New — ChatGPT Learn](https://learn.chatgpt.com/docs/whats-new) — tuần 26–30/10, Terra và nhắn tin dots; kiểm 2026-11-05.
- [ChatGPT & Codex Changelog](https://learn.chatgpt.com/docs/changelog) — các mốc 23, 26, 27, 29/10/2026; kiểm 2026-11-05.
- [Models](https://learn.chatgpt.com/docs/models) — đối tượng áp dụng của Astra, Sol, Terra, Luna; kiểm 2026-11-05.
- [Model Selection](https://learn.chatgpt.com/docs/model-selection) — ví dụ so Terra với Sol theo cùng input và mức suy luận; kiểm 2026-11-05.
- [Meet dots](https://learn.chatgpt.com/docs/dots) — tin nhắn iMessage/RCS và giới hạn rollout; kiểm 2026-11-05.

## 4. Phân biệt nội dung đã hoàn thành

Đã thực hiện: rà soát nguồn công khai, cập nhật bản đồ module, bổ sung cảnh báo quyền/rollout và ghi lại báo cáo này.

**Chưa thực hiện:** chạy benchmark Terra, kiểm thử iOS/dots/CLI trên thiết bị người học, viết lại toàn bộ bài M02–M11, phát hành X01, hoàn thành U06 pilot. Tránh mô tả nhầm nguồn đã đọc là kiểm thử sản phẩm.

## 5. Checklist lần đồng bộ sau

1. Đọc What's New, Changelog, Models và các trang tính năng có thay đổi; phân biệt ngày đăng, ngày sự kiện và ngày kiểm nguồn.
2. So với báo cáo gần nhất; chỉ giữ những gì ảnh hưởng tới chương trình, khả năng truy cập, an toàn hoặc workflow.
3. Ghi rõ module, rủi ro bị lỗi thời, điều kiện tài khoản và bài thực hành cần sửa; kiểm thêm Help Center khi có thông báo thay đổi model/availability.
4. Cập nhật tài liệu và tạo commit khi GitHub cho phép; kiểm commit, các liên kết nguồn và trạng thái của PROGRESS.
5. Báo cáo tiếng Việt những gì đã thay đổi, không có thay đổi hoặc những gì chưa thể kiểm.

**Bảo toàn:** không sửa PROGRESS.md, không tự chuyển PLANNED thành READY và không tự đặt PASS.
