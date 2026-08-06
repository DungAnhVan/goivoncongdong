# Onboarding nguồn lực ngoài tiền

> **Mục tiêu:** Giúp thành viên mới biến một câu chung chung như “dự án cần chuyên gia, dữ liệu và thiết bị” thành một hệ thống resource needs, offers, matches, commitments và bằng chứng sử dụng có thể vận hành.

## 1. Kết quả bắt buộc

Người hoàn thành onboarding phải tạo được:

```text
1. Resource taxonomy
2. Resource need register
3. Resource offer register
4. Need–offer matching table
5. Resource pledge lifecycle log
6. Acceptance checklist
7. Proof-of-use plan
8. Resource gap memo
```

Không hoàn thành nếu chỉ lập một bảng “nguồn lực — giá trị tiền”.

## 2. Tài liệu phải đọc

```text
1. [[Nguồn lực ngoài tiền - Bản đồ thuật ngữ]]
2. [[In-kind contribution]]
3. [[Time and labor contribution]]
4. [[Data contribution]]
5. [[Asset and access contribution]]
6. [[Multi-resource matching]]
7. [[Resource pledge lifecycle]]
8. [[Commitment ladder]]
9. [[Proof of use và proof of outcome]]
```

## 3. Tình huống pilot

Một dự án tuyên bố:

> “Chúng tôi đã huy động được 1,8 tỷ đồng nguồn lực ngoài tiền và đã đủ điều kiện triển khai.”

Dữ liệu thô:

```text
- một doanh nghiệp hứa cho mượn máy CNC trị giá 1,2 tỷ;
- máy chỉ rảnh 2 ngày trong tháng sau;
- chưa có operator;
- ba kỹ sư nói sẽ hỗ trợ khi rảnh, tổng 120 giờ ước tính;
- một trường cho phép dùng phòng lab nhưng chưa xác nhận lịch;
- một đơn vị gửi dataset 50.000 dòng nhưng chưa rõ quyền dùng;
- một mentor giới thiệu hai khách hàng tiềm năng;
- nhà cung cấp giảm giá 20% vật liệu;
- 100 triệu tiền mặt đã chuyển.
```

Người onboarding phải viết lại tuyên bố công khai trung thực và xác định dự án thực sự còn thiếu gì.

## 4. Ngày 1 — Resource taxonomy

Tạo taxonomy tối thiểu:

```text
Money
Time and labor
Material
Equipment
Venue
Infrastructure
Data
Knowledge/IP
Market access
Institutional access
Reputation/endorsement
```

Với mỗi nhóm, ghi:

- Đơn vị đo.
- Thuộc tính chất lượng.
- Quyền cần kiểm tra.
- Bằng chứng bàn giao.
- Acceptance criteria.

## 5. Ngày 2 — Resource needs

Chuyển nhu cầu dự án thành record:

```text
need_id
resource_category
specification
quantity
unit
quality_or_skill
location
required_window
dependencies
acceptable_substitutes
acceptance_criteria
priority
```

Yêu cầu:

- Có ít nhất một bottleneck resource.
- Có ít nhất một dependency bundle.
- Không dùng từ “chuyên gia”, “thiết bị” hoặc “dữ liệu” mà không có specification.

## 6. Ngày 3 — Resource offers

Mỗi offer phải ghi:

```text
offer_id
provider_id
resource_category
description
quantity_or_capacity
availability
location
rights_or_transfer_type
conditions
withdrawal_rule
expiry
related_party_status
evidence_ids
status
```

Phải tách:

- Hứa cho mượn máy và máy đã reserve.
- Mentor giới thiệu và quyền tiếp cận khách hàng.
- File dữ liệu đã gửi và quyền sử dụng dữ liệu.
- Discount và donation.

## 7. Ngày 4 — Matching

Tạo bảng:

| Need | Offer | Technical fit | Time fit | Rights fit | Dependency | Gap | Decision |
|---|---|---|---|---|---|---|---|

Phải có:

- Một partial match.
- Một offer bị từ chối vì điều kiện.
- Một nguồn lực miễn phí nhưng net value âm.
- Một bottleneck chưa được giải quyết.
- Một bundle không thể tách.

