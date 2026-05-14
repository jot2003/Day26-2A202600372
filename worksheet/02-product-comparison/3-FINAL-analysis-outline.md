---
artifact: 3 — Outline 5 mục cho slide deck Analysis Report
bai-tap: 2 — Phân tích 2 sản phẩm AI (nhóm 2 học viên)
phase: Phase 3 — Dựng slide deck
nop-cuoi: Có gián tiếp — outline này là cốt cho `analysis-report.pdf`
---

# 3 — Outline slide deck: Grammarly vs Microsoft Copilot

## Thông tin chung

- **Mã 2 thành viên**: 2A202600372 (Hoàng Kim Trí Thành) + 2A202600228 (Nguyễn Trọng Tiến)
- **Ngành**: C — Viết lách (AI writing & workplace productivity)
- **Nhiệm vụ chung**: Rewrite rough business email thành professional email + 3 subject lines
- **Sản phẩm A**: Grammarly — https://coda.grammarly.com
- **Sản phẩm B**: Microsoft Copilot — https://copilot.microsoft.com
- **Câu prompt**: "Rewrite this rough business email into a professional, concise, persuasive email for a client. Keep the tone polite but confident. Then suggest 3 subject lines and explain why your version is better. [email thô]"

---

## S1 — Product Moment (slide 1–2)

### S1.1 — Bảng so sánh nhanh

| Yếu tố | Grammarly | Microsoft Copilot |
|---|---|---|
| Tên + URL | Grammarly — coda.grammarly.com | Microsoft Copilot — copilot.microsoft.com |
| Entry point | Doc editor (Coda-based) + AI panel bên phải với 4 agents | Chat interface chuẩn, "Ask anything" |
| Ý định người dùng | Chỉnh sửa văn bản trong document — "polish my writing" | Tạo draft email từ đầu — "do the work for me" |
| Surface chính | Document canvas + AI agent panel | Conversational chat |
| Đăng nhập / paywall | Cần login; free tier có "Free sample" limit | Cần login; free tier full-featured cho task này |

### S1.2 — Bằng chứng

- `screenshots/grammarly-entry.png` — Grammarly: doc editor với 4 agent panel (Proofreader, Detector, Humanizer, Expert Review)
- `screenshots/copilot-input-output.png` — Copilot: chat interface với output email send-ready

### S1.3 — Nhận định so sánh entry point

Grammarly định vị như **writing enhancement tool** — người dùng paste text vào doc rồi mới dùng AI. Copilot định vị như **AI writing assistant** — người dùng đưa yêu cầu, AI tạo từ đầu. Với task "viết email chuyên nghiệp cho khách hàng", Copilot có intent alignment tốt hơn ngay từ lần đầu tiếp xúc; Grammarly phù hợp hơn khi user đã có draft và muốn cải thiện.

---

## S2 — Workflow Evidence (slide 3–4)

### S2.1 — Luồng người dùng

```
TRƯỚC khi gặp AI:
- Người dùng có email thô cần gửi cho khách hàng, muốn nâng cấp lên chuyên nghiệp

TRONG khi dùng Grammarly:
1. Mở coda.grammarly.com → tạo blank doc
2. Paste email thô vào document
3. Chọn (select) toàn bộ text
4. Trigger Proofreader agent → popup "Rewrite for professionalism"
5. Accept hoặc Dismiss
6. Copy text từ doc → paste sang email client riêng để gửi
(6-7 bước, chuyển đổi giữa 2 ứng dụng)

TRONG khi dùng Microsoft Copilot:
1. Mở copilot.microsoft.com
2. Paste toàn bộ prompt + email thô vào chat box
3. Nhận email draft format sẵn (Subject, To, Body) + Suggested Subject Lines
4. Bấm "Send with Outlook" để gửi trực tiếp
(2-3 bước, không cần rời giao diện)

SAU khi dùng AI:
- Grammarly: còn cần copy-paste sang Gmail/Outlook + viết subject line thủ công
- Copilot: "Send with Outlook" — gửi ngay từ trong giao diện
```

### S2.2 — 3 Friction Areas

