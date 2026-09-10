# Feature Availability — Điều kiện tính năng

> Snapshot: 2026-09-10. Khả năng hiển thị và quyền sử dụng có thể khác theo tài khoản, gói, khu vực, nền tảng và thời điểm.

## Quy tắc

- Kiểm tra nguồn OpenAI hiện tại trước khi viết thao tác UI.
- Ghi environment, account/plan assumption, feature status và ngày kiểm tra trong lesson.
- Nếu không có tính năng, dùng fallback và ghi `not tested`; không gọi mô phỏng là đã chạy thật.
- Foundation không yêu cầu mua gói hoặc kết nối tài khoản ngoài.

| Năng lực | Nguồn | Fallback |
|---|---|---|
| Chat / prompting | [Use ChatGPT](https://learn.chatgpt.com/docs/use-chatgpt), [Prompting](https://learn.chatgpt.com/docs/prompting) | chat văn bản cơ bản |
| Models / reasoning | [Models](https://learn.chatgpt.com/docs/models) | benchmark cùng một model |
| Projects / memory | [Projects](https://learn.chatgpt.com/docs/projects), [Personalize](https://learn.chatgpt.com/docs/personalize) | chat và file mẫu |
| Search / research | [Web Search](https://learn.chatgpt.com/docs/web-search), [Deep Research FAQ](https://help.openai.com/en/articles/10500283-deep-research-faq) | nguồn chính thức mở bằng trình duyệt |
| Files / images / voice | [Files](https://learn.chatgpt.com/docs/artifacts-viewer), [Image generation](https://learn.chatgpt.com/docs/image-generation), [Voice](https://learn.chatgpt.com/docs/features/voice) | text, ảnh mẫu hoặc transcript |
| Work / browser / computer | [Work](https://learn.chatgpt.com/docs/get-started-with-work), [Browser](https://learn.chatgpt.com/docs/browser), [Computer Use](https://learn.chatgpt.com/docs/computer-use) | chat ngắn hoặc screenshot |
| Plugins / skills / tasks | [Skills & Plugins](https://learn.chatgpt.com/docs/skills-and-plugins), [Build Skills](https://learn.chatgpt.com/docs/build-skills), [Tasks](https://learn.chatgpt.com/docs/automations) | workflow spec trên dữ liệu giả lập |
| Codex / API / MCP / Agents | [OpenAI Developers](https://developers.openai.com/) | architecture + eval cases |

## Metadata bắt buộc

```text
Source snapshot: YYYY-MM-DD
Environment tested: web / desktop / mobile / API / other
Account or plan assumption: ...
Feature status: available / limited / not tested
Fallback exercise: ...
```