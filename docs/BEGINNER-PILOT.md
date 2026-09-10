# Beginner Pilot — Kịch bản thử học người mới

> **Status:** PREPARED — NOT RUN  
> **Prepared in:** U05  
> **Execution target:** U06  
> **Important:** AI/self-review không được ghi là pilot với người mới thật.

## 1. Purpose — Mục tiêu

Kiểm tra xem một người mới có thể tự học BOOT + M00 + M01 mà không cần tác giả giải thích miệng hay không.

Pilot không nhằm chứng minh “nội dung hay”; nó nhằm phát hiện điểm chặn:

- không biết bắt đầu ở đâu;
- thuật ngữ chưa được giải thích;
- instruction khó làm theo;
- file/link không tìm thấy;
- exercise không thể tái lập;
- rubric không đủ rõ để tự chấm;
- learner không biết khi nào được PASS.

## 2. Pilot participant — Người thử học

Ghi sau khi có người thử thật:

- Participant ID / mã ẩn danh:
- Prior ChatGPT experience:
- Prior GitHub experience:
- English comfort level:
- Device / surface:
- Date:

Không lưu tên thật hoặc dữ liệu riêng tư nếu không cần.

## 3. Scope — Phạm vi

Pilot v0.2.0 preview gồm 11 lesson READY:

- BOOT.1–BOOT.4
- M00.1–M00.3
- M01.1–M01.4

Checkpoints/labs:

- BOOT Check
- M00 Check
- M01 Check
- P-001 Summary
- P-002 Planning
- P-003 Comparison

## 4. Test rule — Quy tắc thử

Người thử:

1. bắt đầu từ `README.md` / `START-HERE.md`;
2. tự tìm lesson tiếp theo;
3. làm theo instruction mà không được tác giả giải thích thêm;
4. ghi nơi bị mắc trước khi nhận trợ giúp;
5. dùng dữ liệu giả lập khi phù hợp;
6. tự chấm checkpoint theo rubric;
7. lưu evidence đã làm sạch.

Người quan sát chỉ can thiệp nếu learner không thể tiếp tục; mọi can thiệp phải được ghi lại vì đó là dấu hiệu tài liệu chưa self-service.

## 5. Observation log — Nhật ký quan sát

| Step / lesson | Start–end | Blocker | Needed help? | Evidence | Fix candidate |
|---|---|---|---|---|---|
| | | | | | |

## 6. Blocker severity — Mức độ lỗi

| Severity | Meaning | Release action |
|---|---|---|
| S0 | wording/style, không cản học | có thể sửa sau |
| S1 | gây chậm/nhầm nhưng learner tự vượt qua | nên sửa trước release |
| S2 | learner không thể tiếp tục hoặc hiểu sai core concept | bắt buộc sửa + retest |
| S3 | privacy/safety hoặc evidence workflow gây rủi ro đáng kể | dừng pilot/release cho tới khi sửa |

## 7. Minimum evidence for U06 — Evidence tối thiểu

U06 chỉ có thể nói beginner pilot đã chạy khi có:

- participant profile ẩn danh;
- actual time per major section;
- blocker log;
- ít nhất một assessment được learner tự làm;
- điểm/rubric + evidence;
- danh sách fixes;
- retest cho mọi S2/S3 blocker;
- release decision.

## 8. Pilot questions — Câu hỏi sau buổi học

### Navigation
- Bạn có biết bắt đầu ở đâu không?
- Có lúc nào không biết bài tiếp theo là gì không?

### Language
- Có thuật ngữ tiếng Anh nào được dùng trước khi giải thích không?
- Phần song ngữ có giúp hiểu hay làm bài dài/khó hơn quá mức?

### Practice
- Bạn có hiểu chính xác cần tạo output gì không?
- Bạn có biết dùng dữ liệu nào và kiểm đáp án ở đâu không?

### Verification
- Bạn có phân biệt được “AI nói đúng” và “có evidence” không?
- Bạn có biết khi nào cần source/calculation/test/human review không?

### PASS
- Bạn có thể tự trả lời “Tôi đã PASS chưa? Vì sao?” không?

## 9. Release decision — Quyết định phát hành

Chỉ đánh dấu sau pilot:

- [ ] 11 lesson READY vẫn usable sau test thực tế.
- [ ] Không còn S2/S3 blocker chưa sửa.
- [ ] 3 prompt labs làm được bằng input đã cung cấp.
- [ ] Rubric đủ rõ để learner tự chấm với sai lệch chấp nhận được.
- [ ] Mọi link chặn đường học hoạt động.
- [ ] Evidence/privacy instructions không dẫn learner tới chia sẻ dữ liệu nhạy cảm.
- [ ] Các fixes quan trọng đã retest.

### Decision

`PENDING — U06 beginner pilot has not been run.`

## 10. Important distinction — Phân biệt quan trọng

U05 self-QA có thể chứng minh rằng file tồn tại, logic/rubric nhất quán và lab có ground truth. Nó **không** chứng minh người mới thật có thể tự học. Chỉ evidence từ U06 mới được dùng cho tuyên bố đó.
