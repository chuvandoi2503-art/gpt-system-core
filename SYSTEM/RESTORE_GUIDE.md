# RESTORE_GUIDE

Phiên bản: 01.000

Trạng thái: Áp dụng toàn hệ

---

# 1. MỤC ĐÍCH

File này mô tả quy trình khôi phục hoàn chỉnh một GPT từ GitHub.

Mục tiêu:

* Không phụ thuộc GPT cũ.
* Không phụ thuộc bộ nhớ hội thoại.
* Không phụ thuộc người tạo ban đầu.
* Có thể dựng lại GPT bất kỳ lúc nào.

---

# 2. TRIẾT LÝ

GPT có thể mất.

GPT có thể bị xóa.

GPT có thể bị lỗi.

GitHub mới là thứ tồn tại lâu dài.

---

Nguyên tắc:

```text id="2gtnca"
GitHub
=
Nguồn chân lý

GPT
=
Lớp suy luận
```

---

# 3. ĐIỀU KIỆN KHÔI PHỤC

Cần:

* GitHub Repository.
* OpenAPI Schema.
* GitHub Token.
* GPT Builder Backup.

---

Nếu có đủ 4 thành phần:

Có thể dựng lại GPT.

---

# 4. THÀNH PHẦN TỐI THIỂU

Bắt buộc:

```text id="8s8x3f"
MEMORY_INDEX

RULE_COMMON

RULE_<GPT>

WM_03A_<GPT>

WM_04_1_<GPT>
```

---

Đây là tập tối thiểu để GPT hoạt động.

---

# 5. THÀNH PHẦN ĐẦY ĐỦ

Khuyến nghị:

```text id="c1m2e0"
KN_00

KN_01

KN_02_<GPT>

RULE_COMMON

RULE_<GPT>

WM_03A_<GPT>

WM_04_1_<GPT>

LM_03B_<GPT>

LM_04_<GPT>

GPT_BUILDER_BACKUP
```

---

# 6. QUY TRÌNH KHÔI PHỤC

Bước 1

Tạo GPT mới.

---

Bước 2

Đặt tên GPT.

---

Bước 3

Dán Instructions từ:

```text id="nvq5mz"
GPT_BUILDER_BACKUP
```

---

Bước 4

Import OpenAPI Schema.

---

Bước 5

Cấu hình GitHub Action.

---

Bước 6

Gắn Token.

---

Bước 7

Kiểm tra đọc GitHub.

---

PASS.

---

# 7. KIỂM TRA ĐỌC

Đọc:

```text id="y9r8d4"
SYSTEM/MEMORY_INDEX.md
```

---

Nếu đọc được:

PASS.

---

Nếu không đọc được:

Dừng khôi phục.

---

# 8. KIỂM TRA BỘ NHỚ

Đọc:

```text id="glk3ht"
RULE_COMMON

RULE_<GPT>

WM_03A_<GPT>

WM_04_1_<GPT>
```

---

Nếu đọc được:

PASS.

---

# 9. KIỂM TRA GHI

Tạo file:

```text id="aw4r29"
TEST_CREATE_FILE.md
```

---

Commit:

```text id="jtwjhf"
TEST_CREATE_FILE
```

---

Nếu tạo được:

PASS.

---

Sau đó có thể xóa file test.

---

# 10. KHÔI PHỤC SAU KHI MẤT GPT

Tình huống:

GPT bị xóa.

---

Giải pháp:

```text id="e5o5af"
Tạo GPT mới

↓

Dán GPT_BUILDER_BACKUP

↓

Kết nối GitHub

↓

PASS
```

---

Không cần khôi phục bộ nhớ thủ công.

---

# 11. CHUYỂN TÀI KHOẢN CHATGPT

Tình huống:

Đổi tài khoản.

---

Giải pháp:

```text id="wuj0it"
GPT_BUILDER_BACKUP

+

GitHub

+

Schema
```

---

Khôi phục đầy đủ.

---

# 12. CHUYỂN NGƯỜI QUẢN TRỊ

Tình huống:

Người vận hành mới tiếp quản.

---

Yêu cầu:

* Có GitHub.
* Có Token.
* Có Backup.

---

Không cần truy cập GPT cũ.

---

# 13. KIỂM TRA HOÀN THIỆN

Checklist:

```text id="2cn4rk"
Đọc MEMORY_INDEX

Đọc RULE_COMMON

Đọc WM_03A

Đọc WM_04_1

Ghi file test

Đọc file test
```

---

Nếu PASS toàn bộ:

GPT hoạt động bình thường.

---

# 14. NHỮNG GÌ KHÔNG CẦN KHÔI PHỤC

Không cần:

* Hội thoại cũ.
* Context cũ.
* Chat History.
* Memory ChatGPT.

---

GitHub mới là thứ cần khôi phục.

---

# 15. BACKUP NGOÀI GITHUB

Khuyến nghị:

Backup định kỳ:

* PC cá nhân.
* NAS.
* Google Drive.

---

Tần suất:

* KN
* RULE

khi thay đổi.

---

WM và LM:

Hàng tuần hoặc khi có thay đổi lớn.

---

# 16. ĐỊNH NGHĨA THÀNH CÔNG

Một GPT được xem là:

Có thể khôi phục

khi:

Người khác

↓

Không cần GPT cũ

↓

Chỉ dùng GitHub

↓

Có thể dựng lại GPT hoạt động bình thường.

---

# 17. QUY TẮC CUỐI CÙNG

Nếu một GPT không thể dựng lại từ GitHub:

Kiến trúc đó chưa đạt chuẩn.

Mục tiêu cuối của toàn hệ là:

```text id="8dzvzb"
Xóa GPT

↓

Tạo GPT mới

↓

Kết nối GitHub

↓

Hoạt động bình thường
```

mà không mất tri thức và không mất khả năng vận hành.
