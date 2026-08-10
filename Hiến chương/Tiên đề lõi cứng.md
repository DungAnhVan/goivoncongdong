---
type: tien-de
status: cho-phe-chuan
updated: 2026-08-10
tags:
  - goi-von-cong-dong
  - hien-chuong
  - tien-de
  - loi-cung
---

# Tiên đề lõi cứng

> [!abstract] Địa vị của văn bản này
> Sáu điều dưới đây là phần **không bao giờ được cân đo**. Vi phạm một điều lõi cứng thì mọi lợi ích thu được đều không cứu được tính chính đáng của hệ thống.
>
> Không có ngoại lệ khẩn cấp. Không có "lần này thì chấp nhận được". Không có "vì mục tiêu xã hội tốt".
>
> **Trạng thái: chờ phê chuẩn.** Danh sách này là đề xuất; sau khi phê chuẩn thì chỉ được thêm, không được bớt.

## Nguyên tắc đọc

Lõi cứng cấm một **hành vi**, không quy định một **phương pháp**.

```text
LC-02 cấm tạo người góp giả.
→ Nó KHÔNG bắt buộc phải dùng eKYC.
→ Chọn phương pháp nào là việc của tầng Luật.
```

Nhầm hai thứ này sẽ biến lõi cứng thành cái cớ áp đặt công nghệ, và làm hỏng cả tiên đề tính tỷ lệ.

---

## LC-01 — Không chiếm dụng

> **Nguồn lực được giao không bao giờ trở thành tài sản tự do của người đang giữ nó.**

**Vì sao tuyệt đối.** Đây là điều kiện tồn tại của khái niệm "gọi vốn cộng đồng". Nếu người giữ tiền có thể coi tiền là của mình, thì hoạt động này không khác gì chuyển nhượng tài sản, và toàn bộ tầng quản trị trở nên vô nghĩa.

**Hành vi bị cấm:**

```text
Dùng tiền chiến dịch A cho việc B rồi định "trả lại sau"
Trộn tiền dự án vào tài khoản vận hành không truy vết được
Coi số dư còn lại là lợi nhuận của tổ chức
Coi lãi phát sinh mặc nhiên thuộc bên giữ tiền
Coi danh sách người góp là tài sản marketing tự do
```

**Dấu hiệu vi phạm:** không ai biết tài khoản đứng tên ai; số trên trang dự án không khớp ngân hàng; tiền dư mặc định thuộc dự án mà không có quy tắc công bố trước.

**Nguồn:** canon 10 và 11 — *Quỹ là lời hứa được vật chất hóa*; *Người giữ tiền là quản thác của mục đích*. Chi tiết vận hành tại [[Custody và safeguarding]] và [[Restricted funds]].

---

## LC-02 — Không gian lận

> **Không làm giả bằng chứng, không tạo người góp giả, không che giấu xung đột lợi ích.**

**Vì sao tuyệt đối.** Mọi cơ chế khác của hệ thống — ngưỡng, matching, giải ngân theo mốc, tiền lệ — đều lấy đầu vào từ dữ liệu. Dữ liệu bị bịa thì cả cỗ máy chạy đúng quy trình nhưng ra kết quả sai, và không cách nào phát hiện từ bên trong.

**Hành vi bị cấm:**

```text
Bằng chứng được tạo hoặc chỉnh sửa để khớp tiêu chí
Người góp giả, tài khoản chia nhỏ, thông đồng cụm tài khoản
Thanh tiến độ hiển thị số chưa xác thực
"Đóng góp vừa xảy ra" được tạo giả
Quan hệ bên liên quan không công bố khi phê duyệt hoặc nghiệm thu
```

**Dấu hiệu vi phạm:** chứng từ do một bên tự tạo và tự xác nhận; số người góp tăng đột biến từ cụm tài khoản mới; người phê duyệt có lợi ích trong nhà cung cấp.

> [!warning] Điều này chưa có trong canon 12
> `LC-02` đang nằm rải rác trong [[Campaign failure, recovery and termination]] mục *integrity failure* và các mục "dấu hiệu cảnh báo". Nó cần được nâng lên thành tiên đề.

---

## LC-03 — Không tự phán

> **Người nhận nguồn lực không được là người duy nhất xác nhận điều kiện để nhận nguồn lực đó.**

**Vì sao tuyệt đối.** Đây là lỗi cấu trúc, không phải lỗi đạo đức. Kể cả người hoàn toàn trung thực cũng không thể chứng minh mình trung thực nếu chỉ có mình họ xác nhận. Tự phán phá huỷ khả năng chứng minh của cả người tốt.

**Hành vi bị cấm:**

```text
Người giữ tiền đồng thời là người xác nhận milestone
Founder tự đánh giá mức trọng yếu của thay đổi có lợi cho mình
Founder tự xác nhận đã phục hồi sau thất bại
Bên bị nghi ngờ tự điều tra chính mình
Một người vừa phê duyệt, chuyển tiền, ghi sổ và nghiệm thu
```

**Áp cho chính bộ máy này.** `LC-03` không chỉ áp cho người gây quỹ. Nó là nguồn của các cặp vai bị cấm trùng tại [[Vai trò và cặp vai bị cấm]] — người soạn luật không được kiểm hợp hiến chính luật mình soạn.

> [!warning] Điều này chưa có trong canon 12
> Đang nằm trong [[Custody và safeguarding]] mục 1 và [[Verification protocol và decision rule]] mục 10.

---

## LC-04 — Không hồi tố bất lợi, không hạ chuẩn sau kết quả

> **Không sửa tiêu chí sau khi đã biết kết quả để hợp thức hóa kết quả đó.**

