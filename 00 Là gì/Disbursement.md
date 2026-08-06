# Disbursement

> **Định nghĩa ngắn:** *Disbursement* là việc giải ngân — đưa tiền đã được cam kết hoặc phê duyệt ra khỏi nơi đang giữ để thanh toán cho chủ dự án, nhà cung cấp, người thụ hưởng hoặc một bên đủ điều kiện.

Giải ngân không đồng nghĩa với huy động thành công. Nó là một bước riêng, xảy ra sau khi tiền đã được tiếp nhận và các điều kiện cần thiết đã được kiểm tra.

## 1. Dòng cơ bản

```text
Cam kết hoặc huy động
→ tiền được nhận/giữ
→ kiểm tra điều kiện
→ phê duyệt giải ngân
→ thực hiện thanh toán
→ xác nhận người nhận
→ đối soát
→ báo cáo sử dụng
```

Mỗi mũi tên là một điểm kiểm soát. Bỏ qua các bước giữa khiến “đạt mục tiêu gọi vốn” biến thành “chuyển toàn bộ tiền ngay”, dù dự án chưa đủ khả năng thực hiện.

## 2. Giải ngân khác thanh toán thế nào?

- **Disbursement** nhấn mạnh việc phát hành nguồn tiền từ quỹ/chương trình theo quyền và điều kiện.
- **Payment** là giao dịch thanh toán cụ thể.
- Một quyết định giải ngân có thể tạo nhiều lần thanh toán.
- Một lần thanh toán chỉ hợp lệ nếu nằm trong khoản giải ngân đã được phê duyệt.

Ví dụ:

```text
Phê duyệt giải ngân 300 triệu cho milestone sản xuất thử
→ 120 triệu trả nhà cung cấp vật liệu
→ 80 triệu trả gia công
→ 50 triệu kiểm định
→ 50 triệu giữ lại đến nghiệm thu
```

## 3. Các mô hình giải ngân

### Giải ngân toàn bộ một lần

Toàn bộ số tiền được chuyển khi chiến dịch thành công.

Phù hợp hơn khi:

- Giá trị nhỏ.
- Đầu ra đơn giản.
- Người nhận có lịch sử tin cậy.
- Cần thanh toán một khoản duy nhất.

Rủi ro cao khi dự án dài, nhiều bước hoặc chưa có năng lực vận hành.

### Milestone-based disbursement

[[Milestone-based disbursement]] là giải ngân theo từng mốc đã xác định.

```text
Mốc 1 đạt
→ giải ngân phần 1
→ tạo đầu ra và bằng chứng
→ [[Milestone verification|kiểm chứng mốc]]
→ mốc 2 được mở
```

Ưu điểm:

- Giới hạn tổn thất nếu dự án thất bại sớm.
- Buộc kế hoạch thành các đầu ra kiểm chứng được.
- Tạo dữ liệu uy tín theo thời gian.

Nhược điểm:

- Tăng chi phí giám sát.
- Dễ làm dự án thiếu vốn lưu động nếu milestone thiết kế quá cứng.
- Có thể phát sinh tranh chấp về việc “đã hoàn thành” hay chưa.

### Reimbursement

Chủ dự án chi trước, sau đó được hoàn lại khi cung cấp chứng từ và chứng minh khoản chi đủ điều kiện.

Ưu điểm: giảm nguy cơ chi sai trước khi kiểm tra.

Nhược điểm: loại trừ nhóm không có vốn ứng trước; có thể đi ngược mục tiêu hỗ trợ người yếu nguồn lực.

### Direct-to-vendor payment

Quỹ trả trực tiếp cho nhà cung cấp.

Phù hợp khi:

- Mua thiết bị.
- Thanh toán nhà thầu.
- Cần giảm nguy cơ tiền bị chuyển sang mục đích khác.

Nhưng vẫn phải kiểm tra nhà cung cấp, hợp đồng, chất lượng và xung đột lợi ích.

### Tranche / đợt giải ngân

Tiền được chia thành nhiều đợt theo thời gian, kế hoạch hoặc điều kiện. *Tranche* không nhất thiết là milestone; có thể đơn giản là lịch quý/tháng.

## 4. Điều kiện giải ngân

Một disbursement package có thể yêu cầu:

- Quyết định phê duyệt.
- Ngân sách còn đủ.
- Khoản chi thuộc [[Restricted funds|mục đích được phép]].
- Hợp đồng hoặc đơn đặt hàng.
- Hóa đơn/chứng từ.
- [[Milestone verification|Kết quả kiểm chứng milestone]].
- Kiểm tra KYC của người nhận.
- Tài khoản ngân hàng đã xác minh.
- Không có xung đột lợi ích chưa xử lý.
- Báo cáo kỳ trước đã nộp.
- Phần vốn đối ứng đã được đóng góp.

Không phải mọi dự án đều cần tất cả, nhưng checklist phải được xác định trước bằng [[Verification protocol và decision rule|protocol và decision rule]] phù hợp.

## 5. Milestone tốt là gì?

Milestone không nên chỉ là hoạt động:

```text
“Bắt đầu nghiên cứu”
“Tiến hành truyền thông”
“Tiếp tục phát triển”
```

Milestone tốt cần:

- Đầu ra cụ thể.
- Tiêu chí chấp nhận.
- Thời hạn.
- Người xác nhận.
- Bằng chứng.
- Ngân sách liên quan.
- Quy tắc khi chỉ hoàn thành một phần.

Ví dụ:

