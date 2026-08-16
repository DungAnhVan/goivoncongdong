---
ai_authored: true
type: giao-thuc
status: cho-phe-chuan
updated: 2026-08-10
tags:
  - goi-von-cong-dong
  - hien-chuong
  - vai-tro
---

# Vai trò và cặp vai bị cấm

> [!abstract] Nguyên tắc thiết kế
> Vai trò được định nghĩa theo **chức năng trong cỗ máy suy dẫn**, không theo chức danh hay thâm niên.
>
> Một người có thể giữ nhiều vai — trừ các cặp bị cấm ở mục 3.

## 1. Tám vai

| Vai | Việc phải làm | Điều kiện vào |
|---|---|---|
| **Người nêu vấn đề** | Nêu tình huống chưa có luật, hoặc luật đang ra kết quả sai | Bất kỳ ai |
| **Người đặt câu hỏi** | Nêu điều chưa rõ trong hiến chương | Bất kỳ ai |
| **Người mang ca thực** | Mang dự án hoặc tình huống thật vào để thử luật | Bất kỳ ai có ca thật |
| **Người soạn dẫn** | Nối vấn đề về tiên đề, viết dự thảo kèm chuỗi truy nguyên | Cần hiểu hiến chương |
| **Người phản biện** | Tìm cách **bẻ** dự thảo | Cần độc lập với người soạn |
| **Người kiểm hợp hiến** | Chạy phép kiểm 6 bước, kết luận đạt hoặc không | Cần độc lập với người soạn |
| **Người phân xử** | Chỉ vào cuộc khi có xung đột tiên đề; ra tiền lệ | Hội đồng, không phải cá nhân |
| **Người giữ sổ** | Đánh mã, giữ phiên bản, không cho sửa lén | Cần kỷ luật, không cần chuyên môn sâu |

Ba vai đầu **không cần biết gì về hiến chương**. Đây là chủ ý: rào cản tham gia phải thấp ở đầu vào, cao ở đầu ra.

---

## 2. Chi tiết ba vai khó tuyển nhất

### Người phản biện

Nhiệm vụ **không phải** góp ý cho dự thảo tốt lên. Nhiệm vụ là chứng minh nó hỏng.

Bốn câu bắt buộc trả lời:

```text
Cách tôi sẽ lách luật này nếu tôi là người xấu:
Trường hợp luật này ra kết quả vô lý:
Chi phí mà luật này áp lên người trung thực:
Tiên đề nào có thể bị luật này vi phạm gián tiếp:
```

> [!important] Không có phản biện thì không có luật
> Một dự thảo không có người phản biện **đứng tên** sẽ không được đưa ra kiểm hợp hiến.
>
> Đứng tên là bắt buộc. Phản biện ẩn danh không tạo được trách nhiệm, và ở giai đoạn này nhóm còn nhỏ nên không có rủi ro trả đũa đáng kể.

Đây là vai thiếu người nhất và có giá trị nhất hiện nay.

### Người kiểm hợp hiến

Không phải người quyết định luật hay dở. Chỉ trả lời: **6 bước có đạt không**.

```text
Đạt 6/6      → chuyển sang ban hành
Không đạt    → trả về kèm chỉ rõ bước nào hỏng và vì sao
Không rõ     → yêu cầu bổ sung, KHÔNG tự suy đoán ý người soạn
```

Người kiểm hợp hiến không được sửa dự thảo. Sửa là việc của người soạn.

### Người phân xử

**Phải là hội đồng, không được là cá nhân.** Lý do: một cá nhân phân xử xung đột tiên đề sẽ dần biến sở thích của mình thành hiến chương, và không có ai ghi lại ý kiến thiểu số.

Số lượng tối thiểu ở pilot: 3 người, trong đó ít nhất 1 người không tham gia soạn hoặc phản biện luật liên quan.

---

## 3. Các cặp vai bị cấm trùng

```text
Người soạn dẫn      ≠  Người kiểm hợp hiến   (cùng một luật)
Người soạn dẫn      ≠  Người phản biện        (cùng một luật)
Người mang ca thực  ≠  Người phân xử          (cùng một ca)
Người giữ sổ        ≠  mọi vai ra quyết định
```

