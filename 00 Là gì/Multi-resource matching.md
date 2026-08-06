# Multi-resource matching

> **Định nghĩa làm việc của dự án:** *Multi-resource matching* là quá trình ghép các nhu cầu nguồn lực của dự án với nhiều offer khác nhau về tiền, thời gian, kỹ năng, dữ liệu, tài sản, địa điểm và quyền tiếp cận, dựa trên mức tương thích, điều kiện và phụ thuộc giữa chúng.

Đây là **thuật ngữ làm việc của dự án**, không phải tên chuẩn duy nhất của một ngành.

## 1. Vì sao cần một node riêng?

Matching fund chỉ ghép một nguồn tài trợ với một nguồn tài trợ khác theo công thức. Dự án thực tế cần một tổ hợp dị biệt:

```text
40 giờ thiết kế
+ máy CNC 2 ngày
+ 100 kg vật liệu
+ địa điểm thử nghiệm
+ dữ liệu người dùng
+ luật sư review
+ 60 triệu tiền mặt
```

Một dự án có thể đủ tiền nhưng vẫn không triển khai được vì thiếu một nguồn lực then chốt.

## 2. Ranh giới

```text
[[Matching fund]]
→ đối ứng nguồn tài chính theo tỷ lệ hoặc điều kiện

[[Conditional cooperation]]
→ hành vi đóng góp phụ thuộc hành vi người khác

[[Commitment ladder]]
→ actor đang ở cấp cam kết nào

Multi-resource matching
→ need nào tương thích với offer nào và tạo thành tổ hợp khả thi không

[[Resource pledge lifecycle]]
→ offer đã hứa, giữ chỗ, bàn giao hay hết hạn
```

## 3. Need–offer matching

### Need

```text
need_id:
resource_category:
specification:
quantity:
unit:
quality_threshold:
skill_or_capacity:
location:
required_window:
priority:
dependencies:
substitution_rule:
acceptance_criteria:
```

### Offer

```text
offer_id:
provider_id:
resource_category:
description:
quantity_or_capacity:
quality_or_skill:
location:
available_window:
conditions:
restrictions:
withdrawal_rule:
related_party_status:
status:
evidence_ids:
```

### Match

```text
match_id:
need_id:
offer_ids:
compatibility_result:
coverage_percentage:
remaining_gap:
conflicts:
dependencies_met:
reviewer:
decision:
```

## 4. Các chiều tương thích

| Chiều | Câu hỏi |
|---|---|
| Type | Có đúng loại nguồn lực không? |
| Specification | Có đạt thông số hoặc kỹ năng không? |
| Quantity | Có đủ số lượng/công suất không? |
| Timing | Có đúng cửa sổ thời gian không? |
| Location | Có ở nơi sử dụng được không? |
| Rights | Có đủ quyền sử dụng/chia sẻ/chuyển giao không? |
| Conditions | Điều kiện của provider có phù hợp không? |
| Integration | Chi phí tích hợp có chấp nhận được không? |
| Dependency | Các nguồn lực bổ trợ khác đã có chưa? |
| Reliability | Offer có còn hiệu lực và đủ độ cứng không? |

Không dùng một điểm similarity đơn giản để thay review chuyên môn ở nguồn lực trọng yếu.

## 5. Substitution và complementarity

### Substitute

Hai nguồn lực có thể thay thế nhau một phần:

```text
20 giờ chuyên gia senior
↔ 50 giờ nhân sự junior + review
```

Nhưng quy tắc thay thế phải được người chịu trách nhiệm chuyên môn phê duyệt.

### Complement

Một nguồn lực chỉ có giá trị khi đi cùng nguồn lực khác:

```text
Máy CNC
+ operator
+ jig
+ vật liệu
+ bản vẽ được duyệt
```

Không nên báo “đã đủ thiết bị” khi các complement thiết yếu còn thiếu.

## 6. Bottleneck resource

Một nguồn lực có thể nhỏ về giá trị tiền nhưng quyết định toàn bộ tiến độ:

- Chữ ký pháp lý.
- Một bộ dữ liệu được phép dùng.
- Slot thử nghiệm tại bệnh viện.
- Chuyên gia chứng nhận.
- Jig hoặc linh kiện đặc thù.

Nên có:

```text
criticality:
- blocking
- high
- medium
- optional
```

Tổng giá trị nguồn lực không cho biết bottleneck đã được giải quyết chưa.

## 7. Partial matching

Một need có thể được phủ bởi nhiều offer:

```text
Need: 100 giờ thiết kế
Offer A: 30 giờ
Offer B: 50 giờ
Offer C: 40 giờ có điều kiện
```

