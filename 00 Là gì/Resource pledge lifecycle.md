---
ai_authored: true
---

# Resource pledge lifecycle

> **Định nghĩa làm việc của dự án:** *Resource pledge lifecycle* là chuỗi trạng thái dùng để theo dõi một nguồn lực từ lúc được đề nghị hoặc hứa cung cấp đến khi được giữ chỗ, kích hoạt, bàn giao, nghiệm thu, hoàn trả hoặc hết hiệu lực.

Node này không định nghĩa loại nguồn lực và không đánh giá độ cứng của cam kết. Nó chỉ trả lời:

> Nguồn lực đang ở đâu trong vòng đời vận hành?

## 1. Ranh giới

```text
[[Commitment ladder]]
→ hành vi của actor thuộc Pre-commitment hay Resource contribution?

[[Soft commitment và hard commitment]]
→ cam kết khó rút đến đâu?

Resource pledge lifecycle
→ nguồn lực đang promised, reserved, delivered hay accepted?

[[Evidence ledger và provenance]]
→ bằng chứng cho từng chuyển trạng thái là gì?

[[Proof of use và proof of outcome]]
→ nguồn lực đã được dùng đúng và tạo kết quả gì?
```

## 2. State machine làm việc

```text
Offered
→ Confirmed
→ Conditional
→ Reserved
→ Activated
→ Partially delivered
→ Delivered
→ Accepted
→ In use
→ Completed / Returned / Released
```

Các nhánh ngoại lệ:

```text
Withdrawn
Expired
Rejected
Breached
Cancelled
Superseded
Lost / Damaged
```

Không phải mọi nguồn lực đi qua tất cả trạng thái.

## 3. Ý nghĩa từng trạng thái

### Offered

Provider bày tỏ khả năng cung cấp nhưng chưa xác nhận điều kiện đầy đủ.

### Confirmed

Provider xác nhận nội dung, phạm vi, thời hạn và người có thẩm quyền.

### Conditional

Cam kết chỉ kích hoạt nếu điều kiện xảy ra.

Ví dụ:

- Đủ số người tham gia.
- Có bảo hiểm.
- Dự án đạt milestone.
- Có operator.
- Một nguồn lực bổ trợ đã được reserve.

### Reserved

Nguồn lực đã được giữ cho dự án trong một cửa sổ xác định. Nó chưa nhất thiết được bàn giao.

### Activated

Điều kiện kích hoạt đã đạt và nguồn lực được phép bước vào thực hiện/bàn giao.

### Partially delivered

Một phần số lượng, công suất hoặc thời gian đã được cung cấp.

### Delivered

Nguồn lực đã được bàn giao theo record, nhưng chưa mặc định đạt acceptance criteria.

### Accepted

Người có thẩm quyền xác nhận nguồn lực đúng yêu cầu.

### In use

Nguồn lực đang được dự án sử dụng.

### Completed / Returned / Released

- `Completed`: dịch vụ/công việc hoàn tất.
- `Returned`: tài sản mượn đã hoàn trả.
- `Released`: capacity giữ chỗ không còn bị khóa.

## 4. Pledge không phải contribution đã nhận

```text
Promised value
≠ Reserved value
≠ Delivered value
≠ Accepted value
≠ Used value
```

Khi công bố, phải tách tối thiểu:

- Tổng offer.
- Tổng confirmed.
- Tổng reserved.
- Tổng delivered.
- Tổng accepted.

Không dùng tổng pledge để nói “đã huy động được”.

## 5. Transition rule

Mỗi chuyển trạng thái cần:

```text
transition_id:
resource_pledge_id:
from_status:
to_status:
trigger:
actor:
timestamp:
evidence_ids:
reviewer:
notes:
```

Ví dụ:

```text
Conditional → Reserved
Trigger: dự án đạt 50 người tham gia hợp lệ
Evidence: E-220, E-221
Reviewer: operations lead
```

## 6. Record tối thiểu

