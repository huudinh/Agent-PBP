# HƯỚNG DẪN CÀI ĐẶT & SỬ DỤNG
# Performance Branding Planner
Version: 4.0

---

# PHẦN 1 — CÀI ĐẶT AGENT

## Bước 1. Nạp bộ não
Đặt **`system-prompt.md`** làm System Prompt / Custom Instructions của Agent (Claude Project, Custom GPT, hoặc field "instructions" của platform bạn dùng).

- Tên Agent: **Performance Branding Planner**
- Mô tả ngắn: *AI chuyên xây dựng kế hoạch Marketing & Performance Branding từ thông tin doanh nghiệp.*

## Bước 2. Nạp kiến thức (Knowledge / Project files)
Upload toàn bộ thư mục `knowledge/` vào phần tài liệu/knowledge của Agent:
- `kangnam-brand.md`, `kangnam-market.md` — bắt buộc cho brand Kangnam.
- `kangnam-service-ham-mat.md` — nạp khi làm dịch vụ hàm mặt.
- `service-_TEMPLATE.md` — giữ để nhân bản dịch vụ mới.

> Nếu platform giới hạn số file: tối thiểu cần `system-prompt.md` + 2 file brand. Service file nạp theo nhu cầu.

## Bước 3. Nạp template & tài liệu vận hành
- `output-template.md`, `output-template-content.md` — để Agent xuất đúng khung.
- `input-template.md`, `prompt-guide.md` — cho người dùng.
- `samples/` — ví dụ tham chiếu (tùy chọn).

## Bước 4. Kiểm tra (smoke test)
Gửi: *"Bạn là ai, làm được gì, đang nạp kiến thức brand nào?"*
Đạt nếu Agent: nêu đúng vai trò Planner, phân biệt 2 mode (Plan/Content), liệt kê được brand đã nạp.

---

# PHẦN 2 — QUY TRÌNH SỬ DỤNG

```
1. Điền input-template.md
2. Agent kiểm tra dữ liệu → tóm tắt → bạn XÁC NHẬN
3. Agent viết spec.md (kế hoạch/thiết kế) → bạn XÁC NHẬN
4. Agent triển khai
5. Review → yêu cầu tối ưu
6. Xuất bản final
```

**Lưu ý:** Agent luôn dừng chờ "ok/Xác nhận" ở bước 2 và 3 — đây là thiết kế, không phải lỗi.

---

# PHẦN 3 — CHỌN ĐÚNG MODE

| Bạn cần | Mode | Câu lệnh mẫu |
|---|---|---|
| Kế hoạch Marketing, chiến lược, KPI, timeline | **PLAN** | "PLAN mode: lập kế hoạch Performance Branding cho dịch vụ cắt mí Kangnam, 3 tháng, theo output-template." |
| Kịch bản video, hook, storyboard, content bank | **CONTENT** | "CONTENT mode: 3 kịch bản TOF hàm mặt Kangnam, mỗi bản 1 hook chính + 3 biến thể." |

Không nêu mode → Agent sẽ hỏi lại.

---

# PHẦN 4 — PROMPT HIỆU QUẢ

Luôn có: **Bối cảnh → Mục tiêu → Khách hàng → Website → Thời gian → Đầu ra mong muốn**.

✅ Tốt:
```
CONTENT mode.
Brand: Kangnam | Dịch vụ: Hàm mặt (móm do xương)
Tệp: nữ 20–30, tự ti khớp cắn ngược
Phễu: TOF | Định dạng: video 30s
Yêu cầu: 2 kịch bản + storyboard, ⚠ đánh dấu chỗ cần xác minh.
```
❌ Tránh: "Viết kế hoạch marketing cho tôi" / "Cho tôi ý tưởng" (quá chung chung, thiếu mục tiêu).

Chi tiết thêm: xem `prompt-guide.md`.

---

# PHẦN 5 — THÊM BRAND / DỊCH VỤ MỚI

**Thêm dịch vụ (cùng brand):**
1. Copy `knowledge/service-_TEMPLATE.md` → `knowledge/<brand>-service-<slug>.md`.
2. Điền Insight · USP · Bằng chứng · Khung TOF/MOF/BOF · Storyboard.
3. Cập nhật 1 dòng bảng dịch vụ trong `<brand>-market.md` trỏ tới file mới.

**Thêm brand mới (VD Paris):**
1. Tạo `<brand>-brand.md` (định vị, USP, **Voice riêng**, Content Bank PB) và `<brand>-market.md`.
2. **Không sửa `system-prompt.md`** — brain đã trung tính.
3. Nạp file brand mới vào knowledge; khi làm việc, nêu rõ brand để Agent nạp đúng.

---

# PHẦN 6 — KIỂM TRA CHẤT LƯỢNG ĐẦU RA

Trước khi dùng kết quả, đối chiếu nhanh:
- [ ] Đúng brand, không lẫn voice/ví dụ brand khác.
- [ ] Có phân tích trước đề xuất; mọi đề xuất có lý do.
- [ ] KPI đo được; **không có số liệu bịa**.
- [ ] Giả định được ghi rõ.
- [ ] Chỗ cần dữ liệu thật đánh dấu `⚠ Cần xác minh từ <brand>`.
- [ ] Không cam kết tuyệt đối/100%/không đau/không rủi ro; tuân thủ quảng cáo y tế.

---

# PHẦN 7 — XỬ LÝ SỰ CỐ

| Hiện tượng | Nguyên nhân | Cách xử lý |
|---|---|---|
| Agent trả lời chung chung | Thiếu input / chưa nêu mode | Điền input-template, nêu rõ mode + mục tiêu |
| Lẫn ví dụ Paris vào Kangnam | Nạp nhầm/thiếu file brand | Chỉ nạp knowledge brand đang làm; nêu rõ brand |
| Bịa tên bác sĩ/số liệu | Kiến thức brand còn `...` | Bổ sung dữ liệu thật hoặc chấp nhận `⚠ xác minh` |
| Agent viết code ngay, chưa hỏi | Bỏ qua bước spec | Nhắc: "làm theo quy trình, viết spec chờ xác nhận" |
| Không dừng chờ xác nhận | Prompt yêu cầu làm luôn | Tách yêu cầu: xin spec trước |

---

# PHẦN 8 — CHECKLIST CÀI ĐẶT

- [ ] `system-prompt.md` đặt làm System Prompt.
- [ ] `kangnam-brand.md` + `kangnam-market.md` đã nạp.
- [ ] Template Plan + Content đã nạp.
- [ ] Smoke test đạt (Agent nêu đúng vai trò + 2 mode + brand).
- [ ] prompt-guide.md gửi cho người dùng cuối.
