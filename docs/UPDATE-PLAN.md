# Repository Update Plan — Kế hoạch hoàn thiện khóa học ChatGPT

> Ngày lập: 2026-09-10  
> Phiên bản kế hoạch: 1.0  
> Baseline review: commit `9d70449b6309c3ce6c3e1289fae15bbbd4b9f20c`  
> Trạng thái: IN PROGRESS — U01/P0, U02/P1 và U03–U04/P2 đã triển khai; P3 là gate tiếp theo.  
> Current implementation: P0–P2 content scope is complete; 11 lessons BOOT–M01 are READY. P3 labs/pilot/release evidence is not complete yet.  
> Phạm vi cập nhật gần nhất: phát hành M00.1–M00.3, M01.1–M01.4, M00/M01 checkpoints, QA evidence và đồng bộ trạng thái/điều hướng.

## 1. Mục tiêu và hiện trạng

Mục tiêu là giúp một người chưa biết ChatGPT có thể mở repo, biết bắt đầu ở đâu, tự làm bài, tự kiểm tra kết quả và tiếp tục học mà không cần người hướng dẫn bổ sung phần còn thiếu.

Khóa học đồng thời rèn tiếng Anh chuyên ngành: giữ thuật ngữ tiếng Anh chuẩn, giải thích tiếng Việt ngay lần đầu sử dụng, có ví dụ và mẫu câu thực dụng. Không yêu cầu biết lập trình để hoàn thành khóa nền tảng.

### Baseline đã kiểm tra

| Thành phần | Hiện trạng tại baseline | Khoảng trống cần xử lý |
|---|---|---|
| Toàn repo | 25 file Markdown, 12 module | Có cấu trúc nhưng chưa có đường tự học hoàn chỉnh |
| Curriculum | 52 lesson ID, chia 3 stage | Mỗi bài mới có tên và mô tả ngắn |
| Modules | Mỗi module chỉ có README | Chưa có bài giảng chi tiết, bài làm mẫu và bài tự luyện |
| Điểm bắt đầu | README hướng tới M00.1 | Thiếu hướng dẫn thao tác đầu tiên và cách lưu bài |
| Labs | Hai mẫu Prompt Lab và Evaluation Lab | Chưa có bộ bài tập, dữ liệu đầu vào, đáp án giải thích |
| PASS | Có nguyên tắc, đầu ra cấp module | Thiếu ngưỡng, mô tả mức điểm và cách học lại |
| Song ngữ | Có tiêu chuẩn, template và 13 thuật ngữ khởi đầu | Chưa có lesson hoàn chỉnh áp dụng tiêu chuẩn |
| Capstone | Bài tổng hợp agentic workflow | Thiếu bài tốt nghiệp riêng cho người dùng cơ bản |

Nguồn nội bộ: [Curriculum](../CURRICULUM.md), [Study Method](../STUDY-METHOD.md), [Lesson Template](../LESSON-TEMPLATE.md), [Bilingual Standard](BILINGUAL-LESSON-STANDARD.md), [Capstone](../capstone/README.md).

## 2. Quyết định về phạm vi và cấu trúc

1. Giữ 52 lesson ID hiện có để tránh làm hỏng lịch sử học và các tham chiếu. Bổ sung 4 bài BOOT trước M00; tổng mục tiêu là 56 bài, không tính bài kiểm tra và capstone.
2. Giữ nguyên phân nhóm Stage A/B/C hiện tại. Tạo đường học nền tảng gồm BOOT + M00–M05, đi qua cả Stage A và phần đầu Stage B. M05 không bị chuyển module hay đổi ID.
3. Cho phép hoàn thành khóa nền tảng mà không học API/MCP/Agents. M06–M08 là đường mở rộng Power User; M09–M11 là Builder.
4. M00.1 vẫn tồn tại, nhưng được học sau khi người học đã trải nghiệm chat ở BOOT. Phần chọn môi trường làm việc dùng ví dụ ngắn, không yêu cầu cài mọi công cụ.
5. Phần kiến thức cơ bản phải có bài thực hành không cần mua thêm dịch vụ. Các bài cần tính năng riêng phải ghi điều kiện và bài thay thế; không mặc định mọi tài khoản có cùng giao diện.
6. Dùng ví dụ đời thường trước, rồi thêm bài chuyển giao sang nghiên cứu dự án hoặc affiliate. Không yêu cầu kiến thức affiliate đầu vào.
7. Bảo toàn mọi evidence và trạng thái học hiện có. Không đánh dấu người học PASS vì tài liệu đã được biên soạn.

