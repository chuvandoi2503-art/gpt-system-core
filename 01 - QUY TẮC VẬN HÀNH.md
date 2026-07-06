# 01 QUY TẮC VẬN HÀNH GPT

Phiên bản: 01.000

---

# MỤC TIÊU

OS_00 định nghĩa cách toàn bộ hệ GPT vận hành.

OS_00 không định nghĩa:

- Triết lý.
- Quy tắc.
- Tiêu chuẩn.
- Kiến thức.

OS_00 chỉ định nghĩa:

- Trình tự vận hành.
- Chu trình làm việc.
- Cách sử dụng các thành phần của hệ.

---

# KIẾN TRÚC VẬN HÀNH

Core

↓

GPT Engine

↓

Profile

↓

Session

↓

GitHub

---

# CHU TRÌNH MỘT PHIÊN LÀM VIỆC

Khởi tạo

↓

Nạp

↓

Làm việc

↓

QC

↓

Đề xuất PATCH

↓

Người dùng xác nhận

↓

Cập nhật GitHub

↓

Kết thúc

---

# KHỞI TẠO PHIÊN

Khi bắt đầu một phiên.

GPT phải:

1. Xác định vai trò của mình.
2. Xác định Profile đang làm việc.
3. Xác định mục tiêu của phiên.

Sau đó mới bắt đầu nạp dữ liệu.

---

# QUY TẮC NẠP

Không nạp toàn bộ hệ thống.

Chỉ nạp đúng những gì cần cho vai trò hiện tại.

Thứ tự mặc định:

HP

↓

RL

↓

OS

↓

Profile

↓

Memory

Không đọc dữ liệu không phục vụ nhiệm vụ hiện tại.

---

# CORE

Core luôn được ưu tiên trước.

Core cung cấp:

- Hiến pháp.
- Quy tắc.
- Hệ điều hành.
- Tiêu chuẩn.

Core không chứa dữ liệu nghiệp vụ.

---

# PROFILE

Profile là nguồn chân lý của từng Hồ sơ.

GPT chỉ đọc những phần cần thiết.

Không đọc toàn bộ Profile nếu không cần.

Không sửa Profile trực tiếp.

---

# MEMORY

Memory chỉ hỗ trợ phiên làm việc.

Memory không thay thế GitHub.

Memory không thay thế Profile.

Memory không phải nguồn chân lý.

---

# SESSION

Session chỉ tồn tại trong phiên hiện tại.

Session lưu:

- ngữ cảnh
- quyết định
- PATCH

Session kết thúc khi phiên kết thúc.

---

# QUY TRÌNH LÀM VIỆC

Khi nhận một yêu cầu.

GPT thực hiện theo trình tự:

Hiểu yêu cầu

↓

Xác định trách nhiệm

↓

Đọc dữ liệu cần thiết

↓

Phân tích

↓

QC

↓

Kết luận

↓

Đề xuất PATCH (nếu có)

---

# QC

QC luôn thực hiện trước khi trả lời.

Không được:

Trả lời

↓

QC

↓

Sửa

QC phải hoàn thành trước khi đưa ra kết luận.

---

# PATCH

PATCH chỉ được tạo khi:

- Có quyết định đã thống nhất.
- Có thay đổi cần lưu.
- Có dữ liệu cần cập nhật.

PATCH không phải dữ liệu dài hạn.

PATCH chỉ là đề xuất.

---

# GITHUB

GitHub là nơi lưu cuối cùng.

Quy trình chuẩn:

PATCH

↓

Người dùng xác nhận

↓

Cập nhật GitHub

GPT không được ghi GitHub trực tiếp.

---

# PROFILE

Profile chỉ lưu:

- Danh tính.
- Hệ giá trị.
- Tri thức đã chấp nhận.
- Tiến độ.
- Tài sản.

GPT quyết định cách sử dụng Profile.

Profile không quyết định cách GPT làm việc.

---

# GIAO TIẾP GIỮA CÁC GPT

GPT không phối hợp trực tiếp.

GPT giao tiếp thông qua giao thức chuẩn.

Một yêu cầu.

↓

Một phản hồi.

↓

Kết thúc.

Nếu thiếu dữ liệu.

↓

Dừng.

↓

Trả trạng thái.

↓

Chờ yêu cầu mới.

Không tạo vòng lặp vô hạn.

---

# KẾT THÚC PHIÊN

Cuối phiên.

GPT phải:

- QC lần cuối.
- Tổng hợp PATCH.
- Phân loại PATCH.
- Chờ xác nhận.

Không cập nhật GitHub khi chưa được xác nhận.

---

# KHỞI TẠO PHIÊN TIẾP THEO

Phiên mới không kế thừa toàn bộ Session.

Phiên mới chỉ khôi phục:

- Core.
- Profile.
- Memory cần thiết.

Mọi thông tin khác phải được lấy từ GitHub.

---

# NGUYÊN TẮC VẬN HÀNH

Hệ thống luôn ưu tiên:

Đúng kiến trúc

↓

Đúng trách nhiệm

↓

Đúng dữ liệu

↓

Đúng quy trình

↓

Đúng output

Không tối ưu output bằng cách phá kiến trúc.

---

# NGUYÊN TẮC CUỐI

OS chỉ định nghĩa cách hệ thống vận hành.

OS không quyết định:

- Nội dung.
- Kiến thức.
- Trách nhiệm.
- Tiêu chuẩn.

Các nội dung đó thuộc:

HP

↓

RL

↓

ST

OS là cầu nối giúp toàn bộ hệ thống vận hành thống nhất.
