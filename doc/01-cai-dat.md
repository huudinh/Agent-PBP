# Cài đặt — Performance Branding Planner

## 1. Ba thành phần

| # | Thành phần | Đặt ở đâu | Nội dung |
|---|---|---|---|
| 1 | **Instructions / Chỉ dẫn** | Ô Chỉ dẫn của Agent | Toàn bộ [`SYSTEM-PROMPT.md`](../SYSTEM-PROMPT.md) (giữa 2 vạch ▼▲) |
| 2 | **Knowledge / Tri thức** | Mục Tri thức | File `.md` trong `knowledge/` |
| 3 | **Templates Excel** | Mục Tri thức (tùy chọn) | File `templates/*.xlsx` |

**Tên Agent:** `Performance Branding Planner`
**Mô tả:** `AI chuyên xây dựng kế hoạch Marketing & Performance Branding từ thông tin doanh nghiệp.`

> System Prompt đã tối ưu cho Gem/GPT/Claude: bỏ giả định file-system, tham chiếu Tri thức, nhúng sẵn các template Plan/Content/Content Plan (không tốn slot file).

---

## 2. Chiến lược file (nền tảng giới hạn)

Giới hạn Tri thức: **Gemini = 10 file · ChatGPT = 20 file · Claude Project = theo dung lượng.** Chặt nhất là Gemini → thiết kế ≤5 file.

| Mức | Upload vào Knowledge | Số file |
|---|---|---|
| Tối thiểu | `kangnam-brand.md` + `kangnam-market.md` | 2 |
| **Khuyến nghị** | + `kangnam-service-ham-mat.md` | 3 |
| Có xuất Excel | + `templates/*.xlsx` (xem mục 4) | 5+ |

**KHÔNG upload:** README, các file trong `doc/`, `service-_TEMPLATE.md` (chỉ dùng khi soạn dịch vụ mới). System Prompt → **dán Instructions**, không phải file Tri thức.

---

## 3. Cài trên từng nền tảng

**A. Gemini (Gem):** Gem manager (◇) → New Gem → điền Tên/Mô tả → **Chỉ dẫn:** dán `SYSTEM-PROMPT.md` → **Tri thức:** upload mức Khuyến nghị (tối đa 10 file) → Lưu, test ở khung Xem trước.
- Gem hay bỏ qua file khi Instructions dài → giữ dòng "LỆNH ƯU TIÊN… tham chiếu Tri thức trước" ở đầu. Có thể connect Google Drive để tự cập nhật. Người nhận link thấy Instructions + tên file.

**B. ChatGPT (Custom GPT):** Explore GPTs → Create → Configure → điền Name/Description → **Instructions:** dán `SYSTEM-PROMPT.md` → **Knowledge:** upload (tới 20 file). Conversation starters gợi ý:
```
PLAN mode: kế hoạch Performance Branding cắt mí Kangnam 3 tháng.
CONTENT mode: 3 kịch bản TOF hàm mặt Kangnam, mỗi bản 1 hook + 3 biến thể.
Lập Bảng Kế hoạch nội dung 3 tầng (TOF-MOF-BOF) cho HN và HCM.
```

**C. Claude (Project):** Projects → Create project → **Custom instructions:** dán `SYSTEM-PROMPT.md` → **Project knowledge:** thêm file brand + service → chat.

**Smoke test (mọi nền tảng):** gửi *"Bạn là ai, làm được gì, đang nạp brand nào? Phân biệt 2 mode."* → đạt khi Agent nêu đúng vai trò, phân biệt PLAN/CONTENT, liệt kê đúng brand, hỏi lại khi thiếu.

---

## 4. Upload file mẫu Excel (tùy chọn — giúp Agent bám format)

Muốn Agent tái tạo format chính xác tuyệt đối, upload file mẫu vào **Tri thức**:

| File | Nội dung | Header |
|---|---|---|
| `templates/Kangnam-Content-Bank-Performance-Branding.xlsx` | Bank tổng | navy `#2E5496` |
| `templates/Kangnam-Content-Bank-Ham-Mat.xlsx` | Bank dịch vụ + sheet *"Khung 4 tầng TOF"* | tím `#6B2E85` |
| `templates/Kangnam-Content-Plan.xlsx` | Bảng Kế hoạch nội dung 3 tầng (11 cột). 2 sheet: *"Kế hoạch nội dung"* (khung nhận dữ liệu) + *"Ví dụ (nâng mũi)"* | teal `#1F6F5C` |

**Cách upload:**
1. **Gemini:** New/Edit Gem → **Tri thức → Add files** → chọn file `.xlsx` (tính vào giới hạn 10 file).
2. **ChatGPT:** Configure → **Knowledge → Upload files** → chọn file.
3. **Claude:** Project → **Add to project knowledge** → chọn file.

> Nếu chạm giới hạn file (Gemini): **bỏ upload** mẫu — schema đã mô tả đầy đủ trong System Prompt §12.3/§15/§19, Agent vẫn tái tạo đúng.

Chi tiết hành vi xuất Excel & cách dán dữ liệu → [03-output-mau.md](03-output-mau.md).

---

## 5. Thêm brand / dịch vụ

**Dịch vụ mới:** copy `service-_TEMPLATE.md` → `<brand>-service-<slug>.md` → điền → cập nhật 1 dòng bảng dịch vụ trong `<brand>-market.md`.

**Brand mới (VD Paris):** tạo `<brand>-brand.md` + `<brand>-market.md`. **Không sửa System Prompt** (brain trung tính).

---

## 6. Xử lý sự cố

| Sự cố | Xử lý |
|---|---|
| Agent bỏ qua Tri thức | Giữ dòng "LỆNH ƯU TIÊN…" đầu Instructions; rút gọn nếu quá dài |
| Trả lời chung chung | Nêu rõ mode + mục tiêu (công thức trong [02-cau-lenh.md](02-cau-lenh.md)) |
| Lẫn ví dụ giữa các brand | Mỗi Agent nạp 1 brand, hoặc nêu rõ brand mỗi lượt |
| Bịa tên bác sĩ/số liệu | Bổ sung dữ liệu thật; chấp nhận `⚠ Cần xác minh` |
| Sửa knowledge mà Agent chưa thấy | Nạp lại file vào Knowledge (xóa file cũ → upload lại); Gemini có thể để Google Drive tự đồng bộ |
| Chạm giới hạn 10 file | Tách brand ra Gem riêng; bỏ upload template |