```text
Mốc: hoàn thành 20 sản phẩm thử
Tiêu chí: đúng bản vẽ phiên bản V3, kiểm tra 5 kích thước trọng yếu,
ít nhất 18/20 sản phẩm đạt
Bằng chứng: biên bản kiểm tra, ảnh lô hàng, hóa đơn gia công
Người xác nhận: kỹ thuật độc lập + đại diện dự án
Giải ngân tiếp: 35% ngân sách
```

Cách thiết kế đầy đủ nằm tại [[Milestone verification]].

## 6. Holdback và retention

Một phần tiền có thể được giữ lại đến khi:

- Nghiệm thu cuối.
- Hết thời gian bảo hành ban đầu.
- Hoàn thành báo cáo.
- Khắc phục lỗi.

Khoản giữ lại giúp tạo động lực hoàn tất nghĩa vụ, nhưng không nên lớn đến mức khiến bên thực hiện không đủ vốn hoàn thành.

## 7. Phân quyền giải ngân

```text
Người đề nghị chi
→ người kiểm tra hồ sơ
→ người phê duyệt
→ người thực hiện lệnh
→ người đối soát
```

Các ngưỡng có thể khác nhau:

| Giá trị | Quyền phê duyệt gợi ý |
|---:|---|
| Nhỏ | Một người có thẩm quyền + kiểm tra sau |
| Trung bình | Hai người phê duyệt |
| Lớn/trọng yếu | Hội đồng hoặc biên bản quyết định |
| Bên liên quan | Công bố xung đột + người độc lập phê duyệt |

Con số cụ thể phải tùy quy mô và cấu trúc pháp lý.

## 8. Áp vào nền tảng Gọi vốn cộng đồng

Mỗi lần giải ngân nên tạo một bản ghi:

```text
disbursement_id:
project_id:
fund_id:
amount:
currency:
payee:
purpose:
budget_line:
restriction_check:
milestone:
evidence_ids:
verification_id:
decision_rule_id:
requested_by:
reviewed_by:
approved_by:
executed_by:
payment_reference:
reconciled_by:
status:
```

Bằng chứng phải được đăng ký trong [[Evidence ledger và provenance]] thay vì chỉ đính kèm một folder không có chỉ mục.

Trạng thái có thể gồm:

```text
Draft
→ Submitted
→ Under review
→ Approved
→ Payment initiated
→ Paid
→ Reconciled
→ Reported
```

Không nên coi `Paid` là trạng thái cuối. Phải có `Reconciled`, [[Proof of use và proof of outcome|proof of use]] và bằng chứng kết quả phù hợp với giai đoạn.

## 9. Xử lý sai lệch

Nếu milestone chậm hoặc ngân sách thay đổi:

- Tạm dừng đợt tiếp theo.
- Yêu cầu kế hoạch khắc phục.
- Phê duyệt variation có ghi dấu vết.
- Giảm hoặc chia nhỏ giải ngân.
- Thanh toán trực tiếp cho nhà cung cấp.
- Kết thúc dự án và xử lý số dư.
- Công bố thay đổi trọng yếu cho người góp.

Mục tiêu không phải phạt mọi thất bại. Mục tiêu là không để thay đổi âm thầm biến lời hứa ban đầu thành dự án khác.

## 10. Dấu hiệu cảnh báo

- Giải ngân toàn bộ chỉ dựa trên số lượt ủng hộ.
- Milestone không có tiêu chí kiểm tra.
- Người xác nhận milestone là người trực tiếp nhận tiền.
- Tài khoản nhận thay đổi nhưng không xác minh lại.
- Chia nhỏ giao dịch để né ngưỡng phê duyệt.
- Hóa đơn có nhưng không chứng minh đầu ra.
- Khoản chi đúng ngân sách nhưng sai restriction.
- Không đối soát sau thanh toán.
- Claim được gắn `verified` nhưng không rõ phạm vi hoặc evidence IDs.

## 11. Kết luận cho dự án

> **Giải ngân là việc chuyển một lời hứa có điều kiện thành tiền có thể sử dụng.**

Thiết kế giải ngân tốt phải cân bằng:

- Bảo vệ người góp.
- Không bóp nghẹt vốn lưu động của chủ dự án.
- Giảm gian lận và sai mục đích.
- Cho phép thay đổi hợp lý nhưng có phê duyệt.
- Tạo bằng chứng để dự án xây uy tín cho vòng sau.

Lớp [[Bằng chứng và kiểm chứng - Bản đồ thuật ngữ|bằng chứng và kiểm chứng]] bảo đảm quyết định giải ngân không chỉ dựa vào tài liệu được nộp, mà dựa vào claim, provenance, protocol và kết quả kiểm tra có dấu vết.

## Khái niệm liên quan

- [[Tài chính và quản lý quỹ - Bản đồ thuật ngữ]]
- [[Bằng chứng và kiểm chứng - Bản đồ thuật ngữ]]
- [[Fund management]]
- [[Restricted funds]]
- [[Custody và safeguarding]]
- [[Milestone-based disbursement]]
- [[Milestone verification]]
- [[Evidence ledger và provenance]]
- [[Verification protocol và decision rule]]
- [[Proof of use và proof of outcome]]
- [[Eligible expenditure]]
- [[Payment approval]]
- [[Reconciliation]]
- [[Audit trail]]
- [[Working capital]]

## Nguồn tham khảo

- Charity Commission — internal financial controls: https://www.gov.uk/government/publications/internal-financial-controls-for-charities-cc8/internal-financial-controls-for-charities
- SEC — custody of client funds or securities: https://www.sec.gov/rules-regulations/2002/07/custody-funds-or-securities-clients-investment-advisers
- World Bank — Program-for-Results Financing: https://www.worldbank.org/en/programs/program-for-results-financing