### Các mốc phát hành dự kiến

| Mốc | Nội dung có thể học | Điều kiện công bố |
|---|---|---|
| v0.1.2 | Kế hoạch và mô tả đúng hiện trạng | Kế hoạch được lưu, liên kết hoạt động; không quảng bá đã có khóa hoàn chỉnh |
| v0.2.0 | BOOT + M00–M01: 11 bài | Qua gate P3; có thử học và kết quả được ghi lại |
| v0.3.0 | Khóa nền tảng: 27 bài + capstone cơ bản | Qua gate P4; nêu rõ bài cần quyền truy cập riêng |
| v0.4.0 | Thêm 14 bài M06–M08 | Qua gate P5; thực hành quyền hạn và automation được kiểm chứng |
| v1.0.0 | Thêm 15 bài M09–M11 và capstone Builder | Qua gate P6–P7; toàn bộ 56 bài có trạng thái và bằng chứng nghiệm thu |

Các phiên bản sau v0.1.2 là mục tiêu, chưa phải bản phát hành đã có. Lịch chỉ được chốt sau khi đo thời gian biên soạn và thử học đợt đầu.

## 3. Trạng thái tài liệu và trạng thái người học

Tạo `docs/CONTENT-STATUS.md` để theo dõi biên soạn với các cột: Lesson ID, Path, Content status, Source checked, Reviewer, QA evidence, Estimate, Actual effort.

| Content status | Ý nghĩa |
|---|---|
| PLANNED | Có trong kế hoạch, chưa có bài hoàn chỉnh |
| DRAFT | Có bản thảo, chưa đủ điều kiện phát hành |
| IN REVIEW | Đang kiểm tra nguồn, thực hành hoặc chất lượng song ngữ |
| READY | Đạt các gate của bài và có bằng chứng kiểm tra |
| NEEDS UPDATE | Bài từng READY nhưng có thay đổi hoặc lỗi cần sửa |

`PROGRESS.md` tiếp tục dùng NOT STARTED / IN PROGRESS / PASS / REVIEW cho năng lực người học. Chỉ đổi trạng thái này dựa trên bài làm của người học. Khi triển khai BOOT, thêm 4 dòng NOT STARTED; giữ tất cả các dòng cũ. Chỉ đổi bài tiếp theo sang BOOT.1 khi tài liệu BOOT.1 đã READY và phù hợp tiến độ thực tế.

Một bài dùng phương án mô phỏng chỉ được ghi nhận năng lực đã chứng minh. Không dùng mô phỏng để chứng nhận đã thực hiện thành công tính năng thật chưa truy cập được.

## 4. P0 — Chuẩn hóa điểm bắt đầu và hạ tầng học

**Ưu tiên:** bắt buộc trước khi phát hành bài đầu. **Phụ thuộc:** không có. **Trạng thái:** COMPLETED in U01.

| File | Thao tác dự kiến | Nội dung cần có |
|---|---|---|
| `README.md` | Sửa | Người học mục tiêu, điều kiện đầu vào, phạm vi đã READY, đường học và nút bắt đầu |
| `START-HERE.md` | Tạo | Đọc repo trên trình duyệt; chọn đường học; mở bài; làm, lưu và tự chấm bài |
| `CURRICULUM.md` | Sửa | Thêm BOOT; liên kết lesson đã có; chỉ rõ prerequisites, thời lượng và capstone nền tảng |
| `docs/LEARNING-PATHS.md` | Tạo | Foundation / Power User / Builder; điểm vào, điểm kết thúc, điều kiện chuyển chặng |
| `docs/CONTENT-STATUS.md` | Tạo | Danh sách 56 bài, trạng thái biên soạn và bằng chứng QA |
| `docs/FEATURE-AVAILABILITY.md` | Tạo | Tính năng, môi trường, điều kiện tài khoản, ngày kiểm tra, nguồn, cách thay thế |
| `docs/TROUBLESHOOTING.md` | Tạo | Không thấy nút/tính năng, hết quota, upload lỗi, câu trả lời sai, link bài không mở được |
| `LESSON-TEMPLATE.md` | Sửa | Metadata về prerequisite, môi trường, thời lượng, file đầu vào, nguồn và bài trước/sau |
| `STUDY-METHOD.md` | Sửa | Buổi học 30–60 phút; nhánh ôn tập; quy trình PASS và lưu evidence cho người mới |
| `docs/BILINGUAL-LESSON-STANDARD.md` | Sửa | Giới hạn từ mới, nhắc lại từ cũ, không dùng thuật ngữ chưa giải thích |
| `OFFICIAL-SOURCES.md` | Sửa | Gắn nguồn cụ thể với module/lesson và ngày kiểm tra |
| `evidence/README.md` | Tạo | Cách lưu bài bằng giao diện GitHub; kiểm tra nội dung trước khi công khai |
| `evidence/TEMPLATE.md` | Tạo | Lesson, task, prompt, result, verification, score, reflection; không cần link chat công khai |

