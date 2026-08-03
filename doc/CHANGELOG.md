# Changelog — Performance Branding Planner

> Ghi lại thay đổi tầng Tri thức, Output template và tài liệu. Mới nhất trên cùng.
> System Prompt (brain trung tính) hiện ở **Version 4.2** — cập nhật brand/dịch vụ không đổi version brain.

---

## 2026-08-03 · Tái cấu trúc tài liệu

- Tách **System Prompt** ra file riêng [`SYSTEM-PROMPT.md`](../SYSTEM-PROMPT.md) (để dán vào Instructions).
- README rút gọn còn overview + quick-start + bản đồ file.
- Tách hướng dẫn vào `doc/`: [01-cai-dat.md](01-cai-dat.md) · [02-cau-lenh.md](02-cau-lenh.md) · [03-output-mau.md](03-output-mau.md) · CHANGELOG.md.

## 2026-08-03 · Output template — Bảng Kế hoạch nội dung 3 tầng (TOF–MOF–BOF)

- **System Prompt §19. CONTENT PLAN TEMPLATE** — schema 11 cột `Vùng | Tầng | Mục tiêu CD | Tệp nhắm | Định dạng Ads | % Ngân sách | KPI chính | Insight/Nỗi đau | Góc nội dung | Hook (đúng giọng vùng) | Ghi chú`. Tham chiếu ở §3 (mode) và §11 (Content Strategy).
- **`kangnam-market.md` §5:** thêm **"Nguyên tắc xây dựng nội dung 3 tầng theo vùng"** — dữ liệu TOF/MOF/BOF cho **HN** (chuyên môn/uy tín) và **HCM** (trend/cảm hứng/social proof).
- **File mẫu mới:** `templates/Kangnam-Content-Plan.xlsx` (11 cột, header teal `#1F6F5C`) — 2 sheet: khung nhận dữ liệu + "Ví dụ (nâng mũi)".
- **Xuất tự động:** §15 + §19 — Content Plan **tự xuất bảng phẳng (không gộp ô), KHÔNG hỏi "(có/không)"**. Gemini bấm *Export to Sheets*; ChatGPT/Claude sinh thẳng `.xlsx`.

**Test:**
```
PLAN mode. Brand: Kangnam | Dịch vụ: Nâng mũi
Lập Bảng Kế hoạch nội dung 3 tầng (TOF-MOF-BOF) cho 2 vùng HN và HCM.
```
→ Đạt: bảng 11 cột, mỗi vùng đủ TOF/MOF/BOF, hook HN thiên chuyên môn – HCM thiên trend, % NS/vùng ≈ 100%, tự xuất bản Export to Sheets.

## 2026-08-03 · Knowledge update — Insight khách hàng Kangnam

- **`kangnam-market.md` §1:** thêm **"6 Nhóm khách hàng & Insight chuyên sâu"** — bảng index + 6 khối persona, mỗi nhóm đủ 4 lớp *Chân dung · Pain Point · Insight cảm xúc · Key tâm lý*.

  | Nhóm | Định danh | Tệp |
  |---|---|---|
  | 1 | Công sở & Người lao động tích góp | 25–45, làm đẹp an toàn – đầu tư xứng đáng |
  | 2 | Doanh nhân / Giới tinh hoa | 35–55, đẳng cấp riêng – đẹp kín tiếng |
  | 3 | KOC/KOL trẻ, Creative, Gen Z | 20–30, theo trend – đẹp nhanh hợp vibe |
  | 4 | Sinh viên / NV mới đi làm | 18–25, thay đổi vì tương lai |
  | 5 | Khách sửa lại (từng làm hỏng nơi khác) | 28–50, tái tạo niềm tin |
  | 6 | Trung niên muốn trẻ hóa | 40–55+, tìm lại tuổi xuân |

- **`kangnam-market.md` §2:** bổ sung dịch vụ — **Filler** (Da), **Tạo hình môi · Cấy mỡ mặt** (Khuôn mặt), **Cấy mỡ mắt · Sửa mí lỗi** (Mắt), **Sửa hút mỡ hỏng/lồi lõm** (Vóc dáng), **Sửa mũi hỏng/co rút**. Quy trình/chi phí vẫn `⚠ Cần xác minh từ Kangnam`.

**Test:**
```
Liệt kê đủ 6 nhóm khách hàng Kangnam kèm tên định danh truyền thông và dịch vụ trọng tâm.
```
→ Đạt: ra đúng 6 nhóm (Nhóm 1 "Công sở & tích góp" … Nhóm 6 "Tìm lại tuổi xuân").

> **Lưu ý nạp lại:** sửa file `.md` chưa đủ — phải cập nhật vào nền tảng thì Agent mới thấy. Claude/ChatGPT: xóa file cũ → upload lại. Gemini: Edit Gem → Tri thức → thay file (hoặc Google Drive tự đồng bộ).