| Friction | Grammarly | Microsoft Copilot |
|---|---|---|
| Physical load | 5-6 bước: doc → paste → select → trigger → accept → copy sang email | 2-3 bước: paste prompt → nhận draft → Send with Outlook |
| Cognitive burden | Cần biết doc editor paradigm + 4 agents + cách trigger inline rewrite | Chat interface quen thuộc, không cần biết gì thêm |
| User workarounds | Copy-paste sang email client; upgrade để thoát "Free sample" giới hạn | Bấm "Enable Outlook" lần đầu; scroll để thấy Suggested Subject Lines |

### S2.3 — Bằng chứng

- `screenshots/grammarly-input-output.png` — popup rewrite overlay, Accept/Dismiss, context notes panel phải
- `screenshots/copilot-input-output.png` — email send-ready output với Subject field + "Send with Outlook" button

### S2.4 — Nhận định

Copilot giảm friction rõ rệt cho task "viết email từ đầu": từ 6-7 bước xuống 2-3 bước, không cần chuyển đổi ứng dụng nhờ Outlook integration. Grammarly phù hợp hơn với user đã quen workflow doc-based và muốn kiểm soát từng thay đổi — nhưng với người dùng mới hoặc deadline gấp, Copilot là lựa chọn ít friction hơn đáng kể.

---

## S3 — Output & Trust (slide 5–6)

### S3.1 — Chất lượng output

- **Grammarly** (`screenshots/grammarly-input-output.png`):
  - Trả lời đúng yêu cầu: **Có** — email rewrite professional, concise, polite
  - Hallucination: **Không** — rewrite dựa trên text gốc, không thêm thông tin bịa
  - Đầy đủ: **Không hoàn toàn** — "Free sample" label, KHÔNG có subject line suggestions trong visible output

- **Microsoft Copilot** (`screenshots/copilot-input-output.png`):
  - Trả lời đúng yêu cầu: **Có** — email rewrite professional + Subject field + Suggested Subject Lines section
  - Hallucination: **Không** — rewrite từ email thô, không thêm thông tin sai
  - Đầy đủ: **Có** — full output không bị cắt trong free tier; cả subject lines lẫn explanation đều có

### S3.2 — 6 Tín hiệu đáng tin

| Tín hiệu | Grammarly | Microsoft Copilot |
|---|---|---|
| 1. Dẫn nguồn | Không cần — task rewriting | Không cần — task rewriting |
| 2. Disclaimer khi không chắc | Không thấy | Không thấy |
| 3. Fallback khi out-of-scope | Không quan sát được | Không quan sát được |
| 4. Consistency (2 lần cùng prompt) | Không test | Không test |
| 5. User control | **Accept / Dismiss** — kiểm soát từng thay đổi | **Follow-up chat** + "Send with Outlook" |
| 6. Explanation ("vì sao AI nói thế") | **Có** — context notes: "Organizing for better impact", "Expressing appreciation" | **Không** — output là email final, không giải thích rationale |

### S3.3 — Nhận định

Grammarly transparent hơn về lý do rewrite (context notes giải thích từng chỉnh sửa) — tốt cho user muốn học và kiểm soát. Copilot actionable hơn với send-ready format — tốt cho user muốn xong việc nhanh. Điểm trừ Grammarly: "Free sample" tạo uncertainty về tính đầy đủ của output; điểm trừ Copilot: không giải thích tại sao version mới tốt hơn (dù prompt yêu cầu).

---

## S4 — Business Signal (slide 7)

### S4.1 — Định vị tam giác

- **Grammarly**: **mạnh-đắt** — writing quality + grammar accuracy cao; phải trả $12-30/tháng để unlock full GenAI; brand voice enforcement cho enterprise. Trade-off: friction cao + cần upgrade.
- **Microsoft Copilot**: **cân bằng + distribution advantage** — free tier đủ mạnh cho task thông thường; lợi thế thực sự là Microsoft 365 ecosystem (Word/Outlook/Teams), không phải AI quality.

### S4.2 — Pricing pattern

| Yếu tố | Grammarly | Microsoft Copilot |
|---|---|---|
| Mô hình giá | Freemium (limited) → Seat-based Pro | Freemium (robust) → M365 bundle |
| Free tier giới hạn | "Free sample" output, không có brand voice, limited GenAI | Full chat capability; Outlook integration cần enable |
| Gói trả phí chính | Pro: $12-30/user/month | Microsoft 365 Copilot: $30/user/month |
| Paywall | "Free sample" label xuất hiện trong rewrite popup | Ít thấy paywall trong consumer tier; enterprise features trong M365 |

