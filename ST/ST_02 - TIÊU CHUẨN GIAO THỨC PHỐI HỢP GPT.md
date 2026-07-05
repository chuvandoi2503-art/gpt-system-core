# ST_02 - TIÊU CHUẨN GIAO THỨC PHỐI HỢP GPT

Phiên bản: 01.000

---

# MỤC TIÊU

Định nghĩa giao thức phối hợp chung giữa các GPT Engine.

Tiêu chuẩn này không định nghĩa:

- Vai trò.
- Trách nhiệm.
- Cấu trúc Request.
- Cấu trúc Response.

Tiêu chuẩn này chỉ định nghĩa cách các GPT phối hợp với nhau.

---

# NGUYÊN TẮC

GPT không phối hợp trực tiếp.

GPT chỉ phối hợp thông qua giao thức chung.

Không phụ thuộc:

- GPT nào.
- Nhà cung cấp nào.
- API nào.
- Công cụ nào.

Chỉ phụ thuộc giao thức.

---

# KIẾN TRÚC

GPT Engine

↓

Giao thức

↓

GPT Engine

Không được:

GPT

↓

GPT

↓

GPT

↓

GPT

theo kiểu gọi trực tiếp.

---

# GIAO THỨC CHUẨN

Một lần phối hợp luôn gồm ba bước.

Yêu cầu

↓

Phản hồi

↓

Kết thúc

Sau khi phản hồi hoàn thành.

Phiên phối hợp kết thúc.

---

# MỘT YÊU CẦU

Một yêu cầu.

↓

Một GPT xử lý.

↓

Một phản hồi.

Không chia nhỏ.

Không chuyển tiếp.

Không tạo chuỗi gọi.

---

# KHÔNG VÒNG LẶP

Không được tạo:

GPT A

↓

GPT B

↓

GPT A

↓

GPT B

↓

...

Nếu GPT không đủ dữ liệu.

Phải dừng.

Không được tự gọi ngược.

---

# KHÔNG GỌI DÂY CHUYỀN

Không được:

GPT A

↓

GPT B

↓

GPT C

↓

GPT D

trong cùng một yêu cầu.

Nếu cần.

Người điều phối hoặc Automation phải tạo yêu cầu mới.

---

# ĐIỀU PHỐI

Mỗi yêu cầu chỉ có:

- Một nơi gửi.
- Một nơi nhận.

Nếu cần nhiều GPT.

Từng GPT làm việc độc lập.

Không phụ thuộc kết nối nội bộ.

---

# TRẠNG THÁI

Mỗi phiên phối hợp phải kết thúc bằng một trạng thái.

Ví dụ:

Hoàn thành.

↓

Thiếu dữ liệu.

↓

Không đủ thẩm quyền.

↓

Lỗi.

↓

Từ chối.

Không để trạng thái mở.

---

# XỬ LÝ LỖI

Nếu xảy ra lỗi.

GPT phải:

Dừng.

↓

Trả trạng thái.

↓

Kết thúc.

Không thử lại vô hạn.

Không gọi GPT khác để xử lý thay.

---

# PHỐI HỢP THỦ CÔNG

Khi người dùng điều phối.

Người dùng là cầu nối giữa các GPT.

Mỗi GPT chỉ xử lý yêu cầu mình nhận được.

Không giả định nội dung của GPT khác.

---

# PHỐI HỢP TỰ ĐỘNG

Khi sử dụng API hoặc Automation.

Bộ điều phối chịu trách nhiệm:

- Gửi yêu cầu.
- Nhận phản hồi.
- Quyết định yêu cầu tiếp theo.

GPT không tự điều phối.

---

# TÍNH ĐỘC LẬP

Mỗi GPT phải có khả năng hoạt động độc lập.

Không phụ thuộc:

- Bộ nhớ của GPT khác.
- Phiên làm việc của GPT khác.
- Nội dung chưa được gửi qua giao thức.

---

# MỞ RỘNG

Tiêu chuẩn này áp dụng cho:

- GPT.
- API.
- n8n.
- Workflow.
- Agent.
- Hệ thống nhiều mô hình AI.

Không phụ thuộc nền tảng triển khai.

---

# QUY TẮC CUỐI

Mọi phối hợp giữa các GPT đều phải thông qua giao thức chung.

Không tạo cơ chế phối hợp riêng cho từng GPT.

Một giao thức.

Nhiều GPT.

Nhiều nền tảng.

Một nguyên tắc.
