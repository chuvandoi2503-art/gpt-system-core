# ST_08 - TIÊU CHUẨN ĐỊNH TUYẾN PATCH

Phiên bản: 01.000

---

# MỤC TIÊU

Định nghĩa cách xác định đích đến của một PATCH.

Tiêu chuẩn này không quy định:

- Nội dung PATCH.
- Cách tạo PATCH.
- Cách lưu GitHub.

Tiêu chuẩn này chỉ quy định:

- PATCH thuộc hệ nào.
- PATCH được phép cập nhật đâu.
- PATCH không được phép cập nhật đâu.

---

# NGUYÊN TẮC

Một PATCH.

↓

Một đích đến chính.

Không được lưu cùng một nội dung ở nhiều nơi.

Nếu nhiều nơi cùng cần.

Ưu tiên:

Một nguồn chân lý.

Các nơi còn lại chỉ liên kết.

---

# QUY TRÌNH ĐỊNH TUYẾN

PATCH

↓

Xác định loại thay đổi

↓

Xác định chủ sở hữu

↓

Xác định đích đến

↓

Đề xuất cập nhật

---

# BƯỚC 1

XÁC ĐỊNH LOẠI THAY ĐỔI

PATCH thuộc một trong các nhóm:

- Kiến trúc.
- Quy tắc.
- Tiêu chuẩn.
- Hồ sơ.
- Tri thức.
- GPT.
- Memory.
- Phiên làm việc.
- Hạ tầng.

Nếu chưa xác định được.

Không định tuyến.

---

# BƯỚC 2

XÁC ĐỊNH CHỦ SỞ HỮU

PATCH phải có đúng một chủ sở hữu.

Ví dụ.

Kiến trúc

↓

Core

---

Tri thức của Hồ sơ

↓

Profile

---

Quy trình của GPT

↓

GPT Engine

---

Memory

↓

Memory

---

Nếu không xác định được chủ sở hữu.

Không cập nhật.

---

# BƯỚC 3

XÁC ĐỊNH ĐÍCH ĐẾN

Sau khi biết chủ sở hữu.

PATCH mới được xác định nơi lưu.

Ví dụ.

---

Kiến trúc

↓

Core

---

Tri thức Hồ sơ

↓

Profile

---

Memory

↓

WM hoặc LM

---

GPT

↓

Repository của GPT

---

Phiên làm việc

↓

Session

---

# QUY TẮC MỘT NGUỒN CHÂN LÝ

Mỗi nội dung chỉ có một nơi lưu chính thức.

Không sao chép cùng một nội dung sang nhiều nơi.

Nếu nhiều thành phần cần sử dụng.

Ưu tiên:

- Chỉ mục.
- Liên kết.
- Tham chiếu.

Không nhân bản dữ liệu.

---

# PATCH KHÔNG ĐỦ ĐIỀU KIỆN

Không định tuyến khi:

- Chưa QC.
- Chưa xác nhận.
- Chưa xác định chủ sở hữu.
- Chưa xác định phạm vi.

PATCH phải dừng.

---

# CẬP NHẬT PROFILE

Chỉ định tuyến vào Profile khi:

- Tri thức đã được chấp nhận.
- Phù hợp hệ giá trị của Profile.
- Có giá trị sử dụng lâu dài.

Không đưa:

- Ý tưởng.
- PATCH tạm.
- Nội dung chưa kiểm chứng.

vào Profile.

---

# CẬP NHẬT CORE

Chỉ định tuyến vào Core khi:

- Thay đổi nguyên lý.
- Thay đổi kiến trúc.
- Thay đổi tiêu chuẩn.
- Thay đổi quy tắc.

Không đưa tri thức nghiệp vụ vào Core.

---

# CẬP NHẬT GPT

Chỉ định tuyến vào GPT khi:

- Thay đổi năng lực GPT.
- Thay đổi Rule riêng.
- Thay đổi Prompt.
- Thay đổi Workflow của GPT.

Không cập nhật tri thức của Profile vào GPT.

---

# CẬP NHẬT MEMORY

Memory chỉ nhận:

- Nội dung phục vụ phiên.
- Nội dung cần nối tiếp.

Memory không nhận:

- Tri thức chính thức.
- Kiến trúc.
- Tiêu chuẩn.

---

# KHÔNG CẬP NHẬT

Một PATCH có thể kết thúc bằng:

Không cập nhật.

Khi:

- Không đủ giá trị.
- Không đúng phạm vi.
- Đã có dữ liệu tương đương.
- Không được người dùng xác nhận.

---

# KHẢ NĂNG MỞ RỘNG

Khi xuất hiện thành phần mới.

Không sửa quy trình định tuyến.

Chỉ bổ sung:

Loại chủ sở hữu mới.

Đích đến mới.

---

# QUY TẮC CUỐI

PATCH không quyết định nơi lưu.

Định tuyến quyết định nơi lưu.

Mỗi thay đổi phải đi đúng chủ sở hữu.

Mỗi chủ sở hữu chỉ có một nguồn chân lý.
