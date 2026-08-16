---
ai_authored: true
type: ban-do
status: cho-phe-chuan
updated: 2026-08-10
tags:
  - goi-von-cong-dong
  - hien-chuong
  - onboarding
---

# Hiến chương — Bản đồ

> [!abstract] Bắt đầu từ đây
> Đây là cửa vào của tầng hiến chương. Nếu anh chị chỉ có 5 phút, đọc mục 1 và mục 4 là đủ để tham gia.
>
> Toàn bộ tầng này đang ở trạng thái **chờ phê chuẩn**. Nội dung có thể sửa; điều không sửa được là *cách* sửa.

## 1. Hệ này hoạt động thế nào trong 60 giây

```text
Tiên đề      điều không bao giờ được vi phạm
   ↓
Nguyên tắc   nguyên lý xử lý một loại vấn đề
   ↓
Luật         quy tắc cụ thể, đo được đạt hay không đạt
   ↓
Tiền lệ      cách một ca thật đã được xử, ràng buộc ca sau
```

Hai quy tắc chi phối toàn bộ:

> [!important] Quy tắc 1 — Truy nguyên bắt buộc
> Một luật không chỉ ra được nó thực thi tiên đề nào là **luật vô hiệu**, kể cả khi nội dung nghe hợp lý.

> [!important] Quy tắc 2 — Tiên đề không mặc cả
> Tiên đề lõi cứng không bao giờ bị cân đo. Tiên đề vòng ngoài không bị bác bỏ, nhưng khi hai điều va nhau thì được cân bằng theo [[Giao thức xử lý xung đột]] và phải ghi thành tiền lệ.

## 2. Các văn bản của tầng này

| Văn bản | Nội dung | Trạng thái |
|---|---|---|
| [[Tiên đề lõi cứng]] | `LC-01`…`LC-06` — tuyệt đối, không ngoại lệ | Chờ phê chuẩn |
| [[Tiên đề vòng ngoài]] | `TĐ-01`…`TĐ-12` — không bác bỏ, có thể cân bằng | Chờ phê chuẩn |
| [[Giao thức suy dẫn luật]] | Phép kiểm hợp hiến 6 bước | Chờ phê chuẩn |
| [[Giao thức xử lý xung đột]] | Khi hai tiên đề chỉ ngược nhau | Chờ phê chuẩn |
| [[Vai trò và cặp vai bị cấm]] | Ai làm gì, ai không được kiêm gì | Chờ phê chuẩn |
| `Tiền lệ/` | Các phán quyết đã ra | 1 tiền lệ mẫu |

Bản thiết kế tổng thể nằm ở [[Kiến trúc hiến chương và suy dẫn luật]].

## 3. Quan hệ với phần còn lại của vault

Tầng hiến chương nằm **trên** dây chuyền `00`–`06`, không phải một khâu trong đó.

```text
        Hiến chương  ← tầng này
             │ ràng buộc
             ▼
00 Là gì → 01 Nguồn → 02 Mở rộng → 03 Vấn đề
                → 04 Giải pháp → 05 Phương án → 06 Thực làm
```

| Tầng hiến chương | Sống ở thư mục |
|---|---|
| Tiên đề | `Hiến chương/` |
| Nguyên tắc (`NT-xxx`) | `04 Giải pháp/` |
| Luật (`L-xxx`) | `05 Phương án/` |
| Tiền lệ (`TL-xxx`) | `Hiến chương/Tiền lệ/` |
| Vấn đề, câu hỏi (`VD-`, `CH-`) | `03 Vấn đề/` |
| Ca thực (`CA-xxx`) | `06 Thực làm/` |

> [!warning] Đừng nhầm hai chữ "hiến chương"
> [[Campaign charter]] là hiến chương của **một chiến dịch**. Tầng này là hiến chương của **nền tảng**.
>
> Điều khoản trong hiến chương chiến dịch trái với tiên đề nền tảng thì vô hiệu, kể cả khi người góp đã bấm đồng ý.

