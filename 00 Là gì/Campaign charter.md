# Campaign charter

> **Định nghĩa ngắn:** *Campaign charter* — hiến chương chiến dịch — là văn bản quy tắc gốc xác định mục đích, phạm vi, quyền, nghĩa vụ, giới hạn thay đổi, cách xử lý thất bại và cách đóng một chiến dịch.

Campaign charter không phải nội dung quảng bá. Nó là cấu trúc dùng để trả lời:

> Người tham gia đang giao nguồn lực cho lời hứa nào, trong phạm vi nào và dưới cơ chế trách nhiệm nào?

## 1. Vì sao cần charter?

Một trang chiến dịch thường có:

- Câu chuyện.
- Hình ảnh.
- Mục tiêu vốn.
- Các mức đóng góp.
- Timeline.

Nhưng các nội dung đó chưa chắc trả lời:

```text
Ai có quyền đổi mục tiêu?
Use of funds có ràng buộc không?
Nếu thiếu nguồn lực thì sao?
Nếu dự án chậm thì ai quyết định?
Nếu còn tiền hoặc tài sản thì xử lý thế nào?
Khi nào contributor được rút?
Ai chịu trách nhiệm công bố thất bại?
```

Charter biến các câu trả lời thành quy tắc trước khi nhận cam kết.

## 2. Charter khác campaign page

```text
Campaign page
→ truyền thông, giải thích và kêu gọi tham gia

Campaign charter
→ xác định quyền, giới hạn và quy tắc vận hành
```

Campaign page có thể được trình bày lại để dễ hiểu, nhưng không được thay đổi nội dung trọng yếu trái với charter.

Nếu campaign page và charter mâu thuẫn, chiến dịch phải có quy tắc xác định văn bản nào chi phối và cách xử lý người tham gia đã dựa vào thông tin sai.

## 3. Charter khác project plan

```text
Project plan
→ ai làm việc gì, khi nào và bằng nguồn lực nào

Campaign charter
→ người tham gia được hứa gì và cơ chế nào bảo vệ lời hứa đó
```

Project plan có thể thay đổi thường xuyên hơn. Charter chỉ nên thay đổi theo [[Commitment versioning and amendment|quy trình amendment]].

## 4. Thành phần tối thiểu

### Identity

```text
campaign_id
campaign_name
project_entity
campaign_operator
contact_point
charter_version
effective_at
```

### Purpose

- Vấn đề cần giải quyết.
- Kết quả chung được hứa.
- Nhóm hưởng lợi.
- Điều nằm ngoài mục đích.

### Scope

- Minimum viable scope.
- Full scope.
- Geographical scope.
- Time period.
- In-scope và out-of-scope activities.

### Resource model

- Tiền.
- Thời gian và lao động.
- Thiết bị, địa điểm, dữ liệu và access.
- Loại nguồn lực không được nhận.
- Eligibility và acceptance rule.

### Provision point

Xem [[Provision point và threshold mechanism]]. Charter phải xác định:

- Ngưỡng tiền.
- Ngưỡng nguồn lực khác.
- Blocking conditions.
- Deadline.
- Cách đo.
- Người xác minh.

### Funding and activation rule

- All-or-nothing, keep-it-all hoặc hybrid.
- Pledge có điều kiện nào.
- Khi nào collect, release hoặc activate.
- Cách xử lý không đạt ngưỡng.

### Use of funds and restrictions

- Eligible costs.
- Ineligible costs.
- Dự phòng.
- Phí nền tảng và phí thanh toán.
- Biên độ điều chỉnh.
- [[Restricted funds|Restriction source]].

### Governance

- Ai đề xuất.
- Ai kiểm tra.
- Ai phê duyệt.
- Ai giữ hoặc điều khiển tài sản.
- Ai xác minh milestone.
- Ai xử lý conflict of interest.
- Ai có quyền pause, terminate hoặc transfer.

### Milestones and evidence

- Milestone.
- Acceptance criteria.
- Evidence requirement.
- Decision rule.
- Disbursement liên quan.

### Contributor relationship

- Donation, reward, pre-order, membership, loan, investment hoặc contribution khác.
- Benefit được hứa.
- Quyền và giới hạn quyền.
- Risk disclosure.

Không dùng một ngôn ngữ quan hệ cho nhiều bản chất pháp lý khác nhau.

### Change control

- Editorial correction.
- Minor variation.
- Material change.
- Prohibited change.
- Notification, consultation và re-consent.

### Failure and remedy

- Failure classification.
- Pause rule.
- Corrective action period.
- Transfer rule.
- Termination rule.
- Refund/release rule.

### Residual and closure

- Tiền hoặc tài sản còn dư.
- Contributor benefit chưa fulfil.
- Dữ liệu và IP.
- Hồ sơ cuối.
- Archive và retention.

## 5. Mục đích phải đủ cụ thể

Không nên viết:

> “Hỗ trợ cộng đồng và thúc đẩy đổi mới.”

Nên viết:

```text
Tạo và vận hành thử một thư viện công cụ tại phường X trong 6 tháng,
phục vụ ít nhất 100 thành viên xác minh,
với 50 loại dụng cụ đạt tiêu chuẩn an toàn đã công bố.
```

Purpose tốt phải xác định:

- Trạng thái muốn tạo ra.
- Ai được hưởng.
- Phạm vi.
- Thời gian.
- Tiêu chí hoàn thành.

## 6. Scope phải có ranh giới

Charter cần nói rõ:

