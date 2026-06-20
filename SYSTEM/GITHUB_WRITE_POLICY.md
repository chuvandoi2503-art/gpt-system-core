# GITHUB_WRITE_POLICY

Phiên bản: 01.000

Trạng thái: Áp dụng toàn hệ

---

# 1. MỤC ĐÍCH

File này quy định cách GPT được phép đọc và ghi GitHub.

Mục tiêu:

* Tránh ghi nhầm.
* Tránh mất dữ liệu.
* Tránh ghi đè bộ nhớ.
* Dễ kiểm soát thay đổi.
* Dễ khôi phục.

---

# 2. TRIẾT LÝ

GitHub là nguồn chân lý.

GPT chỉ là lớp suy luận.

Mọi thay đổi quan trọng phải đi qua GitHub.

---

# 3. NGUYÊN TẮC AN TOÀN

Ưu tiên:

An toàn dữ liệu

cao hơn

Tốc độ ghi dữ liệu.

---

Nếu có nghi ngờ:

Không ghi.

---

# 4. QUY TẮC ĐỌC FILE

GPT được phép:

Đọc GitHub bằng:

```text
getContent
```

---

Mục đích:

* Tra cứu tri thức.
* Tra cứu bộ nhớ.
* Tra cứu rule.
* Tra cứu cấu hình.

---

# 5. QUY TẮC TẠO FILE MỚI

Nếu file chưa tồn tại:

GPT được phép:

* Tạo PATCH.
* Hiển thị nội dung.
* Chờ xác nhận.
* Tạo file mới.

---

Không cần SHA.

---

Commit ví dụ:

```text
TEST_CREATE_FILE
```

hoặc

```text
CREATE_RULE
CREATE_MEMORY
CREATE_KNOWLEDGE
```

---

# 6. QUY TẮC SỬA FILE

Nếu file đã tồn tại:

Bắt buộc:

Bước 1

Đọc file.

---

Bước 2

Lấy SHA.

---

Bước 3

Tạo PATCH.

---

Bước 4

Chờ xác nhận.

---

Bước 5

Ghi GitHub.

---

Không được bỏ qua bất kỳ bước nào.

---

# 7. QUY TẮC MEMORY

Các file sau được xem là bộ nhớ hệ thống:

```text
KN_*
RULE_*
WM_*
LM_*
```

---

Không được ghi trực tiếp.

Luôn phải:

PATCH

↓

Xác nhận

↓

Ghi

---

# 8. QUY TẮC SYSTEM

Các file trong:

```text
SYSTEM/
```

được xem là file hệ thống.

---

Không được tự sửa.

Phải có xác nhận rõ ràng.

---

# 9. QUY TẮC GHI ĐÈ

Không được ghi đè khi:

* Chưa đọc file.
* Chưa có SHA.
* Chưa có PATCH.
* Chưa có xác nhận.

---

Nếu thiếu bất kỳ điều kiện nào:

Không ghi.

---

# 10. QUY TẮC COMMIT

Commit phải thể hiện mục đích.

Ví dụ:

```text
TEST_CREATE_FILE

UPDATE_WM

UPDATE_LM

UPDATE_RULE

UPDATE_KN

UPDATE_SYSTEM
```

---

Không dùng:

```text
update

fix

save
```

---

Quá chung chung.

---

# 11. QUY TẮC XÁC NHẬN

Các câu được xem là xác nhận hợp lệ:

```text
Đồng ý

Ghi GitHub

Tiến hành

OK ghi

Xác nhận ghi
```

---

Nếu chưa rõ:

Phải hỏi lại.

---

# 12. QUY TẮC KHÔNG ĐỦ DỮ LIỆU

Nếu GPT không chắc chắn:

Phải nói rõ:

```text
Tôi chưa đủ cơ sở để ghi GitHub an toàn.
```

---

Không được suy đoán.

---

# 13. QUY TẮC REPOSITORY

GPT không được yêu cầu người dùng nhập lại:

* Owner
* Repo
* Path

nếu đã có trong:

```text
MEMORY_INDEX
```

hoặc

Repository mặc định của GPT.

---

# 14. QUY TẮC MEMORY_INDEX

Khi người dùng nhắc:

```text
WM_03A_CONTENT

WM_04_1_CONTENT

LM_03B_CONTENT
```

GPT phải:

Đọc:

```text
SYSTEM/MEMORY_INDEX.md
```

↓

Tìm path

↓

Đọc file

---

Không tự suy đoán path.

---

# 15. QUY TẮC GHI HÀNG LOẠT

Nếu nhiều file cần thay đổi:

Ưu tiên:

PATCH toàn bộ

↓

Người dùng duyệt

↓

Ghi lần lượt

---

Không tự ghi nhiều file khi chưa được duyệt.

---

# 16. QUY TẮC BACKUP

GitHub là nguồn chân lý.

Tuy nhiên:

Người dùng nên có backup ngoài GitHub.

Ví dụ:

* PC cá nhân.
* NAS.
* Cloud backup.

---

GPT không chịu trách nhiệm cho backup ngoài GitHub.

---

# 17. QUY TẮC CUỐI CÙNG

Nếu phải lựa chọn giữa:

Ghi nhanh

và

Ghi an toàn

Luôn ưu tiên:

Ghi an toàn.

Không có dữ liệu nào đáng để đánh đổi tính toàn vẹn của hệ thống.
