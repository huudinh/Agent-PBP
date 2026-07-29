# HƯỚNG DẪN CÀI ĐẶT ĐA NỀN TẢNG
# Performance Branding Planner — Gemini · ChatGPT · Claude
Version: 4.1

---

# TỔNG QUAN 2 THÀNH PHẦN

Mọi nền tảng đều cần đúng 2 thứ:

1. **Instructions (Chỉ dẫn / System Prompt)** ← dán **`system-prompt-platform.md`**
   → bản này đã nhúng sẵn 2 template (Plan §16 + Content §17), bỏ mọi tham chiếu đường dẫn file, đổi sang "tham chiếu Tri thức". Không tốn slot file.
2. **Knowledge (Tri thức)** ← upload **các file brand + service**.

> ⚠ Dùng `system-prompt-platform.md`, KHÔNG dùng `system-prompt.md` gốc cho Gemini/GPT — bản gốc còn giả định file-system (đọc theo path, `ls`, ghi `spec.md`) không chạy trên Gem/GPT.

---

# CHIẾN LƯỢC FILE (vì các nền tảng giới hạn số lượng)

Giới hạn tri thức: **Gemini Gem = 10 file · ChatGPT (Custom GPT) = 20 file · Claude Project = theo dung lượng ngữ cảnh (không đếm cứng).**
Ràng buộc chặt nhất là **Gemini 10 file** → thiết kế để ≤5 file, vừa mọi nền tảng.

## Cấp độ nạp

| Mức | Upload gì | Số file | Dùng khi |
|---|---|---|---|
| **Tối thiểu** | `kangnam-brand.md` · `kangnam-market.md` | 2 | Chỉ làm Plan/chiến lược Kangnam |
| **Khuyến nghị** | + `kangnam-service-ham-mat.md` | 3 | Làm cả Content/kịch bản dịch vụ |
| **Đầy đủ** | + template gốc `output-template.md` · `output-template-content.md` | 5 | Muốn Agent bám khung xuất tuyệt đối |

## KHÔNG cần upload

- **`system-prompt-platform.md`** → dán vào Instructions, không phải file tri thức.
- **`service-_TEMPLATE.md`** → chỉ dùng khi *bạn* soạn dịch vụ mới; Agent không cần lúc chạy.
- **`README.md` · `INSTALL-PLATFORMS.md` · `SETUP-GUIDE.md` · `prompt-guide.md` · `input-template.md` · `samples/`** → tài liệu cho người, không nạp vào Agent.
- **2 template** đã nhúng trong Instructions → chỉ upload thêm ở mức "Đầy đủ" nếu muốn nhấn mạnh; bình thường bỏ qua để tiết kiệm slot.

## Thêm brand mới (VD Paris) mà không vượt giới hạn
Mỗi brand cộng ~2–3 file. Nếu chạm trần 10 file Gem → **tách mỗi brand thành 1 Gem riêng** (mỗi Gem chỉ nạp tri thức 1 brand). ChatGPT/Claude dư sức gom nhiều brand trong 1 Agent.

---

# A. GEMINI (Gem)

1. Gemini → **Gem manager** (icon ◇) → **New Gem**.
2. **Tên:** `Performance Branding Planner`.
3. **Mô tả:** `AI chuyên xây dựng kế hoạch Marketing & Performance Branding từ thông tin doanh nghiệp.`
4. **Chỉ dẫn:** dán TOÀN BỘ `system-prompt-platform.md`.
5. **Tri thức:** upload theo mức Khuyến nghị (3 file). Tối đa 10 file.
6. **Lưu** → test ở khung Xem trước.

**Lưu ý Gemini:**
- Gem đôi khi bỏ qua file khi Instructions quá dài → bản platform đã có dòng "LỆNH ƯU TIÊN: luôn tham chiếu Tri thức trước khi trả lời" ở đầu, giữ nguyên dòng đó.
- Có thể connect Google Drive để file tự cập nhật (thay vì upload tĩnh).
- Người nhận link Gem **thấy được Instructions + tên file** → đừng để thông tin nhạy cảm.

---

# B. CHATGPT (Custom GPT)

1. ChatGPT → **Explore GPTs** → **Create** → tab **Configure**.
2. **Name:** `Performance Branding Planner`. **Description:** như trên.
3. **Instructions:** dán `system-prompt-platform.md`.
4. **Knowledge:** upload tới 20 file (thoải mái nạp mức Đầy đủ + nhiều service/brand).
5. **Capabilities:** bật Web Search nếu cần tra cứu; tắt nếu muốn Agent chỉ bám Tri thức.
6. **Conversation starters** (gợi ý):
   - "PLAN mode: kế hoạch Performance Branding cắt mí Kangnam 3 tháng."
   - "CONTENT mode: 3 kịch bản TOF hàm mặt Kangnam, mỗi bản 1 hook + 3 biến thể."
7. **Save / Update**.

---

# C. CLAUDE (Project)

1. Claude → **Projects** → **Create project**.
2. Đặt tên project `Performance Branding Planner`.
3. **Set project instructions / Custom instructions:** dán `system-prompt-platform.md`.
   *(Claude Project có file-system nhẹ hơn — nếu bạn dùng qua môi trường có đọc file thật thì có thể dùng `system-prompt.md` gốc; với Project chat thông thường, dùng bản platform.)*
4. **Project knowledge:** thêm file brand + service. Claude không giới hạn số file cứng nhưng có trần dung lượng — nạp mức Khuyến nghị/Đầy đủ đều ổn.
5. Bắt đầu chat trong project.

---

# SMOKE TEST (mọi nền tảng)

Gửi: **"Bạn là ai, làm được gì, đang nạp kiến thức brand nào? Phân biệt 2 mode giúp tôi."**

Đạt khi Agent:
- [ ] Nêu đúng vai trò *Performance Branding Planner* (tư vấn chiến lược, không chỉ viết content).
- [ ] Phân biệt **PLAN** vs **CONTENT** mode.
- [ ] Liệt kê đúng brand đang có trong Tri thức.
- [ ] Không bịa; hỏi lại khi thiếu dữ liệu.

Thử tiếp 1 lệnh mỗi mode để chắc Agent bám template.

---

# XỬ LÝ SỰ CỐ NHANH

| Hiện tượng | Cách xử lý |
|---|---|
| Agent bỏ qua file tri thức | Giữ dòng "LỆNH ƯU TIÊN… tham chiếu Tri thức trước" ở đầu Instructions; rút gọn bớt Instructions nếu quá dài |
| Trả lời chung chung | Nêu rõ **mode** + mục tiêu; điền biểu mẫu đầu vào |
| Lẫn ví dụ Paris vào Kangnam | Mỗi Gem/Agent chỉ nạp tri thức 1 brand, hoặc nêu rõ brand mỗi lượt |
| Bịa tên bác sĩ/số liệu | Bổ sung dữ liệu thật vào file brand; chấp nhận `⚠ Cần xác minh` |
| Chạm giới hạn 10 file (Gemini) | Tách brand ra Gem riêng; bỏ upload template (đã nhúng Instructions) |

---

# CHECKLIST CÀI ĐẶT

- [ ] Đã dán `system-prompt-platform.md` vào Instructions (không phải bản gốc).
- [ ] Tên + Mô tả đầy đủ (không bị cắt).
- [ ] Upload tri thức mức Khuyến nghị (≥ brand + market).
- [ ] Giữ dòng LỆNH ƯU TIÊN ở đầu Instructions.
- [ ] Smoke test đạt 4 mục.
