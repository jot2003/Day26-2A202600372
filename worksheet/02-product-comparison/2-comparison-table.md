---
artifact: 2 - Bảng so sánh 2 sản phẩm theo 5 mục
bai-tap: 2 - Phân tích 2 sản phẩm AI (nhóm 2 học viên)
phase: Chuyển giao Phase 2 - Phase 3 (5 phút)
status: Hoàn thành - dựa trên screenshots + research Lab 1
input: 1-research-notes.md + screenshots/ + 01-bigtech-disruption/1-research.md
---

# 2 - Bảng so sánh Grammarly vs Microsoft Copilot theo 5 mục

**Ngành**: C — AI writing & workplace productivity
**Sản phẩm A**: Grammarly (coda.grammarly.com - free tier)
**Sản phẩm B**: Microsoft Copilot (copilot.microsoft.com - free tier)
**Nhiệm vụ test**: Rewrite rough business email + suggest 3 subject lines + explain why better

---

## Phần A - Bảng so sánh 5 mục

| Mục | Grammarly (Sản phẩm A) | Microsoft Copilot (Sản phẩm B) |
|---|---|---|
| **S1 - Product Moment**<br><sup>Entry point + ý định người dùng + surface chính</sup> | Doc editor (coda.grammarly.com) — người dùng paste text vào document, chọn text để trigger rewrite, hoặc dùng agent panel bên phải. Surface: document canvas + AI panel. Có 4 specialized agents: Proofreader, Detector, Humanizer, Expert Review. | Chat interface chuẩn — người dùng paste toàn bộ prompt + email thô vào chat box, nhận response ngay. Surface: chat canvas. Không cần biết trước cấu trúc giao diện để bắt đầu. |
| **S2 - Workflow Evidence**<br><sup>Trước / trong / sau khi dùng AI. Friction chính</sup> | Workflow: mở doc editor → paste text → chọn text → trigger Proofreader agent → Accept/Dismiss popup → copy từ doc sang email client. Friction: nhiều bước thao tác; sau Accept vẫn phải copy-paste sang email client riêng. | Workflow: mở copilot.microsoft.com → paste full prompt → nhận email draft format sẵn → bấm "Send with Outlook" để gửi trực tiếp. Friction thấp hơn: Copilot format output như email thật, có Outlook integration để gửi mà không cần rời giao diện. |
| **S3 - Output & Trust**<br><sup>Chất lượng output + dẫn nguồn + disclaimer + control</sup> | Output quality: rewrite tốt, concise, chuyên nghiệp. Có context notes giải thích lý do rewrite ("Organizing for better impact", "Expressing appreciation"). **KHÔNG có subject line** trong visible output — có thể bị giới hạn bởi free tier ("Free sample" label). Control: Accept/Dismiss. | Output quality: rewrite tốt, có Subject field rõ ("Draft Report and Next Steps"), body 3-4 câu professional. Có "Suggested Subject Lines" section. Output format như email send-ready. Chạy full prompt trong free tier không bị cắt. Control: follow-up chat + "Send with Outlook". |
| **S4 - Business Signal**<br><sup>Pricing + giới hạn / paywall + Cost-Capability-Speed</sup> | Free tier có giới hạn ("Free sample" label gợi ý output có thể bị cắt). Grammarly Pro: $12/member/month (trả năm) hoặc $30/month. Định vị: mạnh về writing quality + grammar correction + brand voice (enterprise). Phải trả để unlock full GenAI features. | Free tier cho phép dùng custom prompt đầy đủ, không thấy paywall rõ trong test. Microsoft 365 Copilot Enterprise: $30/user/month, nhưng integrated vào Word/Outlook/Teams — bundle value cao hơn so với standalone. Định vị: workflow integration thắng bằng distribution. |
| **S5 - Product Judgment**<br><sup>Verdict 1 dòng: Strong / Promising / Weak / At Risk + lý do</sup> | **Promising — nhưng At Risk nếu không thoát khỏi grammar checker positioning**. Writing quality tốt, agent UX thú vị, nhưng distribution bị Big Tech AI tấn công từ cấp platform. Coda acquisition cho thấy đúng hướng nhưng chuyển đổi chưa hoàn tất. | **Strong về workflow integration, Promising về writing specialization**. Lợi thế rõ nhất là Outlook integration và chat UX đơn giản. Nhưng output writing quality không vượt trội rõ so với Grammarly — thắng vì distribution, không phải vì AI writing tốt hơn. |

---

