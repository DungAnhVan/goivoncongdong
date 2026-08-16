---
ai_authored: true
---

# Provision point và threshold mechanism

> **Định nghĩa ngắn:** *Provision point* là mức tối thiểu của tiền, nguồn lực, số người, quyền hoặc điều kiện mà tại đó một dự án hay kết quả chung trở nên khả thi. *Threshold mechanism* là quy tắc dùng ngưỡng đó để quyết định khi nào cam kết được kích hoạt, nguồn lực được giải phóng hoặc dự án được phép đi tiếp.

Provision point không nhất thiết là một con số tiền.

## 1. Từ fundraising goal đến provision point

```text
Fundraising goal
→ con số muốn huy động

Provision point
→ mức tối thiểu thực sự cần để tạo ra kết quả đã hứa
```

Hai con số có thể khác nhau.

Ví dụ:

```text
Mục tiêu truyền thông: 500 triệu

Nhưng mức khả thi tối thiểu:
- 300 triệu tiền mặt;
- 200 giờ kỹ thuật;
- địa điểm 6 tuần;
- giấy phép;
- 100 người dùng pilot.
```

Nếu thiếu giấy phép thì đạt 500 triệu vẫn chưa đủ provision point.

## 2. Các loại ngưỡng

### Financial threshold

Mức tiền tối thiểu.

### Participant threshold

Số người hoặc số tổ chức tối thiểu.

### Diversity threshold

Yêu cầu độ rộng hoặc tính đại diện:

- tối thiểu số nhóm địa lý;
- số đơn vị độc lập;
- số beneficiary xác minh;
- giới hạn một actor chiếm tỷ trọng quá lớn.

### Resource threshold

Mức tối thiểu của giờ lao động, thiết bị, dữ liệu, vật liệu hoặc capacity.

### Role-completion threshold

Đủ các vai trò thiết yếu:

```text
project lead
+ finance/control
+ technical owner
+ legal/compliance
```

### Legal or authorization threshold

Đã có giấy phép, quyền truy cập, consent hoặc phê duyệt cần thiết.

### Quality threshold

Nguồn lực hoặc output phải đạt tiêu chuẩn tối thiểu, không chỉ đủ số lượng.

### Multi-dimensional threshold

Một bundle nhiều điều kiện cùng phải đạt.

## 3. Hard threshold và soft threshold

```text
Hard threshold
→ thiếu một điều kiện là dự án không thể hoặc không được phép chạy

Soft threshold
→ thiếu điều kiện vẫn chạy được nhưng scope, tốc độ hoặc chất lượng giảm
```

Ví dụ:

```text
Giấy phép vận hành
→ hard threshold

Thêm 50 giờ truyền thông
→ có thể là soft threshold
```

Không nên gộp cả hai vào cùng một phần trăm “đã hoàn thành 82%”.

## 4. Threshold đơn và threshold bundle

### Threshold đơn

```text
Đạt 100 triệu trước ngày 30/09
```

### Threshold bundle

```text
Tiền mặt ≥ 100 triệu
AND giờ kỹ thuật accepted ≥ 120
AND venue status = Reserved
AND project lead status = Confirmed
```

Trong dự án này, threshold bundle thường có ý nghĩa hơn vì tiền chỉ là một loại nguồn lực.

Xem [[Multi-resource matching]] và [[Resource pledge lifecycle]].

## 5. Provision point phải bắt nguồn từ execution model

Không chọn ngưỡng chỉ vì:

- Con số tròn đẹp.
- Muốn tạo cảm giác cấp bách.
- Thấy chiến dịch khác dùng.
- Muốn tỷ lệ hoàn thành trông cao.

Provision point phải được suy từ:

```text
Scope tối thiểu
→ activities bắt buộc
→ resource needs
→ dependencies
→ bottlenecks
→ contingency hợp lý
→ provision point
```

Mỗi thành phần nên có [[Claim-evidence mapping|claim–evidence mapping]].

## 6. Quy tắc đo ngưỡng

Một threshold spec cần ghi:

```text
threshold_id:
metric:
unit:
operator:
target_value:
eligible_statuses:
eligible_actor_types:
measurement_source:
calculation_time:
deadline:
verifier:
rounding_rule:
related_party_rule:
```

Ví dụ, không chỉ ghi `120 giờ kỹ thuật`, mà phải nói giờ nào được tính:

```text
Chỉ tính giờ:
- thuộc skill đã phê duyệt;
- có scope;
- provider đã xác minh;
- trạng thái Reserved hoặc Accepted theo rule;
- không trùng lịch;
- còn hiệu lực tại deadline.
```

## 7. Partial satisfaction

Không phải mọi ngưỡng chỉ có `đạt` hoặc `không đạt`.

Có thể thiết kế:

```text
< 60%
→ không kích hoạt

60–99%
→ chuyển sang scope tối thiểu đã công bố trước

≥ 100%
→ kích hoạt full scope
```

Nhưng fallback scope phải được xác định trước. Không được nhận cam kết cho full scope rồi sau đó tự ý đổi thành dự án khác.

## 8. Nested và staged provision points

Dự án nhiều giai đoạn có thể dùng:

```text
P0 — đủ điều kiện lập hồ sơ
P1 — đủ nguồn lực chạy pilot
P2 — đủ bằng chứng mở rộng
P3 — đủ năng lực vận hành lâu dài
```

Mỗi provision point phải gắn với một quyết định khác nhau.

Không nhầm với [[Milestone verification]]:

```text
Provision point
→ điều kiện nguồn lực trước khi bắt đầu hoặc kích hoạt

Milestone verification
→ kiểm tra mốc sau khi thực hiện
```

## 9. Dynamic threshold

Có trường hợp ngưỡng cần thay đổi vì:

- Giá đầu vào thay đổi.
- Scope được cộng đồng phê duyệt thay đổi.
- Một nguồn lực được thay thế.
- Quy định pháp lý mới.
- Bằng chứng mới cho thấy dự toán sai.

Thay đổi chỉ hợp lệ nếu có:

```text
change reason
→ impact analysis
→ quyền phản đối
→ quyền rút/hoàn
→ version mới
→ lịch sử version cũ
```

Không sửa ngưỡng âm thầm khi chiến dịch gần thất bại.

## 10. Threshold và tính đại diện

Một ngưỡng tiền có thể đạt nhờ một contributor lớn nhưng không cho thấy sự ủng hộ rộng.

Có thể bổ sung:

```text
minimum_unique_contributors
maximum_single_contributor_share
minimum_target-segment_participants
minimum_geographic_coverage
```

Nhưng các điều kiện này không tự động chứng minh demand. Xem [[Proof of need và demand validation]].

## 11. Threshold với nguồn lực ngoài tiền

Ví dụ:

```text
Need:
- 1 máy trong 5 ngày;
- 1 operator;
- 200 kg vật liệu.

Offer:
- máy 10 ngày nhưng không operator;
- operator 3 ngày;
- vật liệu đủ.

Kết luận:
- tổng value lớn;
- provision point chưa đạt vì operator coverage thiếu 2 ngày.
```

Threshold phải đánh giá **khả năng sử dụng**, không chỉ gross value.

## 12. Điều kiện kích hoạt

Một threshold mechanism hoàn chỉnh phải nói:

```text
Khi nào đo?
Dữ liệu nào được tính?
Ai xác nhận?
Đạt ngưỡng thì điều gì được kích hoạt?
Không đạt thì điều gì xảy ra?
Đạt một phần thì sao?
Có grace period không?
Có thể thay thế resource không?
Ai có quyền sửa rule?
```

## 13. Rủi ro thiết kế

- Ngưỡng thấp hơn chi phí thực để dễ thành công.
- Ngưỡng cao giả tạo để tạo social proof khi đạt.
- Chỉ đo tiền, bỏ qua nguồn lực blocking.
- Đếm pledge mềm như nguồn lực chắc chắn.
- Thay đổi ngưỡng sau khi nhận cam kết.
- Không công bố fallback scope.
- Một actor liên quan tự tạo contribution để đạt ngưỡng.
- Đếm cùng nguồn lực ở nhiều threshold.
- Không tính chi phí tích hợp và contingency.

## 14. Template provision point

```text
collective_outcome:
minimum_viable_scope:
threshold_bundle:
- component:
  metric:
  target:
  hard_or_soft:
  eligible_statuses:
  evidence:
deadline:
measurement_time:
verifier:
activation_decision:
partial_rule:
failure_rule:
change_control:
```

## 15. Kết luận cho dự án

> **Provision point không phải con số marketing. Nó là phát biểu có thể kiểm tra về tổ hợp tối thiểu khiến lời hứa của dự án trở nên khả thi.**

## Khái niệm liên quan

- [[Cơ chế phối hợp tập thể - Bản đồ thuật ngữ]]
- [[Collective action problem và free-rider problem]]
- [[All-or-nothing và keep-it-all]]
- [[Assurance contract và conditional pledge]]
- [[Multi-resource matching]]
- [[Resource pledge lifecycle]]
- [[Milestone verification]]
- [[Proof of need và demand validation]]

## Nguồn tham khảo

- Mark Bagnoli & Barton Lipman — Provision of Public Goods: Fully Implementing the Core through Private Contributions, 1989: https://doi.org/10.2307/2297552
- Douglas Davis & Charles Holt — *Experimental Economics*, provision point mechanisms, 1993.
