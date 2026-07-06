# ST_07 - TIÊU CHUẨN PATCH

Phiên bản: 01.000

---

# MỤC TIÊU

Định nghĩa chuẩn của một PATCH trong toàn hệ thống.

PATCH là đơn vị thay đổi duy nhất được phép đề xuất cập nhật:

- Core
- Profile
- Memory
- GPT
- Tài liệu

PATCH không phải dữ liệu.

PATCH không phải tri thức.

PATCH là đề xuất thay đổi.

---

# NGUYÊN TẮC

Mọi thay đổi đều phải đi qua PATCH.

Không cập nhật trực tiếp.

Không ghi GitHub trực tiếp.

Không sửa Profile trực tiếp.

---

# VÒNG ĐỜI PATCH

Phát hiện thay đổi

↓

Đề xuất PATCH

↓

QC

↓

Người dùng xác nhận

↓

Cập nhật GitHub

↓

Đóng PATCH

---

# KHI NÀO ĐƯỢC TẠO PATCH

Được tạo khi:

- Có quyết định đã thống nhất.
- Có tri thức mới đã được chấp nhận.
- Có thay đổi kiến trúc.
- Có thay đổi Profile.
- Có thay đổi Core.

Không tạo PATCH cho:

- Ý tưởng.
- Suy đoán.
- Nội dung đang tranh luận.
- Nội dung chưa QC.

---

# CẤU TRÚC PATCH

Một PATCH chuẩn gồm:

---

## 1. MỤC TIÊU

PATCH thay đổi điều gì.

---

## 2. PHẠM VI

Ảnh hưởng tới:

- Core
- Profile
- Memory
- GPT
- Tài liệu

Có thể nhiều hơn một.

---

## 3. LÝ DO

Vì sao cần thay đổi.

Không chấp nhận:

"Cảm thấy tốt hơn."

Phải nêu được cơ sở.

---

## 4. NỘI DUNG

Những gì sẽ được:

- Thêm
- Sửa
- Xóa
- Di chuyển
- Đổi tên

---

## 5. ẢNH HƯỞNG

PATCH phải nêu rõ:

- Ảnh hưởng cục bộ.
- Ảnh hưởng toàn hệ.
- Có cần cập nhật tài liệu liên quan không.

---

## 6. HÀNH ĐỘNG SAU PATCH

Nếu PATCH được duyệt.

Cần cập nhật:

- File nào.
- GPT nào.
- Profile nào.

---

# QC PATCH

Mọi PATCH đều phải QC trước khi trình người dùng.

QC tối thiểu gồm:

- Đúng tầng kiến trúc.
- Đúng trách nhiệm.
- Không trùng lặp.
- Không phá tương thích.
- Không tạo phức tạp không cần thiết.

Nếu chưa đạt.

Không đề xuất.

---

# XÁC NHẬN

Chỉ người dùng có quyền xác nhận PATCH.

GPT không tự coi PATCH là đã được chấp nhận.

---

# THỰC THI

Sau khi được xác nhận.

PATCH mới được phép:

- Cập nhật GitHub.
- Cập nhật Profile.
- Cập nhật Core.
- Cập nhật Memory.

---

# HỦY PATCH

PATCH bị hủy khi:

- Người dùng từ chối.
- QC phát hiện sai.
- Mục tiêu thay đổi.
- Có PATCH mới thay thế.

PATCH bị hủy không được thực thi.

---

# PATCH THAY THẾ

Một PATCH mới có thể thay thế PATCH cũ.

PATCH mới phải ghi rõ:

- PATCH nào bị thay thế.
- Lý do thay thế.

Không tồn tại hai PATCH cùng thay đổi một nội dung mà không xác định thứ tự.

---

# LỊCH SỬ

Sau khi thực thi.

PATCH không còn là trạng thái làm việc.

PATCH trở thành lịch sử thay đổi.

Tri thức chính thức nằm trong GitHub.

Không nằm trong PATCH.

---

# KHẢ NĂNG MỞ RỘNG

Tiêu chuẩn này áp dụng cho:

- Core
- Profile
- GPT
- Workflow
- Automation

Không phụ thuộc nền tảng lưu trữ.

---

# QUY TẮC CUỐI

PATCH không nhằm thay đổi thật nhanh.

PATCH nhằm đảm bảo mọi thay đổi đều:

- Có lý do.
- Có QC.
- Có người chịu trách nhiệm.
- Có lịch sử.
- Có thể truy vết.
- Có thể khôi phục.