**Gate P0:** người kiểm tra mở README và xác định được trong 2 phút: học bài nào, cần gì, lưu bài ở đâu, chấm thế nào. Chỉ liên kết đến file đã tồn tại; bài tương lai được ghi PLANNED bằng văn bản.

## 5. P1 — Bốn bài khởi động BOOT

**Ưu tiên:** bắt buộc. **Phụ thuộc:** P0. **Thư mục:** `modules/BOOT-getting-started/`. **Trạng thái:** COMPLETED in U02.

Tạo README module, 4 lesson bên dưới và bài kiểm tra `assessments/BOOT-CHECK.md`.

| ID / File trong module | Kết quả học tập và thực hành | Bằng chứng bắt buộc |
|---|---|---|
| BOOT.1 / `BOOT.1-first-chat.md` | Mở ChatGPT, nhận biết ô nhập, gửi một yêu cầu tiếng Việt, hiểu prompt/response | Một cuộc hội thoại đầu tiên và giải thích prompt, response bằng lời mình |
| BOOT.2 / `BOOT.2-conversation-basics.md` | Yêu cầu rút gọn/đổi định dạng/bổ sung; thử yêu cầu tiếp nối trong chat mới để nhận ra ngữ cảnh | Prompt gốc, ít nhất 2 lượt sửa và nhận xét về chat mới |
| BOOT.3 / `BOOT.3-safe-use-and-verification.md` | Hiểu câu trả lời có thể sai; kiểm tra một claim; làm sạch thông tin cá nhân trên dữ liệu giả lập | Bảng 3 claim và cách kiểm tra; bản dữ liệu đã che thông tin |
| BOOT.4 / `BOOT.4-save-evidence.md` | Đọc Markdown cơ bản; lưu bài qua GitHub web hoặc ghi chú riêng; hiểu repo/commit/evidence ở mức cần dùng | Một bản evidence có prompt, kết quả, kiểm chứng và tự nhận xét |

Thời lượng mục tiêu: 20–40 phút/bài, sẽ điều chỉnh theo thử học. Tài khoản/đăng nhập, nhãn nút, cài đặt quyền riêng tư và các bước giao diện phải được kiểm tra với nguồn chính thức trước khi viết hướng dẫn cụ thể.

**Gate P1:** hoàn thành toàn bộ 4 tác vụ không cần CLI, API key hoặc cài môi trường lập trình; dữ liệu mẫu không chứa thông tin cá nhân thật; hướng dẫn có cách xử lý khi giao diện khác.

## 6. P2 — Hoàn thiện M00 và M01

**Ưu tiên:** bắt buộc. **Phụ thuộc:** P1 và template P0. **Trạng thái:** COMPLETED in U03–U04.

### M00 — Hiểu ChatGPT và giao việc

| File trong `modules/M00-mental-model/` | Nội dung chi tiết | Bài tập / đầu ra |
|---|---|---|
| `M00.1-chat-work-codex.md` | Giải thích Chat, Work, Codex bằng 3 nhu cầu thực tế; môi trường phù hợp; lựa chọn khi không có tính năng | Bộ 10 tình huống chọn môi trường/công cụ, có lý do và đáp án giải thích |
| `M00.2-how-chatgpt-works.md` | Phân biệt model, context, tool; khả năng sai/bịa; thông tin mới cần nguồn; context không phải trí nhớ vô hạn | Phân tích 3 câu trả lời có lỗi được cung cấp sẵn; nêu cách kiểm chứng |
| `M00.3-task-and-verification.md` | Outcome → Context → Tools → Verification; chuyển thuật ngữ thành câu hỏi dễ hiểu | Viết một task brief và cách xác định hoàn thành |

### M01 — Viết và cải thiện yêu cầu