**Vì sao tuyệt đối.** Nếu tiêu chí có thể đổi sau khi biết kết quả thì mọi cam kết trước đó chỉ là trang trí. Điều này phá huỷ giá trị của hiến chương, của luật, của tiền lệ và của mọi lời hứa với người góp cùng một lúc.

**Hành vi bị cấm:**

```text
Hạ ngưỡng milestone sau khi kiểm tra không đạt
Đổi protocol giữa lúc đang review để có kết quả thuận lợi
Công bố stretch goal sau khi tiền đã vượt mục tiêu
Chuyển all-or-nothing thành keep-it-all sau hạn mà không re-consent
Áp luật mới lên ca đã xử theo luật cũ, theo hướng bất lợi
Trình bằng chứng tạo sau hạn như bằng chứng ban đầu
```

**Điều được phép.** Sửa luật cho tương lai. Lật một tiền lệ có nêu lý do. Cả hai đều không hồi tố bất lợi.

> [!warning] Điều này chưa có trong canon 12
> Đang nằm trong [[Verification protocol và decision rule]] mục 9 và 11, và [[Material change, pivot and re-consent]] mục 16.

---

## LC-05 — Không xâm phạm phẩm giá để huy động

> **Không dùng xấu hổ, cưỡng ép hay phơi bày để tạo ra đóng góp.**

**Vì sao tuyệt đối.** Một hệ thống huy động được nhiều tiền bằng cách làm nhục người không góp hoặc bắt người thụ hưởng biểu diễn nỗi đau đã tự phản bội mục đích công ích mà nó viện dẫn. Không có con số nào bù lại được.

**Hành vi bị cấm:**

```text
Bảng xếp hạng số tiền làm chế độ mặc định
Giao diện gây cảm giác tội lỗi khi từ chối
Mặc định tick sẵn ô đóng góp
Buộc người thụ hưởng cung cấp hình ảnh hoặc dữ liệu cá nhân quá mức
Buộc thể hiện lòng biết ơn công khai như điều kiện nhận hỗ trợ
Công khai tên và số tiền mà không cho chọn
```

**Nguồn:** canon 5 — *Ghi nhận phải phục vụ phẩm giá, không phục vụ cưỡng chế*. Xem thêm tiên đề danh dự tự nguyện và tiên đề không biến quà thành nợ bí mật trong [[Khung thiết kê nền tảng cho gọi vốn cộng đồng]].

---

## LC-06 — Không lời hứa không thể phản bác

> **Tuyên bố nào không thể bị chứng minh sai thì không thể được công nhận là đạt.**

**Vì sao tuyệt đối.** Đây là điều kiện để toàn bộ tầng bằng chứng có nghĩa. Nếu chấp nhận một lời hứa không thể phản bác, hệ thống mất khả năng phân biệt dự án thành công với dự án chỉ kể chuyện hay.

**Hành vi bị cấm:**

```text
Milestone chỉ mô tả hoạt động: "tiếp tục phát triển", "đẩy mạnh truyền thông"
Chỉ tiêu không có đơn vị, cửa sổ thời gian hoặc cách xử lý dữ liệu thiếu
"Nâng cao nhận thức cộng đồng" làm tiêu chí nghiệm thu
Dùng hóa đơn để chứng minh tác động
Dùng một câu chuyện thành công để chứng minh tiền đã dùng đúng
```

**Hệ quả hai tầng bằng chứng.** `LC-06` buộc tách *proof of use* — tiền đã chi vào đâu — khỏi *proof of outcome* — việc chi đó tạo ra thay đổi gì. Xem [[Proof of use và proof of outcome]].

**Nguồn:** canon 3 — *Mọi lời hứa tác động phải có điều kiện phản bác*.

---

## Điều gì KHÔNG thuộc lõi cứng

Để tránh lạm phát lõi cứng, ghi rõ những thứ **không** ở đây dù rất quan trọng:

| Không phải lõi cứng | Vì sao |
|---|---|
| All-or-nothing | Phụ thuộc công nghệ sản xuất của dự án; keep-it-all đôi khi đúng hơn |
| Escrow bắt buộc | Là một phương án thực thi `LC-01`, không phải bản thân nguyên lý |
| Quadratic funding | Một cơ chế trong nhiều cơ chế |
| Ẩn danh tuyệt đối | Là quyền vòng ngoài, có thể cân bằng — xem `TL-001` |
| Công khai toàn bộ chứng từ | Va với bảo vệ dữ liệu người thụ hưởng |
| Bỏ phiếu toàn cộng đồng | Không phải mọi quyết định đều cần |

Mọi điều trong bảng trên đều thuộc tầng vòng ngoài hoặc tầng luật, và đều có thể bàn.

## Quy tắc sửa

| Hành động | Được phép | Điều kiện |
|---|---|---|
| Thêm một điều lõi cứng | Có | Ngưỡng đồng thuận rất cao + thời gian chờ |
| Làm rõ nội dung một điều | Có | Không được thu hẹp phạm vi trên thực tế |
| Thu hẹp hoặc bỏ một điều | **Không** | — |

Cơ chế bánh cóc một chiều này là thứ làm cho câu *"tiên đề không thể mặc cả"* có hiệu lực thật thay vì chỉ là một lời hứa.

## Liên kết

- [[Hiến chương - Bản đồ]]
- [[Tiên đề vòng ngoài]]
- [[Giao thức xử lý xung đột]]
- [[Vai trò và cặp vai bị cấm]]
- [[Custody và safeguarding]] — nguồn `LC-01`, `LC-03`
- [[Verification protocol và decision rule]] — nguồn `LC-04`
