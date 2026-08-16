---
ai_authored: true
---

# Conditional cooperation

> **Định nghĩa ngắn:** *Conditional cooperation* — hợp tác có điều kiện — là hành vi một người sẵn sàng đóng góp nhiều hơn khi họ tin hoặc quan sát rằng người khác cũng sẽ đóng góp, tuân thủ hoặc chia sẻ gánh nặng.

Khái niệm này mô tả **sự phụ thuộc giữa các cam kết**, không phải hợp đồng pháp lý hay cơ chế thanh toán.

## 1. Cấu trúc cơ bản

```text
Tôi sẵn sàng đóng góp
→ nếu đủ người khác cũng đóng góp
→ hoặc nếu một nhóm chủ chốt thực hiện phần của họ
```

Ví dụ:

- Tôi góp 1 triệu nếu chiến dịch đạt tối thiểu 100 người.
- Doanh nghiệp đối ứng 1 đồng cho mỗi 1 đồng cộng đồng góp.
- Tôi nhận vai trò kỹ thuật nếu đã có người phụ trách vận hành và pháp lý.
- Cư dân tham gia bảo trì nếu chính quyền cung cấp địa điểm và thiết bị.

## 2. Các dạng điều kiện

### Threshold condition — điều kiện ngưỡng

```text
Cam kết được kích hoạt
→ khi đạt số người, số tiền hoặc nguồn lực tối thiểu
```

Ví dụ: all-or-nothing crowdfunding.

### Matching condition — điều kiện đối ứng

```text
Nguồn lực A được đóng góp
→ theo tỷ lệ với nguồn lực B
```

Xem [[Matching fund]].

### Role-completion condition — điều kiện đủ vai trò

Một người chỉ tham gia khi đội hình tối thiểu đã đủ.

### Milestone condition — điều kiện theo mốc

Cam kết được kích hoạt hoặc tiếp tục khi milestone được xác minh.

Xem [[Milestone verification]].

### Reciprocity condition — điều kiện có đi có lại

Người tham gia tiếp tục hợp tác khi người khác cũng tuân thủ cam kết hoặc chuẩn mực chung.

## 3. Không đồng nhất với matching fund

```text
Conditional cooperation
→ mô tả hành vi và động lực phụ thuộc người khác

[[Matching fund]]
→ cơ chế tài chính đối ứng cụ thể
```

Một matching fund có thể khai thác conditional cooperation, nhưng conditional cooperation còn áp dụng cho thời gian, kỹ năng, tuân thủ và vai trò.

## 4. Không đồng nhất với soft/hard commitment

```text
[[Soft commitment và hard commitment]]
→ cam kết bị ràng buộc mạnh đến đâu

Conditional cooperation
→ cam kết phụ thuộc điều kiện tập thể nào
```

Một cam kết có điều kiện có thể rất cứng sau khi kích hoạt, hoặc vẫn mềm nếu người tham gia có quyền rút dễ dàng.

## 5. Không đồng nhất với social proof

```text
[[Social proof và authentic social proof|Social proof]]
→ tôi bị ảnh hưởng vì thấy người khác tham gia

Conditional cooperation
→ cam kết của tôi được xác định rõ là phụ thuộc hành vi người khác
```

Social proof có thể ảnh hưởng tâm lý ngay cả khi không có điều kiện chính thức. Conditional cooperation cần biểu diễn điều kiện phụ thuộc cụ thể.

## 6. Điều kiện phải có thể kiểm tra

Không nên viết:

> “Tôi sẽ góp khi cộng đồng đủ ủng hộ.”

Nên viết:

```text
Tôi cam kết góp 20 giờ thiết kế
nếu trước ngày 30/09:
- có ít nhất 3 thành viên vận hành đã xác minh;
- ngân sách pilot đạt 80 triệu;
- scope V1 không thay đổi trọng yếu.
```

Một điều kiện tốt cần:

- Chỉ số.
- Ngưỡng.
- Thời hạn.
- Nguồn dữ liệu.
- Người xác nhận.
- Quy tắc khi đạt một phần.
- Quy tắc khi điều kiện thay đổi.

## 7. Coordination problem

Nhiều người có thể cùng muốn dự án xảy ra nhưng không ai đi trước vì sợ:

- Mình là người duy nhất đóng góp.
- Người khác free-ride.
- Dự án không đủ nguồn lực.
- Vai trò thiết yếu còn trống.
- Tiền bị khóa dù mục tiêu không đạt.

