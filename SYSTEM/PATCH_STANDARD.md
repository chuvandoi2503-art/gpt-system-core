# PATCH_STANDARD

Phiên bản: 01.000

Trạng thái: Áp dụng toàn hệ

---

# 1. MỤC ĐÍCH

File này quy định chuẩn PATCH dùng chung cho toàn bộ hệ GPT.

Mục tiêu:

* Thống nhất cập nhật bộ nhớ.
* Giảm ghi nhầm GitHub.
* Dễ review.
* Dễ kiểm tra.
* Dễ khôi phục.

---

# 2. TRIẾT LÝ

GPT không được sửa bộ nhớ trực tiếp.

Quy trình chuẩn:

PATCH

↓

Người dùng duyệt

↓

Ghi GitHub

---

Không được bỏ qua bước PATCH.

---

# 3. KHI NÀO TẠO PATCH

Bắt buộc tạo PATCH khi:

* Kết thúc phiên.
* Thay đổi Memory.
* Thay đổi Rule.
* Thay đổi Knowledge.
* Thay đổi System.

---

# 4. PHÂN LOẠI PATCH

Toàn hệ sử dụng 5 nhóm chuẩn:

```text
UPDATE_03A

UPDATE_03B

UPDATE_04_1

UPDATE_04_ARCHIVE

DISCARD
```

---

# 5. UPDATE_03A

Mục đích:

Cập nhật Working Memory lõi.

Ví dụ:

* Mục tiêu GPT thay đổi.
* Module GPT thay đổi.
* Nguyên tắc GPT thay đổi.
* Danh tính GPT thay đổi.

---

Tần suất:

Rất thấp.

---

File đích:

```text
WM_03A_<GPT>
```

---

# 6. UPDATE_03B

Mục đích:

Cập nhật Long-term Memory.

Chỉ lưu:

Tri thức đã xác nhận.

---

Ví dụ:

* Format thắng.
* Hook thắng.
* Bài học đã kiểm chứng.
* Quy trình đã xác nhận.

---

File đích:

```text
LM_03B_<GPT>
```

---

# 7. UPDATE_04_1

Mục đích:

Cập nhật trạng thái công việc.

Ví dụ:

* Việc đang làm.
* Ý tưởng đang triển khai.
* Backlog.
* Kế hoạch ngắn hạn.

---

File đích:

```text
WM_04_1_<GPT>
```

---

# 8. UPDATE_04_ARCHIVE

Mục đích:

Lưu lịch sử.

Ví dụ:

* Quyết định.
* Học tập.
* Thử nghiệm.
* Nhật ký.

---

File đích:

```text
LM_04_<GPT>
```

---

# 9. DISCARD

Mục đích:

Loại bỏ.

---

Bao gồm:

* Ý tưởng chưa đủ cơ sở.
* Kết luận chưa xác nhận.
* Thông tin tạm thời.
* Nội dung không còn giá trị.

---

Không ghi GitHub.

---

# 10. CẤU TRÚC PATCH CHUẨN

Ví dụ:

```text
UPDATE_04_1

- Đã chốt tên kênh:
  Đợi Làm Bố

- Cập nhật mã:
  DLB

- Cập nhật hệ kênh gia đình
```

---

# 11. KHÔNG GHI NGAY

Sau khi tạo PATCH:

Không được ghi GitHub ngay.

Phải chờ xác nhận.

---

Ví dụ:

Đúng:

```text
PATCH
↓
Người dùng đồng ý
↓
Ghi GitHub
```

---

Sai:

```text
PATCH
↓
Ghi GitHub
```

---

# 12. QUY TẮC FILE MỚI

Nếu tạo file mới:

Được phép tạo PATCH.

Sau khi xác nhận:

Được phép tạo file.

---

Không cần SHA.

---

# 13. QUY TẮC FILE CŨ

Nếu sửa file cũ:

Bắt buộc:

* Đọc file.
* Lấy SHA.
* Tạo PATCH.
* Chờ xác nhận.
* Mới được ghi.

---

# 14. QUY TẮC KẾT THÚC PHIÊN

Khi người dùng nói:

"Kết thúc phiên"

GPT phải tự động rà soát.

Phân loại:

```text
UPDATE_03A
UPDATE_03B
UPDATE_04_1
UPDATE_04_ARCHIVE
DISCARD
```

---

Không được bỏ qua bước này.

---

# 15. QUY TẮC CHẤT LƯỢNG

PATCH phải:

* Ngắn gọn.
* Rõ ràng.
* Có lý do.
* Có giá trị.

---

Không đưa toàn bộ hội thoại vào PATCH.

---

# 16. QUY TẮC KHÔNG PHÌNH BỘ NHỚ

Không lưu:

* Caption hàng ngày.
* Hook hàng ngày.
* Script hàng ngày.
* Nội dung ngắn hạn không còn giá trị.

---

Chỉ lưu:

Những gì ảnh hưởng tới tương lai.

---

# 17. QUY TẮC CUỐI CÙNG

Nếu phân vân:

Lưu

hay

Không lưu

Ưu tiên:

Không lưu.

Chỉ lưu khi thực sự tạo giá trị dài hạn.

Bộ nhớ chất lượng cao luôn tốt hơn bộ nhớ số lượng lớn.
