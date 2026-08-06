# Commitment versioning and amendment

> **Định nghĩa ngắn:** *Commitment versioning and amendment* là cơ chế quản lý lịch sử của một lời hứa hoặc nghĩa vụ: phiên bản nào đang có hiệu lực, nội dung nào đã thay đổi, ai phê duyệt, ai bị ảnh hưởng và có cần thông báo, re-consent hoặc quyền rút hay không.

Node này không hỏi nguồn lực đang ở trạng thái nào. Nó hỏi:

> Nội dung cam kết hiện tại là gì, khác phiên bản trước ở đâu và việc thay đổi có hợp lệ không?

## 1. Ranh giới với lifecycle

```text
[[Resource pledge lifecycle]]
→ Offered, Reserved, Delivered, Accepted hay Released?

Commitment versioning
→ cam kết ở phiên bản nào và nội dung nghĩa vụ đã đổi ra sao?
```

Một pledge có thể vẫn ở trạng thái `Reserved` nhưng nội dung bị sửa từ 100 giờ xuống 60 giờ. Lifecycle không đủ để mô tả thay đổi đó.

## 2. Những đối tượng cần versioning

Không chỉ pledge của contributor. Ít nhất gồm:

```text
Campaign charter
Purpose and scope
Use of funds
Provision point
Milestone and acceptance criteria
Contributor pledge
Matching commitment
Reward or contributor benefit
Delivery schedule
Refund rule
Residual resource rule
Governance role
Risk disclosure
```

Mỗi loại có mức độ sửa đổi cho phép khác nhau.

## 3. Không ghi đè lịch sử

Không nên:

```text
Version 1: giao sản phẩm tháng 10
→ sửa trực tiếp thành tháng 12
→ không còn dấu vết
```

Nên:

```text
V1 — giao tháng 10
V2 — đề xuất giao tháng 12
Reason — mất nhà cung cấp chính
Approved by — governance body
Effective after — notification/re-consent rule
V1 status — Superseded
```

Người tham gia phải xem được nội dung họ đã đồng ý tại thời điểm cam kết.

## 4. Version khác amendment event

```text
Version
→ trạng thái nội dung tại một thời điểm

Amendment event
→ hành động sửa đổi tạo ra phiên bản mới
```

Một amendment event phải lưu:

- Ai đề xuất.
- Lý do.
- Trường nào đổi.
- Tác động.
- Cơ sở phê duyệt.
- Thời điểm có hiệu lực.
- Re-consent hoặc withdrawal window.

## 5. Các loại thay đổi

### Editorial correction

Sửa lỗi chính tả, định dạng hoặc liên kết mà không đổi nghĩa.

### Clarification

Làm rõ nội dung vốn đã có nhưng không mở rộng nghĩa vụ hoặc giảm quyền.

### Administrative update

Thay thông tin liên hệ, người phụ trách hoặc chi tiết vận hành không trọng yếu.

### Operational amendment

Điều chỉnh lịch, ngân sách hoặc execution plan trong biên độ charter cho phép.

### Material amendment

Thay đổi có thể làm một người hợp lý thay đổi quyết định tham gia.

### Replacement / novation-like change

Thay chủ thể thực hiện, người nhận nghĩa vụ hoặc cấu trúc quan hệ. Dạng này cần đánh giá pháp lý riêng, không chỉ versioning kỹ thuật.

## 6. Semantic versioning làm việc

Dự án có thể dùng quy ước:

```text
MAJOR.MINOR.PATCH
```

Ví dụ:

```text
1.0.0
→ charter đầu tiên có hiệu lực

1.0.1
→ sửa lỗi trình bày

1.1.0
→ thay đổi vận hành không cần re-consent

2.0.0
→ thay đổi trọng yếu cần re-consent hoặc quyền rút
```

Đây là quy ước vận hành, không thay thế phân tích materiality.

## 7. Version scope

Không phải mọi tài liệu dùng cùng một version.

```text
charter_version
use_of_funds_version
milestone_version
pledge_version
benefit_version
refund_policy_version
```

Một campaign snapshot nên liên kết các version đang có hiệu lực tại cùng thời điểm.

## 8. Effective date

Phải phân biệt:

```text
proposed_at
approved_at
published_at
effective_at
accepted_at
```

Một amendment đã được phê duyệt nhưng chưa hết withdrawal window có thể chưa có hiệu lực với toàn bộ actor.

## 9. Actor bị ảnh hưởng

Mỗi amendment cần xác định:

- Contributor nào bị ảnh hưởng.
- Beneficiary nào bị ảnh hưởng.
- Provider nào phải thay đổi reservation.
- Sponsor hoặc matching party nào có quyền review.
- Verifier nào phải sửa protocol.
- Affected community nào cần consultation.

Không mặc định một thông báo chung cho toàn campaign là đủ.

## 10. Notification, acknowledgement và consent

```text
Notification
→ hệ thống gửi thông tin

Acknowledgement
→ actor xác nhận đã nhận/đọc

Consent
→ actor chấp thuận thay đổi

Re-consent
→ actor chấp thuận lại để cam kết tiếp tục
```

`Seen` hoặc mở email không đồng nghĩa consent.

## 11. Amendment threshold

Một charter nên xác định trước:

```text
Schedule variance ≤ 14 ngày
→ operational change

Budget-line variance ≤ 10%
→ operational approval

Total use-of-funds shift > 15%
→ materiality review

Output reduction > 20%
→ re-consent

Change of beneficiary group
→ prohibited or mandatory re-consent
```

Ngưỡng phải phù hợp từng dự án; không dùng các con số trên như chuẩn mặc định.

## 12. Versioning pledge cá nhân

Ví dụ:

```text
Pledge V1:
100 giờ kỹ thuật, tháng 9–10, conditional on venue

Pledge V2:
60 giờ, tháng 10–11, conditional on venue + insurance
```

Phải ghi:

- Provider tự sửa hay dự án yêu cầu.
- Có ảnh hưởng provision point không.
- Match nào bị invalid.
- Actor khác có cần được thông báo không.
- V1 đã `Superseded` hay vẫn áp dụng một phần.

## 13. Versioning milestone

Sửa milestone sau khi đã bắt đầu dễ tạo moral hazard.

Không nên:

```text
Không đạt tiêu chí cũ
→ hạ tiêu chí
→ gắn trạng thái “verified”
```

Nên:

```text
M1-V1 không đạt
→ tạo corrective action
→ nếu cần, đề xuất M1-V2
→ công bố vì sao sửa
→ giữ kết quả V1
→ quyết định lại disbursement
```

Xem [[Milestone verification]].

## 14. Versioning use of funds

Mỗi thay đổi phải chỉ ra:

```text
old_budget_line
new_budget_line
amount_shifted
restriction_check
reason
impact_on_scope
approval
reconsent_requirement
```

Không dùng nhãn `tối ưu ngân sách` để che chuyển tiền sang mục đích khác.

## 15. Record schema

```text
amendment_id:
object_type:
object_id:
from_version:
to_version:
change_class:
changed_fields:
old_values:
new_values:
reason:
proposed_by:
reviewed_by:
approved_by:
materiality_assessment:
affected_actor_groups:
notification_rule:
reconsent_rule:
withdrawal_window:
proposed_at:
approved_at:
effective_at:
supersedes:
evidence_ids:
```

## 16. Public change log

Public log nên hiển thị:

- Ngày thay đổi.
- Tóm tắt khác biệt.
- Lý do.
- Tác động đến output, thời gian và nguồn lực.
- Quyền của người tham gia.
- Bản cũ và bản mới.

Không nên chỉ ghi:

> “Cập nhật kế hoạch dự án.”

## 17. Conflict và rollback

Cần có rule khi:

- Hai amendment mâu thuẫn.
- Amendment được phê duyệt sai thẩm quyền.
- Dữ liệu dùng để phê duyệt bị sai.
- Actor không được thông báo đúng cách.
- Re-consent không đạt.

Rollback không được xóa lịch sử. Nó tạo version mới khôi phục nội dung cũ và giải thích lý do.

## 18. Dấu hiệu cảnh báo

- Tài liệu không có version.
- `Last updated` nhưng không có diff.
- Founder sửa trực tiếp sau khi nhận tiền.
- Contributor không xem được bản họ đã đồng ý.
- Milestone bị sửa sau khi không đạt.
- Thay đổi có lợi cho dự án nhưng giảm quyền contributor.
- Thông báo không nói quyền rút.
- Bản cũ bị xóa.
- Version kỹ thuật mới nhưng nghĩa vụ cũ vẫn được quảng cáo.

## 19. Kết luận

> **Versioning giữ cho một lời hứa có lịch sử; amendment governance giữ cho lịch sử đó không bị viết lại bởi bên đang nắm quyền vận hành.**

## Khái niệm liên quan

- [[Campaign charter]]
- [[Material change, pivot and re-consent]]
- [[Resource pledge lifecycle]]
- [[Evidence ledger và provenance]]
- [[Milestone verification]]
- [[Restricted funds]]
