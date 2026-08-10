---
type: tien-le
status: mau-chay-thu
updated: 2026-08-10
tags:
  - goi-von-cong-dong
  - hien-chuong
  - tien-le
---

# TL-001 — Ẩn danh và chống Sybil

> [!warning] Đây là tiền lệ mẫu, chưa có hiệu lực
> `TL-001` được viết để **chạy thử giao thức**, cho thấy một tiền lệ trông như thế nào. Nó chưa qua hội đồng phân xử thật.
>
> Dùng nó làm khuôn, đừng dùng nó làm căn cứ.

## Hồ sơ

```text
tien_le_id:     TL-001
ngay:           2026-08-10
xung_dot_giua:  TĐ-05  ↔  TĐ-09
nguoi_phan_xu:  chưa có hội đồng
trang_thai:     mẫu chạy thử
```

## Xung đột

| Bên | Tiên đề | Đang bảo vệ điều gì |
|---|---|---|
| A | `TĐ-05` Ghi nhận phục vụ phẩm giá | Quyền của người góp được ẩn danh hoàn toàn, kể cả với nền tảng |
| B | `TĐ-09` Cộng đồng không đồng nhất tổng tiền | Tính toàn vẹn của tín hiệu "độ rộng ủng hộ" mà matching và quadratic funding dựa vào |

**Tình huống cụ thể:** Nền tảng áp dụng matching theo số người ủng hộ. Một người muốn góp mà không để lại bất kỳ dấu vết định danh nào. Nếu cho phép, cơ chế matching bị mở cửa cho Sybil attack — một người tạo nhiều danh tính để giả mạo độ rộng.

---

## B0 — Có phải xung đột thật không?

**Kiểm phạm vi:**

```text
TĐ-05 nói về HIỂN THỊ CÔNG KHAI — ai nhìn thấy tên tôi
TĐ-09 nói về XÁC MINH NỘI BỘ — hệ thống có đếm đúng số người không
→ Hai miền khác nhau
```

Phần lớn xung đột tan ở đây. Một người có thể **ẩn danh với công chúng** mà vẫn **được xác minh là duy nhất** trong hệ thống — đây là hai việc hoàn toàn khác nhau, thường bị gộp làm một.

**Phần xung đột còn lại là thật:** khi người góp không muốn để lại dấu vết định danh cho **cả nền tảng**, không chỉ cho công chúng.

→ Đi tiếp B1.

---

## B1 — Lõi cứng có liên quan không?

`LC-02` không gian lận **có liên quan** — người góp giả là gian lận.

Nhưng:

> `LC-02` cấm **hành vi tạo người góp giả**. Nó **không** quy định phải xác minh bằng phương pháp nào.

Đây đúng là cạm bẫy mà [[Giao thức xử lý xung đột]] cảnh báo ở B1. Không thể viện `LC-02` để áp đặt eKYC bắt buộc.

→ Lõi cứng liên quan gián tiếp. Đi tiếp B2.

---

## B2 — Phép cân bằng

### a. Mỗi bên bảo vệ gì

- **Bên A:** quyền không bị phơi bày. Quan trọng nhất với người góp ít tiền, người ở vị thế xã hội nhạy cảm, và người muốn tránh bị xin tiếp.
- **Bên B:** nếu độ rộng bị giả mạo, matching sẽ chuyển tiền công về phía kẻ gian lận. Thiệt hại rơi vào các dự án trung thực.

### b. Giải pháp thứ ba

> **Tách "chứng minh là người duy nhất" khỏi "danh tính là ai".**

```text
Bên thứ ba xác minh tính duy nhất
   → cấp một token không liên kết ngược được
      → nền tảng đếm token
         → nền tảng KHÔNG biết ai
```

Thoả cả `TĐ-05` lẫn `TĐ-09`. Đây là kết quả mong muốn.

**Điều kiện để dùng được:** phải có một bên thứ ba đủ tin cậy và một cơ chế token không liên kết. Ở quy mô pilot hiện tại, chưa có.

