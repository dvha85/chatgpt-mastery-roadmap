# Feature Availability — Điều kiện tính năng

| Năng lực | Environment tested | Account/plan assumption | Feature status | Source checked | Date | Fallback |
|---|---|---|---|---|---|---|
| Chat / prompting | web, mobile | tài khoản ChatGPT | AVAILABLE | [Use ChatGPT](https://learn.chatgpt.com/docs/use-chatgpt), [Prompting](https://learn.chatgpt.com/docs/prompting) | 2026-09-10 | chat văn bản cơ bản |
| Models / reasoning | web | phụ thuộc model hiển thị | LIMITED | [Models](https://learn.chatgpt.com/docs/models) | 2026-09-10 | benchmark cùng một model |
| Projects / memory | web | phụ thuộc tài khoản | LIMITED | [Projects](https://learn.chatgpt.com/docs/projects), [Personalize](https://learn.chatgpt.com/docs/personalize) | 2026-09-10 | chat và file mẫu |
| Search / research | web | phụ thuộc quyền search | LIMITED | [Web Search](https://learn.chatgpt.com/docs/web-search), [Deep Research FAQ](https://help.openai.com/en/articles/10500283-deep-research-faq) | 2026-09-10 | nguồn chính thức mở bằng trình duyệt |
| Files / images / voice | web, mobile | phụ thuộc loại file/thiết bị | LIMITED | [Files](https://learn.chatgpt.com/docs/artifacts-viewer), [Image generation](https://learn.chatgpt.com/docs/image-generation), [Voice](https://learn.chatgpt.com/docs/features/voice) | 2026-09-10 | text, ảnh mẫu hoặc transcript |
| Work / browser / computer | Work/web | phụ thuộc workspace/quota | NOT VERIFIED HERE | [Work](https://learn.chatgpt.com/docs/get-started-with-work), [Browser](https://learn.chatgpt.com/docs/browser), [Computer Use](https://learn.chatgpt.com/docs/computer-use) | 2026-09-10 | chat ngắn hoặc screenshot |
| Plugins / skills / tasks | web | phụ thuộc kết nối/tài khoản | NOT VERIFIED HERE | [Skills & Plugins](https://learn.chatgpt.com/docs/skills-and-plugins), [Build Skills](https://learn.chatgpt.com/docs/build-skills), [Tasks](https://learn.chatgpt.com/docs/automations) | 2026-09-10 | workflow spec trên dữ liệu giả lập |
| Codex / API / MCP / Agents | API/dev environment | cần runtime và quota phù hợp | NOT VERIFIED HERE | [OpenAI Developers](https://developers.openai.com/) | 2026-09-10 | architecture + eval cases |

## Quy tắc sử dụng

Không dùng bảng này để khẳng định mọi tài khoản có cùng tính năng. Lesson phải ghi môi trường đã thử, giả định tài khoản, ngày kiểm tra và fallback. `AVAILABLE` chỉ có nghĩa đã được xác nhận ở môi trường ghi trong bảng.

Các thao tác nhạy cảm như gửi email, sửa dữ liệu, commit, xuất bản hoặc thanh toán luôn cần human review theo lesson.