> [!important] Hệ thống tự áp tiên đề lên chính nó
> Bốn cặp cấm trên chính là [[Tiên đề lõi cứng|LC-03 — không tự phán]] áp cho **bộ máy quản trị nội bộ**, không chỉ cho người gây quỹ.
>
> Một hệ thống đòi hỏi người khác tách biệt vai trò nhưng tự mình gộp hết vào một người sẽ mất tính chính đáng ngay từ ngày đầu — và sẽ bị nhà đầu tư hỏi đúng câu đó.

### Cấm theo ca, không cấm theo người

Lưu ý cách viết: *"cùng một luật"*, *"cùng một ca"*.

```text
Được phép:
Chị B soạn luật L-003, đồng thời phản biện luật L-007 của người khác.

Không được phép:
Chị B soạn luật L-003 rồi tự kiểm hợp hiến L-003.
```

Đây là điều làm cho hệ vận hành được với nhóm nhỏ.

---

## 4. Bộ khung tối thiểu cho pilot

Nhóm hiện chưa có phân công. Số người tối thiểu để cỗ máy chạy được:

| Số người | Chạy được không | Cách bố trí |
|---|---|---|
| 1 | **Không** | Vi phạm `LC-03` ngay từ đầu |
| 2 | Miễn cưỡng | A soạn / B phản biện + kiểm; đổi vai theo từng luật |
| 3 | Được | Thêm người giữ sổ tách riêng |
| 5 | Tốt | Đủ lập hội đồng phân xử 3 người |

> [!warning] Ngưỡng 2 người là ngưỡng sàn
> Dưới 2 người thì không nên ban hành luật nào — chỉ nên tích luỹ vấn đề và câu hỏi ở trạng thái `hoãn vì thiếu ca thực`.
>
> Ghi "chưa đủ người để chốt" là một kết quả trung thực. Chốt một mình rồi gọi đó là hiến chương thì không.

---

## 5. Người giữ sổ — vai bị đánh giá thấp nhất

Không cần chuyên môn về gọi vốn. Nhưng nếu vai này trống thì cả kiến trúc sụp, vì [[Giao thức suy dẫn luật|quy tắc truy nguyên]] cần mã số ổn định để hoạt động.

Việc cụ thể:

```text
Cấp mã cho vấn đề, câu hỏi, luật, tiền lệ, ca thực
Bảo đảm không có hai thứ trùng mã
Giữ phiên bản: bản cũ không bị xoá, chỉ bị đánh dấu superseded
Kiểm tra mỗi luật ban hành có đủ tên người soạn / phản biện / kiểm
Phát hiện và báo khi có cặp vai bị cấm trùng
Không được bỏ phiếu, không được phê duyệt
```

Việc cuối cùng trong danh sách là điều làm cho vai này đáng tin: người giữ sổ tích trữ được rất nhiều thông tin, nên không được có quyền quyết định.

---

## 6. Cách nhận vai

Chưa cần thủ tục. Ở giai đoạn này:

```text
1. Ghi tên vào bảng dưới, kèm vai muốn nhận
2. Nếu nhận vai soạn dẫn hoặc phản biện,
   đọc [[Tiên đề lõi cứng]] và [[Giao thức suy dẫn luật]] trước
3. Vai có thể trả lại bất cứ lúc nào, chỉ cần bàn giao việc đang dở
```

| Tên | Vai | Ghi chú |
|---|---|---|
| *(trống)* | | |

> Bảng này cố tình để trống. Buổi thảo luận 2-8 kết thúc mà chưa có phân công nào — đây là việc cần chốt ở buổi tiếp theo, xem [[Buổi thảo luận sắp tới]].

## Liên kết

- [[Hiến chương - Bản đồ]]
- [[Tiên đề lõi cứng]]
- [[Giao thức suy dẫn luật]]
- [[Giao thức xử lý xung đột]]
- [[Mẫu phản biện]]
- [[Buổi thảo luận sắp tới]]