| File trong `modules/M01-prompting/` | Nội dung chi tiết | Bài tập / đầu ra |
|---|---|---|
| `M01.1-prompt-foundations.md` | Goal + Context + Output + Boundaries; prompt ngắn vẫn tốt nếu đủ thông tin | 5 yêu cầu mơ hồ được viết lại; cặp prompt trước/sau |
| `M01.2-iterate-and-decompose.md` | Bổ sung thông tin, chia tác vụ, yêu cầu sửa có mục tiêu; biết khi nào mở chat mới | Một tác vụ qua ít nhất 2 vòng sửa, chỉ ra thay đổi nào có ích |
| `M01.3-output-contracts.md` | Định dạng, ví dụ, checklist; bảng và cấu trúc văn bản trước; schema kỹ thuật là phần mở rộng | Một bảng đầu ra có cột/quy tắc rõ và checklist đối chiếu |
| `M01.4-verify-answers.md` | Kiểm tra claim, nguồn, tính toán, giả định; AI tự nói đúng không đủ để chứng minh | Bảng claim → evidence → kết luận, có một lỗi được phát hiện và sửa |

Mỗi bài có 1 ví dụ làm trọn vẹn, 1 bài có hướng dẫn, 1 bài tự làm khác tình huống mẫu và đáp án/rubric riêng. Không phụ thuộc vào việc model phải tự sinh ra lỗi đúng như dự đoán: cung cấp sẵn một đầu ra lỗi để bài tập tái lập được.

**Gate P2:** PASS về phạm vi nội dung. 7 bài M00–M01 đã READY, thuật ngữ được giải thích trước khi yêu cầu sử dụng, input thực hành có sẵn/inline, checkpoints có rubric và QA evidence tại `labs/examples/M00-qa-check.md` và `labs/examples/M01-qa-check.md`.

## 7. P3 — Labs, PASS, thử học và phát hành v0.2.0

**Ưu tiên:** bắt buộc trước khi gọi đợt đầu là có thể tự học. **Phụ thuộc:** P2. **Trạng thái:** PLANNED — NEXT.

### File và bộ bài cần bổ sung

| File / thư mục | Nội dung |
|---|---|
| `labs/PROMPT-LAB.md` | Giữ mẫu hiện có, thêm hướng dẫn và liên kết bài làm mẫu |
| `labs/examples/P-001-summary.md` | Tóm tắt đoạn văn giả lập: đầu vào, prompt ban đầu, lỗi, prompt sửa, kết quả và kiểm chứng |
| `labs/examples/P-002-planning.md` | Lập kế hoạch từ các ràng buộc; kiểm tra thời gian và việc thiếu dữ liệu |
| `labs/examples/P-003-comparison.md` | So sánh từ bảng dữ liệu được cung cấp; không tự bịa thông số còn thiếu |
| `labs/data/README.md` | Mô tả từng dữ liệu mẫu, nguồn gốc giả lập, bài sử dụng, điều kiện tái sử dụng |
| `labs/data/sample-brief.md` | Đầu vào đủ thông tin cho tóm tắt/lập kế hoạch |
| `labs/EVALUATION-LAB.md` | Mô tả mức 0/1/2; ví dụ đã chấm; phân biệt lỗi kiến thức, làm bài và diễn đạt tiếng Anh |
| `assessments/README.md` | Cách làm, chấm, nộp evidence, xử lý chưa đạt |
| `assessments/M00-CHECK.md` | 10 tình huống; đáp án chấp nhận nhiều lựa chọn nếu có lý do phù hợp |
| `assessments/M01-CHECK.md` | 5 yêu cầu mơ hồ; rubric và bài mẫu ở các mức chất lượng |
| `assessments/ANSWER-KEY.md` | Đáp án, lý do, lỗi thường gặp và bài cần ôn; đặt phần đáp án sau bài tự làm |
| `docs/BEGINNER-PILOT.md` | Kịch bản thử học, kết quả thực tế, chỗ bị mắc, thời gian, bản sửa và kiểm tra lại |

### PASS dự kiến, cần hiệu chỉnh qua thử học

