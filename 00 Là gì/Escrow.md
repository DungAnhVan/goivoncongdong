# Escrow

> **Định nghĩa ngắn:** *Escrow* là một cơ chế trong đó tiền, tài sản hoặc tài liệu được một bên thứ ba giữ thay cho các bên trong giao dịch và chỉ được giải phóng khi các điều kiện đã thỏa thuận được đáp ứng hoặc khi có quy tắc xử lý khác.

Có thể dịch gần nghĩa là **ký quỹ có điều kiện**, **tài khoản trung gian có điều kiện** hoặc **cơ chế bên thứ ba giữ tài sản**. Không nên mặc định mọi tài khoản “giữ hộ” đều là escrow đúng nghĩa pháp lý.

## 1. Cấu trúc cơ bản

```text
Bên góp/chuyển tài sản
        ↓
Bên escrow giữ tài sản
        ↓ chỉ hành động theo thỏa thuận
Điều kiện đạt ─────────→ giải phóng cho bên nhận
Điều kiện không đạt ───→ hoàn lại hoặc xử lý theo quy tắc
```

Ba thành phần bắt buộc:

1. Tài sản được giữ.
2. Điều kiện giải phóng rõ ràng.
3. Bên giữ có nghĩa vụ hành động theo thỏa thuận, không theo ý riêng của một bên.

## 2. Escrow giải quyết vấn đề gì?

Hai bên có thể chưa đủ tin nhau:

```text
Người góp sợ chuyển tiền rồi dự án không làm
Chủ dự án sợ đã làm xong nhưng người mua không trả
```

Escrow thay đổi cấu trúc:

```text
Người góp chứng minh khả năng thanh toán bằng cách nạp tiền
→ chủ dự án thực hiện điều kiện
→ bên trung gian kiểm tra hoặc nhận chỉ thị hợp lệ
→ tiền được giải phóng
```

Nó giảm rủi ro một bên phải thực hiện toàn bộ trước khi bên còn lại có cam kết đáng tin.

## 3. Escrow account và escrow agreement

### Escrow account

Tài khoản dùng để giữ tiền cho mục đích escrow. HMRC mô tả escrow account là tài khoản do bên thứ ba giữ thay cho beneficial owner của tiền.

### Escrow agreement

Thỏa thuận xác định:

- Các bên.
- Tài sản.
- Chủ sở hữu hưởng lợi.
- Điều kiện giải phóng.
- Bằng chứng được chấp nhận.
- Phí.
- Thời hạn.
- Quy trình tranh chấp.
- Hoàn tiền.
- Trường hợp bất khả kháng.
- Trách nhiệm của escrow agent.

Chỉ có tài khoản mà không có quy tắc rõ thì chưa giải quyết được tranh chấp “điều kiện đã đạt hay chưa”.

## 4. Khác gì với tài khoản tách biệt?

| [[Segregated account]] | Escrow |
|---|---|
| Tách tiền khỏi tài sản khác | Giữ tiền cho đến khi điều kiện xảy ra |
| Trọng tâm là phân biệt quyền sở hữu và bảo vệ tiền | Trọng tâm là thực thi điều kiện giao dịch |
| Không nhất thiết có ba bên | Thường có bên gửi, bên nhận và escrow agent |
| Có thể tồn tại lâu dài | Thường kết thúc theo giao dịch hoặc milestone |

Một escrow account nên được tách biệt, nhưng một tài khoản tách biệt không mặc nhiên là escrow.

## 5. Khác gì với milestone-based disbursement?

[[Milestone-based disbursement]] là logic giải ngân theo mốc. Escrow là một cấu trúc có thể dùng để thực hiện logic đó.

```text
Milestone-based disbursement
→ quy tắc: đạt mốc thì được nhận tiền

Escrow
→ cơ chế: bên thứ ba đang giữ tiền và thực hiện quy tắc
```

Nền tảng có thể theo dõi milestone nhưng để ngân hàng, cổng thanh toán hoặc đối tác phù hợp giữ và giải phóng tiền.

## 6. Các mô hình dùng escrow trong dự án

### All-or-nothing campaign

```text
Người góp cam kết/nạp tiền
→ đủ ngưỡng trước thời hạn: giải phóng
→ không đủ ngưỡng: hoàn tiền hoặc không thu
```

### Pre-order

```text
Người mua trả tiền
→ dự án chứng minh sản xuất/giao hàng theo điều kiện
→ tiền được giải phóng
```

### Mua thiết bị

```text
Quỹ đặt tiền vào escrow
→ nhà cung cấp giao thiết bị
→ nghiệm thu
→ thanh toán
```

### Dự án nhiều milestone

Tiền có thể được giải phóng từng phần, nhưng thỏa thuận phải định nghĩa rõ mỗi phần.

