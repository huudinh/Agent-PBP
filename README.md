# 🚀 Performance Branding Planner

> Version: 4.0
> **AI chuyên xây dựng kế hoạch Marketing & Performance Branding từ thông tin doanh nghiệp** — theo tư duy Marketing Manager & Brand Strategist, vận hành cho hệ sinh thái HCI Group.

---

# 1. Giới thiệu

Performance Branding Planner hỗ trợ Marketing Team, Brand Team và Agency xây dựng kế hoạch một cách có hệ thống. Agent không chỉ tạo nội dung mà còn phân tích doanh nghiệp, xác định mục tiêu, xây dựng chiến lược, đề xuất kế hoạch triển khai — và sản xuất content/kịch bản theo phương pháp Performance Branding.

Đầu ra là tài liệu có cấu trúc rõ ràng, logic, dùng nội bộ hoặc trình bày khách hàng.

---

# 2. Kiến trúc 3 tầng

```
Bộ não (trung tính, dùng chung mọi brand)
   → system-prompt.md
Kiến thức brand (riêng từng thương hiệu)
   → knowledge/<brand>-brand.md · <brand>-market.md
Kiến thức dịch vụ (sâu, có kịch bản mẫu)
   → knowledge/<brand>-service-*.md  (khung: service-_TEMPLATE.md)
```

**Nguyên tắc:** brain biết *cách làm*; brand file cung cấp *voice + dữ liệu*; service file cung cấp *nội dung sâu + kịch bản đã kiểm chứng*. **Không trộn voice/ví dụ giữa các brand.**

---

# 3. Hai chế độ đầu ra

| Mode | Dùng khi | Template |
|---|---|---|
| **PLAN** | Cần kế hoạch/chiến lược | `output-template.md` |
| **CONTENT** | Cần sản xuất content/kịch bản (Output Engine) | `output-template-content.md` |

---

# 4. Cấu trúc thư mục

```
Performance-Branding-Planner/
├── README.md                       ← tài liệu này
├── SETUP-GUIDE.md                  ← hướng dẫn cài đặt & sử dụng
├── system-prompt.md                ← BỘ NÃO (nạp đầu tiên)
├── prompt-guide.md                 ← cách viết prompt + chọn mode
├── input-template.md               ← biểu mẫu đầu vào
├── output-template.md              ← template Plan mode
├── output-template-content.md      ← template Content mode
├── samples/
│   ├── sample-input.md
│   └── sample-output.md
└── knowledge/
    ├── kangnam-brand.md            ← định vị, USP, voice, Content Bank Kangnam
    ├── kangnam-market.md           ← khách hàng, dịch vụ, funnel, promotion, FAQ
    ├── service-_TEMPLATE.md        ← khung dịch vụ tái sử dụng
    └── kangnam-service-ham-mat.md  ← dịch vụ mẫu (hàm mặt) + storyboard
```

---

# 5. Đầu vào tối thiểu

Tên thương hiệu · Ngành · Sản phẩm/Dịch vụ · Mục tiêu chiến dịch.
Khuyến khích: Website · Fanpage · TikTok · USP · Tệp KH · Đối thủ · Ngân sách · Thời gian · Ưu đãi hiện tại.
Thiếu dữ liệu → Agent ghi rõ "Giả định", không suy diễn.

---

# 6. Quy trình sử dụng

```
Điền input-template → Agent kiểm tra & tóm tắt → Xác nhận
→ Agent lập spec/kế hoạch → Review → Tối ưu → Xuất bản
```

Agent làm việc theo thứ tự: Phân tích → Kết luận → Đề xuất → Hành động. Không bỏ bước.

---

# 7. Nguyên tắc & giới hạn

✔ Phân tích trước khi đề xuất · mọi đề xuất có lý do · không viết chung chung · thiếu dữ liệu thì hỏi/ghi giả định · trình bày Markdown chuyên nghiệp.
❌ Không bịa số liệu · không cam kết doanh thu/KPI · không sao chép nguyên mẫu · không kết luận khi thiếu dữ liệu · không vi phạm quảng cáo y tế.

---

# 8. Phạm vi phiên bản

**V4 (hiện tại):** Business/Customer Analysis · Strategy · Performance Branding · Content Production (Output Engine) · Promotion · KPI · Timeline · Content Bank · Service knowledge.
**Chưa gồm:** Media Plan · phân bổ ngân sách chi tiết · SEO Audit · Social Listening · Competitor Crawling · AI Research → phiên bản sau.

---

# 9. Mở rộng brand mới

1. Copy `knowledge/service-_TEMPLATE.md` cho từng dịch vụ.
2. Tạo `<brand>-brand.md` (voice + Content Bank) và `<brand>-market.md`.
3. Không sửa `system-prompt.md` — brain đã trung tính.

---

# 10. Mục tiêu cuối

Không thay thế Marketing Manager — Agent là **Strategic Assistant**: rút ngắn thời gian lập kế hoạch, chuẩn hóa phân tích, đề xuất có hệ thống, tạo tài liệu chuyên nghiệp. **Quyết định cuối luôn thuộc người dùng.**
"# Agent-PBP" 
