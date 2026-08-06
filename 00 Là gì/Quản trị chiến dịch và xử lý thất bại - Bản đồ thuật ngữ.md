# Quản trị chiến dịch và xử lý thất bại — Bản đồ thuật ngữ

> **Định nghĩa làm việc của dự án:** *Quản trị chiến dịch và xử lý thất bại* là tập hợp quy tắc xác định chiến dịch được phép làm gì, ai có quyền thay đổi lời hứa, thay đổi nào cần hỏi lại người tham gia, cách xử lý thất bại, hoàn trả, nguồn lực còn dư và cách đóng chiến dịch có trật tự.

Mảng này trả lời câu hỏi mà một trang gọi vốn thường né tránh:

> Nếu kế hoạch thay đổi, nguồn lực không còn đủ, mục tiêu không thể hoàn thành hoặc chiến dịch phải dừng, ai có quyền quyết định và các nghĩa vụ được xử lý thế nào?

## 1. Kiến trúc của mảng

```text
[[Campaign charter]]
→ hiến chương gốc xác định mục đích, phạm vi, quyền và quy tắc của chiến dịch

[[Commitment versioning and amendment]]
→ quản lý phiên bản và sửa đổi lời hứa mà không ghi đè lịch sử

[[Material change, pivot and re-consent]]
→ phân loại thay đổi, pivot và trường hợp phải hỏi lại người tham gia

[[Campaign failure, recovery and termination]]
→ phân loại thất bại, chọn phục hồi, chuyển giao hoặc chấm dứt

[[Refund and release mechanism]]
→ hoàn tiền hoặc giải phóng các cam kết chưa sử dụng

[[Residual funds and unused resources]]
→ xử lý tiền, tài sản và quyền còn lại sau thực hiện

[[Campaign closure, wind-down and dissolution]]
→ đóng chiến dịch, xử lý nghĩa vụ và lưu hồ sơ
```

Các node trên có thể cùng xuất hiện trong một sự kiện, nhưng không dùng thay thế nhau.

## 2. Chuỗi vòng đời

```text
Draft charter
→ Approve charter
→ Open campaign
→ Receive commitments
→ Reach provision point
→ Activate
→ Execute and disburse
→ Detect variance or change
→ Approve minor variation / request re-consent / pause
→ Recover, transfer or terminate
→ Refund and release
→ Handle residual resources
→ Close and archive
```

Một chiến dịch đáng tin phải thiết kế cả hai nhánh:

```text
Success path
Failure path
```

Không chỉ mô tả dự án sẽ làm gì khi mọi thứ thuận lợi.

## 3. Ranh giới với các mảng đã có

| Khái niệm | Câu hỏi chính |
|---|---|
| [[Cơ chế phối hợp tập thể - Bản đồ thuật ngữ]] | Làm sao các cam kết rời rạc vượt qua ngưỡng tập thể? |
| [[Campaign charter]] | Chiến dịch được phép làm gì và ai có quyền quyết định? |
| [[Restricted funds]] | Tiền hoặc tài sản bị ràng buộc vào mục đích nào? |
| [[Commitment versioning and amendment]] | Nội dung lời hứa hiện ở phiên bản nào? |
| [[Material change, pivot and re-consent]] | Thay đổi nào cần công bố, phê duyệt hoặc hỏi lại? |
| [[Disbursement]] | Khi nào nguồn tiền được chuyển ra? |
| [[Milestone verification]] | Mốc thực hiện đã đạt theo tiêu chí chưa? |
| [[Refund and release mechanism]] | Khi nào tài sản phải quay lại hoặc reservation được giải phóng? |
| [[Residual funds and unused resources]] | Phần còn lại sau thực hiện đi đâu? |
| [[Campaign failure, recovery and termination]] | Dự án phục hồi, chuyển giao hay dừng? |
| [[Campaign closure, wind-down and dissolution]] | Các nghĩa vụ được đóng và lưu hồ sơ thế nào? |

## 4. Ba tầng quản trị phải tách

```text
Normal operations
→ quyết định trong phạm vi charter đã phê duyệt

Change control
→ xử lý sai lệch hoặc sửa đổi nhưng chiến dịch vẫn tiếp tục

Failure and closure governance
→ phục hồi, chấm dứt, hoàn trả và đóng nghĩa vụ
```

Không nên dùng một quyền phê duyệt cho cả ba tầng.

Ví dụ:

```text
Project lead
→ có thể điều chỉnh lịch trong biên độ nhỏ

Campaign governance body
→ phê duyệt thay đổi trọng yếu

Independent reviewer / designated authority
→ xác nhận điều kiện refund, termination hoặc xử lý xung đột
```

## 5. Campaign charter là nguồn quy tắc gốc

Charter tối thiểu phải xác định:

```text
purpose
scope
beneficiary groups
provision point
eligible commitments
use of funds
milestones
roles and authorities
change thresholds
re-consent rule
refund and release rule
residual resource rule
failure and recovery rule
closure rule
record-retention rule
```

Trang truyền thông có thể tóm tắt charter, nhưng không được thay thế charter.

## 6. Thay đổi phải được phân loại

```text
Editorial correction
→ không đổi quyền hoặc nghĩa vụ

Minor operational change
→ nằm trong biên độ charter cho phép

Material change
→ có thể làm một người hợp lý thay đổi quyết định tham gia

Prohibited change
→ biến chiến dịch thành mục đích khác; phải đóng và tạo campaign mới
```

Không dùng chữ `pivot` để tránh gọi đúng tên một thay đổi mục đích.

## 7. Re-consent không chỉ là thông báo

