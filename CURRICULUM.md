# Curriculum — Chương trình học ChatGPT

> **Curriculum nền:** 2026-10-22. **Cập nhật thông tin mới nhất:** 2026-11-05, xem [Learn Sync 2026-11-05](docs/LEARN-SYNC-2026-11-05.md). Ngày rà soát không phải ngày phát hành sản phẩm hay QA toàn bộ lesson.
> **Phạm vi:** giữ 56 bài cốt lõi (4 BOOT + 52 bài M00–M11), bổ sung 4 chuyên đề tùy chọn ở trạng thái PLANNED.
> **Publication status:** có đề cương không có nghĩa đã có bài giảng. Xem [Content Status](docs/CONTENT-STATUS.md).
> **Tiến độ cá nhân:** chỉ lấy từ [PROGRESS.md](PROGRESS.md); cập nhật chương trình không làm thay đổi PASS.

## Ngôn ngữ và cách học

Giải thích, prompt, bài tập, phản hồi và kiểm chứng dùng **tiếng Việt**. Giữ tên tiếng Anh chuẩn kèm giải nghĩa dễ hiểu. English track hiện là **Vocabulary-first: Recognize + Understand** — nhận diện và hiểu từ vựng. Viết câu/prompt tiếng Anh là **DEFERRED**, không bắt buộc và không chặn PASS. Không tự tăng yêu cầu tiếng Anh khi chuyển chặng.

Mỗi bài: đọc → giải thích lại → thực hành → kiểm chứng → lưu bằng chứng → rút kinh nghiệm. Không đánh giá bằng việc đã đọc, lời AI tự xác nhận hoặc số tính năng đã bật.

**Đường học hiện tại:** tiếp tục BOOT.3 → BOOT.4 → M00 → M01 → ba guided labs → M01 Check. Chỉ chuyển sang bài đã READY. M02–M11 là đề cương triển khai tiếp; chưa phải toàn bộ khóa học đã hoàn thiện.

## Bản đồ với ChatGPT Learn

| Nhóm tài liệu Learn | Đặt trong chương trình |
|---|---|
| Get started / Foundations | BOOT, M00, M01, M02; phần nền tảng của M03, M07, M08 |
| Features / Workflows | M03–M08; dots, Space, Sites ở nhánh tùy chọn |
| Configuration | M03, M06.5, M09.2; cấu hình nâng cao học sau nền tảng |
| Developers | M09–M11; API dùng thêm OpenAI Developer Docs |
| Security | BOOT.3, M06.5, M07.2, M09.5, M11 |
| Administration | Chuyên đề X04; không bắt người mới có quyền quản trị |
| Use cases / Resources / Training | Nguồn gợi ý lab; không thay thế bằng chứng thực hành |

Nguồn và thay đổi chi tiết: [Official Sources](OFFICIAL-SOURCES.md), [Learn Sync 2026-10-22](docs/LEARN-SYNC-2026-10-22.md). Không biến toàn bộ mục lục tài liệu sản phẩm thành các bài bắt buộc.

## Bổ sung đã xác minh ngày 2026-11-05

