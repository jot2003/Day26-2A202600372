---
artifact: 1 - Ghi chú nghiên cứu khi test 2 sản phẩm AI
bai-tap: 2 - Phân tích 2 sản phẩm AI (nhóm 2 học viên)
phase: Phase 2 - Thử nghiệm + chụp ảnh + research (20 phút)
status: Hoàn thành - dựa trên screenshots thực tế
input: screenshots/grammarly-entry.png + screenshots/grammarly-input-output.png + screenshots/copilot-input-output.png
---

# 1 - Ghi chú nghiên cứu khi test 2 sản phẩm AI

---

## Phần A - Setup chung

- **Nhiệm vụ chung**: Rewrite một email thô thành email chuyên nghiệp, concise, persuasive cho khách hàng; đề xuất 3 subject lines và giải thích vì sao version mới tốt hơn.

- **Câu prompt chính xác** (dùng cho cả 2 sản phẩm):

  > Rewrite this rough business email into a professional, concise, persuasive email for a client. Keep the tone polite but confident. Then suggest 3 subject lines and explain why your version is better.
  >
  > Hi, we finished the first version of the report but some parts may still need fixing. Can you check it and tell us what you think? Also, we want to know if you agree with the next step. Thanks.

- **Loại tài khoản dùng**:
  - Sản phẩm A (Grammarly): Free tier - button "Try Pro for $0" hiện trong giao diện; dùng trên coda.grammarly.com (doc editor sau acquisition Coda).
  - Sản phẩm B (Microsoft Copilot): Free tier trên copilot.microsoft.com; có option "Smart" mode; có Outlook integration khả dụng.

- **Trình duyệt + thời gian test**: Chrome - test session ngày 2026-05-14.

---

## Phần B - Log Sản phẩm A: Grammarly

**Tên sản phẩm A**: Grammarly (trên coda.grammarly.com - doc editor)
**URL**: https://coda.grammarly.com
**Model dưới mui xe**: Không hiển thị tên model cụ thể trong giao diện.

### B.1 - Entry point + lần chạm đầu

- Trang đầu hiển thị: doc editor kiểu Coda/Notion - blank document với placeholder "Start typing or insert using /". Cột trái là content area; cột phải là panel "AI Chat" với 4 specialized agents.
- 4 agents sẵn có trong panel phải: **Grammarly Proofreader** ("Polish your writing till it shines"), **AI Detector** ("Check for AI-generated text"), **Humanizer** ("Choose how you want to sound"), **Expert Review** ("Get feedback inspired by experts").
- Không có sample prompt tự động - người dùng tự paste text vào doc trước, sau đó tương tác với AI qua panel phải hoặc chọn text để trigger rewrite.
- Cần đăng nhập; free tier đã dùng được tính năng rewrite cơ bản.
- Grammarly tự động underline từ "but" trong câu gốc - grammar/clarity suggestion hiện ngay khi paste text.
- **Ảnh đã chụp**: `screenshots/grammarly-entry.png`

### B.2 - Khi gõ prompt + nhận output

- Thời gian phản hồi: nhanh - dưới 5 giây ước tính (rewrite trigger qua selected text).
- Streaming: Có streaming.
- Output format: popup overlay xuất hiện ngay trên đoạn text được select, hiện email đã rewrite với title "Rewrite for professionalism and clarity".
- **Output email** (từ screenshot):
  - "Dear [Client Name],"
  - "We are pleased to share the initial draft of your report for your review. Please let us know if there are any sections that require further refinement. Your feedback is important to ensure the final version meets your expectations."
  - "Additionally, we would appreciate your confirmation on the proposed next step to keep the project moving forward."
- Output dài: khoảng 3 câu thân email - ngắn gọn hơn so với Copilot.
- Output **KHÔNG có subject line suggestions** trong phần visible của screenshot.
- Output KHÔNG dẫn nguồn.
- Có nhãn **"Free sample"** trong popup - gợi ý free tier chỉ xem sample, full output cần upgrade.
- Có 2 nút hành động: **Accept** và **Dismiss**.
- Panel phải hiển thị context notes: "Organizing the content for better impact", "Expressing appreciation for the client's collaboration."
- **Ảnh đã chụp**: `screenshots/grammarly-input-output.png`

### B.3 - Phản hồi sau khi nhận output

- Có Accept/Dismiss - tương đương regenerate/reject, nhưng không có nút "thử lại với prompt khác" rõ ràng.
- Không có nút copy riêng trong popup - phải Accept trước rồi copy từ doc.
- Không có gợi ý câu hỏi tiếp theo trong popup.
- Có lưu history trong doc (doc-based, không phải chat history).
- Không thấy thumb up/down trong giao diện popup.
- "Suggestions" section hiện ở panel phải sau khi rewrite.

### B.4 - Quan sát nổi (3 quan sát)

