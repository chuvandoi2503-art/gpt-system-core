# 04 - TIÊU CHUẨN PATCH

Phiên bản: 01.000

---

# MỤC TIÊU

Quy định cấu trúc của một PATCH.

PATCH là đơn vị thay đổi duy nhất của hệ thống.

Mọi thay đổi muốn lưu vào GitHub đều phải đi qua PATCH.

---

# NGUYÊN TẮC

Một PATCH phải đủ thông tin để:

- GPT thực hiện được.
- Người dùng lưu thủ công được.

Không cần suy luận thêm.

---

# CẤU TRÚC PATCH

Mỗi PATCH gồm các mục sau.

---

## 1. MỤC TIÊU

PATCH này nhằm thay đổi điều gì.

---

## 2. DANH SÁCH THAY ĐỔI

Mỗi thay đổi phải ghi rõ.

---

### Repository

Ví dụ.

gpt-system-core

---

### File

Ví dụ.

03 - TIÊU CHUẨN HỒ SƠ.md

---

### Thao tác

Chỉ được chọn một.

- Tạo mới
- Thay thế toàn bộ
- Chèn thêm
- Sửa một phần
- Xóa

---

### Vị trí

Nếu không thay toàn bộ.

Phải ghi rõ.

Ví dụ.

- Sau mục "Hệ giá trị"
- Trước mục "Tri thức"
- Thay mục số 03

Không dùng:

"Chèn vào chỗ hợp lý."

---

### Nội dung

Ghi đầy đủ nội dung Markdown cần lưu.

Không mô tả.

Không rút gọn.

---

## 3. LÝ DO

Vì sao cần thay đổi.

---

## 4. ẢNH HƯỞNG

PATCH ảnh hưởng tới.

- Core
- Profile
- GPT

Nếu không ảnh hưởng.

Ghi rõ:

"Không có."

---

## 5. PHỤ THUỘC

Nếu PATCH cần PATCH khác trước.

Phải ghi rõ.

Nếu độc lập.

Ghi:

"Không."

---

## 6. TRẠNG THÁI

Một PATCH chỉ có một trạng thái.

- Đề xuất
- Đã duyệt
- Đã lưu
- Hủy

---

# NGUYÊN TẮC THỰC THI

Sau khi người dùng xác nhận.

PATCH được thực hiện theo đúng thứ tự đã ghi.

Không tự thay đổi.

Không tự tối ưu.

---

# XỬ LÝ SỰ CỐ

Nếu không thể lưu tự động.

GPT phải xuất đầy đủ nội dung PATCH.

Người dùng có thể lưu thủ công mà không cần hỏi thêm.

Nếu một thay đổi thất bại.

Dừng tại thay đổi đó.

Báo rõ:

- Đã hoàn thành gì.
- Chưa hoàn thành gì.

Không tiếp tục nếu có phụ thuộc.

---

# NGUYÊN TẮC CUỐI

PATCH không phải nơi lưu tri thức.

PATCH chỉ là đề xuất thay đổi.

Tri thức chính thức chỉ tồn tại sau khi đã được lưu vào GitHub.
