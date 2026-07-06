# ST_06 - TIÊU CHUẨN TRUY XUẤT TRI THỨC

Phiên bản: 01.000

---

# MỤC TIÊU

Định nghĩa cách GPT truy xuất tri thức từ Profile.

Tiêu chuẩn này không quy định:

- GPT làm gì.
- Profile lưu gì.
- Tri thức nào đúng.

Tiêu chuẩn này chỉ quy định:

- GPT đọc ở đâu.
- Đọc theo nguyên tắc nào.
- Khi nào dừng đọc.
- Khi nào cần đọc thêm.

---

# NGUYÊN TẮC

GPT không đọc toàn bộ Profile.

GPT chỉ đọc đúng lượng tri thức cần thiết để hoàn thành nhiệm vụ hiện tại.

Mục tiêu là:

Đọc ít nhất.

↓

Hiểu đúng nhất.

---

# ĐIỂM VÀO

Mọi lần truy xuất đều bắt đầu từ:

PF_00 - MỤC LỤC HỒ SƠ

GPT không được bắt đầu bằng việc đọc ngẫu nhiên.

---

# XÁC ĐỊNH NHIỆM VỤ

Trước khi đọc.

GPT phải xác định:

- Vai trò hiện tại.
- Mục tiêu của phiên.
- Hồ sơ đang làm việc.

Nếu chưa xác định được.

Không truy xuất.

---

# XÁC ĐỊNH PHẠM VI

Sau khi biết mục tiêu.

GPT xác định:

- Cần lĩnh vực nào.
- Cần giai đoạn nào.
- Cần loại tri thức nào.

Chỉ sau đó mới đọc Profile.

---

# THỨ TỰ TRUY XUẤT

PF_00

↓

PF_01

↓

PF_02

↓

PF_03

↓

PF_04

↓

PF_05

↓

PF_06

Không bỏ qua PF_00.

---

# ĐỌC THEO NHU CẦU

GPT chỉ đọc phần phục vụ nhiệm vụ hiện tại.

Không đọc toàn bộ chỉ vì Profile tồn tại.

Nếu đã đủ dữ liệu.

Dừng truy xuất.

---

# ĐỌC THEO VAI TRÒ

Mỗi GPT đọc khác nhau.

Ví dụ.

Research.

↓

Ưu tiên:

PF_03

PF_04

PF_05

---

Content.

↓

Ưu tiên:

PF_01

PF_03

PF_05

---

Archi.

↓

Ưu tiên:

PF_00

PF_01

PF_02

PF_06

---

Automation.

↓

Ưu tiên:

PF_00

PF_02

PF_04

PF_05

Đây chỉ là thứ tự ưu tiên.

Không phải giới hạn tuyệt đối.

---

# KHOẢNG TRỐNG TRI THỨC

Nếu phát hiện thiếu tri thức.

GPT không tự suy diễn.

GPT phải:

- Ghi nhận khoảng trống.
- Đề xuất yêu cầu mới.
- Tiếp tục với dữ liệu hiện có hoặc dừng theo quy định.

---

# KHÔNG GHI NHỚ THAY PROFILE

GPT không được lưu tri thức dài hạn trong Session.

Sau phiên làm việc.

Mọi tri thức cần giữ lại phải đi qua PATCH.

---

# KHÔNG SAO CHÉP

Không sao chép nguyên Profile sang Session.

Không tạo bản sao Profile.

Session chỉ giữ phần đang sử dụng.

---

# DỪNG TRUY XUẤT

GPT phải dừng đọc khi:

- Đủ dữ liệu.
- Vượt phạm vi yêu cầu.
- Phát hiện khoảng trống cần Research.
- Không còn tài liệu liên quan.

Không đọc thêm nếu không tạo giá trị.

---

# PHỤC HỒI PHIÊN

Khi mở phiên mới.

GPT không đọc lại toàn bộ Profile.

GPT thực hiện lại quy trình truy xuất từ PF_00.

Không sử dụng Session cũ làm nguồn chân lý.

---

# KHẢ NĂNG MỞ RỘNG

Tiêu chuẩn này áp dụng cho mọi GPT.

Không cần sửa khi thêm GPT mới.

GPT mới chỉ cần học:

- Cách xác định nhiệm vụ.
- Cách xác định phạm vi.
- Cách truy xuất.

Không cần thay đổi Profile.

---

# QUY TẮC CUỐI

Profile được thiết kế để nhiều GPT cùng sử dụng.

GPT phải học cách đọc Profile.

Không yêu cầu Profile thay đổi để phù hợp với từng GPT.
