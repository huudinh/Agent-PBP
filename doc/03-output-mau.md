# Output mẫu & Xuất Excel — Performance Branding Planner

## 1. Hành vi xuất Excel

Sau mỗi kết quả dạng bảng, Agent xử lý theo nền tảng:

| Nền tảng | Cách xuất |
|---|---|
| **ChatGPT (Data Analysis)** / **Claude** | Sinh thẳng file `.xlsx` khớp mẫu, gửi link tải |
| **Gemini** | Xuất bảng phẳng → bấm **Export to Sheets** (hoặc dán vào file mẫu từ dòng 6, giữ nguyên dòng 1–5) |

**Content Bank / storyboard / KPI / Timeline:** Agent hỏi 1 lần *"Bạn có muốn xuất ra Excel theo mẫu Kangnam không?"* → trả lời "có" mới xuất.

**Bảng Kế hoạch nội dung (Content Plan):** **XUẤT TỰ ĐỘNG, KHÔNG HỎI** — Agent luôn kèm bản bảng phẳng (không gộp ô, lặp tên vùng mỗi dòng) để *Export to Sheets* chạy trực tiếp.

> **Dán tay vào file mẫu (Gemini):** mở đúng file trong `templates/` → dán dữ liệu **từ dòng 6**, giữ nguyên dòng 1–5 (tiêu đề/framework/nguyên tắc/header). Với `Kangnam-Content-Plan.xlsx`: dán vào sheet **"Kế hoạch nội dung"**; sheet **"Ví dụ (nâng mũi)"** chỉ để tham chiếu.

---

## 2. Output mẫu — Bảng Kế hoạch nội dung 3 tầng

Schema **11 cột**. Ví dụ dịch vụ **Nâng mũi**, 2 vùng HN/HCM (dữ liệu nguồn: `kangnam-market.md` §5). Bảng phẳng — mỗi vùng lặp tên ở cột 1:

| Vùng | Tầng | Mục tiêu CD | Tệp nhắm | Định dạng | % NS | KPI | Insight/Nỗi đau | Góc nội dung | Hook (giọng vùng) | Ghi chú |
|---|---|---|---|---|---|---|---|---|---|---|
| HN | TOF | Xem video / Tương tác | Nữ 28–45 HN+tỉnh, làm đẹp/công sở; broad + LLA 1–3% | Video bác sĩ | 25% | CPM·ThruPlay·CTR | Sợ chọn sai nơi/bác sĩ | Khẳng định chuyên môn | Đằng sau dáng mũi đẹp tự nhiên, không phải may rủi | Bật rộng gom tệp warm |
| HN | MOF | Traffic / Tin nhắn / Lead | Xem video ≥25%, tương tác Page/IG 365 ngày | Video chuyên sâu · carousel | 40% | CPL·landing view | Cần chuyên môn rõ ràng | Giáo dục & so sánh | Trước khi nâng mũi, 5 câu nên hỏi thẳng bác sĩ | Nhấn chuyên môn & an toàn |
| HN | BOF | Tin nhắn / Lead / CĐ | LP 30 ngày, lead chưa đặt, LLA đã đặt lịch | Testimonial · mời đặt lịch | 35% | Booking·show-up·CPA | Cần an tâm trước quyết | Mời trải nghiệm tư vấn | Đặt lịch đo vẽ dáng mũi 1-1 cùng bác sĩ | Retarget mạnh, ABO |
| HCM | TOF | Xem video / Tương tác | Nữ 22–40 HCM+tỉnh, KOL beauty/thời trang; broad | Video biến đổi (KOC/KOL) | 35% | ThruPlay·CTR·CPM | Muốn nâng tầm nhan sắc | Truyền cảm hứng · bắt trend | Mũi đẹp là 'chìa khóa' thay đổi cả gương mặt! | Nhiều creative trend, test liên tục |
| HCM | MOF | Traffic / Tin nhắn | Xem video, tương tác, truy cập web | Video KOC review · carousel | 30% | CPL·time-view | Muốn thấy người giống mình | Review thật · cá nhân hoá | Review thật: 30 ngày sau nâng mũi trông thế nào? | Social proof là chính |
| HCM | BOF | Tin nhắn / Chuyển đổi | LP, người nhắn tin, LLA chuyển đổi, CRM | Before–after · ưu đãi | 35% | Booking·CPA | Quyết khi thấy kết quả | Bằng chứng + mời | Nhìn kết quả thật của khách giống bạn — đặt lịch | Ưu đãi trải nghiệm; ABO |

**Nguyên tắc:** Hook đúng giọng vùng (HN chuyên môn/uy tín · HCM trend/cảm hứng) · tổng % NS mỗi vùng ≈ 100% · số liệu là gợi ý khởi điểm, chưa xác minh → `⚠ Cần xác minh từ Kangnam`.

---

## 3. Output mẫu — Content Bank (15 cột)

Ví dụ 1 dòng bank Performance Branding (Mã `PB01`):

| Trường | Giá trị |
|---|---|
| Mã | PB01 |
| Trụ cột | Uy tín bệnh viện & chuẩn y khoa |
| Phễu | TOF |
| Mục tiêu KD | Tăng nhận biết có định hướng chuyển đổi |
| Khách hàng/Insight | Người phân vân giữa nhiều nơi, chưa biết chọn dựa trên gì |
| Hook | Trước khi quyết định làm thẩm mỹ, hãy kiểm tra 5 điều này |
| Thông điệp thương hiệu | Kangnam được chọn vì đạt chuẩn bệnh viện thẩm mỹ |
| Bằng chứng | Giấy phép bệnh viện; chuyên khoa; đội ngũ bác sĩ; phòng mổ |
| Offer | Checklist 5 tiêu chí chọn nơi làm thẩm mỹ an toàn |
| CTA | Chọn nhu cầu MẮT–MŨI–HÀM MẶT–VÓC DÁNG–DA–NHA KHOA |
| Format | Video checklist 30–45s |
| Biến thể test | Hook checklist / bác sĩ nói / khách kể / cảnh báo nhẹ |
| KPI sớm | Tỷ lệ xem 3s; CTR; lượt chọn dịch vụ |
| KPI kinh doanh | Qualified lead; booking; doanh thu theo content |
| Ưu tiên | P1 |

Bank dịch vụ kèm bảng phụ **"Khung 4 tầng TOF"** (6 cột): `Tầng | Thời lượng | Vai trò | Nguyên tắc | Ví dụ <Dịch vụ> (Kangnam) | Lưu ý thương hiệu`.

→ Format đầy đủ trong các file `templates/*.xlsx` và System Prompt §12.3 / §15 / §19.