## Phần B - 3 Friction Areas (Lens 3)

- **Physical load** (số click / tab / lần copy-paste):
  - Grammarly: cao hơn — mở doc editor, paste text, chọn text, trigger agent, Accept popup, rồi vẫn cần copy sang email client riêng. ~5-6 bước.
  - Copilot: thấp hơn — paste prompt vào chat, nhận email draft, bấm "Send with Outlook". ~2-3 bước.

- **Cognitive burden** (cần học prompt / có hint sẵn / nhớ ngữ cảnh):
  - Grammarly: cao hơn với người mới — cần biết doc editor paradigm, biết 4 agents làm gì, biết cách trigger inline rewrite bằng selected text.
  - Copilot: thấp hơn — chat interface familiar với bất kỳ ai đã dùng ChatGPT; paste prompt là xong.

- **User workarounds** (phải tự làm gì để bù yếu điểm):
  - Grammarly: phải copy-paste email draft từ doc sang email client; có thể phải upgrade để nhận full output không bị "Free sample" giới hạn.
  - Copilot: phải bấm "Enable Outlook" lần đầu để dùng Send with Outlook; "Suggested Subject Lines" cần scroll để thấy.

---

## Phần C - 6 Trust Signals

| Tín hiệu đáng tin | Grammarly (A) | Microsoft Copilot (B) |
|---|---|---|
| 1. Dẫn nguồn (citation) | Không có — phù hợp với task rewriting | Không có — phù hợp với task rewriting |
| 2. Disclaimer khi không chắc | Không thấy trong screenshot | Không thấy trong screenshot |
| 3. Fallback khi out-of-scope | Không quan sát được | Không quan sát được |
| 4. Consistency (chạy 2 lần) | Không test 2 lần | Không test 2 lần |
| 5. User control (sửa, dừng, regenerate) | Accept / Dismiss rõ ràng | Follow-up chat + "Send with Outlook" |
| 6. Explanation ("vì sao AI nói thế") | **Có** — context notes giải thích lý do rewrite ("Organizing for impact", "Expressing appreciation") | **Không thấy** — output là email final, không có explanation về rationale |

**Điểm nổi bật**: Grammarly transparent hơn về lý do rewrite; Copilot actionable hơn với send-ready format.

---

## Phần D - Định vị Cost-Capability-Speed

- **Grammarly nghiêng về**: **mạnh-đắt** — tập trung writing quality, grammar accuracy, brand voice (enterprise); cần upgrade để unlock full GenAI. Free tier bị giới hạn.
- **Copilot nghiêng về**: **cân bằng với lợi thế distribution** — free tier đủ mạnh cho task thông thường; lợi thế thực sự không phải AI quality mà là Outlook/Teams/Word integration trong Microsoft 365 ecosystem.

---

## Phần E - Verdict sơ bộ

- **Grammarly**: **Promising — chuyển đổi chiến lược đúng hướng nhưng chưa hoàn tất**
  - Writing quality tốt, agent UX phân tầng rõ, nhưng free tier friction cao và distribution moat đang bị Big Tech tấn công. Coda acquisition đúng hướng nhưng người dùng vẫn thấy Grammarly là grammar checker.

- **Copilot**: **Strong về distribution, Promising về AI quality**
  - "Send with Outlook" integration là lợi thế không thể replicate bằng extension — distribution moat từ platform ownership. Nhưng nếu tách khỏi Microsoft 365 ecosystem, writing quality không vượt trội rõ so với Grammarly.

---

## Liên hệ Lab 1 (Chegg case)

Kết quả test này xác nhận luận điểm từ Lab 1:

1. **Distribution beats product speed**: Copilot không ra mắt sớm hơn GrammarlyGO (cả hai tháng 3/2023), nhưng thắng trong enterprise vì Microsoft sở hữu bề mặt viết — Word, Outlook, Teams. Tương tự ChatGPT sở hữu kênh trực tiếp đến sinh viên, phá Chegg's distribution.
2. **Core feature commoditisation**: Cả hai cho output rewrite tương đương. Sự khác biệt không ở AI writing quality mà ở workflow integration — giống Chegg vs ChatGPT: cùng giải được bài tập, ChatGPT thắng vì không cần trả tiền riêng.
3. **Grammarly's strategic repositioning visible**: coda.grammarly.com là minh chứng Grammarly đang chuyển khỏi grammar checker — URL đã là Coda, interface là doc editor. Đây là "pivot late" tương tự CheggMate ra mắt 5 tháng sau ChatGPT.