```text
resource_pledge_id:
provider_id:
project_id:
resource_type:
resource_object_id:
quantity_or_capacity:
unit:
conditions:
availability_window:
withdrawal_rule:
expiry_at:
reservation_rule:
delivery_method:
acceptance_criteria:
return_or_release_rule:
current_status:
status_updated_at:
related_need_ids:
related_match_ids:
evidence_ids:
```

## 7. Expiry

Mọi pledge nên có thời hạn hoặc quy tắc review.

```text
No expiry
→ dễ làm dự án tưởng nguồn lực vẫn còn

Expired pledge
→ không được tính vào resource coverage

Renewed pledge
→ tạo version hoặc event mới
```

Khi offer thay đổi về số lượng, thời gian hoặc điều kiện, không ghi đè âm thầm. Dùng `Superseded` và tạo record mới/version mới.

## 8. Withdrawal

`Withdrawn` không tự động là vi phạm.

Phải phân biệt:

```text
Permitted withdrawal
→ rút theo quyền đã thỏa thuận

Withdrawal after reservation
→ có thể gây chi phí hoặc cần notice

Breach
→ không thực hiện nghĩa vụ đã kích hoạt mà không có căn cứ

Project-caused cancellation
→ dự án đổi điều kiện hoặc không đạt mốc
```

Cần ghi reason code và ảnh hưởng đến các match/dependency khác.

## 9. Partial delivery

Ví dụ:

```text
Pledge: 100 giờ kỹ thuật
Delivered: 60 giờ
Accepted: 45 giờ
Rejected/rework: 15 giờ
Remaining: 40 giờ
```

Không được coi 100 giờ pledge là 100 giờ contribution.

Tương tự:

```text
Venue reserved 10 ngày
→ dự án dùng 6 ngày
→ 4 ngày released
```

## 10. Acceptance khác delivery

Acceptance criteria phụ thuộc loại nguồn lực:

- Vật liệu: số lượng, grade, chứng từ.
- Thiết bị: model, tình trạng, calibration.
- Dịch vụ: deliverable, quality review.
- Dữ liệu: quyền, format, quality, provenance.
- Access: slot, quyền tiếp cận và khả năng thực thi.

`Delivered` chỉ nói việc chuyển giao đã xảy ra; `Accepted` nói dự án xác nhận nó phù hợp.

## 11. Dependency propagation

Nếu một pledge quan trọng bị rút hoặc hết hạn, hệ thống phải truy ra:

```text
resource pledge
→ match nào phụ thuộc?
→ milestone nào bị ảnh hưởng?
→ ngân sách nào cần đổi?
→ actor nào cần thông báo?
→ decision nào cần review?
```

Đây là nơi nối với [[Multi-resource matching]] và [[Verification protocol và decision rule]].

## 12. Public status và private detail

Có thể công khai:

- Loại nguồn lực.
- Số lượng/công suất.
- Trạng thái.
- Thời hạn.
- Provider nếu được phép.
- Tóm tắt điều kiện.

Giữ hạn chế:

- Dữ liệu cá nhân.
- Điều khoản thương mại.
- Chi tiết bảo mật.
- Metadata có thể gây rủi ro.

## 13. Rủi ro

- Không có expiry.
- Gộp promised và delivered.
- Không có acceptance.
- Một offer được reserve cho nhiều dự án.
- Không cập nhật khi điều kiện thay đổi.
- Không lưu ai chuyển trạng thái.
- Provider rút nhưng số liệu public vẫn giữ nguyên.
- Tài sản đã trả nhưng vẫn hiển thị đang dùng.
- Pledge mềm được dùng để mở khóa matching cứng.

## 14. Kết luận

> **Resource pledge lifecycle biến lời hứa nguồn lực thành một chuỗi trạng thái có thể vận hành, kiểm tra và rút kinh nghiệm.**

## Khái niệm liên quan

- [[Nguồn lực ngoài tiền - Bản đồ thuật ngữ]]
- [[Commitment ladder]]
- [[Soft commitment và hard commitment]]
- [[Conditional cooperation]]
- [[Multi-resource matching]]
- [[Evidence ledger và provenance]]
- [[Proof of use và proof of outcome]]