- ChatGPT track: chấm 5 năng lực Explain / Execute / Diagnose / Verify / Transfer, mỗi năng lực 0–2. Mức 0: chưa chứng minh hoặc sai cốt lõi; 1: làm được một phần/cần gợi ý; 2: tự làm đúng và có bằng chứng. PASS khi đạt ít nhất 8/10, không năng lực nào 0, Execute và Verify đều 2. Mỗi lesson phải bổ sung mô tả quan sát được cho từng năng lực.
- English track: nhận ra ít nhất 4/5 từ được kiểm tra, giải thích đúng 3 từ trọng tâm bằng tiếng Việt, tự viết một yêu cầu tiếng Anh dùng đúng nghĩa. Không trượt chỉ vì lỗi ngữ pháp nhỏ không đổi ý định.
- M00 checkpoint: ít nhất 8/10 tình huống có lựa chọn và lý do hợp lý; không để lại hiểu lầm rằng câu trả lời AI tự nó là bằng chứng hoặc công cụ luôn được quyền hành động.
- M01 checkpoint: nộp đủ 5 task spec; ít nhất 4/5 đạt yêu cầu rubric; phải có bằng chứng chạy và kiểm tra ít nhất một spec. Sửa lỗi nghiêm trọng trước khi chuyển module.
- Evidence phải được làm sạch trước khi đưa lên repo. Nếu còn secret/dữ liệu riêng tư, dừng bước công khai và sửa evidence; không biến việc lộ dữ liệu thành điều kiện nộp bài.
- Khi chưa đạt: chỉ rõ tiêu chí thiếu → quay về ví dụ tương ứng → làm một bài tương đương mới → lưu lần đánh giá lại. Không yêu cầu học lại toàn bộ module khi chỉ vướng một năng lực.

### Thử học

Chạy một lượt kiểm tra tài liệu không nhờ tác giả giải thích miệng. Sau đó thử với ít nhất một người mới thật, có thể là chủ repo khi bắt đầu học; ghi riêng ai thực hiện, bài nào, mất bao lâu, gặp vấn đề gì. Kiểm tra bằng AI không được ghi là thử nghiệm với người mới thật. Không đánh dấu PASS thay cho người học.

**Gate P3:** đủ 11 bài READY; không có đường dẫn nội bộ hỏng; 3 lab mẫu chạy/kiểm tra được; rubric được áp dụng vào ít nhất một bài đạt và một bài chưa đạt; lỗi chặn học từ pilot đã sửa. Nếu chưa có người thử học thật, chỉ công bố bản preview và ghi giới hạn này, chưa tuyên bố đã xác nhận khả năng tự học.

## 8. P4 — Hoàn thiện khóa nền tảng M02–M05

**Phụ thuộc:** P3; dùng phản hồi đợt đầu để chỉnh độ dài bài. **Trạng thái:** PLANNED.

Mỗi lesson ID bên dưới tạo một file riêng trong module hiện hữu, theo mẫu `Mxx.n-short-title.md`. Không gộp cả module thành một bài README.

| Module / phạm vi ID | Nội dung triển khai theo bài | Đầu ra cấp module |
|---|---|---|
| M02 / M02.1–M02.3, 3 bài | Chọn model theo tác vụ; mức suy luận nếu có trong môi trường; benchmark 5 tác vụ với cùng đầu vào và rubric | Bảng 5 tác vụ, kết quả, thời gian và lựa chọn; nếu chỉ có 1 model thì không kết luận model nào tốt hơn |
| M03 / M03.1–M03.5, 5 bài | Phân biệt nguồn context; instructions; tạo Project; giới hạn memory; dùng file và trích chứng cứ | Một Project hoặc bộ context thay thế, có instructions, dữ liệu sạch, quy tắc cập nhật và kiểm tra câu trả lời |
| M04 / M04.1–M04.4, 4 bài | Search; chất lượng nguồn; Deep Research và điều kiện sử dụng; tổng hợp có kiểm chứng | Memo có ít nhất 3 nguồn, 5 claim được ánh xạ bằng chứng, ngày kiểm tra và phần chưa chắc chắn |
| M05 / M05.1–M05.4, 4 bài | Đọc ảnh; tạo/sửa ảnh; thao tác file; voice | Sản phẩm dùng ít nhất 2 dạng đầu vào/đầu ra và có vòng review; ghi rõ năng lực chưa thực hành nếu thiếu tính năng |

M05.3 giữ một lesson ID nhưng chia thành các mini-lab văn bản, bảng tính, trình chiếu và PDF để tránh một buổi học quá tải. Chỉ dùng số liệu giả lập; kết quả tính toán có đáp án đối chiếu.

Tạo thêm `assessments/M02-CHECK.md` đến `assessments/M05-CHECK.md`, dữ liệu mẫu dưới `labs/data/`, bài mẫu dưới `labs/examples/` và `capstone/FOUNDATION.md`.

### Capstone nền tảng

Đầu vào: một brief công việc/dự án không nhạy cảm. Đầu ra: một văn bản hữu ích, một bảng so sánh hoặc kế hoạch, và một ghi chú nghiên cứu có nguồn. Evidence gồm prompt ban đầu, ít nhất 2 lần cải thiện, bảng kiểm chứng 5 claim và tự tổng kết song ngữ ngắn. Không yêu cầu code, agent hay API.

