# ChatGPT & AI English Glossary — Từ điển Anh–Việt tích lũy

> This glossary grows with the course. Terms are explained in context rather than translated mechanically.  
> Glossary này được bổ sung theo từng bài. Thuật ngữ được giải thích theo ngữ cảnh thay vì dịch từng chữ.

## How to use — Cách sử dụng

For each term, learn three levels:

1. **Recognize** — nhìn thấy và nhận ra thuật ngữ.
2. **Understand** — hiểu nó có nghĩa gì trong AI/ChatGPT.
3. **Use** — sử dụng đúng thuật ngữ khi nói hoặc viết prompt/workflow.

## Starter vocabulary — Bộ từ vựng khởi đầu

| Term | Nghĩa gần đúng | Plain-English meaning | Ghi chú trong AI/ChatGPT |
|---|---|---|---|
| `prompt` | yêu cầu/chỉ dẫn đầu vào | The instruction or input you give an AI model. | Không chỉ là một câu hỏi; có thể chứa mục tiêu, context, constraints và format. |
| `context` | ngữ cảnh | Information available to the model for the current task. | Có thể đến từ cuộc chat, file, project, tool result hoặc dữ liệu kết nối. |
| `model` | mô hình | The AI system that processes input and produces output. | Các model có thể khác nhau về năng lực, tốc độ và reasoning. |
| `reasoning` | suy luận | The process of working through a problem to reach an answer. | `reasoning effort` nói đến mức tài nguyên/suy luận dành cho tác vụ. |
| `output` | đầu ra | The result produced by the model. | Có thể là text, code, file, image, structured data, v.v. |
| `constraint` | ràng buộc | A rule or limit the output should follow. | Ví dụ: độ dài, format, nguồn được phép dùng. |
| `tool` | công cụ | A capability the AI can use to perform an action or get information. | Ví dụ web search, code execution, connected app. |
| `workflow` | quy trình làm việc | A repeatable sequence of steps used to complete a task. | Có thể gồm model + tools + human review + automation. |
| `hallucination` | thông tin bịa/sai nhưng nghe có vẻ hợp lý | A confident-looking answer that is unsupported or incorrect. | Không đồng nghĩa với mọi lỗi; trọng tâm là nội dung không được grounding/verification phù hợp. |
| `verification` | kiểm chứng | Checking whether a result is correct and supported. | Có thể bằng source, calculation, test, comparison hoặc human review. |
| `grounding` | neo vào nguồn/bằng chứng | Connecting an AI answer to reliable source information. | Giúp giảm câu trả lời dựa trên suy đoán. |
| `agent` | tác tử AI | An AI system that can pursue a goal using steps and tools. | Khái niệm rộng; không phải mọi chatbot đều là agent. |
| `automation` | tự động hóa | Making a task run with reduced manual intervention. | Automation có thể đơn giản hơn agent. |

## M00 — Mental Model vocabulary

| Term | Nghĩa gần đúng | Plain-English meaning | Ghi chú trong AI/ChatGPT |
|---|---|---|---|
| `surface` | bề mặt/môi trường làm việc | The product environment where you do the task. | Ví dụ Chat, Work hoặc Codex; surface khác tool. |
| `Chat` | chế độ hội thoại | A conversational surface for questions, drafting and iterative work. | Phù hợp tác vụ ngắn hoặc tương tác theo lượt. |
| `Work` | chế độ giao việc nhiều bước | A surface for longer work that produces reviewable deliverables. | Dùng khi cần nhiều bước, files/sources và sản phẩm hoàn chỉnh. |
| `Codex` | môi trường coding agent | A coding-focused environment for repositories, code changes and tests. | Phù hợp khi code/repo/test là trọng tâm. |
| `task brief` | bản giao việc ngắn | A compact specification of what should be done and checked. | M00 dùng Outcome → Context → Tools → Verification. |
| `outcome` | kết quả cần đạt | The useful result you want at the end. | Nên mô tả sản phẩm hoặc quyết định, không chỉ chủ đề. |
| `boundary` | ranh giới | A limit the task must not cross. | Ví dụ không gửi, mua, xóa hoặc sửa dữ liệu trước review. |
| `acceptance criteria` | tiêu chí chấp nhận | Observable conditions that define PASS. | Giúp review output nhất quán. |

## M01 — Prompting vocabulary

| Term | Nghĩa gần đúng | Plain-English meaning | Ghi chú trong AI/ChatGPT |
|---|---|---|---|
| `goal` | mục tiêu | What you want the task to achieve. | Một thành phần nền tảng của prompt/task specification. |
| `audience` | đối tượng đọc/sử dụng | The people who will use the output. | Ảnh hưởng mức giải thích, từ vựng và tone. |
| `tone` | giọng điệu | The style or attitude of the writing. | Ví dụ friendly, professional, neutral. |
| `iteration` | vòng lặp cải thiện | Repeating work with targeted changes. | Prompt → response → inspect → revise → verify. |
| `decomposition` | chia nhỏ tác vụ | Breaking a large task into smaller reviewable parts. | Nên chia tại dependency hoặc verification boundary. |
| `follow-up` | yêu cầu tiếp nối | A later request that continues the current task. | Dùng context của cùng conversation. |
| `steering` | điều hướng | Guiding the work while it progresses. | Chỉ ra phần giữ, phần sửa và tiêu chí mới. |
| `checkpoint` | điểm kiểm tra | A planned pause for review. | Hữu ích trước bước phụ thuộc hoặc hành động rủi ro. |
| `scope` | phạm vi | The part of the work included in the task. | Giúp tránh sửa/làm ngoài yêu cầu. |
| `output contract` | hợp đồng đầu ra | A clear description of output shape and rules. | Có thể gồm format, fields, missing-data rules và criteria. |
| `field` | trường thông tin | One named piece of structured information. | Ví dụ Price, Risk, Evidence status. |
| `schema` | lược đồ | A formal description of data structure. | Stage A chỉ cần hiểu khái niệm; schema kỹ thuật học sau. |
| `checklist` | danh sách kiểm | A list of items used to review completion. | Có thể chấm PASS/FAIL cho output. |
| `claim` | nhận định có thể kiểm | A statement that can be checked. | Fact quan trọng nên được nối với evidence. |
| `evidence` | bằng chứng | Information that supports or challenges a claim. | Source, file row, calculation, test output. |
| `source` | nguồn | Where information comes from. | Ưu tiên source phù hợp và hiện tại với claim thay đổi theo thời gian. |
| `assumption` | giả định | Something treated as true without full evidence. | Cần được nêu rõ khi ảnh hưởng kết luận. |
| `cross-check` | đối chiếu chéo | Checking a claim by another independent route. | Dùng cho claim quan trọng hoặc nguồn xung đột. |
| `uncertainty` | mức chưa chắc chắn | A limit on how confident a conclusion should be. | Không dùng suy đoán để lấp Unknown. |

> Detailed pronunciation, examples and common confusions are introduced inside the lesson where each term first becomes important.
