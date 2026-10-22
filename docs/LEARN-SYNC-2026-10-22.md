# Learn Sync — Đồng bộ chương trình ngày 2026-10-22

> **Phạm vi hoàn thành của đợt này:** đề cương, bản đồ nguồn, điều kiện tính năng, điều hướng và trạng thái biên soạn.
> **Không phải:** phát hành toàn bộ bài M02–M11, kiểm thử mọi tính năng, hoàn tất pilot hoặc xác nhận tài khoản có các tính năng mới.

## 1. Nguồn và mốc thời gian

Đã đọc [ChatGPT Learn](https://learn.chatgpt.com/docs), [index](https://learn.chatgpt.com/docs/llms.txt), các trang tính năng được liệt kê tại [Official Sources](../OFFICIAL-SOURCES.md), [What's new](https://learn.chatgpt.com/docs/whats-new) và [Changelog](https://learn.chatgpt.com/docs/changelog).

Tại lần đọc ngày 2026-10-22, mục tuần gần nhất nhìn thấy trên What's new là **October 12–16, 2026**; mục changelog đầu trang là **2026-10-14**. Không gọi ngày rà soát là ngày ra mắt tính năng. Không tuyên bố đã duyệt mọi trang nằm trong index.

## 2. Những điều thay đổi trong chương trình

| Phần | Điều chỉnh | Nguồn |
|---|---|---|
| BOOT / M00 / M01 | Giữ thứ tự dễ học; giao việc theo kết quả, ngữ cảnh, đầu ra và ranh giới; không biến prompting thành công thức bắt buộc | [Use ChatGPT](https://learn.chatgpt.com/docs/use-chatgpt), [Prompting](https://learn.chatgpt.com/docs/prompting) |
| M02 | Chọn model/mức suy luận bằng benchmark của chính người học; không học thuộc danh sách model | [Model selection](https://learn.chatgpt.com/docs/model-selection) |
| M03 | Tách chat, Project, local project, memory, file và dữ liệu kết nối; nhận biết Space nhưng học riêng | [Projects](https://learn.chatgpt.com/docs/projects), [Personalize](https://learn.chatgpt.com/docs/personalize) |
| M04 | Giữ Deep Research; làm rõ kế hoạch, phạm vi nguồn, quyền đọc của app và phương án nghiên cứu thủ công | [Deep research](https://help.openai.com/en/articles/10500283-deep-research-in-chatgpt) |
| M05 | Sản phẩm file phải có đầu vào, định dạng, preview và phép kiểm; phương tiện khác nhau có cách review khác nhau | [Work with files](https://learn.chatgpt.com/docs/artifacts-viewer) |
| M06 | Thêm phân biệt local/cloud, bước cần máy online, theo dõi tác vụ và quyền trước khi chạy | [Work](https://learn.chatgpt.com/docs/get-started-with-work), [Permissions](https://learn.chatgpt.com/docs/permission-modes) |
| M07 / M08 | Tách tool, skill, plugin, kết nối và lịch chạy; sự kiện chỉ khi sản phẩm/app hỗ trợ | [Skills & Plugins](https://learn.chatgpt.com/docs/skills-and-plugins), [Tasks](https://learn.chatgpt.com/docs/automations) |
| M09–M11 | Bổ sung định tuyến tới AGENTS.md, môi trường local/cloud, worktrees, review và security; API đọc thêm Developer Docs | [Learn index](https://learn.chatgpt.com/docs/llms.txt) — các trang kỹ thuật phải được đọc lại khi viết lesson |
| X01–X04 | Bổ sung dots, Space, Sites và quản trị; có prerequisite và fallback; không chặn phần cốt lõi | Các nguồn ở từng chuyên đề bên dưới |

### Model snapshot — Chỉ để biết thay đổi, không để học thuộc

[Model selection](https://learn.chatgpt.com/docs/model-selection) hiện nêu Astra, GPT-6.1 Sol và Luna; khả năng chọn thực tế phụ thuộc sản phẩm/model version/tài khoản. Giữ nguyên đề bài benchmark khi so sánh, rồi chọn phương án nhẹ nhất đạt tiêu chí của mình. Không suy model nào có sẵn chỉ từ tên gói.

Theo [Models](https://learn.chatgpt.com/docs/models) và [Changelog](https://learn.chatgpt.com/docs/changelog), GPT-5.5 ngừng trên **Codex đăng nhập bằng ChatGPT** từ **2026-10-14 19:00 UTC**. Thông báo này không áp dụng cho OpenAI API hoặc phiên Codex xác thực bằng API key. Đây là ví dụ đọc đúng phạm vi thông báo, không là hướng dẫn bắt buộc đổi model cho người đang học BOOT.

## 3. X01 — dots: giao trách nhiệm liên tục

**Status:** PLANNED. **Prerequisite:** M06–M08. **Nguồn đã đọc:** [Meet dots](https://learn.chatgpt.com/docs/dots); các hướng dẫn setup/control cần kiểm lại trước lesson.

**Mục tiêu:** phân biệt câu hỏi một lần, việc theo lịch và trách nhiệm liên tục; xác định đầu vào, quyền, giới hạn và lúc cần hỏi người dùng. Learn mô tả dots đang rollout dần; không coi việc chưa có dots là lỗi người học.

**Lab dự kiến:** thiết kế nhiệm vụ tổng hợp thay đổi từ một tập nguồn thử. Viết rõ điều gì đáng báo, điều gì không gửi, hành động bị cấm và cách dừng. Chỉ chạy thật khi đã xác minh quyền, nguồn và điều kiện.

**Evidence/đánh giá dự kiến:** bản giao trách nhiệm, ít nhất 3 tình huống (không có thay đổi, có thay đổi, nguồn lỗi), cách báo lỗi và dừng. Có quyền thì bổ sung kết quả chạy thật đã kiểm. Không có quyền: ghi DESIGN ONLY, không nhận đã vận hành dots.

**Từ vựng:** responsibility — trách nhiệm; escalation — chuyển vấn đề cần quyết định cho người; stop condition — điều kiện dừng.

## 4. X02 — Space: Pages, nguồn và cộng tác

**Status:** PLANNED. **Prerequisite:** M03, M05, M07.2. **Nguồn:** [ChatGPT Space](https://learn.chatgpt.com/docs/space).

**Mục tiêu:** tổ chức một trang tổng hợp, sửa cùng AI và kiểm phạm vi chia sẻ. Phân biệt workspace của tài khoản, space nhóm nội dung và page là tài liệu. Không gọi Space là tên mới của Projects.

**Lab dự kiến:** tạo trang học tập từ dữ liệu giả lập, giữ link nguồn và phân vai người xem/người sửa. So sánh link tới file nguồn với đoạn nội dung sao chép vào trang: quyền của link gốc không tự bảo vệ nội dung đã chép.

**Evidence/đánh giá dự kiến:** trang có nguồn, lịch sử sửa và ma trận quyền; kiểm hai tình huống người có/không có quyền. Chưa có tính năng: trang Markdown và bản thiết kế quyền, ghi DESIGN ONLY; không thử cấp quyền cho người thật khi chưa được phép.

**Từ vựng:** page — trang tài liệu; collaborator — người cộng tác; permission — quyền truy cập/hành động.

## 5. X03 — Sites: website và công cụ nhỏ

**Status:** PLANNED. **Prerequisite:** M05–M07. **Nguồn:** [Sites](https://learn.chatgpt.com/docs/sites); hướng dẫn data/publish cần đọc lại trước khi triển khai.

**Mục tiêu:** từ mô tả nhu cầu tới bản mẫu có thể kiểm; tách tạo, preview, lưu dữ liệu và xuất bản. Quyền và giới hạn thực tế phải kiểm trước buổi thực hành.

**Lab dự kiến:** bản mẫu Website Stack Builder hoặc bộ tra cứu thuật ngữ từ dữ liệu giả lập. Có trường nhập, trường hợp thiếu dữ liệu, kết quả và nguồn. Không dùng dữ liệu khách hàng, không kết nối tài khoản thật hoặc xuất bản tự động.

**Evidence/đánh giá dự kiến:** brief, bản mẫu, tối thiểu 5 ca kiểm, danh sách người được xem và bước duyệt xuất bản. Chưa có Sites: mockup hoặc bản HTML riêng; không ghi đã deploy. Bản mẫu không chứng minh có người dùng hay doanh thu.

**Từ vựng:** prototype — bản mẫu; publish — xuất bản; access — quyền/khả năng truy cập.

## 6. X04 — Workspace administration: quản trị theo vai trò

**Status:** PLANNED. **Prerequisite:** M07–M08; chỉ thực hành admin khi có quyền hợp lệ.

**Nguồn định tuyến:** [Administration](https://learn.chatgpt.com/docs/administration), [Team Tasks](https://learn.chatgpt.com/docs/enterprise/teams), [Workspace connections](https://learn.chatgpt.com/docs/enterprise/shared-connections), [Agent Security](https://learn.chatgpt.com/docs/enterprise/agent-security). Đợt này mới xác nhận vị trí trong Learn index; chưa QA hướng dẫn thao tác quản trị.

**Mục tiêu:** hiểu vai trò, kết nối, chính sách, quyền và log; biết câu hỏi nào cần quản trị viên. Không yêu cầu nâng gói hoặc xin quyền admin để học phần thiết kế.

**Lab dự kiến:** thiết kế ma trận quyền cho nhóm giả lập gồm owner, người tạo workflow và người chỉ xem; chọn nguồn dữ liệu, hành động được phép và quy trình thu hồi quyền. Không thay đổi workspace thật.

**Evidence/đánh giá dự kiến:** ma trận quyền, checklist triển khai/thu hồi, ít nhất 3 tình huống vượt quyền và cách xử lý. Thực hành thật chỉ sau khi có môi trường thử, quyền và tiêu chí duyệt.

**Từ vựng:** workspace — không gian làm việc; role — vai trò; audit — kiểm tra lịch sử hoạt động.

## 7. Bảo toàn tiến độ và phạm vi phát hành

Giữ nguyên 56 ID cốt lõi; không sửa `PROGRESS.md` hoặc evidence người học. BOOT.1–BOOT.2 vẫn PASS, BOOT.3 IN PROGRESS; không reset và không tự cấp PASS. M00/M01 chưa được coi là đã học chỉ vì bài giảng đã tồn tại.

Giữ **11 READY / 45 PLANNED** và ngày source/QA lịch sử của từng bài. X01–X04 là bốn chuyên đề PLANNED ngoài số 56, chưa có bài hoàn chỉnh. Chỉ bổ sung tiến độ chuyên đề khi người học chọn và bài được phát hành.

Giữ **Vocabulary-first**: giải thích và prompt tiếng Việt; English Recognize + Understand; English Use DEFERRED. Bài tham khảo hoặc mẫu cũ có yêu cầu viết tiếng Anh không trở thành điều kiện PASS của người học hiện tại.

Pilot đã bắt đầu ở BOOT theo PROGRESS, nhưng P3 release gate chưa hoàn tất. Không dùng cập nhật chương trình để tuyên bố v0.2.0 đã release hoặc đã validated toàn khóa.

## 8. Việc biên soạn tiếp theo — Chưa hoàn thành trong đợt này

| Ưu tiên | Việc cần làm | Điều kiện hoàn thành |
|---|---|---|
| 1 | Tiếp tục pilot BOOT.3 → BOOT.4 → M00 → M01 | Evidence thật; xử lý blocker, retest, ghi quyết định gate |
| 2 | Viết M02–M04 theo đề cương và nguồn mới | Lesson + từ vựng + lab + đáp án + rubric + QA; không chỉ README |
| 3 | Viết M05–M08 với kiểm availability | Phân biệt thiết kế/mô phỏng/vận hành thật; có fallback an toàn |
| 4 | Viết M09–M11 khi tới nhánh Builder | Kiểm phiên bản SDK/API, môi trường, quyền, chi phí và tests |
| 5 | Viết X01–X04 theo nhu cầu | Không chặn bài cốt lõi; nguồn và điều kiện phải kiểm lại |

[Update Plan](UPDATE-PLAN.md) giữ lịch sử U01–U14. Tài liệu này bổ sung phạm vi đồng bộ mới, không đánh dấu các gói triển khai cũ là hoàn tất.

## 9. Checklist review của đợt đồng bộ

- Không đổi mã bài, evidence hoặc trạng thái học; kiểm lại diff và blob PROGRESS trước/sau khi đưa lên nhánh chính.
- Không nâng PLANNED thành READY, không sửa ngày QA cũ thành ngày hôm nay.
- Đường học trong README/START-HERE/CURRICULUM cùng trỏ tới BOOT.3 cho người học hiện tại.
- Phân biệt nguồn đã đọc với nguồn chỉ định tuyến; không tuyên bố kiểm thử UI/API.
- Nội dung mới có nguồn, điều kiện truy cập, prerequisite, sản phẩm mục tiêu và fallback.
- Chưa chạy bộ kiểm thử sản phẩm hoặc pilot đầu-cuối trong đợt này. Review tài liệu không thay thế những kiểm thử đó.