PASS: áp dụng rubric năng lực ở P3, đạt checklist riêng cho cả 3 sản phẩm, không còn claim quan trọng chưa kiểm chứng và có thể làm lại với brief mới. Bài thực hành thay thế phải ghi rõ kỹ năng được chứng minh; không công nhận thao tác tính năng chưa được thử.

**Gate P4:** 27 bài BOOT–M05 READY; hoàn thành một lượt capstone mẫu và một lượt thử học thực tế trước khi công bố khóa nền tảng đã được kiểm chứng; tài liệu chỉ rõ người học có thể dừng ở đây.

## 9. P5 — Power User: M06–M08

**Phụ thuộc:** P4. **Trạng thái:** PLANNED. Mọi yêu cầu về sản phẩm và quyền truy cập được xác minh tại thời điểm viết bài.

| Module / phạm vi ID | Nội dung cần triển khai | Bài thực hành và gate |
|---|---|---|
| M06 / M06.1–M06.5, 5 bài | Giao việc Work; việc dài; browser/search; computer use; quyền hạn | Brief nhiều bước, deliverable để review, điểm kiểm tra và cách dừng; thực hành trong môi trường thử nghiệm |
| M07 / M07.1–M07.4, 4 bài | Công cụ tích hợp/plugin; phạm vi dữ liệu; workflow kết nối; hành động cần con người xem xét | Workflow qua 2 hệ thống trên dữ liệu thử nghiệm; phân biệt đọc, soạn nháp, sửa và gửi; có đường mô phỏng nếu chưa kết nối |
| M08 / M08.1–M08.5, 5 bài | Skill/plugin; hướng dẫn tái sử dụng; lịch chạy/trigger được hỗ trợ; độ tin cậy; đánh giá trước tự động hóa | Quy trình thủ công qua 5 test case, bản tái sử dụng, lịch thử, cách tắt và báo lỗi; mô phỏng không được ghi là automation đã chạy thật |

Tạo `assessments/M06-CHECK.md` đến `assessments/M08-CHECK.md`, `labs/examples/POWER-USER-WORKFLOW.md`, `capstone/POWER-USER.md`. Khi cần dùng tài khoản thật hoặc hành động gửi/xuất bản, bài học phải nêu đúng phạm vi ủy quyền và bước review tương ứng.

**Gate P5:** 14 bài mới READY; ví dụ có xử lý thiếu quyền/công cụ lỗi; workflow mẫu chạy được trong môi trường đã ghi rõ; không gọi mọi loại trigger là có sẵn khi chưa xác minh.

## 10. P6 — Builder: M09–M11

**Phụ thuộc:** P5 và kiểm tra đầu vào Builder. **Trạng thái:** PLANNED.

Tạo `docs/BUILDER-PREREQUISITES.md`: kiến thức file/thư mục, Git/branch/commit, terminal, đọc code đơn giản, môi trường chạy, xác thực và chi phí API. Người chưa đủ điều kiện được dẫn tới bài chuẩn bị cụ thể; không mặc định đã biết vì học xong ChatGPT cơ bản.

| Module / phạm vi ID | Nội dung cần triển khai | Bài thực hành và gate |
|---|---|---|
| M09 / M09.1–M09.5, 5 bài | Chọn môi trường Codex; đọc repo; giao tác vụ code; GitHub workflow; kiểm tra và hoàn tác | Một sửa lỗi nhỏ có cách tái hiện, test phù hợp, diff review và commit/PR evidence |
| M10 / M10.1–M10.5, 5 bài | ChatGPT/API; Responses và tools; MCP; Agents SDK; evals | Sơ đồ hệ thống, ví dụ tối thiểu phù hợp docs hiện tại, ít nhất 5 eval case và giới hạn chi phí do người học đặt |
| M11 / M11.1–M11.5, 5 bài | Workflow hay agent; state/tools; human review; quan sát và cải tiến; readiness | Design review có nguồn trạng thái, quyền, lỗi, chi phí và phương án fallback trước khi xây capstone |

Tạo `assessments/M09-CHECK.md` đến `assessments/M11-CHECK.md`, `capstone/BUILDER.md`. Cập nhật `capstone/README.md` thành trang chọn 3 capstone, giữ lại yêu cầu hữu ích của bản agentic hiện tại trong Builder.

