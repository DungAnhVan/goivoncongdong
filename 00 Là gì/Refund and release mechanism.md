---
ai_authored: true
---

# Refund and release mechanism

> **Định nghĩa ngắn:** *Refund and release mechanism* là tập hợp quy tắc xác định khi nào tiền phải được hoàn, authorization phải bị hủy, pledge hoặc reservation phải được giải phóng và actor nhận lại quyền kiểm soát đối với phần nguồn lực chưa sử dụng.

Mảng này không chỉ nói về tiền. Trong mô hình của dự án, một cam kết có thể là tiền, giờ làm việc, thiết bị, địa điểm, dữ liệu hoặc quyền tiếp cận.

## 1. Refund khác release

```text
Tiền đã thu
→ refund

Authorization chưa capture
→ cancel authorization

Pledge chưa kích hoạt
→ cancel / expire pledge

Thiết bị hoặc venue đã reserve
→ release reservation

Giờ chuyên môn đã giữ lịch
→ release time commitment

Access right chưa dùng
→ revoke or close access
```

Nếu nguồn lực đã được dùng một phần, cần reconciliation và remedy, không thể chỉ `release` toàn bộ.

## 2. Các trigger thường gặp

- Không đạt provision point.
- Campaign bị hủy trước activation.
- Material change và actor không re-consent.
- Project termination.
- Contributor benefit không thể fulfil.
- Duplicate hoặc erroneous payment.
- Fraud/integrity finding.
- Resource không được accepted.
- Overpayment.
- Residual restricted balance phải hoàn.
- Legal hoặc payment requirement.

Trigger phải được viết trong [[Campaign charter]].

## 3. Refund types

### Automatic refund

Hệ thống tự hoàn khi event được xác nhận.

Ví dụ:

```text
AON campaign không đạt threshold
→ refund tự động
```

### Contributor-requested refund

Actor gửi yêu cầu trong cửa sổ được phép.

### Mandatory refund

Chiến dịch có nghĩa vụ hoàn dù actor chưa yêu cầu.

### Partial refund

Chỉ hoàn phần chưa sử dụng hoặc phần liên quan nghĩa vụ không fulfil.

### Pro-rata refund

Chia nguồn hoàn theo tỷ lệ đã công bố.

### Refund after deduction

Có thể trừ phí hoặc chi phí không thể đảo ngược nếu:

- Được công bố trước.
- Phù hợp restriction và pháp luật.
- Có cách tính rõ.
- Không chuyển rủi ro bất công sang contributor.

### Goodwill refund

Hoàn ngoài nghĩa vụ để xử lý tranh chấp hoặc bảo vệ uy tín. Không được ghi như refund bắt buộc nếu bản chất khác.

## 4. Release types

```text
Release pledge
Release payment authorization
Release equipment reservation
Release venue slot
Release labor schedule
Release matching commitment
Release data/access obligation
```

Mỗi loại cần một event và bằng chứng riêng.

## 5. Eligibility

Một refund/release rule phải trả lời:

```text
Ai đủ điều kiện?
Contribution nào đủ điều kiện?
Phần nào đã dùng?
Phần nào còn khả dụng?
Trigger đã được xác minh chưa?
Có deadline yêu cầu không?
Có conflict hoặc dispute không?
```

Không chỉ dựa vào số tiền actor từng chuyển.

## 6. Amount calculation

Ví dụ:

```text
Original contribution
- valid and accepted use
- non-refundable disclosed cost
+ vendor refund allocated back
± correction
= refundable amount
```

Không mặc định toàn bộ chi phí đã phát sinh đều được trừ. Khoản trừ phải đủ điều kiện, có bằng chứng và phù hợp charter.

## 7. Refund theo trạng thái tiền

```text
Pledged
→ chưa thu; cancel pledge

Authorized
→ cancel authorization

Held / safeguarded
→ release/refund theo rule

Disbursed but unused
→ recover then refund nếu khả thi

Spent on eligible purpose
→ thường không còn refundable toàn phần

Spent outside purpose
→ recovery/remedy process
```

Xem [[Custody và safeguarding]], [[Escrow]] và [[Disbursement]].

## 8. Non-financial resource release

### Time and labor

- Hủy lịch tương lai.
- Xác nhận giờ đã làm.
- Xử lý deliverable dở dang.
- Trả dữ liệu hoặc tài sản công việc.
- Giải quyết IP và bảo mật.

### Equipment

- Dừng sử dụng.
- Kiểm kê tình trạng.
- Hoàn trả.
- Xử lý hư hỏng.
- Giải phóng bảo hiểm hoặc deposit.

### Venue

- Hủy slot.
- Thanh toán cancellation fee nếu hợp lệ.
- Hoàn chìa khóa/quyền truy cập.

### Data

- Dừng xử lý.
- Thu hồi quyền truy cập.
- Return/delete theo consent và agreement.
- Giữ phần bắt buộc cho audit/legal retention nếu có căn cứ.

