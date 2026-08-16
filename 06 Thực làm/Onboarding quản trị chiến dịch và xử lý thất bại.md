---
ai_authored: true
---

# Onboarding quản trị chiến dịch và xử lý thất bại

> **Mục tiêu:** Giúp thành viên mới thiết kế và vận hành một chiến dịch có khả năng thay đổi, thất bại và đóng lại có trách nhiệm; không chỉ mô tả success path.

## 1. Kết quả bắt buộc

Người hoàn thành onboarding phải tạo được:

```text
1. Campaign charter
2. Commitment/version register
3. Materiality assessment matrix
4. Re-consent and withdrawal plan
5. Failure classification and recovery plan
6. Refund/release calculation
7. Residual resource register
8. Wind-down plan
9. Final closure report
10. Decision and evidence log
```

Không hoàn thành nếu chỉ viết “trường hợp có thay đổi sẽ thông báo cộng đồng”.

## 2. Tài liệu phải đọc

```text
1. [[Quản trị chiến dịch và xử lý thất bại - Bản đồ thuật ngữ]]
2. [[Campaign charter]]
3. [[Commitment versioning and amendment]]
4. [[Material change, pivot and re-consent]]
5. [[Campaign failure, recovery and termination]]
6. [[Refund and release mechanism]]
7. [[Residual funds and unused resources]]
8. [[Campaign closure, wind-down and dissolution]]
9. [[Restricted funds]]
10. [[Disbursement]]
11. [[Resource pledge lifecycle]]
12. [[Evidence ledger và provenance]]
```

## 3. Case thực hành

Chiến dịch `ToolLab Pilot` công bố:

```text
Purpose:
Mở một thư viện công cụ cộng đồng trong 6 tháng,
phục vụ 100 thành viên pilot.

Provision point:
300 triệu usable cash
+ 4 máy accepted/reserved
+ 200 giờ kỹ thuật reserved
+ venue 24 tuần
+ bảo hiểm

Output:
50 loại dụng cụ hoạt động
+ hệ thống booking
+ 12 workshop an toàn

Timeline:
Mở cửa ngày 01/11

Funding rule:
AON cho provision point ban đầu;
milestone-based disbursement sau activation.
```

Campaign đã activated.

## 4. Dữ liệu sau 3 tháng

```text
Tiền nhận: 420 triệu
Tiền đã giải ngân: 230 triệu
Chi hợp lệ đã reconcile: 205 triệu
Khoản chi đang tranh chấp: 25 triệu
Tiền còn safeguarded: 190 triệu

Máy:
- 2 máy donated và accepted
- 2 máy loaned, đang sử dụng
- 1 máy offered nhưng chưa delivered

Giờ kỹ thuật:
- 200 giờ reserved
- 130 giờ delivered
- 100 giờ accepted

Venue:
- hợp đồng 24 tuần
- đã dùng 8 tuần

User:
- 180 đăng ký
- 42 thành viên trả phí
- 31 người đã sử dụng
```

Sự kiện:

1. Technical lead rời ngay lập tức.
2. Một máy loaned bị hỏng.
3. Bảo hiểm từ chối một claim vì operator chưa được chứng nhận.
4. Nhóm đề xuất bỏ workshop và chuyển phần lớn ngân sách sang app marketplace.
5. Ngày mở cửa dự kiến trễ ít nhất 4 tháng.
6. Sponsor matching yêu cầu giữ nguyên mục đích thư viện công cụ.
7. 18 contributor yêu cầu hoàn tiền.
8. Nhà cung cấp hoàn lại 12 triệu cho đơn hàng bị hủy.
9. Còn 60 triệu contingency chưa dùng.
10. Campaign page vẫn quảng cáo “đúng tiến độ”.

## 5. Bài tập 1 — Dựng charter

Tạo charter V1 gồm:

```text
identity
purpose
beneficiary_scope
minimum_scope
full_scope
provision_point
eligible_contributions
use_of_funds
restrictions
governance_roles
milestones
change_tolerances
material_changes
reconsent_rule
refund_release_rule
residual_rule
failure_rule
closure_rule
```