**Gate P6:** 15 bài mới READY; ví dụ kỹ thuật đã chạy ở môi trường được ghi lại; capstone Builder có ít nhất 10 eval case, tiêu chí đạt rõ, tài liệu chạy lại và kiểm soát chi phí. Không yêu cầu người học cung cấp secret trong repo để chứng minh hoàn thành.

## 11. P7 — Nghiệm thu toàn khóa và duy trì

**Phụ thuộc:** P6. **Trạng thái:** PLANNED.

- Kiểm tra đủ 56 lesson ID duy nhất; mỗi bài có file, nguồn, status, prerequisite, bài tập, đáp án/rubric và đường điều hướng.
- Đối chiếu README, CURRICULUM, CONTENT-STATUS, PROGRESS và module README để không có bài đã đổi tên nhưng mất đường dẫn.
- Kiểm tra thuật ngữ và ví dụ song ngữ trên toàn khóa; không dùng glossary để thay thế giải thích tại bài.
- Dùng `docs/RELEASE-CHECKLIST.md` ghi bằng chứng phát hành, giới hạn đã biết và các môi trường đã thử.
- Ghi thời điểm kiểm tra nguồn cho từng bài. Rà lại trước mỗi lần sửa hoặc phát hành; UI/tính năng đổi thì chuyển bài bị ảnh hưởng sang NEEDS UPDATE và đánh dấu phạm vi lỗi.
- Không dùng ngày của bản kế hoạch làm bằng chứng rằng mọi tính năng đã được xác minh. URL nguồn chung phải được bổ sung bằng trang trực tiếp hỗ trợ nội dung bài khi triển khai.
- Chỉ bổ sung script/CI kiểm tra link và cấu trúc khi bắt đầu có bộ bài thật cần bảo trì; không dựng hệ thống kiểm thử phức tạp chỉ cho kế hoạch Markdown.

**Gate P7:** mọi điều kiện phát hành v1.0.0 có bằng chứng; không còn lỗi chặn người học; giới hạn tính năng và các phần chưa được thử trên tài khoản thật được công bố rõ.

## 12. Tiêu chuẩn READY cho từng bài

| Nhóm kiểm tra | Điều kiện nghiệm thu |
|---|---|
| Mục tiêu | 2–4 kết quả quan sát được, phù hợp prerequisite |
| Hướng dẫn | Có bước thực hiện, đầu vào và cách xử lý lỗi; không chỉ yêu cầu “hãy thực hành” |
| Song ngữ | Giải thích EN/VI tương ứng; khoảng 3–7 thuật ngữ mới và 3–5 mẫu câu cho bài đầu; từ khó giải thích tại chỗ |
| Ví dụ | Ít nhất 1 ví dụ trọn vẹn gồm đầu vào, prompt, đầu ra minh họa và cách kiểm chứng |
| Thực hành | Có bài có hướng dẫn, bài tự làm khác ví dụ và bài chuyển giao; có thể tích hợp để giữ buổi học vừa sức |
| Nguồn | Link trực tiếp, ngày kiểm tra, phân biệt nguyên lý với chi tiết UI; không dẫn người mới tự mò cả trang docs |
| Khả năng truy cập | Ghi môi trường, điều kiện, quota/chi phí nếu liên quan và phương án thay thế |
| Chấm bài | Có rubric cụ thể, đáp án giải thích và đường ôn tập; không yêu cầu kết quả AI giống hệt chuỗi mẫu |
| Dữ liệu | Dữ liệu giả lập hoặc có quyền sử dụng, có cách che thông tin trước khi lưu |
| Evidence | Ghi rõ cần lưu gì; mẫu hoàn chỉnh; không đánh đồng evidence của tác giả với bài làm người học |
| Điều hướng | Có link bài trước/sau đã tồn tại, hoặc ghi rõ bài tiếp theo chưa phát hành |

## 13. Backlog có thể triển khai thành commit

Trạng thái từng gói Uxx được cập nhật theo implementation thực tế. Người biên soạn hoặc trợ lý thực hiện từng gói; người review kiểm tra evidence; người học chỉ xác nhận năng lực qua bài làm của chính mình. Chưa chỉ định người phụ trách bên ngoài và chưa tạo issue hay gửi thông báo.