Thiết kế conditional cooperation giúp biến sự chờ đợi thành cam kết có điều kiện có thể quan sát.

## 8. Free-riding và crowding-out

### Free-riding

Một người hưởng lợi nhưng không đóng góp, kỳ vọng người khác chịu chi phí.

### Crowding-out

Một nguồn lực lớn hoặc trợ cấp có thể làm người khác giảm đóng góp vì nghĩ dự án đã đủ tiền hoặc trách nhiệm thuộc bên tài trợ.

Do đó matching và threshold phải được thiết kế cẩn thận:

- Công bố phần còn thiếu.
- Không làm mất vai trò của đóng góp nhỏ.
- Tránh để một whale khiến cộng đồng ngừng tham gia.
- Phân biệt mục tiêu tiền với mục tiêu số người hoặc độ phân tán.

## 9. Sequential và simultaneous commitment

### Sequential

Người sau quan sát người trước rồi quyết định.

Ưu điểm: tạo đà và social proof.

Rủi ro: herd behavior và lợi thế quá lớn cho tín hiệu ban đầu.

### Simultaneous / sealed

Cam kết được thu trong một khoảng rồi công bố hoặc kích hoạt cùng lúc.

Ưu điểm: giảm áp lực chạy theo đám đông.

Rủi ro: ít social proof trong quá trình huy động.

Có thể kết hợp:

```text
Thu pre-commitment riêng
→ xác minh
→ công bố tổng hợp
→ mở giai đoạn kích hoạt
```

## 10. Trạng thái cam kết có điều kiện

```text
Draft
→ Confirmed
→ Waiting for conditions
→ Partially satisfied
→ Activated
→ Fulfilled
→ Conditions failed
→ Expired
→ Withdrawn under allowed rule
```

Không coi `Conditions failed` là người tham gia thất hứa.

## 11. Data schema gợi ý

```text
conditional_commitment_id:
actor_id:
project_id:
commitment_object:
resource_type:
amount_or_quantity:
condition_type:
condition_expression:
threshold:
measurement_source:
verification_rule:
deadline:
activation_time:
withdrawal_rule:
refund_rule:
status:
evidence_ids:
```

Điều kiện nên có biểu diễn máy đọc được khi có thể, nhưng vẫn cần bản mô tả dễ hiểu cho người tham gia.

## 12. Áp vào nền tảng

### All-or-nothing

```text
Đủ ngưỡng
→ tất cả cam kết tiền được kích hoạt

Không đủ ngưỡng
→ không thu hoặc hoàn theo rule
```

### Conditional resource pool

```text
Kỹ thuật: 200 giờ nếu có project lead
Thiết bị: 3 tháng nếu có bảo hiểm
Địa điểm: 6 tuần nếu có giấy phép
Matching: 1:1 đến trần 100 triệu
```

Nền tảng phải hiển thị không chỉ tổng tiền mà cả **đồ thị phụ thuộc nguồn lực**.

## 13. Dấu hiệu cảnh báo

- Điều kiện mơ hồ hoặc không đo được.
- Thay ngưỡng sau khi đã nhận cam kết.
- Không nói ai xác nhận điều kiện.
- Dùng social proof chưa xác minh để kích hoạt cam kết.
- Không có thời hạn.
- Không có quy tắc khi chỉ đạt một phần.
- Giữ tiền khi điều kiện thất bại mà không có thỏa thuận.
- Điều kiện phụ thuộc bên liên quan tự xác nhận.
- Matching fund công bố lớn nhưng trần đối ứng rất thấp hoặc điều kiện ẩn.

## 14. Kết luận cho dự án

> **Conditional cooperation biến câu “tôi sẽ tham gia nếu những người khác cũng tham gia” thành một cam kết có điều kiện, có thể ghi nhận, kiểm tra và kích hoạt minh bạch.**

## Khái niệm liên quan

- [[Thang cam kết và tín hiệu - Bản đồ thuật ngữ]]
- [[Commitment ladder]]
- [[Soft commitment và hard commitment]]
- [[Social proof và authentic social proof]]
- [[Matching fund]]
- [[Milestone verification]]
- [[Escrow]]

## Nguồn tham khảo

- Fischbacher, Gächter & Fehr — Are People Conditionally Cooperative?, 2001: https://doi.org/10.1016/S0165-1765(01)00394-9
