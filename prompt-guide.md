# PROMPT GUIDE
# Performance Branding Agent
Version: 1.0

---

# Giới thiệu

Performance Branding Agent hoạt động hiệu quả nhất khi nhận được yêu cầu rõ ràng và đầy đủ.

Tài liệu này hướng dẫn cách viết Prompt để Agent hiểu đúng nhu cầu và tạo ra bản kế hoạch chất lượng cao.

---

# Chọn Output Mode (bắt buộc nêu rõ)

Agent có 2 chế độ. Nêu rõ trong prompt để tránh hỏi lại:

- **PLAN mode** — kế hoạch/chiến lược (Marketing Plan, Positioning, Big Idea, Content Strategy, Promotion, KPI, Timeline). Xuất theo `output-template.md`.
- **CONTENT mode** — sản xuất content/kịch bản (video script, hook, storyboard, content bank, nhân bản biến thể). Xuất theo `output-template-content.md`.

Ví dụ: *"CONTENT mode: viết 3 kịch bản TOF dịch vụ hàm mặt Kangnam, mỗi bản 1 hook chính + 3 biến thể."*

---

# Công thức Prompt chuẩn

Sử dụng công thức:

```
Bối cảnh

↓

Mục tiêu

↓

Đầu vào

↓

Yêu cầu đầu ra

↓

Ràng buộc
```

Ví dụ:

```
Tôi cần lập kế hoạch Marketing cho dịch vụ cắt mí của Kangnam.

Mục tiêu:
- Tăng Lead
- Tăng Booking

Khách hàng:
Nữ 22-35 tuổi.

Website:
https://....

Hãy tạo bản kế hoạch theo Output Template.
```

---

# Prompt 1
## Tạo kế hoạch Marketing

```
Hãy đóng vai Marketing Strategy Manager.

Dựa trên thông tin tôi cung cấp, hãy tạo một bản kế hoạch Marketing hoàn chỉnh theo Output Template.

Nếu thiếu dữ liệu, hãy ghi rõ "Giả định" thay vì tự suy diễn.
```

---

# Prompt 2
## Phân tích doanh nghiệp

```
Phân tích doanh nghiệp dưới góc nhìn Marketing.

Bao gồm:

- Điểm mạnh
- Điểm yếu
- USP
- Cơ hội
- Thách thức

Không đề xuất giải pháp ở bước này.
```

---

# Prompt 3
## Phân tích khách hàng

```
Hãy xây dựng chân dung khách hàng.

Bao gồm:

- Persona
- Pain Point
- Need
- Insight
- Objection
- Decision Trigger

Giải thích rõ lý do.
```

---

# Prompt 4
## Xây dựng Big Idea

```
Từ Insight đã phân tích,

hãy đề xuất:

- Big Idea
- Key Message
- Supporting Message

Mỗi đề xuất cần giải thích tại sao phù hợp.
```

---

# Prompt 5
## Content Strategy

```
Hãy xây dựng Content Strategy.

Bao gồm:

- Content Pillar
- Mục tiêu từng Pillar
- Nội dung gợi ý
- KPI

Không viết nội dung chi tiết.
```

---

# Prompt 6
## Promotion Strategy

```
Đề xuất các chương trình Promotion.

Không chỉ tập trung giảm giá.

Ưu tiên:

- Quà tặng
- Combo
- Membership
- Referral
- Loyalty

Giải thích ưu và nhược điểm.
```

---

# Prompt 7
## KPI

```
Đề xuất KPI phù hợp với mục tiêu.

Nếu chưa có dữ liệu,

không tự tạo số liệu.

Chỉ đề xuất nhóm KPI cần theo dõi.
```

---

# Prompt 8
## Timeline

```
Hãy lập Timeline triển khai.

Chia theo:

- Chuẩn bị
- Triển khai
- Tối ưu
- Tổng kết

Có mục tiêu của từng giai đoạn.
```

---

# Prompt 9
## Review kế hoạch

```
Đóng vai Marketing Director.

Đánh giá kế hoạch theo các tiêu chí:

- Logic
- Tính khả thi
- ROI
- Khả năng triển khai
- KPI
- Timeline

Đề xuất cải thiện.
```

---

# Prompt 10
## Cải thiện kế hoạch

```
Đây là bản kế hoạch hiện tại.

Hãy:

- Phát hiện điểm yếu.
- Phân tích nguyên nhân.
- Đề xuất cải tiến.

Không viết lại toàn bộ kế hoạch.

Chỉ tập trung vào phần cần nâng cấp.
```

---

# Prompt 11
## Điều chỉnh theo ngân sách

```
Điều chỉnh kế hoạch với ngân sách:

...

Không thay đổi mục tiêu.

Ưu tiên các hoạt động có hiệu quả cao.
```

---

# Prompt 12
## Chuyển đổi cho ngành khác

```
Giữ nguyên cấu trúc kế hoạch.

Điều chỉnh để phù hợp với ngành:

...

Không sử dụng ví dụ của ngành cũ.
```

---

# Prompt 13
## Xuất bản kế hoạch

```
Xuất toàn bộ kế hoạch theo đúng Output Template.

Không bỏ sót phần nào.

Sử dụng Markdown.

Có bảng.

Có Heading.

Có Checklist khi cần.
```

---

# Các Prompt không nên dùng

❌

```
Viết kế hoạch Marketing cho tôi.
```

Quá chung chung.

---

❌

```
Cho tôi ý tưởng Marketing.
```

Không có mục tiêu.

---

❌

```
Làm sao tăng doanh thu?
```

Thiếu bối cảnh.

---

# Prompt tối ưu

Luôn nên có:

```
1. Bối cảnh

2. Mục tiêu

3. Khách hàng

4. Website

5. Thời gian

6. Đầu ra mong muốn
```

Ví dụ:

```
Thương hiệu:
Kangnam

Dịch vụ:
Cắt mí

Mục tiêu:
Tăng Lead

Khách hàng:
Nữ 22-35

Website:
https://...

Thời gian:
3 tháng

Đầu ra:

- Business Analysis
- Insight
- Big Idea
- Content Strategy
- KPI
- Timeline
```

---

# Quy trình sử dụng Agent

Bước 1

Điền Input Template.

↓

Bước 2

Agent kiểm tra dữ liệu.

↓

Bước 3

Agent xác định phần còn thiếu.

↓

Bước 4

Agent lập kế hoạch.

↓

Bước 5

Người dùng Review.

↓

Bước 6

Agent tối ưu.

↓

Bước 7

Xuất bản Final Plan.

---

# Best Practices

✅ Cung cấp càng nhiều dữ liệu càng tốt.

✅ Đính kèm Website nếu có.

✅ Đính kèm Brand Guideline nếu có.

✅ Nêu rõ mục tiêu kinh doanh.

✅ Chỉ rõ đối tượng khách hàng.

✅ Nêu các ràng buộc (ngân sách, thời gian, kênh triển khai...).

---

# Kết quả mong đợi

Sau khi sử dụng đúng quy trình, Agent có thể tạo ra:

- Kế hoạch Marketing.
- Kế hoạch Performance Branding.
- Content Strategy.
- Promotion Strategy.
- KPI Framework.
- Timeline triển khai.
- Báo cáo đề xuất trình bày cho quản lý hoặc khách hàng.