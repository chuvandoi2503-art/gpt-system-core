# 04 - TIÊU CHUẨN PATCH

Phiên bản: 01.001

---

# MỤC ĐÍCH

Quy định cấu trúc chuẩn của một PATCH.

PATCH là đề xuất thay đổi có kiểm soát.

Mọi thay đổi muốn lưu vào GitHub đều phải đi qua PATCH.

---

# VAI TRÒ RUNTIME

File này được GPT đọc khi cần:

* Đề xuất sửa file.
* Đề xuất tạo file mới.
* Đề xuất cập nhật Memory.
* Đề xuất cập nhật Hồ sơ.
* Chuẩn bị nội dung để người dùng duyệt trước khi ghi GitHub.

File này không dùng để:

* Tự ghi GitHub.
* Thay thế xác nhận của người dùng.
* Lưu tri thức dài hạn.
* Lưu nội dung tạm thời.

---

# NGUYÊN TẮC BẮT BUỘC

GPT không được tự ghi thay đổi vào GitHub nếu chưa có xác nhận rõ ràng của người dùng.

GPT không được tạo PATCH dựa trên suy đoán.

GPT không được bỏ qua PATCH khi thay đổi có ảnh hưởng đến file, Memory, Hồ sơ, Rule hoặc Knowledge.

PATCH phải đủ rõ để người dùng hiểu:

* Thay đổi gì.
* Thay đổi ở đâu.
* Vì sao thay đổi.
* Ảnh hưởng đến phần nào.
* Có phụ thuộc file khác không.
* Trạng thái hiện tại là gì.

---

# CẤU TRÚC PATCH

Một PATCH tối thiểu gồm:

* Mục tiêu
* Danh sách thay đổi
* Lý do
* Ảnh hưởng
* Phụ thuộc
* Trạng thái

---

# 1. MỤC TIÊU

Ghi rõ PATCH nhằm thay đổi điều gì.

Ví dụ:

* Refactor file Core sang dạng runtime-readable.
* Cập nhật Working Memory.
* Bổ sung tiêu chuẩn QC.
* Tạo file Profile mới.
* Sửa lỗi path trong MEMORY_INDEX.

---

# 2. DANH SÁCH THAY ĐỔI

Mỗi thay đổi phải ghi rõ:

* Repository
* File
* Thao tác
* Vị trí
* Nội dung

---

## Repository

Ghi repo bị ảnh hưởng.

Ví dụ:

```md
Repository:
gpt-system-core
```

---

## File

Ghi đúng tên file hoặc path.

Ví dụ:

```md
File:
CORE/04 - TIÊU CHUẨN PATCH.md
```

---

## Thao tác

Chọn một trong các thao tác:

* Tạo mới
* Thay thế toàn bộ
* Chỉnh sửa một phần
* Bổ sung
* Xóa
* Đổi tên
* Di chuyển

---

## Vị trí

Nếu thay thế toàn bộ file:

```md
Vị trí:
Toàn bộ file
```

Nếu chỉnh sửa một phần:

```md
Vị trí:
Sau mục "..."
Trước mục "..."
Thay mục "..."
```

Không ghi vị trí mơ hồ.

---

## Nội dung

Ghi đầy đủ nội dung cần lưu.

Không mô tả chung chung.

Không rút gọn.

Không dùng placeholder nếu nội dung đã có thể xác định.

---

# 3. LÝ DO

Ghi vì sao cần thay đổi.

Lý do phải gắn với mục tiêu vận hành.

Ví dụ:

* Để GPT runtime đọc và hành động rõ hơn.
* Để giảm diễn giải không cần thiết.
* Để chuẩn hóa quy trình cập nhật GitHub.
* Để tránh ghi đè ngoài kiểm soát.

---

# 4. ẢNH HƯỞNG

Ghi rõ PATCH ảnh hưởng tới tầng nào.

Các tầng có thể gồm:

* Core
* Runtime
* Memory
* Knowledge
* Profile
* GPT Engine
* Workflow
* Automation

Nếu không có ảnh hưởng ngoài file đang sửa, ghi:

```md
Ảnh hưởng:
Chỉ ảnh hưởng file được nêu trong PATCH.
```

---

# 5. PHỤ THUỘC

Ghi rõ PATCH có cần PATCH khác trước hoặc sau không.

Nếu có, ghi rõ phụ thuộc.

Nếu không có, ghi:

```md
Phụ thuộc:
Không có.
```

---

# 6. TRẠNG THÁI

Một PATCH chỉ có một trong các trạng thái:

* Đề xuất
* Chờ duyệt
* Đã duyệt
* Đã lưu
* Hủy

GPT chỉ được ghi GitHub khi PATCH ở trạng thái:

```md
Đã duyệt
```

và người dùng đã yêu cầu ghi rõ ràng.

---

# QUY TRÌNH PATCH

Khi cần thay đổi file:

1. Đọc file hiện tại.
2. Xác định nội dung cần thay đổi.
3. Tạo PATCH.
4. Hiển thị PATCH cho người dùng.
5. Chờ người dùng duyệt.
6. Chỉ ghi GitHub sau khi được duyệt rõ ràng.
7. Sau khi ghi, báo lại file đã ghi và trạng thái.

Không tự thay đổi.

Không tự tối ưu thêm ngoài PATCH.

---

# KHI KHÔNG ĐỦ CƠ SỞ TẠO PATCH

Nếu không đủ dữ liệu để tạo PATCH an toàn, GPT phải nói:

```md
Tôi chưa đủ cơ sở để tạo PATCH an toàn.
```

Không tự đoán repo.

Không tự đoán path.

Không tự đoán nội dung cần ghi.

---

# TIÊU CHUẨN PASS

Một PATCH đạt chuẩn khi:

* Có mục tiêu rõ.
* Có đúng repository.
* Có đúng file hoặc path.
* Có thao tác rõ.
* Có vị trí rõ.
* Có nội dung đầy đủ.
* Có lý do.
* Có ảnh hưởng.
* Có phụ thuộc.
* Có trạng thái.
* Không chứa suy đoán.
* Không yêu cầu GPT tự ghi nếu chưa được duyệt.

---

# NGUYÊN TẮC CUỐI CÙNG

PATCH không phải nơi lưu tri thức.

PATCH chỉ là đề xuất thay đổi.

Tri thức chính thức chỉ tồn tại sau khi PATCH đã được duyệt và ghi vào nguồn chân lý.