| ID | Công việc | Phụ thuộc | Điểm kết thúc để commit |
|---|---|---|---|
| U01 | Hướng bắt đầu, learning paths, content status, template | Kế hoạch này | DONE — Gate P0 đã rà lại trong U01 completion pass |
| U02 | BOOT.1–BOOT.4, dữ liệu và evidence mẫu | U01 | DONE — Gate P1 đạt; BOOT READY |
| U03 | Ba lesson M00 và bộ 10 tình huống | U02 | DONE — M00 READY + M00 Check + QA evidence |
| U04 | Bốn lesson M01 và bộ 5 task spec | U03 | DONE — M01 READY + M01 Check + QA evidence; Gate P2 content scope complete |
| U05 | Ba lab mẫu, rubric và kiểm tra tổng hợp | U04 | Tự kiểm tra P3, còn pilot được ghi riêng |
| U06 | Pilot 11 bài, sửa lỗi, phát hành v0.2.0 | U05 | Gate P3 đủ evidence |
| U07 | M02, benchmark mẫu và checkpoint | U06 | 3 bài READY |
| U08 | M03, context/Project mẫu và checkpoint | U07 | 5 bài READY |
| U09 | M04, memo mẫu và checkpoint | U08 | 4 bài READY |
| U10 | M05, mini-lab file/ảnh/voice và checkpoint | U09 | 4 bài READY |
| U11 | Capstone nền tảng, pilot và v0.3.0 | U10 | Gate P4 đạt |
| U12 | M06, M07, M08; chia commit theo module | U11 | Gate P5 đạt; v0.4.0 |
| U13 | Prerequisites Builder, M09, M10, M11 | U12 | Từng module đủ bài và evidence |
| U14 | Capstone Builder, QA toàn khóa và release | U13 | Gate P6–P7 đạt; v1.0.0 |

Ưu tiên triển khai tiếp: **U05 → U06** để hoàn tất P3 trước khi mở rộng sang M02. Chưa mở rộng sang phần nâng cao trước khi sửa các lỗi người mới gặp ở đợt đầu.

## 14. Ước lượng và cách điều chỉnh

Đây là ước lượng công sức biên soạn + kiểm tra, không phải lịch học hay cam kết thời gian của người dùng. Không lấy ngân sách hoặc số giờ của dự án khác làm giả định cho repo này.

| Giai đoạn | Công sức dự kiến | Yếu tố ảnh hưởng |
|---|---:|---|
| P0 | 4–8 giờ | Chuẩn hóa điều hướng, trạng thái và template |
| P1 | 6–10 giờ | Bốn bài đầu, thử giao diện và evidence mẫu |
| P2 | 12–20 giờ | Bảy bài song ngữ, ví dụ và bài tập |
| P3 | 6–12 giờ | Labs, rubric, sửa lỗi pilot; chưa tính thời gian chờ người học |
| P4 | 28–44 giờ | 16 bài, mini-lab và capstone nền tảng |
| P5 | 24–40 giờ | 14 bài và xác minh công cụ/tài khoản |
| P6 | 30–50 giờ | 15 bài, ví dụ chạy thật và capstone Builder |
| P7 | 6–10 giờ | Kiểm tra chéo và phát hành |
| Tổng | 116–194 giờ | Điều chỉnh sau đợt BOOT + M00–M01 |

Mốc tự học đầu tiên P0–P3 dự kiến 28–50 giờ biên soạn/kiểm tra. Thời gian học mục tiêu: BOOT 20–40 phút/bài; bài nền tảng 30–60 phút/bài; checkpoint/capstone tính riêng. Ghi thời gian thực tế trong CONTENT-STATUS và BEGINNER-PILOT, sau đó điều chỉnh tải bài trước khi tiếp tục.

## 15. Quy trình cập nhật và kiểm tra GitHub

1. Đọc phiên bản nhánh hiện tại và hướng dẫn repo nếu có trước mỗi đợt sửa.
2. Viết một gói Uxx hoàn chỉnh; kiểm tra nguồn và bài thực hành tương ứng.
3. Cập nhật CONTENT-STATUS, điều hướng và CHANGELOG đúng với những gì đã hoàn thành. Chỉ cập nhật PROGRESS khi có evidence học tập.
4. Kiểm tra diff, các liên kết nội bộ, lesson ID và trạng thái; dừng bổ sung kiểm thử khi rủi ro cụ thể đã được giải quyết.
5. Commit với mô tả phạm vi rõ; push theo ủy quyền hiện tại và quy tắc nhánh của repo, không force-push. Nếu nhánh đã có commit mới, lấy lại bản mới và áp dụng thay đổi mà không ghi đè công việc khác.
6. Đọc lại file và commit từ GitHub sau khi push để xác minh nội dung đã có trên nhánh đích.

Kế hoạch này không tự tạo lịch chạy, không tự đánh dấu bài học đã hoàn thành và không thay thế việc xác minh tính năng khi biên soạn từng lesson.