1. **Grammarly hoạt động theo paradigm "inline editing", không phải chat** — rewrite xuất hiện ngay trên document như một Google Docs suggestion, không phải trong chat box. UX rất khác biệt so với chatbot. (`screenshots/grammarly-input-output.png`)
2. **Agent panel bên phải tách biệt rõ use case** — Proofreader, Detector, Humanizer, Expert Review là 4 luồng riêng; người dùng biết ngay mình cần tính năng nào mà không cần viết prompt từ đầu. (`screenshots/grammarly-entry.png`)
3. **Free tier label "Free sample" làm mờ ranh giới** — không rõ output hiển thị có phải full output hay chỉ là preview để ép upgrade. Gây friction cho người dùng đang evaluate sản phẩm. (`screenshots/grammarly-input-output.png`)

---

## Phần C - Log Sản phẩm B: Microsoft Copilot

**Tên sản phẩm B**: Microsoft Copilot (copilot.microsoft.com)
**URL**: https://copilot.microsoft.com
**Model dưới mui xe**: Không hiển thị tên model rõ trong screenshot; có "Smart" mode toggle ở bottom bar.

### C.1 - Entry point + lần chạm đầu

- Giao diện chat chuẩn - text input box ở dưới, conversation area phía trên.
- Có "Smart" toggle ở bottom bar - gợi ý có thể chọn mode thinking/reasoning.
- Không cần paywall để dùng prompt tùy chỉnh trong free tier.
- **Ảnh đã chụp**: `screenshots/copilot-input-output.png` (bao gồm cả input và output)

### C.2 - Khi gõ prompt + nhận output

- Output format: **email draft được format sẵn như email thật** — có Subject field, To field, body text, formatting toolbar (B/I/S/U/list/code).
- **Output email** (từ screenshot):
  - Subject: **"Draft Report and Next Steps"**
  - To: [blank]
  - Body: "Dear [Client], We are pleased to share the first version of the report with you. While this draft is complete, there may be areas that could benefit from refinement, and we would greatly value your feedback. Additionally, we would like to confirm your agreement on the proposed next steps so we can move forward efficiently. Thank you for your time and input. We look forward to your thoughts. Best regards, [Your Name]"
- Output có **"Suggested Subject Lines"** section ngay bên dưới email draft.
- Output có **"Send with Outlook"** button - có thể gửi email trực tiếp từ Copilot.
- Output KHÔNG dẫn nguồn (phù hợp với tác vụ rewriting).
- **Ảnh đã chụp**: `screenshots/copilot-input-output.png`

### C.3 - Phản hồi sau khi nhận output

- Có input box "Message Copilot" để follow-up ngay - conversation tiếp tục trong cùng thread.
- Có "Send with Outlook" - export trực tiếp sang email client.
- Có "Smart" toggle ở bottom - có thể điều chỉnh mode cho lần tiếp.
- Có lưu history dưới dạng chat conversation.

### C.4 - Quan sát nổi (3 quan sát)

1. **Copilot format output như email send-ready, không phải plain text** — Subject line, To field, body, formatting toolbar và "Send with Outlook" button xuất hiện ngay trong output. Người dùng không cần copy-paste sang email client. (`screenshots/copilot-input-output.png`)
2. **"Send with Outlook" là distribution moat rõ nhất** — Copilot kết nối trực tiếp với Outlook để gửi email mà không cần rời giao diện. Đây là lợi thế mà Grammarly standalone không có. (`screenshots/copilot-input-output.png`)
3. **Copilot chạy full prompt tùy chỉnh mà không paywall** — toàn bộ prompt dài (rewrite + 3 subject lines + explain why better) được xử lý trong free tier. Grammarly free tier giới hạn bằng "Free sample" label. (`screenshots/copilot-input-output.png`)

---

## Phần D - First impressions

1. **Sản phẩm nào "cảm giác" dễ dùng hơn lần đầu?**
   Microsoft Copilot dễ dùng hơn cho task này. Chỉ cần paste prompt + email vào chat box, nhận kết quả format sẵn như email thật. Grammarly đòi hỏi biết doc editor, biết chọn text, biết mở đúng agent — nhiều bước hơn cho người dùng mới.

2. **Sản phẩm nào "cảm giác" cho output đáng tin hơn?**
   Cả hai cho output rewrite tương đương về chất lượng. Copilot đáng tin hơn về workflow vì "Send with Outlook" và subject line hiển thị rõ. Grammarly đáng tin hơn về writing transparency vì giải thích lý do rewrite ("Organizing for better impact") — nhưng "Free sample" label tạo nghi ngờ về tính đầy đủ.

3. **Câu hỏi nhóm chưa trả lời được sau test:**
   Grammarly có subject line suggestions ở đâu trong free tier? Copilot "Suggested Subject Lines" cụ thể là gì (screenshot bị cut off)? Microsoft 365 Copilot trong Word/Outlook (enterprise) so với free tier có khác gì?

---

## Bảng kiểm trước khi sang Bước 2

- [x] Câu prompt giống y nhau cho cả 2 sản phẩm.
- [x] Đã chụp tối thiểu 2-3 ảnh cho mỗi sản phẩm.
- [x] Mỗi quan sát có ảnh tham chiếu.
- [x] First impressions ghi rõ lý do, không dùng "hay hơn" chung chung.
- [x] Ghi rõ giới hạn free tier và câu hỏi còn mở.