| Phần | Delta từ nguồn chính thức | Lưu ý |
|---|---|---|
| M02 / M06 | [GPT-6.1 Terra](https://learn.chatgpt.com/docs/models) cho Work và Codex, tập trung visual reasoning/computer use; so kết quả theo benchmark. | Không áp dụng cho Chat; cần kiểm quyền thực tế. |
| X01 dots | [Nhắn iMessage/RCS](https://learn.chatgpt.com/docs/whats-new) được công bố ở beta cho Pro tại Mỹ. | Không coi có sẵn tại Việt Nam. |
| M09 | [Codex CLI 0.164–0.166](https://learn.chatgpt.com/docs/changelog) mở rộng presets, tiếp tục queue và kiểm lỗi mạng. | Không bắt học CLI trong BOOT hoặc M00. |
| M05 | [ChatGPT iOS 1.2026.293](https://learn.chatgpt.com/docs/changelog) có phát audio/video trực tiếp trong phản hồi. | Tùy thiết bị, phiên bản và rollout. |

Chi tiết nguồn, ngày, phạm vi và các bài thực hành cần bổ sung: [Learn Sync 2026-11-05](docs/LEARN-SYNC-2026-11-05.md). Chưa đổi status lesson hay tiêu chí PASS.

## Stage 0 — Getting started / Khởi động

**Trạng thái:** 4 bài READY; trạng thái học của từng bài nằm trong PROGRESS.

| Bài | Năng lực cần đạt |
|---|---|
| [BOOT.1 — First chat / Cuộc chat đầu tiên](modules/BOOT-getting-started/BOOT.1-first-chat.md) | Gửi yêu cầu tiếng Việt, phân biệt prompt và response. |
| [BOOT.2 — Conversation basics / Hội thoại cơ bản](modules/BOOT-getting-started/BOOT.2-conversation-basics.md) | Tinh chỉnh, rút gọn, đổi định dạng; biết khi nào giữ chat hoặc mở chat mới. |
| [BOOT.3 — Safe use & verification / An toàn và kiểm chứng](modules/BOOT-getting-started/BOOT.3-safe-use-and-verification.md) | Phân biệt claim có/không có bằng chứng; kiểm nguồn; che dữ liệu nhạy cảm. |
| [BOOT.4 — Save evidence / Lưu bằng chứng](modules/BOOT-getting-started/BOOT.4-save-evidence.md) | Lưu yêu cầu, kết quả, phép kiểm và điều học được; không công khai dữ liệu riêng. |

**PASS BOOT:** hoàn thành bốn bài, đạt [BOOT Check](assessments/BOOT-CHECK.md), lưu evidence đã làm sạch. Không cần API, Work, Codex, dots hoặc mua thêm gói để học phần nền tảng.

Nguồn: [Use ChatGPT](https://learn.chatgpt.com/docs/use-chatgpt), [Prompting](https://learn.chatgpt.com/docs/prompting).

## Stage A — Operator / Sử dụng ChatGPT hiệu quả

### M00 — Mental model / Hiểu cách ChatGPT làm việc

**Trạng thái:** 3 bài READY. Giữ các bài nền tảng; phần tính năng mới là nội dung mở rộng, không thêm điều kiện PASS vào bài đã học.

| Bài | Năng lực cần đạt |
|---|---|
| [M00.1 — Chat vs Work vs Codex](modules/M00-mental-model/M00.1-chat-work-codex.md) | Chọn cách làm việc theo mục tiêu; phân biệt surface — bề mặt làm việc, model — mô hình, tool — công cụ. |
| [M00.2 — How ChatGPT works](modules/M00-mental-model/M00.2-how-chatgpt-works.md) | Hiểu context — ngữ cảnh, giới hạn, thông tin có thể sai và nhu cầu kiểm chứng. |
| [M00.3 — Task Brief and Verification](modules/M00-mental-model/M00.3-task-and-verification.md) | Giao việc bằng Outcome → Context → Tools → Verification, kèm ranh giới và điều kiện hoàn thành. |

Nhận biết thêm: dots là hướng giao trách nhiệm liên tục khi tài khoản có quyền; không đồng nhất với một câu trả lời Chat hay Scheduled Task. Thực hành dots để ở X01.

**PASS M00:** [M00 Check](assessments/M00-CHECK.md) ≥16/20; giải thích đúng các khái niệm chính; viết một task brief hoàn chỉnh; kiểm chứng ít nhất một nhận định bằng nguồn, phép tính, test hoặc người review phù hợp.

Nguồn: [Use ChatGPT](https://learn.chatgpt.com/docs/use-chatgpt), [Work](https://learn.chatgpt.com/docs/get-started-with-work).

### M01 — Prompting as task specification / Giao việc rõ ràng

**Trạng thái:** 4 bài READY.

| Bài | Năng lực cần đạt |
|---|---|
| [M01.1 — Prompt Foundations](modules/M01-prompting/M01.1-prompt-foundations.md) | Goal + Context + Output + Boundaries; chỉ thêm phần cần thiết, không ép mọi yêu cầu theo một mẫu dài. |
| [M01.2 — Iterate and Decompose](modules/M01-prompting/M01.2-iterate-and-decompose.md) | Sửa kết quả bằng follow-up có mục tiêu; chia việc ở điểm cần kiểm tra; đổi chat theo mục tiêu. |
| [M01.3 — Output Contracts](modules/M01-prompting/M01.3-output-contracts.md) | Quy định cấu trúc, trường bắt buộc, cách xử lý dữ liệu thiếu và tiêu chí chấp nhận. |
| [M01.4 — Verify Answers](modules/M01-prompting/M01.4-verify-answers.md) | Claim → Evidence → Conclusion; kiểm nguồn, phép tính, giả định và yêu cầu sửa sai. |

**PASS M01:** đủ 5/5 task spec trong [M01 Check](assessments/M01-CHECK.md); ít nhất 4/5 đạt mức 2, phần còn lại ≥1; có kết quả chạy và verification thật cho ít nhất một spec. Học ba lab Summary, Planning, Comparison và [Evaluation Lab](labs/EVALUATION-LAB.md) trước checkpoint.

Nguồn: [Prompting](https://learn.chatgpt.com/docs/prompting).

### M02 — Models & reasoning / Chọn mô hình và mức suy luận

**Trạng thái:** PLANNED.

| Bài | Nội dung cập nhật |
|---|---|
| M02.1 — Model selection | Chọn trong các model tài khoản thực sự có; cân bằng chất lượng, tốc độ và mức sử dụng; ghi ngày và môi trường. |
| M02.2 — Reasoning effort | Mức suy luận khác tên model; thử mức mặc định trước; không coi mức cao nhất là mặc định tốt nhất. |
| M02.3 — Personal benchmark | Cùng đầu vào và rubric cho 5 tác vụ; ghi lỗi, thời gian và mức dùng quan sát được; không bịa chi phí. |

**PASS M02:** benchmark 5 tác vụ và giải thích lựa chọn dựa trên kết quả. Nếu chỉ có một model, so sánh cách giao việc hoặc mức suy luận thực sự được cung cấp; ghi rõ không phải so sánh hai model.

Tên model và thông báo ngừng hỗ trợ nằm trong [bản đồng bộ có ngày](docs/LEARN-SYNC-2026-10-22.md), không phải kiến thức phải học thuộc. Không áp dụng thông báo ngừng một model trên Codex cho mọi API.

Nguồn: [Model selection](https://learn.chatgpt.com/docs/model-selection), [Models](https://learn.chatgpt.com/docs/models).

### M03 — Context, personalization, Projects & Memory

**Trạng thái:** PLANNED.

| Bài | Nội dung cập nhật |
|---|---|
| M03.1 — Context architecture | Phân biệt chat hiện tại, nguồn của Project, file đã tải lên, Library và dữ liệu kết nối; chỉ khẳng định đã đọc nguồn khi có bằng chứng. |
| M03.2 — Personalization & instructions | Tách sở thích bền vững, chỉ dẫn Project và yêu cầu riêng của tác vụ; quyền riêng tư khi dùng dữ liệu cá nhân. |
| M03.3 — Projects & chats | Gom công việc liên quan; một mục tiêu rõ cho mỗi chat; phân biệt ChatGPT Project và thư mục local của Codex. |
| M03.4 — Memory | Dùng cho ngữ cảnh hữu ích, không làm cơ sở dữ liệu hay bằng chứng duy nhất; rà soát, sửa và xóa khi cần. |
| M03.5 — Files as source context | Xác định đúng file/phiên bản/phạm vi; trích dẫn và kiểm quyền truy cập; phân biệt link gốc với nội dung đã sao chép. |

**PASS M03:** một Project có instructions, nguồn và quy tắc tách chat; chứng minh ít nhất một câu trả lời bám đúng tài liệu. Không có Projects thì nộp context pack trên dữ liệu giả lập và ghi giới hạn môi trường.

Nguồn: [Projects](https://learn.chatgpt.com/docs/projects), [Personalize](https://learn.chatgpt.com/docs/personalize). Space học thêm ở X02, không coi Space và Project là một khái niệm.

### M04 — Web Search & Deep Research

**Trạng thái:** PLANNED.

| Bài | Nội dung cập nhật |
|---|---|
| M04.1 — Web Search | Nhận ra câu hỏi cần thông tin mới; xác định truy vấn, ngày kiểm tra và nguồn. |
| M04.2 — Source quality | Phân biệt nguồn gốc và nguồn tổng hợp; so ngày sự kiện với ngày đăng; xử lý nguồn mâu thuẫn. |
| M04.3 — Deep Research | Đặt câu hỏi nghiên cứu, chọn phạm vi nguồn, xem kế hoạch và kiểm báo cáo; không coi mọi plugin đều hỗ trợ nghiên cứu. |
| M04.4 — Research workflow | Question → source plan → evidence → synthesis → verification → decision. |

**PASS M04:** research memo có bảng claim–evidence, giới hạn và phần chưa chắc chắn. Thiếu Deep Research thì thực hiện quy trình bằng search/nguồn chính thức và ghi là phương án thay thế, không ghi đã vận hành Deep Research.

Nguồn: [Web search](https://learn.chatgpt.com/docs/web-search), [Deep research](https://help.openai.com/en/articles/10500283-deep-research-in-chatgpt).

## Stage B — Power User / Làm việc nhiều bước

### M05 — Files & multimodal work / File và nhiều loại đầu vào

**Trạng thái:** PLANNED.

| Bài | Nội dung cập nhật |
|---|---|
| M05.1 — Image inputs | Đọc ảnh, sơ đồ, screenshot; chỉ rõ vùng cần xem; phân biệt quan sát và suy luận. |
| M05.2 — Image generation & editing | Giao yêu cầu hình ảnh, sửa có mục tiêu, kiểm chi tiết và tính nhất quán. |
| M05.3 — Documents, spreadsheets, presentations & PDFs | Đầu vào, loại file, cấu trúc, preview và kiểm đầu ra; kiểm phép tính và quyền chia sẻ, không chỉ nhìn hình thức. |
| M05.4 — Voice | Ghi nhận, tóm tắt và xác nhận lại tên, số, việc cần làm; dùng transcript nếu chưa có voice. |

**PASS M05:** một sản phẩm với ít nhất hai loại đầu vào/đầu ra, có vòng review và bản sửa. Công cụ preview khác theo surface; không coi đường dẫn do AI viết là bằng chứng file đã tồn tại.

Nguồn chính: [Work with files](https://learn.chatgpt.com/docs/artifacts-viewer). Appshots và visualizations là phần mở rộng có kiểm điều kiện, không bắt buộc dùng dữ liệu cá nhân.

### M06 — ChatGPT Work, Browser & Computer Use

**Trạng thái:** PLANNED.

| Bài | Nội dung cập nhật |
|---|---|
| M06.1 — ChatGPT Work | Giao kết quả có thể kiểm tra; xác định nguồn, công cụ, sản phẩm và người review. |
| M06.2 — Long-running work | Điều kiện hoàn thành, điểm kiểm tra, đổi hướng và dừng; phân biệt local/cloud và bước cần máy cá nhân online. |
| M06.3 — Browser vs Web Search | Phân biệt tìm thông tin với tương tác website/phiên đăng nhập; không hứa truy cập khi chưa có công cụ hoặc quyền. |
| M06.4 — Computer Use | Chọn khi thật sự cần thao tác giao diện; giới hạn ứng dụng/thư mục; dừng trước bước có tác động bên ngoài. |
| M06.5 — Permissions & sandboxing | Quyền tối thiểu; phân biệt phạm vi sandbox với cách duyệt hành động; kiểm trạng thái quyền thực tế. |

**PASS M06:** brief nhiều bước có lựa chọn môi trường, quyền, checkpoint và cách xác minh kết quả. Mô phỏng phải ghi SIMULATED; không nhận là đã chạy công cụ thật.

Nguồn: [Work](https://learn.chatgpt.com/docs/get-started-with-work), [Permissions](https://learn.chatgpt.com/docs/permission-modes). Việc một sản phẩm hỗ trợ chạy nền không có nghĩa mọi chat đều tự chạy tiếp sau khi trả lời.

### M07 — Plugins & connected data / Kết nối công cụ và dữ liệu

**Trạng thái:** PLANNED.

| Bài | Nội dung cập nhật |
|---|---|
| M07.1 — Built-in tool vs Plugin | Phân biệt công cụ có sẵn và gói cài thêm; plugin có thể chứa skill và MCP server, không chỉ là kết nối tài khoản. |
| M07.2 — Permissions & data boundaries | Quyền của tài khoản nguồn, quyền workspace và quyền công cụ; phân biệt đọc, sửa, chia sẻ; phòng lộ dữ liệu. |
| M07.3 — Connected workflow design | Thiết kế việc qua hai hệ thống như Drive/Gmail/Calendar/GitHub; kiểm đối tượng, phạm vi và dữ liệu mới nhất. |
| M07.4 — Human-in-the-loop actions | Tách đọc → nháp → sửa → gửi/xuất bản; kiểm danh tính đích, diff và khả năng hoàn tác. |

**PASS M07:** workflow qua hai hệ thống có sơ đồ dữ liệu, quyền và điểm review. Ưu tiên dữ liệu giả lập hoặc môi trường thử; không tự gửi thư, chia sẻ hay sửa dữ liệu thật chỉ để chứng minh PASS.

Nguồn: [Skills & Plugins](https://learn.chatgpt.com/docs/skills-and-plugins). Build plugins và migration custom GPTs là nhánh Builder, không yêu cầu chuyển đổi tài khoản hiện tại trong bài nhập môn.

### M08 — Skills & Scheduled Tasks / Quy trình tái sử dụng và tự động hóa

**Trạng thái:** PLANNED.

| Bài | Nội dung cập nhật |
|---|---|
| M08.1 — Skill vs Plugin | Skill đóng gói hướng dẫn/tài nguyên; plugin đóng gói năng lực có thể cài; cả hai khác lịch chạy. |
| M08.2 — Designing a reusable Skill | Một nhiệm vụ rõ, điều kiện kích hoạt, quy trình, mẫu đầu ra, nguồn và cách kiểm; thử cả trường hợp không nên kích hoạt. |
| M08.3 — Scheduled Tasks | Một lần, lặp lại, điều kiện hoặc sự kiện được hỗ trợ; kiểm múi giờ, nguồn, quyền, trạng thái và kết quả từng lượt. |
| M08.4 — Automation reliability | Chống chạy trùng, ghi trạng thái, retry có giới hạn, giảm thông báo thừa, báo lỗi và nút dừng. |
| M08.5 — Evaluate before automate | Chạy thủ công và đối chiếu trước; lập bộ ca thử; không coi cấu hình lịch là bằng chứng lịch đã chạy. |

**PASS M08:** một workflow thủ công đã kiểm, bản đặc tả tái sử dụng và automation spec có điều kiện dừng. Nếu có quyền chạy thật, lưu một run và phép kiểm; nếu không, chỉ ghi đạt phần thiết kế. dots ở X01; không đồng nhất scheduled task với tác nhân luôn hoạt động.

Nguồn: [Skills & Plugins](https://learn.chatgpt.com/docs/skills-and-plugins), [Scheduled tasks](https://learn.chatgpt.com/docs/automations).

## Stage C — Builder / Xây dựng hệ thống, học sau nền tảng

### M09 — Codex & GitHub

**Trạng thái:** PLANNED.

| Bài | Nội dung cập nhật |
|---|---|
| M09.1 — Codex surfaces | Chọn desktop, CLI, IDE hoặc cloud theo việc và quyền thực tế; kiểm môi trường Windows trước khi thực hành. |
| M09.2 — Repository context | README, AGENTS.md, tests, conventions và phạm vi thay đổi; phân biệt chỉ dẫn repo với memory. |
| M09.3 — Coding task specification | Bugfix, feature, refactor; đầu vào, tiêu chí và test chấp nhận; thay đổi nhỏ có thể review. |
| M09.4 — GitHub workflow | Issue → branch → commit → PR → review → CI; phân biệt kết quả test với độ đúng toàn hệ thống. |
| M09.5 — Safe autonomous coding | Môi trường local/cloud, worktree cách ly, quyền, kiểm diff/test và rollback; security scan chỉ khi được phép. |

**PASS M09:** một thay đổi nhỏ có test, diff và commit/PR evidence thật. Không nhận PASS triển khai bằng bản thiết kế. Cloud environments, Code Review và Codex Security được kiểm availability trước khi thêm vào lab.

Nguồn định tuyến: [Learn Developers](https://learn.chatgpt.com/docs/developers), [Codex CLI](https://learn.chatgpt.com/docs/codex/cli), [Code review](https://learn.chatgpt.com/docs/code-review).

### M10 — API, MCP & Agents

**Trạng thái:** PLANNED; nhánh kỹ thuật mở rộng, không phải điều kiện dùng ChatGPT hiệu quả.

| Bài | Nội dung cập nhật |
|---|---|
| M10.1 — ChatGPT vs API mental model | Phân biệt sản phẩm, tài khoản, quyền và chi phí; không suy quyền API từ gói ChatGPT. |
| M10.2 — Responses API & tools | Đọc API hiện hành trước khi code; trạng thái hội thoại, gọi công cụ, đầu ra có cấu trúc và xử lý lỗi. |
| M10.3 — MCP & connectors | Hợp đồng công cụ/dữ liệu, xác thực và quyền; không đồng nhất chuẩn MCP với mọi implementation. |
| M10.4 — Agents SDK | Điều phối, guardrails, trạng thái và quan sát; so với giải pháp đơn giản hơn; đọc thêm Codex SDK/App Server khi phù hợp. |
| M10.5 — Evals | Ít nhất 5 ca đánh giá gồm thành công, thiếu dữ liệu, lỗi công cụ và yêu cầu vượt quyền. |

**PASS M10:** kiến trúc và ≥5 eval cases; phần triển khai API chỉ học khi có môi trường và ngân sách được xác nhận. Không đưa API key, token hay cookie vào repo.

Nguồn: [OpenAI Developer Docs](https://developers.openai.com/), [MCP trong Learn](https://learn.chatgpt.com/docs/extend/mcp). Các API/SDK cần đối chiếu lại phiên bản khi biên soạn bài chi tiết; đợt đồng bộ này không tuyên bố đã kiểm thử API.

### M11 — Agentic system design / Thiết kế hệ thống tác nhân

**Trạng thái:** PLANNED.

| Bài | Nội dung cập nhật |
|---|---|
| M11.1 — Workflow before agent | Chọn quy trình xác định khi đủ dùng; chỉ thêm agent khi lợi ích có thể đo được. |
| M11.2 — State, tools & boundaries | Nơi giữ trạng thái, hợp đồng công cụ, dữ liệu tin cậy/không tin cậy và phạm vi quyền. |
| M11.3 — Human review architecture | Điểm duyệt theo rủi ro, chi phí và khả năng hoàn tác; dừng trước tác động không được phép. |
| M11.4 — Observability & improvement loop | Logs, traces, lỗi, evals, phản hồi và phiên bản; không lưu secret trong log. |
| M11.5 — Production readiness | Độ tin cậy, bảo mật, chi phí, giới hạn, fallback và điều kiện dừng; không coi demo thành công là sẵn sàng vận hành. |

**PASS M11:** review thiết kế capstone với failure cases và tiêu chí cho phép/chưa cho phép triển khai. Tài liệu Security/Administration của Learn là đầu vào; không mặc định người học là quản trị viên.

## Nhánh tùy chọn — Theo tính năng và nhu cầu

Bốn chuyên đề này **PLANNED**, chưa phải bài giảng READY, không cộng vào 56 bài cốt lõi và không chặn tiến độ BOOT–M11. Đề cương, prerequisite, bài thực hành và fallback nằm trong [Learn Sync](docs/LEARN-SYNC-2026-10-22.md).

| Mã | Chuyên đề | Học sau | Sản phẩm mục tiêu |
|---|---|---|---|
| X01 | dots — Giao trách nhiệm liên tục | M06–M08 | Bản giao trách nhiệm có quyền, cách báo cáo, escalation và cách dừng. |
| X02 | ChatGPT Space — Pages và cộng tác | M03, M05, M07.2 | Trang tổng hợp có nguồn và kiểm quyền của người đọc. |
| X03 | Sites — Tạo và chia sẻ website/công cụ | M05–M07 | Bản mẫu từ dữ liệu giả lập, test chức năng và kế hoạch chia sẻ; chưa xuất bản nếu chưa duyệt. |
| X04 | Workspace administration — Quản trị không gian làm việc | M07–M08; theo vai trò | Ma trận vai trò/quyền, kết nối và checklist triển khai; không cần cấp admin để học lý thuyết. |

## Capstone — Một workflow thực tế

Chọn workflow hỗ trợ học tập hoặc dự án bot/affiliate: đầu vào có nguồn → xử lý → sản phẩm → kiểm chứng → người review. Automation chỉ thêm khi tác vụ thủ công đã đạt tiêu chí; mọi hành động rủi ro vẫn có ranh giới và điểm duyệt.

Có thể chọn báo cáo nghiên cứu, trợ lý vận hành hoặc công cụ website mẫu. Sites/dots không bắt buộc; không coi capstone là cam kết thu nhập. Xem [Capstone](capstone/README.md).

## Quy tắc phát hành và cập nhật

Tách ba trạng thái: **đề cương đã cập nhật**, **bài giảng đã READY**, **người học đã PASS**. Một trạng thái không tự kéo theo hai trạng thái còn lại. Giữ ngày QA từng bài trong Content Status; không đổi hàng loạt sang 2026-10-22 chỉ vì rà soát mục lục.

Trước khi dạy tính năng: kiểm nguồn trực tiếp, môi trường, quyền và giới hạn; dùng [Feature Availability](docs/FEATURE-AVAILABILITY.md). Khi không có quyền, ghi rõ phần thiết kế/mô phỏng đã làm, không giả nhận đã chạy công cụ.