### S4.3 — Nhận định chiến lược

Grammarly monetize bằng quality gate (phải trả mới thấy full output); Copilot monetize bằng ecosystem lock-in (free tier đủ dùng, nhưng giá trị thật ở M365 integration mà enterprise đã trả $30/user/month). Chiến lược của Copilot bền hơn: không cần thuyết phục user nâng cấp riêng — enterprise tự adopt vì đã có M365 subscription.

---

## S5 — Product Judgment (slide 8–12)

### S5.1 — Verdict

- **Grammarly**: **Promising** — writing quality và agent UX tốt, đang pivot đúng hướng (Coda acquisition), nhưng distribution moat mỏng và đang bị Big Tech tấn công từ cấp platform. Window of opportunity hẹp dần.
- **Microsoft Copilot**: **Strong** — distribution moat từ Microsoft 365 ecosystem (85,000+ tổ chức) tạo switching cost cao; "Send with Outlook" là tính năng không thể replicate bằng browser extension. Rủi ro: Google Workspace AI đang cạnh tranh cùng chiến lược distribution.

### S5.2 — User base + tăng trưởng

- **Grammarly**: 40M+ daily active users (2024); 50,000+ paying teams — Source: Grammarly blog 2024
- **Microsoft Copilot (M365)**: 85,000+ organizations using M365 Copilot (2024) — Source: Microsoft Build 2024 keynote; tổng Microsoft 365 users: 400M+

### S5.3 — Doanh thu / pricing power

- **Grammarly**: ARR $700M+ (2023, không công khai chính thức) — Source: ước tính từ Forbes/TechCrunch. Freemium → Pro $12-30/tháng → Enterprise custom pricing.
- **Microsoft Copilot**: Revenue đến từ M365 bundle — Microsoft Commercial Cloud revenue $135B+ (FY2024); Copilot add-on $30/user/month chưa tách riêng. Pricing power rất mạnh vì bundle vào subscription enterprise hiện có.

### S5.4 — Moat phân tích

| Moat | Grammarly | Microsoft Copilot |
|---|---|---|
| Data (proprietary) | **Trung bình** — 15+ năm dữ liệu grammar corrections từ 40M DAU | **Mạnh** — OpenAI GPT-4 + Microsoft proprietary data từ Office 365 |
| Network effects | **Yếu** — users không tương tác nhau; không có network compounding | **Trung bình** — Copilot trong Teams tạo network effect trong tổ chức |
| Switching cost | **Thấp** — extension dễ gỡ, thay bằng ChatGPT | **Mạnh** — M365 integration; thay Copilot = thay cả workflow Word/Outlook/Teams |
| Brand | **Mạnh với writers/editors** — "Grammarly" = grammar checker trong văn hóa đại chúng | **Trung bình** — "Copilot" chưa có brand identity mạnh độc lập khỏi Microsoft |
| Distribution | **Yếu-Trung** — browser extension + standalone web | **Rất mạnh** — pre-installed trong Windows, tích hợp Word/Outlook/Teams/Edge |

- **Moat chủ đạo Grammarly**: Brand (trong writing community) + Data (grammar corrections)
- **Moat chủ đạo Copilot**: Distribution (Microsoft 365 ecosystem) + Switching cost (workflow lock-in)

### S5.5 — Data flywheel + feedback loop

- **Grammarly**: Users accept/dismiss suggestions → signal về grammar patterns → cải thiện model grammar detection. Loop **có compounding nhưng yếu** — 40M DAU tạo signal lớn, nhưng grammar feedback không tạo ra user-to-user network.
- **Microsoft Copilot**: Users dùng trong Word/Outlook/Teams → interaction data feed lại OpenAI + Microsoft → model cải thiện. Loop **mạnh hơn** nhờ volume (400M+ M365 users) và context (biết user đang làm gì trong Office suite).

### S5.6 — Niche Down + AI Feature Map

**Grammarly**:
- Niche: Writers, content creators, non-native English speakers, và teams cần brand voice consistency — "polish existing writing"
- AI Feature Map:
  - User Value: **Cao** — giải quyết đúng vấn đề grammar/clarity/tone cho writer
  - User Alignment: **Trung bình** — agent UX tốt nhưng doc editor paradigm có learning curve
  - Business Value: **Trung bình** — freemium conversion OK nhưng GenAI tạo pressure lên pricing model

