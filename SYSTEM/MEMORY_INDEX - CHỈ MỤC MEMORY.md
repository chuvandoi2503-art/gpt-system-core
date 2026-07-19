# MEMORY_INDEX

Phiên bản: 04.000

---

# REPOSITORY

Owner:

chuvandoi2503-art

Repository:

gpt-system-core

---

# MỤC ĐÍCH

Memory Index là điểm vào duy nhất của Core System.

GPT phải đọc file này trước khi truy cập các tài liệu thuộc Core System.

Memory Index dùng để:

- Định vị Core.
- Định vị System.
- Xác định Load Strategy.
- Xác định nguồn chân lý của toàn hệ GPT.

Không tự suy đoán path.

Không sử dụng Memory hội thoại làm nguồn chân lý.

---

# CORE

Repository:

gpt-system-core

CORE là nguồn chân lý duy nhất của toàn bộ hệ GPT.

## 00 - HIẾN PHÁP GPT

Path:

CORE/00 - HIẾN PHÁP GPT.md

Mô tả:

- Hiến pháp của toàn hệ GPT.
- Các nguyên tắc bất biến.
- Người dùng là người quyết định cuối cùng.

---

## 01 - QUY TẮC VẬN HÀNH

Path:

CORE/01 - QUY TẮC VẬN HÀNH.md

Mô tả:

- Quy tắc vận hành chung.
- Thứ tự ưu tiên khi ra quyết định.
- Quy tắc sử dụng hệ thống.

---

## 02 - TIÊU CHUẨN PHÂN TÁCH TRÁCH NHIỆM

Path:

CORE/02 - TIÊU CHUẨN PHÂN TÁCH TRÁCH NHIỆM.md

Mô tả:

- Tiêu chuẩn phân tách trách nhiệm.
- Quy tắc phân chia GPT.
- Quy tắc phân chia Workflow.
- Quy tắc phân chia Capability.

---

## 03 - TIÊU CHUẨN HỒ SƠ

Path:

CORE/03 - TIÊU CHUẨN HỒ SƠ.md

Mô tả:

- Tiêu chuẩn Hồ sơ.
- Tiêu chuẩn Profile.
- Tiêu chuẩn Runtime Context.

---

## 04 - TIÊU CHUẨN PATCH

Path:

CORE/04 - TIÊU CHUẨN PATCH.md

Mô tả:

- Tiêu chuẩn PATCH.
- Quy tắc cập nhật.
- Quy tắc kết thúc phiên.

---

## 05 - NGUYÊN TẮC KIẾN TRÚC

Path:

CORE/05 - NGUYÊN TẮC KIẾN TRÚC.md

Mô tả:

- Nguyên tắc kiến trúc.
- Quy tắc QC tệp hệ thống.
- Quy tắc mở rộng hệ thống.
- Quy tắc nguồn chân lý.

---

# SYSTEM

Repository:

gpt-system-core

Các tài liệu System không được nạp mặc định.

Chỉ được đọc khi có nhu cầu vận hành thực tế.

---

## MEMORY_ARCHITECTURE

Path:

SYSTEM/MEMORY_ARCHITECTURE.md

Mô tả:

Kiến trúc Memory chuẩn của toàn hệ GPT.

---

## PATCH_STANDARD

Path:

SYSTEM/PATCH_STANDARD.md

Mô tả:

Tiêu chuẩn PATCH chi tiết.

---

## GITHUB_WRITE_POLICY

Path:

SYSTEM/GITHUB_WRITE_POLICY.md

Mô tả:

Quy tắc ghi GitHub.

---

## GITHUB_ACTION_SETUP

Path:

SYSTEM/GITHUB_ACTION_SETUP.md

Mô tả:

Thiết lập GitHub Action.

---

## NAMING_CONVENTION

Path:

SYSTEM/NAMING_CONVENTION.md

Mô tả:

Quy tắc đặt tên:

- Repository.
- GPT.
- File.
- Memory.
- Knowledge.
- Profile.

---

## RESTORE_GUIDE

Path:

SYSTEM/RESTORE_GUIDE.md

Mô tả:

Hướng dẫn khôi phục GPT và Memory.

---

# KNOWLEDGE UPLOAD STANDARD

Tất cả GPT trong hệ thống phải tải mặc định:

- CORE/00 - HIẾN PHÁP GPT.md
- CORE/01 - QUY TẮC VẬN HÀNH.md
- CORE/02 - TIÊU CHUẨN PHÂN TÁCH TRÁCH NHIỆM.md
- CORE/05 - NGUYÊN TẮC KIẾN TRÚC.md

---

# SESSION LOAD STANDARD

Khi khởi tạo phiên, GPT phải đọc:

- CORE/03 - TIÊU CHUẨN HỒ SƠ.md
- CORE/04 - TIÊU CHUẨN PATCH.md

Sau đó thực hiện quy trình khởi tạo riêng của từng GPT.

Ví dụ:

- MEMORY_INDEX
- RULE_<GPT>
- WM
- LM
- Runtime Context

---

# LOAD STRATEGY

## AUTO LOAD

Luôn tải:

- 00
- 01
- 02
- 05

---

## SESSION LOAD

Khi khởi tạo phiên:

- 03
- 04

---

## LOAD ON DEMAND

Chỉ đọc khi cần:

- SYSTEM/*
- KNOWLEDGE/*
- MEMORY/*
- PROFILE/*
- RUNTIME/*

---

# MEMORY STRUCTURE STANDARD

Mọi Runtime Repository phải sử dụng cấu trúc:

```text
memory/

├── WM_03A/
├── WM_04_1/
├── LM_03B/
└── LM_04/
```

---

# NGUYÊN TẮC NGUỒN CHÂN LÝ

CORE là nguồn chân lý duy nhất của:

- Hiến pháp.
- Vận hành.
- Phân tách trách nhiệm.
- Hồ sơ.
- Patch.
- Kiến trúc.

Nếu một nội dung đã tồn tại trong CORE:

- Chỉ tham chiếu.
- Không sao chép.
- Không tạo nguồn chân lý thứ hai.

---

# NGUYÊN TẮC CUỐI CÙNG

Memory Index là bản đồ của Repository.

Memory Index không phải nơi lưu:

- Tri thức nghiệp vụ.
- Memory làm việc.
- Knowledge chuyên ngành.

Memory Index chỉ có trách nhiệm:

- Điều hướng.
- Xác định nguồn chân lý.
- Xác định Load Strategy.
- Hỗ trợ khởi tạo phiên.

Mọi quyết định kiến trúc phải tuân thủ:

- Thực tế > Lý thuyết.
- Vận hành được > Kiến trúc đẹp.
- Kiến trúc đi trước thực tế tối đa 1–2 bước.
- Nếu ngày mai không dùng thì hôm nay không xây.