## 8. Ngày 5 — Lifecycle

Với từng pledge, ghi event:

```text
Offered
Confirmed
Conditional
Reserved
Activated
Delivered
Accepted
In use
Completed / Returned / Released
```

Ít nhất phải có:

- Một pledge hết hạn.
- Một pledge bị rút hợp lệ.
- Một partial delivery.
- Một delivery bị từ chối acceptance.
- Một nguồn lực bị overbook giữa hai dự án.

## 9. Acceptance checklist

### Time and labor

- Scope rõ.
- Deliverable rõ.
- Người review.
- Giờ delivered.
- IP và bảo mật.

### Data

- Quyền cung cấp.
- Mục đích sử dụng.
- Format/schema.
- Quality summary.
- Retention và termination.

### Asset and access

- Ownership/use right.
- Serial/định danh.
- Availability.
- Capacity.
- Liability/insurance.
- Return rule.

## 10. Proof-of-use plan

Mỗi nguồn lực accepted phải nối với:

```text
activity
milestone
responsible actor
usage evidence
exception rule
outcome link
```

Ví dụ:

```text
Máy CNC 6 giờ accepted
→ Milestone M-03
→ log máy + job ID + biên bản sản phẩm
→ 18 chi tiết đạt / 2 rework
```

## 11. Viết lại tuyên bố công khai

Không viết:

> “Đã huy động 1,8 tỷ nguồn lực.”

Viết theo trạng thái:

```text
Tiền đã nhận: 100 triệu
Thiết bị: 1 offer cho mượn, chưa reserve, thiếu operator
Thời gian chuyên môn: 120 giờ soft pledge, chưa có lịch
Địa điểm: quyền dùng đang chờ xác nhận lịch
Dữ liệu: file đã nhận, quyền sử dụng đang review
Tiếp cận khách hàng: 2 introductions, chưa có pilot
Giảm giá vật liệu: 20%, áp dụng đến ngày...
```

## 12. Resource gap memo

Người onboarding phải trả lời:

```text
Nguồn lực nào đã đủ và accepted?
Nguồn lực nào mới chỉ promised?
Bottleneck hiện tại là gì?
Nguồn lực nào có thể thay thế?
Điều kiện nào khiến kế hoạch không khả thi?
Cần mua bằng tiền phần nào?
Pledge nào phải xác minh hoặc loại bỏ?
```

## 13. Red-team review

Tìm tối thiểu mười lỗi:

- Quy giá tài sản cho mượn thành giá trị sở hữu.
- Đếm planned hours như delivered hours.
- Gọi introduction là market access.
- Gọi file dữ liệu là dataset được phép dùng.
- Không có expiry.
- Không ghi related party.
- Một nguồn lực bị đếm hai lần.
- Discount được tính như donation toàn phần.
- Không có operator hoặc complement.
- Không có acceptance criteria.
- Tổng giá trị che bottleneck.
- Nguồn lực public vẫn hiển thị dù đã withdrawn.

## 14. Tiêu chuẩn hoàn thành

Đạt khi:

- Need và offer được chuẩn hóa riêng.
- Không gộp promised, reserved, delivered và accepted.
- Quyền sử dụng được tách khỏi sở hữu.
- Time, data, asset và access có schema riêng.
- Match có giải thích về compatibility và gap.
- Mọi resource accepted có proof-of-use plan.
- Tuyên bố công khai không phóng đại.

Không đạt khi:

- Chỉ quy đổi tất cả thành tiền.
- Gọi mọi nguồn lực miễn phí là có giá trị dương.
- Dùng một điểm matching duy nhất.
- Cho rằng pledge cứng đồng nghĩa nguồn lực phù hợp.
- Cho rằng có nguồn lực đồng nghĩa đã có outcome.

## 15. Kết luận

> **Năng lực của người điều phối không nằm ở việc gom được nhiều lời hứa, mà ở khả năng biến đúng tổ hợp nguồn lực thành năng lực thực thi có thể kiểm chứng.**
