---
ai_authored: true
---

# Custody và safeguarding

> **Định nghĩa ngắn:** *Custody* là việc nắm giữ trực tiếp hoặc gián tiếp tài sản của người khác, hoặc có quyền tiếp cận và kiểm soát tài sản đó. *Safeguarding* là tập hợp cơ chế bảo vệ tiền hoặc tài sản được giao, đặc biệt bằng cách tách biệt, ghi nhận đúng và hạn chế việc sử dụng sai.

## 1. Điểm quan trọng nhất

> Người quyết định tiền nên được dùng vào việc gì không nhất thiết phải là người trực tiếp giữ tiền.

Đây là ranh giới nền tảng giữa:

```text
Governance
→ quyết định mục tiêu, điều kiện và phê duyệt

Custody
→ nắm giữ hoặc có khả năng tiếp cận tài sản

Payment execution
→ thực hiện lệnh chuyển tiền

Accounting
→ ghi nhận, đối soát và báo cáo
```

Nếu một người kiểm soát cả bốn mà không có kiểm tra độc lập, rủi ro sai sót, chiếm dụng hoặc che giấu tăng mạnh.

## 2. Custody là gì?

SEC mô tả custody trong bối cảnh tư vấn đầu tư là việc trực tiếp hoặc gián tiếp giữ tiền/chứng khoán của khách hàng, hoặc có quyền lấy quyền sở hữu chúng. Custody có thể xuất hiện khi một người:

- Trực tiếp giữ tiền hoặc tài sản.
- Có quyền rút tiền từ tài khoản.
- Có giấy ủy quyền đủ rộng.
- Giữ vị trí pháp lý cho phép tiếp cận tài sản của phương tiện đầu tư.
- Có khả năng chỉ thị cho bên lưu ký chuyển tài sản theo quyền riêng của mình.

Vì vậy, câu “tiền vẫn nằm trong ngân hàng nên nền tảng không giữ tiền” chưa đủ. Nếu nền tảng có toàn quyền ra lệnh rút hoặc chuyển, nó vẫn có quyền kiểm soát đáng kể.

## 3. Safeguarding là gì?

Safeguarding không chỉ là bảo mật mật khẩu ngân hàng. Nó gồm nhiều lớp:

```text
Tách biệt tài sản
+ xác định chủ sở hữu và quyền lợi
+ kiểm soát quyền truy cập
+ đối soát thường xuyên
+ xử lý thiếu hụt
+ lưu dấu vết giao dịch
+ kế hoạch khi bên giữ tiền thất bại
```

Trong FCA Handbook, tài khoản client money được nhận diện để phân biệt tiền của khách hàng với tiền của chính doanh nghiệp. Đây là ví dụ của nguyên tắc **segregation** — tách tiền được giao khỏi tài sản vận hành của tổ chức.

## 4. Segregation — tách biệt tiền

### Không tách biệt

```text
Tiền nền tảng
+ phí vận hành
+ tiền chiến dịch A
+ tiền chiến dịch B
→ cùng một tài khoản, cùng quyền truy cập
```

Hệ quả:

- Khó xác định tiền nào thuộc dự án nào.
- Dễ dùng nhầm tiền dự án cho chi phí vận hành.
- Khi tổ chức gặp nợ hoặc phá sản, quyền đối với tiền trở nên phức tạp.
- Đối soát và hoàn tiền khó thực hiện.

### Có tách biệt

```text
Tài khoản vận hành của nền tảng
≠ tài khoản giữ tiền chiến dịch
≠ sổ phụ của từng dự án
```

Tách biệt có thể tồn tại ở cấp tài khoản ngân hàng, tài khoản thanh toán, ledger nội bộ hoặc cấu trúc pháp lý. Tuy nhiên, chỉ ghi nhãn trong Excel mà tiền vẫn bị sử dụng tự do không phải safeguarding thực chất.

## 5. Custodian là gì?

[[Custodian]] là đơn vị có chức năng giữ và bảo vệ tài sản. Trong thị trường đầu tư, custodian thường là ngân hàng hoặc tổ chức có quyền thực hiện dịch vụ lưu ký phù hợp.

Custodian không nhất thiết:

- Chọn dự án.
- Quyết định đầu tư.
- Đánh giá tác động.
- Tự ý sử dụng tài sản.

Vai trò của họ chủ yếu là bảo quản, ghi nhận và thực hiện chỉ thị hợp lệ theo cấu trúc đã thống nhất.

## 6. Khác gì với escrow?