```text
Notification
→ actor được biết thay đổi

Consultation
→ actor được góp ý nhưng chưa chắc có quyền từ chối

Re-consent
→ actor phải chấp thuận lại để cam kết tiếp tục bị ràng buộc

Withdrawal right
→ actor có thể rút trong cửa sổ xác định
```

Một banner “chúng tôi đã cập nhật kế hoạch” không mặc nhiên là re-consent.

## 8. Thất bại cần được phân loại

```text
Funding failure
Execution delay
Partial performance
Quality failure
Resource failure
Governance failure
Compliance failure
Purpose failure
Integrity failure
External shock
```

Mỗi loại có response khác nhau:

```text
Continue with monitoring
Pause
Corrective action
Re-scope
Replace actor
Re-consent
Transfer
Partial fulfilment
Refund
Termination
Wind-down
```

Không phải mọi thất bại đều do gian lận. Nhưng cũng không được gọi gian lận là “khó khăn vận hành”.

## 9. Refund khác release

```text
Tiền đã thu
→ refund

Payment authorization chưa capture
→ cancel authorization

Giờ hoặc thiết bị đã giữ lịch
→ release reservation

Pledge chưa kích hoạt
→ expire / cancel pledge

Nguồn lực đã dùng một phần
→ reconciliation + partial remedy
```

Một refund policy chỉ nói về tiền là chưa đủ với mô hình huy động nhiều loại nguồn lực.

## 10. Phần dư không đồng nghĩa tiền tự do

Phải phân biệt:

```text
Overfunding
Budget saving
Unused contingency
Unspent restricted balance
Vendor refund
Residual asset
Unused data/access right
Unfulfilled contributor benefit
```

Mỗi loại có quyền sở hữu, restriction và phương án xử lý khác nhau.

## 11. Closure khác dissolution

```text
Campaign closure
→ ngừng nhận cam kết mới

Campaign completion
→ hoàn thành mục tiêu và nghĩa vụ

Campaign wind-down
→ đóng dần hoạt động và xử lý nghĩa vụ còn lại

Project termination
→ dừng dự án trước khi hoàn thành

Legal entity dissolution
→ giải thể pháp nhân
```

Không dùng `dissolution` cho việc đơn giản là đóng một campaign page.

## 12. Ma trận sự kiện → quyết định

| Sự kiện | Quyết định đầu tiên | Cơ chế liên quan |
|---|---|---|
| Không đạt provision point | Không kích hoạt hoặc release | [[All-or-nothing và keep-it-all]], [[Refund and release mechanism]] |
| Mất nguồn lực blocking sau activation | Pause và đánh giá recovery | [[Campaign failure, recovery and termination]] |
| Đổi nhóm hưởng lợi | Material change review | [[Material change, pivot and re-consent]] |
| Giảm output nhưng vẫn làm được partial scope | Amendment + re-consent tùy mức | [[Commitment versioning and amendment]] |
| Dư ngân sách sau hoàn thành | Xác định restriction và residual rule | [[Residual funds and unused resources]] |
| Integrity concern | Freeze, preserve evidence, independent review | [[Evidence ledger và provenance]] |
| Dự án phải dừng | Termination decision + wind-down plan | [[Campaign closure, wind-down and dissolution]] |

## 13. Hồ sơ quản trị tối thiểu

```text
campaign_id:
charter_version:
current_purpose:
current_scope:
current_status:
governance_roles:
change_thresholds:
active_amendments:
material_change_events:
reconsent_status:
failure_classification:
recovery_plan:
termination_decision:
refund_obligations:
residual_resource_register:
closure_status:
archive_location:
evidence_ids:
```

## 14. Quy tắc chống “múa quản trị”

Không được nói chiến dịch có quản trị tốt nếu chưa trả lời được:

1. Charter phiên bản hiện tại là gì?
2. Ai có quyền sửa phần nào?
3. Thay đổi nào cần công bố?
4. Khi nào cần re-consent?
5. Ai xác định chiến dịch đã thất bại?
6. Nguồn lực nào được hoàn hoặc release?
7. Phần còn lại đi đâu?
8. Ai phê duyệt closure?
9. Hồ sơ nào phải giữ lại?
10. Người tham gia khiếu nại ở đâu?

## 15. Áp vào pilot

Pilot đầu tiên nên có một charter ngắn nhưng đầy đủ:

```text
Purpose:
Chạy thử một dịch vụ cho 50 người dùng xác minh.

Provision point:
100 triệu + 120 giờ kỹ thuật + venue 4 tuần.

Change tolerance:
±10% ngân sách từng dòng; tối đa 30 ngày trễ.

Material changes:
Đổi target group, giảm output >20%, đổi use of funds >15%, mất technical lead.

Re-consent:
7 ngày; actor không đồng ý được rút phần chưa sử dụng theo rule.

Failure rule:
Pause 14 ngày để corrective action; sau đó transfer hoặc terminate.

Residual rule:
Restricted balance hoàn hoặc chuyển theo lựa chọn đã công bố.

Closure:
Final report + reconciliation + evidence archive.
```

## 16. Kết luận cho dự án

> **Một chiến dịch đáng tin không chỉ công bố cách nó sẽ thành công; nó phải công bố trước ai có quyền thay đổi lời hứa, chuyện gì xảy ra khi thất bại và cách mọi nghĩa vụ được đóng lại.**

## Khái niệm liên quan

- [[Campaign charter]]
- [[Commitment versioning and amendment]]
- [[Material change, pivot and re-consent]]
- [[Campaign failure, recovery and termination]]
- [[Refund and release mechanism]]
- [[Residual funds and unused resources]]
- [[Campaign closure, wind-down and dissolution]]
- [[Restricted funds]]
- [[Disbursement]]
- [[Resource pledge lifecycle]]
- [[Evidence ledger và provenance]]
- [[Stakeholder engagement và grievance mechanism]]