### c. Khi chưa có giải pháp thứ ba

Chọn phương án hy sinh ít nhất:

> **Người ẩn danh vẫn góp được bình thường, nhưng khoản của họ không được tính vào trọng số độ rộng.**

```text
Hy sinh cái gì:      một phần hiệu lực của TĐ-09
                     (mẫu tính độ rộng nhỏ hơn thực tế)
Hy sinh bao nhiêu:   tỷ lệ bằng đúng tỷ lệ người chọn ẩn danh tuyệt đối
Ai chịu:             dự án có nhiều người ủng hộ ẩn danh
                     — nhận matching thấp hơn
Bù thế nào:          công bố rõ trước khi chiến dịch mở,
                     để dự án tự chọn có dùng matching hay không
Điều kiện xét lại:   khi có bên thứ ba xác minh duy nhất khả dụng
```

**Phương án bị loại:** cấm ẩn danh tuyệt đối. Lý do — nó hy sinh trọn vẹn `TĐ-05` để bảo vệ một phần `TĐ-09`, trong khi phương án được chọn chỉ hy sinh một phần `TĐ-09` mà giữ nguyên `TĐ-05`.

### d. Cân xứng hẹp

Cái mất: độ chính xác của một cơ chế phân bổ. Cái được: một quyền của người tham gia được giữ nguyên vẹn. Đạt.

---

## B3 — Nguyên tắc rút ra

> **Ẩn danh là quyền đối với công chúng, không phải quyền đối với hệ thống kiểm toán.**
>
> **Khi hệ thống chưa thể xác minh tính duy nhất, hãy loại khoản ẩn danh khỏi trọng số thay vì cấm ẩn danh.**

### Phạm vi ràng buộc

```text
ÁP DỤNG cho:
- mọi cơ chế thưởng hoặc matching tính theo SỐ NGƯỜI
- quadratic funding
- ngưỡng kích hoạt tính theo số người ủng hộ tối thiểu

KHÔNG áp dụng cho:
- cơ chế tính theo TỔNG TIỀN
- yêu cầu định danh phát sinh từ nghĩa vụ pháp lý
  (phòng chống rửa tiền, thuế) — đó là ràng buộc bên ngoài,
  không phải cân bằng tiên đề
```

Ngoại lệ thứ hai quan trọng: tiền lệ này không được dùng để né nghĩa vụ pháp lý.

### Điều kiện xét lại

Tiền lệ này mất hiệu lực khi có bên thứ ba xác minh tính duy nhất mà không lộ danh tính, khả dụng ở chi phí hợp lý cho quy mô của nền tảng.

---

## Kỹ thuật tái dùng được

Cách giải ở bước B2c là một mẫu chung, dùng được cho nhiều xung đột khác:

> **Đổi hình phạt thành đổi trọng số.** Thay vì cấm một hành vi hợp pháp nhưng khó xác minh, hãy để nó tồn tại mà không tính vào các cơ chế phụ thuộc vào sự xác minh đó.

Các xung đột khác có thể dùng lại mẫu này:

```text
Dự án không cung cấp dữ liệu outcome
  → không cấm, nhưng không đủ điều kiện vào bảng xếp hạng tác động

Người góp không xác minh danh tính
  → vẫn góp được, nhưng không có quyền biểu quyết material change

Bằng chứng do chính bên hưởng lợi tạo
  → không loại bỏ, nhưng không đủ một mình để mở milestone
```

## Ý kiến thiểu số

*(chưa có — tiền lệ này chưa qua hội đồng)*

> Mục này bắt buộc phải tồn tại trong mọi tiền lệ thật. Nếu hội đồng nhất trí, ghi "nhất trí". Không được xoá mục.

## Liên kết

- [[Giao thức xử lý xung đột]]
- [[Tiên đề vòng ngoài]]
- [[Tiên đề lõi cứng]]
- [[Mẫu tiền lệ]]