| Custody/safeguarding | [[Escrow]] |
|---|---|
| Khái niệm rộng về nắm giữ và bảo vệ tài sản | Cơ chế ba bên cho một giao dịch hoặc điều kiện cụ thể |
| Có thể kéo dài xuyên suốt vòng đời quỹ | Thường kết thúc khi điều kiện xảy ra hoặc giao dịch hủy |
| Nhấn mạnh tách biệt, quyền sở hữu, đối soát | Nhấn mạnh chỉ giải phóng tài sản khi đủ điều kiện |
| Có thể dùng cho nhiều khách hàng/dự án | Thường gắn với thỏa thuận escrow xác định |

Escrow là một phương án có thể hỗ trợ safeguarding, nhưng không thay thế toàn bộ hệ thống quản trị và kế toán.

## 7. Áp vào dự án Gọi vốn cộng đồng

Mỗi chiến dịch hoặc dự án phải mô tả được:

```text
Người góp chuyển tiền cho ai?
Tài khoản đứng tên pháp nhân nào?
Tiền được ghi nhận là tài sản của ai?
Tiền có bị trộn với tiền vận hành không?
Ai có quyền tạo lệnh thanh toán?
Ai duyệt lệnh?
Có cần hai người cùng chấp thuận không?
Ai đối soát ngân hàng với sổ dự án?
Điều gì xảy ra nếu chiến dịch không đạt ngưỡng?
Điều gì xảy ra nếu nền tảng ngừng hoạt động?
```

Nền tảng có thể chọn nhiều cấu trúc khác nhau theo từng giai đoạn:

- Tiền đi thẳng đến pháp nhân dự án.
- Đối tác thanh toán giữ tiền theo điều kiện.
- Tài khoản tách biệt có kiểm soát nhiều bên.
- Thanh toán trực tiếp cho nhà cung cấp thay vì chuyển vào tài khoản chủ dự án.
- Escrow cho các giao dịch cần xác nhận milestone.

Không có một cấu trúc phù hợp cho mọi loại crowdfunding.

## 8. Kiểm soát tối thiểu cho pilot

1. Không dùng tài khoản cá nhân không được công bố làm nơi gom tiền dài hạn.
2. Tách tiền dự án khỏi tiền vận hành.
3. Ghi rõ số dư của từng dự án.
4. Hai bước cho thanh toán trọng yếu: tạo lệnh và phê duyệt.
5. Lưu hóa đơn, hợp đồng, biên bản nghiệm thu hoặc bằng chứng tương ứng.
6. Đối soát định kỳ giữa ngân hàng, ledger và báo cáo dự án.
7. Công bố sai lệch trọng yếu cho người góp.
8. Có quy tắc hoàn tiền, tiền dư và tài khoản bị phong tỏa.
9. Không một người duy nhất vừa phê duyệt, chuyển tiền, ghi sổ và xác nhận hoàn thành.

## 9. Dấu hiệu cảnh báo

- “Cứ chuyển vào tài khoản này rồi tính sau.”
- Không ai biết tài khoản đứng tên ai.
- Số tiền trên trang dự án không khớp ngân hàng.
- Người giữ tiền cũng là người duy nhất xác nhận milestone.
- Có thể đổi mục tiêu sử dụng mà không cần phê duyệt.
- Tiền dự án được dùng tạm cho chi phí khác.
- Không có phương án khi nền tảng hoặc chủ dự án mất khả năng hoạt động.
- Báo cáo chỉ có ảnh chụp, không có ledger và chứng từ đối soát.

## 10. Kết luận cho dự án

> **Safeguarding bắt đầu bằng việc thừa nhận tiền của dự án không phải tiền tự do của người đang cầm tài khoản.**

Mục tiêu không chỉ là chống trộm. Nó phải bảo vệ người góp trước:

- Chiếm dụng.
- Dùng sai mục đích.
- Trộn lẫn tài sản.
- Sai sót kế toán.
- Phá sản hoặc ngừng hoạt động của trung gian.
- Quyền lực tập trung vào một người.

## Khái niệm liên quan

- [[Tài chính và quản lý quỹ - Bản đồ thuật ngữ]]
- [[Fund management]]
- [[Client money]]
- [[Segregated account]]
- [[Custodian]]
- [[Escrow]]
- [[Reconciliation]]
- [[Internal financial controls]]
- [[Audit trail]]

## Nguồn tham khảo

- SEC — Custody of client funds or securities: https://www.sec.gov/rules-regulations/2002/07/custody-funds-or-securities-clients-investment-advisers
- FCA Handbook — client money: https://handbook.fca.org.uk/glossary/G160
- FCA Handbook — client bank account: https://handbook.fca.org.uk/glossary/G159
- FCA Handbook — designated client bank account: https://handbook.fca.org.uk/glossary/G280
- FCA Handbook — custodian: https://handbook.fca.org.uk/glossary/G248