## 4. Tham gia thế nào

Không cần đọc hết whitepaper. Chọn một trong bốn đường:

### Đường 1 — Nêu một vấn đề (dễ nhất)

Thấy một tình huống mà hệ chưa có luật, hoặc có luật nhưng ra kết quả sai.

```text
Chép [[Mẫu vấn đề]] vào 03 Vấn đề/
Điền: tình huống, vì sao nó là vấn đề, ai chịu thiệt
Không cần biết tiên đề nào liên quan — người soạn dẫn sẽ nối
```

### Đường 2 — Đặt một câu hỏi

Đọc một tiên đề và không hiểu nó nghĩa là gì trong thực tế.

```text
Chép [[Mẫu câu hỏi]] vào 03 Vấn đề/
Câu hỏi ngây thơ là câu hỏi có giá trị nhất ở giai đoạn này
```

### Đường 3 — Mang một ca thật

Có một dự án, một tình huống đã xảy ra ngoài đời để thử luật.

```text
Chép [[Mẫu tiền lệ]] phần "ca thực" vào 06 Thực làm/
Ca thật quan trọng hơn tranh luận giả định
```

### Đường 4 — Phản biện một dự thảo

Nhiệm vụ là **tìm cách bẻ** một dự thảo luật, không phải khen nó.

```text
Chép [[Mẫu phản biện]]
Trả lời: tôi sẽ lách luật này bằng cách nào nếu tôi là người xấu?
```

> [!important] Không có phản biện thì không có luật
> Một dự thảo không có người phản biện đứng tên sẽ không được đưa ra kiểm hợp hiến. Đây là vai thiếu người nhất và có giá trị nhất hiện nay.

## 5. Hai trạng thái dành riêng cho giai đoạn sớm

Dự án đang ở mức luận giải rất sớm. Hai trạng thái sau tồn tại để không phải chốt bừa:

```text
HOÃN VÌ THIẾU CA THỰC
→ Câu hỏi hợp lệ nhưng chưa thể trả lời khi chưa có dự án thật.
  Không đóng, không ép kết luận. Ca thực xuất hiện sẽ kích hoạt lại.

CHỐT TẠM CHO PILOT
→ Luật đủ dùng cho quy mô pilot, BẮT BUỘC có ngày hết hạn xem lại.
  Ngăn quy tắc tạm âm thầm trở thành vĩnh viễn.
```

Ghi "chưa biết" là một kết quả hợp lệ. Đoán bừa rồi khoá lại thì không.

## 6. Hệ mã số

```text
LC-01…LC-06   Tiên đề lõi cứng
TĐ-01…TĐ-12   Tiên đề vòng ngoài
NT-xxx        Nguyên tắc
L-xxx         Luật
TL-xxx        Tiền lệ
VD-xxx        Vấn đề
CH-xxx        Câu hỏi
CA-xxx        Ca thực
```

Mã số không phải hình thức. Không có mã thì chuỗi truy nguyên không kiểm tra được, và toàn bộ Quy tắc 1 sụp.

## 7. Việc cần làm tiếp

| Việc | Ai | Trạng thái |
|---|---|---|
| Phê chuẩn 6 điều lõi cứng | Hội đồng hiến chương | Chờ |
| Chuyển ~30 tiên đề thiết kế trong whitepaper thành `NT-xxx` | Người soạn dẫn | Chưa bắt đầu |
| Rà pháp lý Việt Nam (NĐ 93/2021, trung gian thanh toán, PCRT) | Cần người có chuyên môn | Trống |
| Chốt tiền lệ có ràng buộc hay chỉ tham khảo | Hội đồng hiến chương | Chờ |
| Tìm người nhận vai phản biện | Tất cả | Trống |

## Liên kết

- [[Kiến trúc hiến chương và suy dẫn luật]]
- [[Khung thiết kê nền tảng cho gọi vốn cộng đồng]]
- [[Gọi vốn cộng đồng]]
- [[Các câu hỏi cần được trả lời]]