**Microsoft Copilot**:
- Niche: Enterprise knowledge workers trong Microsoft 365 ecosystem — "generate first draft + send directly"
- AI Feature Map:
  - User Value: **Cao** — output send-ready, giảm friction đáng kể cho email/document workflow
  - User Alignment: **Cao** — chat interface familiar, "Send with Outlook" matches intent
  - Business Value: **Rất cao** — bundle vào M365 tạo revenue tự động, không cần separate conversion funnel

### S5.7 — Spark → Loop → System

- **Grammarly**: Đang ở giai đoạn **Loop → System** (chuyển tiếp) — đã có user base lớn (40M DAU) và revenue ($700M ARR), nhưng đang bị disrupt bởi ChatGPT/Copilot. Coda acquisition là nỗ lực thoát Loop thành System bằng platform play. **Dự báo 12 tháng**: Nếu doc editor + agent UX được adopt rộng, có thể consolidate vị trí System trong niche "professional writing platform". Nếu không, tiếp tục suy giảm market share trong general writing.

- **Microsoft Copilot**: Đã ở giai đoạn **System** — Microsoft 365 với 400M+ users là System đã vững; Copilot là feature extension trên System đó. **Dự báo 12 tháng**: Tiếp tục mở rộng enterprise adoption; GPT-5 integration sẽ nâng quality thêm; cạnh tranh trực tiếp với Google Workspace AI Gemini.

### S5.8 — Liên hệ Lab 1 (Chegg case)

- **Grammarly có rủi ro Chegg-style không?**: **Có** — tương tự Chegg, Grammarly có Data moat (grammar database 15 năm) nhưng switching cost thấp và bị Big Tech (Microsoft Copilot, Google Docs AI) tấn công bằng distribution moat mạnh hơn. Chegg mất 43% subscribers trong 12 tháng vì ChatGPT làm được điều tương tự miễn phí; Grammarly đang bị Copilot làm điều tương tự với email writing — miễn phí hơn, ít friction hơn.
- **Microsoft Copilot có rủi ro Chegg-style không?**: **Thấp** — Copilot đang ở vị trí "big tech AI" tấn công, không phải bị tấn công. Rủi ro duy nhất là Google Workspace AI Gemini với Google Docs distribution tương tự.

**Bài học từ Lab 1 (Chegg) áp dụng cho Lab 2**:

1. **Niche Down là sống còn**: Chegg không niche đủ sâu → ChatGPT thay thế toàn bộ. Grammarly đang đúng hướng khi pivot sang "professional writing platform với brand voice" thay vì cạnh tranh general writing với ChatGPT. Cần đẩy niche sâu hơn nữa (vd: legal writing, academic integrity, multilingual brand voice).
2. **Distribution moat > Data moat trong kỷ nguyên LLM**: Chegg có 68M Q&A database nhưng thua ChatGPT vì ChatGPT đến tay user qua Google/internet. Copilot có distribution moat qua M365 — đây là moat bền nhất, khó replicate bằng extension hay standalone app.
3. **Switching cost phải được build vào product, không phải vào contract**: Chegg switching cost = 0 → churn ngay. Grammarly switching cost thấp (gỡ extension là xong) → vulnerable. Copilot switching cost cao vì embedded vào workflow Word/Outlook/Teams — đây là thiết kế đúng.

---

## Bảng kiểm trước khi build slide

- [x] S1 → S4 đã điền đầy đủ.
- [x] S5.1 Verdict: Grammarly Promising, Copilot Strong.
- [x] S5.6 Niche + AI Feature Map: đã điền cho cả 2 sản phẩm.
- [x] S5.7 Spark→Loop→System: Grammarly Loop→System (chuyển tiếp), Copilot System.
- [x] S5.8 Liên hệ Lab 1 Chegg: Grammarly có rủi ro Chegg-style, Copilot thấp.
- [x] S5.2-S5.5: đã có số liệu + nguồn (Grammarly 40M DAU, Copilot 85K tổ chức).
- [x] Verdict nhất quán với moat + giai đoạn Spark/Loop/System.
- [x] 2 thành viên đồng ý với outline.