## 7. Ai xác nhận điều kiện?

Có nhiều phương án:

- Hai bên cùng xác nhận.
- Một bên xác nhận sau thời hạn phản đối.
- Chuyên gia/đơn vị nghiệm thu độc lập.
- Dữ liệu tự động từ hệ thống.
- Hội đồng dự án.
- Phán quyết theo quy trình tranh chấp.

Escrow agent không nên bị buộc tự đánh giá chuyên môn phức tạp nếu thỏa thuận chỉ cho họ chức năng giữ tiền. Điều kiện cần đủ khách quan để bên giữ có thể thực hiện.

## 8. Điều khoản cần đặc biệt rõ

```text
Điều kiện đạt là gì?
Ai cung cấp bằng chứng?
Ai có quyền phản đối?
Thời hạn phản đối bao lâu?
Nếu hoàn thành một phần thì sao?
Nếu chi phí tăng thì sao?
Nếu hai bên bất đồng thì ai quyết định?
Phí escrow lấy từ đâu?
Lãi phát sinh thuộc về ai?
Nếu escrow agent ngừng hoạt động thì sao?
Hoàn tiền bằng cách nào và trong bao lâu?
```

## 9. Escrow không tự động tạo an toàn tuyệt đối

Rủi ro vẫn tồn tại:

- Escrow agent giả mạo.
- Điều kiện viết mơ hồ.
- Bằng chứng milestone bị làm giả.
- Bên giữ tiền không được phép cung cấp dịch vụ tương ứng.
- Phí và thời gian tranh chấp cao.
- Tiền bị đóng băng dù dự án cần vốn lưu động.
- Một bên có quyền xác nhận quá lớn.
- Người dùng hiểu nhầm escrow là bảo đảm dự án thành công.

Escrow bảo vệ **điều kiện chuyển tiền**, không bảo đảm sản phẩm tốt, dự án có lợi nhuận hay không có gian lận ở các tầng khác.

## 10. Áp vào dự án Gọi vốn cộng đồng

Nền tảng chưa nhất thiết phải tự làm escrow agent. Hướng hợp lý hơn là:

```text
Nền tảng
→ chuẩn hóa điều kiện và milestone
→ lưu bằng chứng và luồng phê duyệt
→ gửi chỉ thị hợp lệ

Đối tác giữ tiền phù hợp
→ nhận/giữ tài sản
→ giải phóng hoặc hoàn lại theo thỏa thuận
```

Tài sản chiến lược của nền tảng nằm ở:

- Định nghĩa milestone.
- Hồ sơ bằng chứng.
- Quy trình phê duyệt.
- Lịch sử thay đổi.
- Giao diện minh bạch cho cộng đồng.

Không nhất thiết nằm ở việc tự mình cầm tiền.

## 11. Checklist đánh giá một phương án escrow

1. Pháp nhân cung cấp là ai?
2. Họ có quyền và năng lực giữ loại tiền/tài sản đó không?
3. Tài khoản có tách biệt không?
4. Ai là beneficial owner trong từng giai đoạn?
5. Điều kiện giải phóng có khách quan không?
6. Ai xử lý tranh chấp?
7. Có giới hạn thời gian không?
8. Phí và thuế ra sao?
9. Hoàn tiền có tự động không?
10. Dữ liệu giữa nền tảng và escrow agent được đối soát thế nào?
11. Có kế hoạch khi bên giữ tiền thất bại không?

## 12. Kết luận cho dự án

> **Escrow không thay thế niềm tin; nó biến một phần niềm tin thành điều kiện có thể thực thi.**

Trong mô hình của dự án, escrow phù hợp nhất khi:

- Tiền đã sẵn sàng nhưng chưa nên thuộc quyền sử dụng tự do của chủ dự án.
- Milestone đủ rõ để xác nhận.
- Có bên thứ ba đủ năng lực giữ và giải phóng tài sản.
- Quy tắc hoàn tiền và tranh chấp được công bố trước.

## Khái niệm liên quan

- [[Tài chính và quản lý quỹ - Bản đồ thuật ngữ]]
- [[Custody và safeguarding]]
- [[Segregated account]]
- [[Beneficial owner]]
- [[Disbursement]]
- [[Milestone-based disbursement]]
- [[Reconciliation]]
- [[Payment service provider]]

## Nguồn tham khảo

- HMRC — Escrow Accounts: https://www.gov.uk/hmrc-internal-manuals/international-exchange-of-information/ieim401860
- CFPB Regulation X — Escrow accounts and definitions: https://www.consumerfinance.gov/rules-policy/regulations/1024/17/
- CFPB — What is an escrow or impound account?: https://www.consumerfinance.gov/ask-cfpb/what-is-an-escrow-or-impound-account-en-140/