Phải chỉ rõ điểm nào trong case chưa được charter gốc quy định.

## 6. Bài tập 2 — Version register

Tạo bảng:

| Object | V1 | Proposed V2 | Change class | Effective? | Consent needed? |
|---|---|---|---|---|---|
| Purpose | | | | | |
| Use of funds | | | | | |
| Output | | | | | |
| Timeline | | | | | |
| Milestone | | | | | |
| Refund rule | | | | | |

Không được ghi đè V1.

Sản phẩm phải chỉ ra:

- Bản nào contributor đã đồng ý.
- Ai đề xuất V2.
- V2 có nằm trong charter không.
- Ai bị ảnh hưởng.
- Khi nào V2 có hiệu lực.

## 7. Bài tập 3 — Materiality assessment

Phân loại từng thay đổi:

```text
Technical lead rời
Máy hỏng
Claim bảo hiểm bị từ chối
Bỏ workshop
Chuyển ngân sách sang marketplace
Trễ 4 tháng
Đổi refund rule nếu có
```

Dùng các trục:

- Purpose.
- Beneficiary.
- Output.
- Time.
- Budget/restriction.
- Team/governance.
- Risk/safety.
- Contributor rights.

Kết luận mỗi item:

```text
Minor
Operational
Material
Prohibited
```

## 8. Bài tập 4 — Re-consent plan

Tách actor:

```text
donor
member/pre-order customer
sponsor/matching provider
volunteer
machine lender
data contributor
beneficiary user
```

Với từng nhóm, ghi:

- Cần notification, consultation hay re-consent?
- Có quyền rút không?
- Phần nào đã dùng?
- Deadline.
- Non-response được xử lý thế nào?
- Quyền khiếu nại.

Không dùng một poll Facebook làm re-consent cho mọi quan hệ.

## 9. Bài tập 5 — Failure classification

Không được kết luận đơn giản `dự án thất bại`.

Phân loại:

- Execution delay.
- Resource failure.
- Quality/safety failure.
- Governance failure.
- Compliance failure.
- Purpose failure.
- Integrity concern.

Phải ghi alternative explanations và evidence cần thu.

Ví dụ:

```text
Campaign page vẫn nói đúng tiến độ
→ có thể là stale content
→ cũng có thể là misrepresentation
→ cần xác định ai biết gì, từ khi nào và quyền sửa page
```

## 10. Bài tập 6 — Immediate controls

Trong 24 giờ đầu, đề xuất:

```text
Pause affected activity
Freeze relevant disbursement
Preserve evidence
Remove/label misleading claim
Inspect machine and safety conditions
Confirm insurance status
Secure project records and access
Notify governance body
Set next public update date
```

Phải tránh đóng toàn bộ hoạt động không cần thiết nếu việc đó gây thêm thiệt hại.

## 11. Bài tập 7 — Recovery options

So sánh ít nhất ba phương án:

### Option A — Recover original purpose

- Thay technical lead.
- Chứng nhận operator.
- Sửa/thay máy.
- Giữ workshop.
- Gia hạn timeline.

### Option B — Reduce to pre-approved fallback

- Giảm số công cụ.
- Giảm thời gian vận hành.
- Giữ purpose cốt lõi.

### Option C — Pivot sang marketplace

Phải đánh giá có còn nằm trong restriction và purpose không.

### Option D — Transfer

Chuyển thư viện cho một tổ chức địa phương đủ năng lực.

### Option E — Terminate

Wind-down và refund/release.

Lập bảng:

| Option | Purpose fit | Resource need | Consent | Risk | Refund | Time | Recommendation |
|---|---|---|---|---|---|---|---|

## 12. Bài tập 8 — Corrective action plan

Tạo:

```text
root_cause
immediate_control
corrective_action
owner
deadline
resource_need
verification_criteria
next_decision_date
escalation_rule
```

Không chấp nhận:

> “Nhóm sẽ cố gắng tìm người thay thế sớm.”

## 13. Bài tập 9 — Refund/release calculation

Phân biệt:

```text
Tiền chưa dùng
Tiền đã dùng hợp lệ
Khoản 25 triệu đang tranh chấp
Vendor refund 12 triệu
Contingency 60 triệu
Payment authorization chưa capture
Machine reservation
Volunteer hours còn lại
Venue tuần chưa dùng
```

Tạo bảng:

| Resource | Original | Used/accepted | Remaining | Refund/release rule | Evidence |
|---|---:|---:|---:|---|---|

Phải chỉ ra:

- Ai eligible.
- Cách tính partial refund.
- Phí.
- Payment destination.
- Timeline.
- Failed/unclaimed rule.

## 14. Bài tập 10 — Residual register

Kiểm kê:

```text
190 triệu safeguarded
12 triệu vendor refund
60 triệu contingency
2 máy donated
2 máy loaned
máy hỏng
source code/app prototype
member list
domain và cloud credits
unused venue period
unfulfilled memberships/workshops
```

Với từng item, ghi:

- Owner.
- Restriction.
- Condition.
- Outstanding obligation.
- Proposed treatment.
- Approval.
- Recipient.

Không gom toàn bộ thành `tài sản còn lại`.

## 15. Bài tập 11 — Termination và wind-down

Giả định recovery thất bại sau 30 ngày.

Tạo wind-down plan:

```text
stop new commitments
lock charter and versions
reconcile
return equipment
settle valid obligations
refund/release
handle residual assets
data closure
beneficiary transition
grievance window
final report
archive
```

Mỗi việc có:

- Owner.
- Deadline.
- Dependency.
- Evidence.
- Public/private status.

## 16. Bài tập 12 — Public communication

Viết ba thông báo:

### Notice 1 — Incident and pause

Phân biệt điều đã biết và chưa biết.

### Notice 2 — Material change/recovery options

Nêu quyền actor.

### Notice 3 — Final decision and closure

Công bố nguồn lực, refund, residual và unresolved obligations.

Không dùng:

- “Do tình hình khách quan”.
- “Dự án vẫn đang phát triển tốt”.
- “Mọi người hãy tiếp tục tin tưởng”.

nếu không có evidence cụ thể.

## 17. Bài tập 13 — Decision log

```text
decision_id
decision_type
question
evidence_reviewed
conflicts
authority
options
reasoning
result
effective_at
affected_actors
appeal_or_grievance
```

Phải có ít nhất:

- Pause decision.
- Materiality decision.
- Re-consent decision.
- Resume/terminate decision.
- Refund calculation approval.
- Residual allocation approval.
- Closure approval.

## 18. Bài tập 14 — Red-team

Một nhóm khác phải cố chứng minh:

- Pivot đang che purpose failure.
- Re-consent không hợp lệ.
- Refund calculation thiên vị founder.
- Vendor refund bị ghi sai.
- Machine lender không được bảo vệ.
- Final report bỏ unresolved obligation.
- Public status misleading.

Người onboarding phải sửa hồ sơ hoặc bảo vệ kết luận bằng evidence.

## 19. Deliverables cuối

```text
campaign-charter-v1.md
amendment-and-version-register.csv
materiality-assessment.md
reconsent-plan.md
failure-and-recovery-plan.md
refund-release-register.csv
residual-resource-register.csv
wind-down-plan.md
final-closure-report.md
decision-log.csv
```

## 20. Definition of done

```text
[ ] Charter có success và failure path
[ ] Không ghi đè version cũ
[ ] Materiality có lý do và authority
[ ] Re-consent khác notification
[ ] Failure được phân loại
[ ] Corrective action có deadline và verification
[ ] Refund khác release
[ ] Residual có owner và restriction
[ ] Wind-down có workstream owner
[ ] Final report nêu unresolved obligations
[ ] Decision liên kết evidence IDs
[ ] Public claims không vượt quá hồ sơ
```

## 21. Kết luận onboarding

> **Người quản trị chiến dịch không được đánh giá bằng khả năng giữ hình ảnh dự án luôn tích cực; họ được đánh giá bằng khả năng giữ nguyên lịch sử lời hứa, phát hiện thay đổi, bảo vệ các bên và đóng nghĩa vụ khi thực tế không còn giống kế hoạch.**
