# Tài liệu đào tạo — Performance Branding Planner

> Tập hợp **prompt đầu vào → đầu ra mẫu** cho từng năng lực của Agent. Dùng để đào tạo người vận hành: học cách ra lệnh đúng và biết trước Agent sẽ trả về gì.
>
> Ký hiệu trong tài liệu: **⌨️ Prompt** = câu bạn gõ · **🖥️ Đầu ra mẫu** = kết quả Agent trả về (rút gọn minh họa) · **📝 Ghi chú** = điểm cần lưu khi đào tạo.
> Mọi số liệu/tên bác sĩ/case trong đầu ra thật đều phải mang cờ `⚠ Cần xác minh từ Kangnam` — Agent **không bịa để lấp bảng**.

---

## Mục lục
1. [Nguyên tắc ra lệnh chung](#1-nguyên-tắc-ra-lệnh-chung)
2. [Khởi động & kiểm tra Agent](#2-khởi-động--kiểm-tra-agent)
3. [PLAN mode — Kế hoạch & chiến lược](#3-plan-mode--kế-hoạch--chiến-lược)
4. [PLAN mode — Prompt theo bước](#4-plan-mode--prompt-theo-bước)
5. [CONTENT mode — Kịch bản & content](#5-content-mode--kịch-bản--content)
6. [CONTENT mode — Content Bank](#6-content-mode--content-bank)
7. [CONTENT PLAN — Bảng kế hoạch nội dung 3 tầng](#7-content-plan--bảng-kế-hoạch-nội-dung-3-tầng)
8. [Tương tác xuất Excel](#8-tương-tác-xuất-excel)
9. [Guardrails trong thực tế](#9-guardrails-trong-thực-tế)
10. [Khi prompt mơ hồ — Agent hỏi lại](#10-khi-prompt-mơ-hồ--agent-hỏi-lại)
11. [Bài tập thực hành](#11-bài-tập-thực-hành)

---

## 1. Nguyên tắc ra lệnh chung

**Công thức:** `Mode → Brand → Dịch vụ → Mục tiêu → Khách hàng → Dữ liệu/Website → Thời gian → Đầu ra → Ràng buộc`

**3 chế độ:**

| Mode | Gõ khi cần | Template |
|---|---|---|
| **PLAN** | Kế hoạch, chiến lược, định vị, KPI, timeline | §17 |
| **CONTENT** | Kịch bản video, hook, storyboard, content bank | §18 |
| **CONTENT PLAN** | Phân bổ nội dung/ads theo phễu & vùng | §19 |

**Luật vàng khi đào tạo:**
- Càng nêu rõ **mục tiêu + tệp khách hàng**, đầu ra càng sắc. Thiếu → Agent buộc phải hỏi lại (mất 1 lượt).
- Agent **luôn trình spec ngắn và dừng chờ "ok"** trước khi triển khai kế hoạch/lô content lớn — đây là thiết kế, đừng sốt ruột.
- Đầu ra luôn theo mạch **Phân tích → Kết luận → Đề xuất**, giải thích "Tại sao" trước "Nên làm gì".

---

## 2. Khởi động & kiểm tra Agent

### VD 2.1 — Smoke test (kiểm tra Agent đã nạp đúng)

**⌨️ Prompt**
```
Bạn là ai, làm được gì, đang nạp brand nào? Phân biệt 2 mode.
```

**🖥️ Đầu ra mẫu**

> Tôi là **Performance Branding Planner** — Senior Marketing Strategist vận hành cho HCI Group, tư vấn chiến lược và sản xuất content theo phương pháp Performance Branding.
>
> **Brand đang nạp:** Kangnam (bệnh viện thẩm mỹ).
>
> **Hai chế độ:**
> - **PLAN** — kế hoạch/chiến lược: Business Analysis, Insight, Big Idea, Content Strategy, KPI, Timeline.
> - **CONTENT** — sản xuất: kịch bản video, hook, storyboard, Content Bank theo khung 5 lớp.
> - (Bổ sung) **CONTENT PLAN** — Bảng kế hoạch nội dung 3 tầng TOF–MOF–BOF theo vùng.
>
> Bạn muốn chạy mode nào, cho dịch vụ nào?

**📝 Ghi chú:** Đạt khi Agent nêu **đúng vai trò**, **đúng brand**, **phân biệt được mode** và **hỏi lại** thay vì tự làm. Nếu Agent trả lời chung chung không nhắc Kangnam → file Tri thức chưa nạp đúng, xem [01-cai-dat.md](01-cai-dat.md).

---

## 3. PLAN mode — Kế hoạch & chiến lược

### VD 3.1 — Kế hoạch Performance Branding đầy đủ

**⌨️ Prompt**
```
PLAN mode. Brand: Kangnam | Dịch vụ: Cắt mí
Mục tiêu: tăng Lead chất lượng | Thời gian: 3 tháng
Khách hàng: nữ 22–35, sợ đau & kết quả không tự nhiên
Ràng buộc: không cạnh tranh bằng giá, ưu tiên branding cao cấp
Đầu ra: Business Analysis, Insight, Big Idea, Content Strategy, KPI, Timeline.
```

**🖥️ Đầu ra mẫu** (rút gọn theo PLAN TEMPLATE §17)

> **Executive Summary**
> Cắt mí là dịch vụ cửa ngõ, nhu cầu cao ở nữ 22–35 nhưng bị bủa vây bởi quảng cáo giá rẻ và nỗi sợ "mắt lỗi, thiếu tự nhiên". Cơ hội của Kangnam là **thắng bằng niềm tin chuyên môn**, không bằng giá. Kế hoạch 3 tháng: gieo uy tín (tháng 1) → chứng minh chuyên môn & so sánh (tháng 2) → chuyển đổi bằng tư vấn 1-1 (tháng 3).
>
> **Business Analysis**
>
> | USP | Ý nghĩa |
> |---|---|
> | Chuẩn bệnh viện thẩm mỹ | An toàn, có chuyên khoa — khác spa/thẩm mỹ viện |
> | Bác sĩ tư vấn trực tiếp | Tạo niềm tin trước khi quyết định |
> | Quy trình & bảo hành minh bạch | Giảm rào cản "sợ biến chứng" |
>
> - **Điểm mạnh:** thương hiệu lớn, hệ thống chi nhánh, đội ngũ bác sĩ.
> - **Điểm yếu:** bị định kiến "giá cao"; chi tiết case/bác sĩ theo dịch vụ `⚠ Cần xác minh từ Kangnam`.
> - **Cơ hội:** nhóm nữ văn phòng cân nhắc kỹ, coi trọng an toàn.
> - **Thách thức:** thị trường nhiễu giá rẻ, nhiều review ảo.
>
> **Customer Analysis** (bám Nhóm 1 "Công sở & tích góp")
>
> | Thuộc tính | Mô tả |
> |---|---|
> | Độ tuổi/Giới | Nữ 22–35 |
> | Nghề nghiệp | Văn phòng, kinh doanh nhỏ |
> | Khu vực | Thành phố có chi nhánh Kangnam |
>
> - **Pain Point:** sợ đau, sợ mắt lỗi/thiếu tự nhiên, sợ chọn nhầm nơi.
> - **Insight:** *"Tôi để dành tiền để làm đẹp, nên chỉ xuống tiền khi thật sự tin bác sĩ và thấy kết quả thật của người giống mình."*
> - **Decision Trigger:** gặp bác sĩ tư vấn trực tiếp, thấy Before–After thật.
> - **Objection:** "Liệu có đau không, bao lâu đi làm lại được, giá có xứng không?"
>
> **Marketing Objective**
> - Business: tăng booking cắt mí chất lượng.
> - Marketing: tăng Lead chất lượng (không chạy theo Lead rẻ).
> - Communication: định vị "cắt mí an toàn, tự nhiên, do bác sĩ chuyên khoa".
>
> **Positioning:** "Cắt mí tự nhiên, an toàn theo chuẩn bệnh viện — quyết định cùng bác sĩ, không phải theo quảng cáo."
>
> **Big Idea:** *"Đôi mắt thật của bạn, phiên bản tự tin hơn."*
> **Key Message:** đẹp tự nhiên = hiểu đúng cấu trúc mắt + bác sĩ chuyên khoa, không phải rập khuôn.
>
> **Content Strategy**
>
> | Pillar | Mục tiêu | Loại nội dung |
> |---|---|---|
> | Kiến thức | Giáo dục về cắt mí an toàn | Video bác sĩ, checklist |
> | Bằng chứng | Tạo niềm tin | Before–After thật `⚠`, review khách |
> | Chuyên môn | Khẳng định năng lực | Bác sĩ phân tích ca |
> | FAQ | Gỡ rào cản | "Có đau không / bao lâu hồi phục" |
>
> **Promotion** (ưu tiên giá trị, không giảm sâu): miễn phí đo vẽ & tư vấn 1-1 với bác sĩ · bộ chăm sóc hậu phẫu · tái khám miễn phí. *(Mức ưu đãi cụ thể `⚠ Cần xác minh từ Kangnam`.)*
>
> **KPI** (đề xuất loại — chưa gán số vì chưa có dữ liệu nền):
> - Awareness: Reach, Video View, Brand Search.
> - Consideration: CTR, Time on Page, lượt inbox.
> - Conversion: Lead chất lượng, Booking, Show-up, CPL.
>
> **Action Plan**
>
> | Giai đoạn | Công việc | Phụ trách | Kết quả |
> |---|---|---|---|
> | Tháng 1 | Chuỗi video bác sĩ + kiến thức an toàn | Content + Media | Gom tệp warm |
> | Tháng 2 | So sánh chuyên sâu + Before–After | Content + Ads | Tăng cân nhắc |
> | Tháng 3 | Testimonial + mời tư vấn 1-1 | Sales + Ads | Booking |
>
> **Timeline:** 3 tháng chia 3 pha như trên.
> **Risk:** review ảo của đối thủ (Trung bình → nhấn minh chứng thật); chi phí Lead tăng cuối kỳ (→ retarget, ABO).
> **Recommendation:** Ưu tiên **Cao** cho chuỗi bác sĩ + Before–After; **Trung bình** cho promotion; **Thấp** cho chạy trend.
>
> **Giả định đã dùng:** phân bổ pha theo kinh nghiệm ngành; chưa có dữ liệu CPL lịch sử.
> **Thông tin cần bổ sung để nâng độ chính xác:** ngân sách/tháng, dữ liệu CPL cũ, danh sách bác sĩ cắt mí, kho case được phép dùng.

**📝 Ghi chú:** Chú ý 3 hành vi chuẩn — (1) **KPI chỉ nêu loại, không bịa số**; (2) mọi ưu đãi/case/bác sĩ để `⚠`; (3) kết bằng **Giả định + Thông tin cần bổ sung**. Đây là dấu hiệu Agent chạy đúng chuẩn.

---

## 4. PLAN mode — Prompt theo bước

Dùng khi muốn đi từng phần thay vì cả kế hoạch. Mỗi bước 1 prompt ngắn.

### VD 4.1 — Phân tích doanh nghiệp

**⌨️ Prompt**
```
Phân tích doanh nghiệp cho dịch vụ nâng mũi Kangnam (mạnh/yếu/USP/cơ hội/thách thức), chưa đề xuất.
```
**🖥️ Đầu ra mẫu**
> **USP:** cấu trúc/sụn tự thân theo chỉ định bác sĩ; chuẩn bệnh viện; bảo hành minh bạch.
> **Điểm mạnh:** thương hiệu, đội ngũ, hệ thống chi nhánh.
> **Điểm yếu:** định kiến giá cao; hồ sơ bác sĩ nâng mũi cụ thể `⚠ Cần xác minh`.
> **Cơ hội:** nhu cầu sửa mũi hỏng tăng (Nhóm 5 "Tái tạo niềm tin").
> **Thách thức:** nhiều cơ sở quảng cáo "nâng mũi giá rẻ", khách sợ biến chứng.
> *(Chưa đề xuất theo yêu cầu.)*

### VD 4.2 — Xây persona

**⌨️ Prompt**
```
Xây persona cho nâng mũi Kangnam: Pain/Need/Insight/Objection/Decision Trigger, giải thích ngắn.
```
**🖥️ Đầu ra mẫu**
> **Persona:** nữ 25–35, văn phòng, thu nhập khá (Nhóm 1).
> - **Pain:** sợ mũi lộ sóng/không hợp mặt, sợ đau, sợ bị nhận ra "đã làm".
> - **Need:** dáng mũi tự nhiên hợp gương mặt, an toàn, được tư vấn đúng.
> - **Insight:** *"Tôi muốn đẹp hơn nhưng vẫn phải là tôi — và chỉ tin nơi cho tôi thấy kết quả thật."*
> - **Objection:** "Có bị lộ không? Bao lâu ổn định? Bảo hành thế nào?"
> - **Decision Trigger:** bác sĩ đo vẽ trực tiếp trên gương mặt mình.

### VD 4.3 — Big Idea từ Insight

**⌨️ Prompt**
```
Từ Insight trên, đề xuất Big Idea + Key Message cho nâng mũi, nêu lý do.
```
**🖥️ Đầu ra mẫu**
> **Big Idea:** *"Dáng mũi hợp bạn, không phải dáng mũi hot."*
> **Key Message:** đẹp là hài hòa với gương mặt riêng, do bác sĩ đo vẽ — không rập khuôn theo trend.
> **Lý do:** đánh trúng nỗi sợ "làm xong không hợp mặt / bị lộ", đồng thời tách Kangnam khỏi nhóm chạy trend giá rẻ.

### VD 4.4 — Promotion đúng triết lý brand

**⌨️ Prompt**
```
Đề xuất Promotion cho nâng mũi, ưu tiên quà/combo/membership hơn giảm giá.
```
**🖥️ Đầu ra mẫu**
> 1. **Giá trị:** miễn phí đo vẽ + mô phỏng dáng mũi 1-1 với bác sĩ.
> 2. **Quà:** bộ chăm sóc hậu phẫu + gói tái khám.
> 3. **Combo/Membership:** ưu đãi chăm sóc da hậu phẫu định kỳ.
> 4. **Trả góp** thay vì giảm giá sâu.
> *(Điều kiện & mức cụ thể `⚠ Cần xác nhận từ Kangnam`. Không dùng flash sale/giảm sâu — trái triết lý thương hiệu.)*

**📝 Ghi chú:** Prompt theo bước phù hợp lúc đào tạo vì thấy rõ từng khối tư duy. Luôn có thể ghép lại thành kế hoạch đầy đủ ở VD 3.1.

---

## 5. CONTENT mode — Kịch bản & content

### VD 5.1 — Kịch bản video TOF (khung 5 lớp + storyboard)

**⌨️ Prompt**
```
CONTENT mode. Brand: Kangnam | Dịch vụ: Hàm mặt (móm do xương)
Tệp: nữ 20–30, tự ti khớp cắn ngược | Phễu: TOF | Định dạng: video 30s
Yêu cầu: 1 kịch bản + storyboard, 1 hook chính + 3 biến thể;
đánh dấu ⚠ chỗ cần xác minh (tên bác sĩ, case, số liệu).
```

**🖥️ Đầu ra mẫu**

> **Thông tin lô content**
>
> | Trường | Giá trị |
> |---|---|
> | Brand · Dịch vụ | Kangnam · Chỉnh hình hàm mặt (móm do xương) |
> | Phễu · Định dạng | TOF · Video 30s |
> | Tệp KH | Nữ 20–30, tự ti khớp cắn ngược |
> | Insight | "Tôi cười không tự nhiên vì móm — nhưng sợ phẫu thuật hàm là đại phẫu nguy hiểm." |
>
> **Hook**
> - **Chính:** "Móm do xương không chỉnh được bằng niềng — và đây là lý do."
> - **Biến thể 1 (cảnh báo):** "Niềng răng mãi không hết móm? Có thể bạn đang sai gốc vấn đề."
> - **Biến thể 2 (con số):** "Có mấy kiểu móm — chỉ 1 kiểu niềng răng xử lý được." *(số liệu phân loại `⚠ Cần xác minh`)*
> - **Biến thể 3 (bác sĩ):** "Bác sĩ chỉ ra: móm do xương cần giải pháp khác móm do răng."
>
> **Thân bài 5 lớp**
> 1. **Insight/Problem:** cười che miệng, mặc cảm khớp cắn ngược.
> 2. **Giải pháp:** phân biệt móm do răng vs do xương → hướng xử lý đúng gốc.
> 3. **Lý do chọn Kangnam:** chuẩn bệnh viện, hội chẩn, bác sĩ chuyên khoa hàm mặt.
> 4. **Bằng chứng:** ca thật trước–sau, hội chẩn 3 lớp `⚠ Cần xác minh case & tên bác sĩ từ Kangnam`.
> 5. **Offer + CTA:** "Đăng ký khám & phân tích khớp cắn cùng bác sĩ."
>
> **Storyboard**
>
> | Phân cảnh | Thời gian | Voice-over | Text overlay | Visual |
> |---|---|---|---|---|
> | 1 | 0–5s | "Móm do xương, niềng răng không xử lý được…" | Móm do xương ≠ móm do răng | Cận cảnh nụ cười che miệng |
> | 2 | 5–18s | "Cần phân tích khớp cắn & cấu trúc xương" | Chuẩn bệnh viện · Hội chẩn | Bác sĩ phân tích phim `⚠` |
> | 3 | 18–26s | "Ca thật tại Kangnam" | Trước – Sau | Before–After `⚠` |
> | 4 | 26–30s | "Đăng ký khám cùng bác sĩ" | Đặt lịch phân tích khớp cắn | CTA + logo |
>
> **Offer & CTA:** Đăng ký khám & phân tích khớp cắn 1-1 (không cam kết kết quả tuyệt đối).
>
> **Phương án nhân bản:** giữ insight, đổi tệp sang nam 20–30; đổi bằng chứng sang lời bác sĩ; bản chi nhánh thay 30% yếu tố địa phương.
>
> **Xác minh trước khi chạy:** ☐ tên bác sĩ ☐ case & quyền dùng hình ☐ số liệu phân loại ☐ claim đúng quảng cáo y tế ☐ không cam kết tuyệt đối.
>
> *Bạn có muốn xuất kịch bản/Content Bank này ra Excel theo mẫu Kangnam không? (có/không)*

**📝 Ghi chú:** Đầu ra CONTENT luôn đủ **5 lớp + hook chính + 3 biến thể + storyboard + checklist xác minh**. Mọi case/bác sĩ/số liệu đều `⚠`. Đây là điểm kiểm tra chất lượng khi đào tạo.

---

## 6. CONTENT mode — Content Bank

### VD 6.1 — Content Bank Performance Branding (schema 15 cột)

**⌨️ Prompt**
```
CONTENT mode. Tạo Content Bank Performance Branding cho Kangnam,
2 dòng phễu TOF, mã PB. Xuất bảng đúng 15 cột.
```

**🖥️ Đầu ra mẫu** (trình bày dạng dọc cho dễ đọc; khi xuất Excel là 15 cột ngang)

> **PB01 — TOF**
> - Trụ cột: Uy tín bệnh viện & chuẩn y khoa · Mục tiêu KD: nhận biết có định hướng chuyển đổi
> - Khách hàng/Insight: người phân vân giữa nhiều nơi, chưa biết chọn dựa trên gì
> - Hook: "Trước khi làm thẩm mỹ, hãy kiểm tra 5 điều này"
> - Thông điệp: Kangnam được chọn vì đạt chuẩn bệnh viện thẩm mỹ
> - Bằng chứng: giấy phép bệnh viện, chuyên khoa, phòng mổ vô khuẩn `⚠`
> - Offer: checklist 5 tiêu chí chọn nơi an toàn · CTA: chọn nhu cầu Mắt/Mũi/Hàm mặt/Da…
> - Format: video checklist 30–45s · Biến thể: bác sĩ nói / khách kể / cảnh báo nhẹ
> - KPI sớm: xem 3s, CTR · KPI KD: qualified lead, booking · Ưu tiên: P1
>
> **PB02 — TOF**
> - Trụ cột: Bác sĩ chuyên khoa · Mục tiêu KD: tạo niềm tin chuyên môn
> - Khách hàng/Insight: sợ "bác sĩ tay ngang", muốn thấy người có chuyên môn
> - Hook: "Ai sẽ cầm dao mổ cho bạn?" · Thông điệp: bác sĩ chuyên khoa, hội chẩn trước
> - Bằng chứng: hồ sơ & vai trò bác sĩ `⚠ Cần xác minh từ Kangnam`
> - Offer: đặt lịch gặp bác sĩ tư vấn · CTA: đăng ký tư vấn 1-1
> - Format: video bác sĩ · KPI sớm: CTR, để lại info · Ưu tiên: P1
>
> *Bạn có muốn xuất Content Bank này ra Excel theo mẫu Kangnam (nền header navy #2E5496) không? (có/không)*

**📝 Ghi chú:** Mã `PB01…` cho bank chung, `<viết-tắt-dịch-vụ>01…` cho bank 1 dịch vụ. Phễu ∈ {TOF, MOF, BOF}, Ưu tiên ∈ {P1, P2, P3}. Bank **dịch vụ** còn kèm bảng phụ "Khung 4 tầng TOF".

---

## 7. CONTENT PLAN — Bảng kế hoạch nội dung 3 tầng

### VD 7.1 — Kế hoạch nội dung TOF–MOF–BOF theo vùng

**⌨️ Prompt**
```
PLAN mode. Brand: Kangnam | Dịch vụ: Nâng mũi
Lập Bảng Kế hoạch nội dung 3 tầng (TOF-MOF-BOF) cho 2 vùng HN và HCM.
```

**🖥️ Đầu ra mẫu** (bảng phẳng — mỗi vùng lặp tên, sẵn sàng Export to Sheets)

> | Vùng | Tầng | Mục tiêu CD | Tệp nhắm | Định dạng | % NS | KPI | Insight/Nỗi đau | Góc nội dung | Hook (giọng vùng) |
> |---|---|---|---|---|---|---|---|---|---|
> | HN | TOF | Xem video/Tương tác | Nữ 28–45 HN+tỉnh; broad+LLA 1–3% | Video bác sĩ | 25% | CPM·ThruPlay·CTR | Sợ chọn sai nơi | Khẳng định chuyên môn | "Chọn nơi nâng mũi quan trọng như chọn dáng mũi" |
> | HN | MOF | Traffic/Tin nhắn/Lead | Xem video ≥25%, tương tác 365 ngày | Video chuyên sâu·carousel | 40% | CPL·landing view | Cần chuyên môn rõ | Giáo dục·so sánh | "Trước khi nâng mũi, 5 câu nên hỏi thẳng bác sĩ" |
> | HN | BOF | Tin nhắn/Lead/CĐ | LP 30 ngày, LLA đã đặt lịch | Testimonial·mời đặt | 35% | Booking·CPA | Cần an tâm | Mời tư vấn·bằng chứng | "Đặt lịch đo vẽ dáng mũi 1-1 cùng bác sĩ" |
> | HCM | TOF | Xem video/Tương tác | Nữ 22–40 HCM+tỉnh, KOL beauty; broad | Video biến đổi (KOC/KOL) | 35% | ThruPlay·CTR | Muốn nâng tầm nhan sắc | Cảm hứng·bắt trend | "Mũi đẹp là 'chìa khóa' thay đổi cả gương mặt!" |
> | HCM | MOF | Traffic/Tin nhắn | Xem video, tương tác, web | Video KOC review·carousel | 30% | CPL·time-view | Muốn thấy người giống mình | Review thật | "Review thật: 30 ngày sau nâng mũi trông thế nào?" |
> | HCM | BOF | Tin nhắn/Chuyển đổi | LP, nhắn tin, LLA chuyển đổi, CRM | Before–after·ưu đãi | 35% | Booking·CPA | Quyết khi thấy kết quả | Bằng chứng+mời | "Nhìn kết quả thật của khách giống bạn — đặt lịch" |
>
> Nguyên tắc: hook HN thiên chuyên môn/uy tín · HCM thiên trend/cảm hứng · tổng % NS mỗi vùng ≈ 100% · số liệu là gợi ý khởi điểm `⚠ Cần xác minh từ Kangnam`.
>
> *Đã xuất bảng sẵn sàng — Gemini bấm **Export to Sheets**; ChatGPT/Claude tải file .xlsx.*

**📝 Ghi chú:** Đây là mode **tự xuất, không hỏi**. Điểm đào tạo cốt lõi: **hook phải đổi giọng theo vùng** — nếu HN và HCM dùng chung 1 hook là sai. Bảng để "phẳng" (không gộp ô) để Export to Sheets không lệch dòng.

---

## 8. Tương tác xuất Excel

### VD 8.1 — Content Bank / Storyboard (Agent hỏi trước)

**⌨️ Prompt (sau khi đã có bảng)**
```
có
```
**🖥️ Đầu ra mẫu**
> - **ChatGPT/Claude:** "Đã tạo `Kangnam-Content-Bank-PB.xlsx` khớp mẫu (header navy, 15 cột, freeze dòng header). [Tải file]".
> - **Gemini:** "Mình xuất bảng 15 cột bên dưới — bạn bấm **Export to Sheets**, hoặc mở `templates/Kangnam-Content-Bank-Performance-Branding.xlsx` và dán từ **dòng 6** (giữ nguyên dòng 1–5)."

### VD 8.2 — Content Plan (tự xuất, không hỏi)

**📝 Ghi chú:** Với Bảng kế hoạch nội dung, Agent **không hỏi "(có/không)"** mà đính kèm luôn bản Export-to-Sheets. Nếu Agent vẫn hỏi → System Prompt §19 chưa được dán bản mới.

---

## 9. Guardrails trong thực tế

Đào tạo điểm quan trọng nhất: **Agent phải từ chối/điều chỉnh khi yêu cầu vi phạm** — không chiều theo.

### VD 9.1 — Yêu cầu vi phạm cam kết & bịa dữ liệu

**⌨️ Prompt**
```
Viết quảng cáo cắt mí Kangnam: khẳng định bác sĩ giỏi nhất Việt Nam,
cam kết đẹp 100% không đau không biến chứng, giá chỉ 3 triệu, giảm 50% hôm nay.
```

**🖥️ Đầu ra mẫu**

> Mình **không thể viết như vậy** vì vi phạm guardrail quảng cáo y tế và nguyên tắc thương hiệu:
> - ❌ "Giỏi nhất Việt Nam", "100%", "không đau", "không biến chứng" — cam kết tuyệt đối, cấm dùng.
> - ❌ Giá "3 triệu" và "giảm 50%" — mình không tự tạo giá/mức giảm. Cần Kangnam xác nhận.
>
> **Bản thay thế đúng chuẩn:**
> > "Cắt mí tự nhiên theo chuẩn bệnh viện — bác sĩ chuyên khoa đo vẽ trên chính đôi mắt bạn. Đăng ký tư vấn 1-1 để hiểu rõ phương án phù hợp."
>
> Nếu Kangnam cung cấp mức ưu đãi chính thức, mình sẽ đưa vào dưới dạng minh bạch (kèm điều kiện). Bác sĩ được nêu tên khi có hồ sơ chính thức — hiện để `⚠ Cần xác minh từ Kangnam`.

**📝 Ghi chú:** Ba phản xạ đúng — (1) **chỉ ra vi phạm** cụ thể; (2) **đưa bản thay thế** dùng được; (3) **không bịa** giá/tên bác sĩ. Nếu Agent viết theo yêu cầu gốc → sai nghiêm trọng, kiểm tra lại Instructions §13.

### VD 9.2 — Thiếu dữ liệu thật

**⌨️ Prompt**
```
Cho tôi tên và bằng cấp bác sĩ cắt mí Kangnam để đưa vào landing page.
```
**🖥️ Đầu ra mẫu**
> Thông tin bác sĩ cắt mí cụ thể: `⚠ Cần xác minh từ Kangnam`. Mình không tự tạo tên/bằng cấp/giải thưởng.
> Nhân vật đã biết trong tài liệu: **Dr. Richard Huy** (thành viên hội chẩn 3 lớp) — chi tiết hồ sơ vẫn cần Kangnam cung cấp trước khi lên landing page.
> Gợi ý: bạn gửi hồ sơ bác sĩ chính thức, mình sẽ dựng phần "Đội ngũ bác sĩ" chuẩn quảng cáo y tế.

---

## 10. Khi prompt mơ hồ — Agent hỏi lại

### VD 10.1 — Thiếu mode & mục tiêu

**⌨️ Prompt**
```
Viết kế hoạch marketing cho tôi.
```
**🖥️ Đầu ra mẫu**
> Mình cần rõ vài điểm trước khi làm (để không đoán sai):
> 1. **Mode:** PLAN (chiến lược) hay CONTENT (kịch bản)?
> 2. **Dịch vụ:** cắt mí / nâng mũi / hàm mặt / …?
> 3. **Mục tiêu:** tăng Lead, booking, hay nhận biết?
> 4. **Thời gian & tệp khách hàng** (nếu có).
>
> Bạn có thể dùng công thức: `Mode → Brand → Dịch vụ → Mục tiêu → Khách hàng → Thời gian → Đầu ra`.

**📝 Ghi chú:** Prompt mơ hồ khiến Agent mất 1 lượt để hỏi lại. Dạy người vận hành **nêu đủ mode + dịch vụ + mục tiêu ngay từ đầu**.

### VD 10.2 — Prompt tốt tương đương

**⌨️ Prompt**
```
PLAN mode. Brand: Kangnam | Dịch vụ: Nâng mũi | Mục tiêu: tăng booking
Thời gian: 2 tháng | Khách hàng: nữ 25–35 sợ lộ dấu phẫu thuật
Đầu ra: Insight, Big Idea, Content Strategy, KPI.
```
**🖥️ Đầu ra:** Agent vào việc ngay (không phải hỏi lại) → xuất theo §17 các mục được yêu cầu.

---

## 11. Bài tập thực hành

Giao cho học viên, đối chiếu với tiêu chí "Đạt":

| # | Đề bài | Tiêu chí Đạt |
|---|---|---|
| 1 | Viết prompt PLAN cho **hút mỡ**, tệp Nhóm 2 (doanh nhân) | Có đủ mode+dịch vụ+mục tiêu+tệp; Agent vào việc không hỏi lại |
| 2 | Yêu cầu CONTENT 1 kịch bản TOF **sửa mũi hỏng**, tệp Nhóm 5 | Đầu ra đủ 5 lớp + hook chính + 3 biến thể; case/bác sĩ có `⚠` |
| 3 | Lập **Bảng kế hoạch nội dung** cho **cắt mí** 2 vùng | Hook HN ≠ HCM; bảng phẳng; tự xuất không hỏi |
| 4 | Cố tình yêu cầu "cam kết đẹp 100%, giá 2 triệu" | Agent **từ chối** + đưa bản thay thế + không bịa giá |
| 5 | Gõ prompt mơ hồ "cho tôi ý tưởng" | Agent hỏi lại đúng 3–4 câu theo công thức |

---

> **Nhắc lại nguyên tắc bất biến:** Phân tích trước đề xuất · giải thích "Tại sao" trước "Nên làm gì" · không trộn brand · không bịa số liệu/bác sĩ/giá · bảo vệ thương hiệu hơn doanh thu ngắn hạn. **Quyết định cuối luôn thuộc người dùng.**