### Access/introduction

Không thể “thu hồi” một cuộc giới thiệu đã xảy ra, nhưng có thể đóng quyền tiếp cận tương lai và giới hạn tiếp tục sử dụng.

## 9. Already-used resources

Phải chia:

```text
Unused
Reserved but reversible
Partially used
Consumed
Irreversible
Converted into project asset
```

Refund/release khác nhau theo từng lớp.

Ví dụ:

```text
100 giờ pledged
60 giờ delivered
45 giờ accepted
15 giờ rejected
40 giờ chưa thực hiện
```

Không được nói `refund 40%` nếu bản chất là release 40 giờ và xử lý riêng 15 giờ rejected.

## 10. Fees

Cần công bố:

- Payment processing fee.
- Currency conversion.
- Platform fee.
- Escrow/custody fee.
- Bank charge.
- Cancellation cost.
- Tax treatment.

Phải nói rõ phí nào:

```text
refundable
non-refundable
borne by campaign
borne by contributor
deducted pro-rata
```

Không tạo surprise deduction sau failure.

## 11. Refund destination

Nguyên tắc ưu tiên:

```text
Return to original payment source
```

Ngoại lệ cần kiểm soát:

- Tài khoản đóng.
- Thẻ hết hạn.
- Người góp qua tổ chức.
- Người góp đã qua đời.
- Chuyển nhượng quyền.
- Sanction/KYC issue.

Không chuyển sang tài khoản khác chỉ dựa trên một email không xác minh.

## 12. Timing

Rule phải ghi:

```text
trigger confirmed at
refund initiated by
expected completion
maximum processing time
failed refund retry
unclaimed amount rule
```

`Sẽ hoàn sớm` không phải SLA.

## 13. Refund status model

```text
Not eligible
Eligible
Pending calculation
Approved
Initiated
Processing
Completed
Failed
Disputed
Unclaimed
```

Không coi `initiated` là hoàn tất.

## 14. Evidence

Mỗi refund/release event cần:

```text
refund_release_id:
actor_id:
contribution_id:
resource_type:
trigger:
eligibility_rule:
original_amount_or_quantity:
used_amount_or_quantity:
refundable_or_releasable:
deductions:
calculation:
approved_by:
initiated_at:
completed_at:
payment_or_release_reference:
status:
evidence_ids:
```

## 15. Dispute

Actor phải có route khi:

- Không được xác định eligible.
- Amount sai.
- Deduction sai.
- Refund thất bại.
- Dự án nói nguồn lực đã dùng nhưng không có proof.
- Equipment bị hỏng.
- Data không được xóa/return như cam kết.

Xem [[Stakeholder engagement và grievance mechanism]].

## 16. Refund không thay thế accountability

Hoàn tiền không tự động xóa:

- Gian lận.
- Vi phạm dữ liệu.
- Thiệt hại cho affected community.
- Nghĩa vụ báo cáo.
- Nghĩa vụ trả tài sản.
- Investigation.

`We refunded everyone` không phải kết luận rằng campaign được quản trị đúng.

## 17. Relation với AON/KIA

```text
[[All-or-nothing và keep-it-all]]
→ funding rule và phân bổ rủi ro

Refund and release mechanism
→ quy trình thực thi quyền hoàn/release
```

AON mà không có refund operation khả thi mới chỉ là lời hứa.

## 18. Refund waterfall khi tiền không đủ

Nếu số tiền còn lại thấp hơn nghĩa vụ refund, phải có rule và legal review.

Có thể cần xác định:

- Priority claims.
- Protected/client funds.
- Pro-rata treatment.
- Recovery từ vendor/founder.
- Insurance.
- Insolvency implications.

Không tự ý chia theo cảm tính.

## 19. Unclaimed refunds

Phải có rule cho:

- Actor không phản hồi.
- Tài khoản không nhận được.
- Số tiền rất nhỏ.
- Hết thời hạn claim.

Không mặc định chuyển unclaimed refund thành doanh thu nền tảng.

## 20. Checklist thiết kế

```text
[ ] Trigger rõ
[ ] Eligibility rõ
[ ] Calculation rõ
[ ] Fee treatment rõ
[ ] Payment destination control
[ ] Non-financial release rule
[ ] Partial-use rule
[ ] Timeline và status
[ ] Evidence và reconciliation
[ ] Failed/unclaimed rule
[ ] Dispute route
[ ] Public reporting
```

## 21. Kết luận

> **Refund trả lại tài sản đã chuyển; release trả lại quyền tự do đối với cam kết chưa sử dụng. Một chiến dịch nhiều nguồn lực phải thiết kế cả hai.**

## Khái niệm liên quan

- [[Campaign charter]]
- [[All-or-nothing và keep-it-all]]
- [[Assurance contract và conditional pledge]]
- [[Escrow]]
- [[Resource pledge lifecycle]]
- [[Residual funds and unused resources]]
- [[Campaign closure, wind-down and dissolution]]