Hệ thống phải ghi:

- Phần chắc chắn.
- Phần có điều kiện.
- Phần trùng lịch.
- Phần vượt nhu cầu.
- Khoảng thiếu còn lại.

Không cộng số lượng trước khi kiểm tra cùng đơn vị, chất lượng và thời gian.

## 8. Matching theo gói

Một provider có thể đưa offer theo gói:

```text
Thiết bị + kỹ thuật viên + vận chuyển
```

Không nên tách thiết bị ra nếu điều kiện yêu cầu phải dùng chung kỹ thuật viên. Tương tự, một địa điểm có thể chỉ được cấp nếu chương trình do bên cung cấp đồng tổ chức.

Record cần hỗ trợ:

```text
bundle_id:
bundle_components:
indivisible:
activation_conditions:
```

## 9. Xung đột và cạnh tranh nguồn lực

Một offer có thể được hứa cho nhiều dự án. Cần kiểm tra:

- Capacity đã bị reserve ở đâu.
- Dự án nào ưu tiên.
- Có được chia sẻ đồng thời không.
- Provider có quyền hủy không.
- Một match mới có làm match cũ mất khả thi không.

Đây là lý do cần nối với [[Resource pledge lifecycle]].

## 10. Matching score chỉ là hỗ trợ quyết định

Có thể tính score nội bộ:

```text
technical_fit
availability_fit
rights_fit
reliability
integration_cost
criticality
conflict_risk
```

Nhưng phải giữ giải thích từng thành phần. Không công bố một con số `92% phù hợp` mà không cho biết vì sao.

## 11. Ví dụ áp dụng

```text
Need N-01:
- máy laser 2 kW;
- cắt thép 6 mm;
- 8 giờ trong tuần 3;
- trong bán kính 50 km.

Offer O-11:
- máy 3 kW;
- rảnh tuần 3;
- cách 35 km;
- cần dự án tự cung cấp file nesting;
- provider vận hành;
- giới hạn 6 giờ.

Kết quả:
- technical fit: đạt;
- time fit: đạt;
- capacity coverage: 75%;
- dependency: thiếu 2 giờ hoặc offer bổ sung;
- decision: partial match.
```

## 12. Quyết định sau matching

```text
Candidate
→ Reviewed
→ Compatible
→ Conditionally compatible
→ Reserved
→ Activated
```

`Compatible` không đồng nghĩa nguồn lực đã có. Chỉ khi offer được reserve/activated theo lifecycle mới có thể dùng trong kế hoạch thực hiện.

## 13. Rủi ro

- Ghép theo tên loại nguồn lực nhưng sai thông số.
- Bỏ qua thời gian và địa điểm.
- Cộng nguồn lực có điều kiện như nguồn lực chắc chắn.
- Không phát hiện cùng một offer bị overbook.
- Chọn nguồn lực miễn phí nhưng chi phí tích hợp cao hơn mua ngoài.
- Tối ưu giá trị tiền thay vì bottleneck.
- Để provider lớn chi phối thiết kế dự án bằng bundle có điều kiện.
- Tự động hóa quá sớm khi taxonomy nguồn lực còn chưa ổn định.

## 14. Mức triển khai

### Pilot

- Spreadsheet `needs`, `offers`, `matches`.
- Review thủ công.
- Mỗi match có lý do và người phê duyệt.

### Nhiều dự án

- Resource taxonomy.
- Availability calendar.
- Capacity reservation.
- Dependency graph.

### Nền tảng

- Matching recommendation.
- Conflict detection.
- Bundle và substitute rules.
- Provenance và lifecycle event log.

## 15. Kết luận

> **Multi-resource matching không tối ưu “tổng giá trị huy động”; nó tìm một tổ hợp nguồn lực đủ đúng để dự án có thể chạy.**

## Khái niệm liên quan

- [[Nguồn lực ngoài tiền - Bản đồ thuật ngữ]]
- [[In-kind contribution]]
- [[Time and labor contribution]]
- [[Data contribution]]
- [[Asset and access contribution]]
- [[Resource pledge lifecycle]]
- [[Matching fund]]
- [[Conditional cooperation]]

## Nguồn tham khảo

- Shen et al. — Ecosystem orchestration practices for industrial firms, 2024: https://arxiv.org/abs/2401.04526
- Addepalli, Andersen & Barnes — Efficient Resource Matching in Heterogeneous Grid Using Resource Vector, 2010: https://arxiv.org/abs/1006.1177

> Các nguồn kỹ thuật chỉ cung cấp tư duy về resource attributes, availability và matching. Khung trong ghi chú này là định nghĩa làm việc riêng cho dự án cộng đồng.