```text
Full scope
Minimum viable scope
Fallback scope
Out-of-scope
```

Fallback scope chỉ có giá trị nếu được công bố trước. Không được nhận nguồn lực cho full scope rồi tự ý đổi sang một dự án khác.

## 7. Quyền quyết định phải gắn với loại quyết định

| Loại quyết định | Chủ thể gợi ý |
|---|---|
| Điều chỉnh vận hành nhỏ | Project lead trong biên độ |
| Thay đổi ngân sách đáng kể | Governance body |
| Thay đổi mục đích/beneficiary | Re-consent hoặc cơ chế cao hơn |
| Milestone đạt hay không | Verifier theo protocol |
| Giải ngân | Người có thẩm quyền tài chính |
| Integrity concern | Independent review hoặc committee |
| Termination | Cơ quan được charter chỉ định |

Không nên để người nhận tiền đồng thời là người duy nhất xác nhận điều kiện nhận tiền.

## 8. Quyền sửa charter

Charter phải xác định:

```text
Ai được đề xuất amendment?
Ai kiểm tra materiality?
Ai phê duyệt?
Ai phải được thông báo?
Khi nào cần re-consent?
Khi nào actor được rút?
Bản cũ được lưu ở đâu?
```

Xem [[Commitment versioning and amendment]].

## 9. Charter không thể hợp pháp hóa mọi thứ

Một điều khoản viết trong charter không tự động:

- Hợp pháp.
- Công bằng.
- Có thể thực thi.
- Loại bỏ nghĩa vụ bắt buộc.
- Cho phép dùng tiền sai restriction.
- Cho phép xâm phạm quyền của affected community.

Charter phải phù hợp với pháp luật, hợp đồng, quy tắc thanh toán và nghĩa vụ của pháp nhân liên quan.

## 10. Charter và nhiều loại contributor

Một campaign có thể có:

```text
donor
pre-order customer
sponsor
volunteer
equipment provider
data contributor
investor
beneficiary contributor
```

Charter phải xác định quyền theo từng loại, không dùng một nút `ủng hộ` cho tất cả.

Ví dụ:

- Donor có thể không có quyền nhận sản phẩm.
- Pre-order customer có quyền liên quan đến giao hàng và refund.
- Volunteer có quyền về an toàn, dữ liệu và công nhận công sức.
- Equipment provider có quyền hoàn trả tài sản.
- Investor có quyền và rủi ro khác hoàn toàn.

## 11. Campaign charter record

```text
campaign_charter_id:
campaign_id:
version:
status:
effective_at:
expires_at:
purpose:
beneficiary_scope:
minimum_scope:
full_scope:
provision_point_ids:
eligible_contribution_types:
use_of_funds:
restriction_ids:
governance_roles:
change_thresholds:
reconsent_rule:
refund_rule:
residual_rule:
failure_rule:
closure_rule:
source_document_hash:
approved_by:
evidence_ids:
```

Trạng thái có thể gồm:

```text
Draft
→ Under review
→ Approved
→ Effective
→ Amended
→ Superseded
→ Closed
→ Archived
```

## 12. Public charter và internal procedures

Không phải mọi chi tiết đều công khai.

### Public charter

Nên gồm:

- Mục đích.
- Phạm vi.
- Provision point.
- Use of funds.
- Quy tắc thay đổi.
- Refund và residual rule.
- Vai trò quyết định chính.
- Grievance route.

### Internal procedures

Có thể gồm:

- Chi tiết security.
- Payment operations.
- Investigation protocol.
- Dữ liệu cá nhân.
- Internal contact.

Tuy nhiên, không được dùng nhãn “nội bộ” để che giấu điều khoản làm thay đổi quyền của contributor.

## 13. Checklist trước khi mở chiến dịch

```text
[ ] Purpose đủ cụ thể
[ ] Beneficiary và affected community đã xác định
[ ] Provision point có căn cứ
[ ] Resource types và lifecycle rule rõ
[ ] Funding rule công bố
[ ] Use of funds và restriction rõ
[ ] Governance roles không xung đột
[ ] Milestone có evidence requirement
[ ] Material change threshold rõ
[ ] Re-consent và withdrawal rule rõ
[ ] Refund/release rule khả thi
[ ] Residual rule rõ
[ ] Failure và closure rule rõ
[ ] Grievance route hoạt động
[ ] Version và approval được lưu
```

## 14. Dấu hiệu cảnh báo

- Charter chỉ lặp lại nội dung marketing.
- Không có version.
- Founder có quyền tự đổi mọi thứ.
- Use of funds không phân biệt kế hoạch và restriction.
- Không có quy tắc khi mất resource blocking.
- Không có thời hạn cho corrective action.
- Refund rule chỉ ghi “tùy trường hợp”.
- Tiền dư mặc định thuộc dự án.
- Contributor không có cách xem bản charter đã đồng ý.
- Có quyền sửa đơn phương nhưng không có quyền rút.

## 15. Kết luận

> **Campaign charter biến lời kêu gọi thành một chế độ trách nhiệm: mục đích có giới hạn, quyền quyết định có chủ thể và thất bại có quy tắc xử lý.**

## Khái niệm liên quan

- [[Quản trị chiến dịch và xử lý thất bại - Bản đồ thuật ngữ]]
- [[Commitment versioning and amendment]]
- [[Material change, pivot and re-consent]]
- [[Restricted funds]]
- [[Provision point và threshold mechanism]]
- [[Verification protocol và decision rule]]
- [[Stakeholder engagement và grievance mechanism]]
