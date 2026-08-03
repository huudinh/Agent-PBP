# 🚀 Performance Branding Planner

> Version 4.2 · AI xây dựng **kế hoạch Marketing & Performance Branding** + sản xuất content/kịch bản cho hệ sinh thái **HCI Group**.

Đóng vai **Senior Marketing Strategist**: phân tích doanh nghiệp → khách hàng → mục tiêu → chiến lược → kế hoạch → KPI → timeline; và sản xuất content/kịch bản theo phương pháp Performance Branding.

---

## Kiến trúc 3 tầng

- **Bộ não (trung tính):** [`SYSTEM-PROMPT.md`](SYSTEM-PROMPT.md) — dán vào ô Chỉ dẫn/Instructions. Dùng chung mọi brand.
- **Kiến thức brand:** `knowledge/<brand>-brand.md` + `<brand>-market.md`.
- **Kiến thức dịch vụ:** `knowledge/<brand>-service-*.md` (khung tái dùng `service-_TEMPLATE.md`).
- **Mẫu Excel:** `templates/*.xlsx` — khóa format khi xuất.

Brain biết *cách làm*; brand file cấp *voice + dữ liệu*; service file cấp *kịch bản kiểm chứng*. **Không trộn voice/ví dụ giữa các brand.**

---

## Quick start (3 bước)

1. **Instructions:** dán toàn bộ [`SYSTEM-PROMPT.md`](SYSTEM-PROMPT.md) vào ô Chỉ dẫn (Gemini) / Instructions (ChatGPT) / Custom instructions (Claude).
2. **Knowledge:** upload file `.md` trong `knowledge/` (mức khuyến nghị: brand + market + service).
3. **Templates (tùy chọn):** upload `templates/*.xlsx` để Agent bám format khi xuất Excel.

→ Chi tiết cài từng nền tảng + smoke test: [doc/01-cai-dat.md](doc/01-cai-dat.md)

**Câu lệnh đầu tiên để test:**
```
Bạn là ai, làm được gì, đang nạp brand nào? Phân biệt 2 mode.
```

---

## Tài liệu

| File | Nội dung |
|---|---|
| [SYSTEM-PROMPT.md](SYSTEM-PROMPT.md) | System Prompt để dán vào Instructions (bộ não Agent) |
| [doc/01-cai-dat.md](doc/01-cai-dat.md) | Cài đặt Gemini/ChatGPT/Claude · chiến lược file · upload template · thêm brand/dịch vụ · xử lý sự cố |
| [doc/02-cau-lenh.md](doc/02-cau-lenh.md) | 2 mode · công thức ra lệnh · prompt ví dụ |
| [doc/03-output-mau.md](doc/03-output-mau.md) | Output mẫu (Content Bank, Kế hoạch nội dung) · hành vi xuất Excel |
| [doc/CHANGELOG.md](doc/CHANGELOG.md) | Lịch sử cập nhật |

---

## Cấu trúc repo

```
SYSTEM-PROMPT.md   Bộ não Agent (dán vào Instructions)
knowledge/         Kiến thức brand / market / service (.md)
templates/         File mẫu Excel (.xlsx)
doc/               Hướng dẫn cài đặt · câu lệnh · output mẫu · changelog
```

---

*Quyết định cuối luôn thuộc người dùng.*
