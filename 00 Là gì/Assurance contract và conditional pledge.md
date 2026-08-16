---
ai_authored: true
---

# Assurance contract và conditional pledge

> **Định nghĩa ngắn:** *Assurance contract* là một cơ chế trong đó người tham gia cam kết đóng góp với điều kiện một provision point được đáp ứng trong thời hạn xác định; nếu điều kiện không đạt, cam kết không được kích hoạt hoặc nguồn lực được hoàn trả/release theo rule. *Conditional pledge* là cam kết cụ thể của một actor phụ thuộc vào các điều kiện đó.

Assurance contract kết hợp nhiều thành phần đã có, nhưng không đồng nhất với từng thành phần riêng lẻ.

## 1. Cấu trúc cơ bản

```text
Dự án công bố kết quả chung
→ công bố provision point
→ actor đưa conditional pledge
→ hệ thống theo dõi tổng cam kết hợp lệ

Đạt provision point trước deadline
→ activate pledges
→ collect/release resources

Không đạt
→ không collect, refund hoặc release reservations
```

## 2. Các thành phần bắt buộc

Một assurance contract cần:

1. Kết quả chung được mô tả rõ.
2. [[Provision point và threshold mechanism|Provision point]] có căn cứ.
3. Contribution đủ điều kiện.
4. Deadline.
5. Conditional pledges.
6. Cách đo và người xác minh.
7. Activation rule.
8. Failure/refund/release rule.
9. Change control.
10. Cơ chế xử lý tranh chấp.

Thiếu các thành phần này thì mới chỉ là câu “chỉ thu khi đủ người”.

## 3. Ranh giới thuật ngữ

```text
[[Conditional cooperation]]
→ động lực: tôi tham gia nếu người khác tham gia

Conditional pledge
→ record: tôi cam kết gì, theo điều kiện nào

[[Provision point và threshold mechanism]]
→ mức tập thể nào được xem là đủ

[[All-or-nothing và keep-it-all|All-or-nothing]]
→ rule xử lý khi đạt/không đạt

Assurance contract
→ cấu trúc kết hợp pledge + provision point + activation + refund/release

[[Escrow]]
→ ai giữ tài sản trong lúc chờ
```

## 4. Conditional pledge không mặc nhiên là hard commitment

Một pledge có thể:

```text
Soft:
“Tôi dự kiến góp 20 giờ nếu đủ đội.”

Harder:
“Tôi ký thỏa thuận giữ lịch 20 giờ; sau khi đạt ngưỡng,
việc rút không đúng rule có hậu quả xác định.”
```

Xem [[Soft commitment và hard commitment]].

Assurance contract phải nói rõ actor đang đưa:

- Expression of intent.
- Revocable pledge.
- Payment authorization.
- Deposit.
- Resource reservation.
- Contractual obligation.

Không trình bày tất cả là “đã huy động”.

## 5. Assurance contract với tiền

Các cách triển khai có thể gồm:

### Authorization then capture

Người góp cho phép thu; chỉ capture khi đạt provision point.

### Funds held then released/refunded

Tiền được bên phù hợp giữ, rồi giải phóng hoặc hoàn theo rule.

### Invoice after activation

Tổ chức cam kết thanh toán khi được thông báo điều kiện đã đạt.

Mỗi phương án khác nhau về độ cứng, phí, rủi ro thất bại thanh toán và yêu cầu pháp lý.

## 6. Assurance contract với nguồn lực ngoài tiền

Ví dụ:

```text
Kỹ sư A:
20 giờ nếu project lead và venue đã confirmed.

Xưởng B:
5 ngày máy nếu bảo hiểm và operator đã reserved.

Tổ chức C:
Dataset access nếu ethics review đạt.
```

Khi provision point đạt:

```text
Waiting for conditions
→ Activated
→ Reserved
→ Delivered
```

Xem [[Resource pledge lifecycle]].

Không thể “hoàn lại” thời gian đã tiêu hoặc dữ liệu đã chia sẻ theo cách giống tiền, nên activation phải xảy ra trước delivery khi có thể.

## 7. Assurance contract nhiều chiều

Ví dụ:

```text
Activate khi:
- tiền hợp lệ ≥ 100 triệu;
- unique contributors ≥ 50;
- giờ kỹ thuật Reserved ≥ 120;
- venue = Reserved;
- project lead = Confirmed.
```

Đây là assurance contract dựa trên một resource bundle, không chỉ funding goal.

## 8. Assurance contract và demand validation

Đạt assurance threshold có thể là bằng chứng về commitment, nhưng không tự động chứng minh:

- Người dùng sẽ sử dụng lặp lại.
- Offer phù hợp thị trường.
- Outcome sẽ xuất hiện.
- Contributor đại diện target population.
- Dự án có năng lực thực hiện.

Phải ghi rõ pledge đến từ:

```text
beneficiary
customer
sponsor
investor
founder
related party
resource provider
```

Xem [[Proof of need và demand validation]].

## 9. Failure rule

Khi không đạt provision point:

```text
Pledge
→ Conditions failed

Payment authorization
→ cancelled

Funds held
→ refunded

Reserved equipment/time
→ released

Delivered resource
→ xử lý theo agreement riêng
```

`Conditions failed` không có nghĩa actor thất hứa.

## 10. Grace period và payment failure

Sau khi đạt ngưỡng, một số pledge có thể không thực hiện được:

- Thẻ thanh toán lỗi.
- Actor mất quyền đại diện.
- Resource không còn available.
- Phát hiện related party bị loại.
- Evidence bị bác bỏ.

Cần rule:

```text
revalidation window
replacement period
grace period
minimum post-failure threshold
recalculation rule
```

Không công bố “đã đạt” trước khi kiểm tra khả năng fulfilment thực tế.

## 11. Dominant assurance contract

*Dominant assurance contract* là một biến thể thêm phần thưởng cho người cam kết nếu dự án không đạt provision point, nhằm làm việc cam kết trở nên hấp dẫn hơn việc đứng ngoài.

Trong repo này, đây là khái niệm mở rộng, chưa phải cơ chế mặc định vì có thêm rủi ro:

- Ai tài trợ bonus khi thất bại?
- Có khuyến khích chiến dịch giả để nhận bonus không?
- Có tạo arbitrage hoặc nhiều tài khoản không?
- Pháp lý của bonus là gì?

Không gọi assurance contract thông thường là dominant assurance contract.

## 12. Điều khoản thay đổi

Nếu dự án thay đổi:

- Scope.
- Provision point.
- Deadline.
- Beneficiary.
- Người giữ tiền.
- Contributor benefit.
- Activation rule.

thì phải xác định:

```text
minor change
→ tiếp tục theo rule

material change
→ tái đồng ý hoặc cho quyền rút
```

Không sử dụng sự im lặng như đồng ý cho thay đổi trọng yếu nếu chưa công bố từ đầu.

## 13. Verification và decision rule

```text
Threshold calculation
→ reviewer kiểm tra dữ liệu
→ loại contribution không hợp lệ
→ xác định result
→ second approver phê duyệt activation
→ system ghi decision log
→ collect/release/refund
```

Xem [[Verification protocol và decision rule]].

## 14. Data schema gợi ý

```text
assurance_contract_id:
collective_outcome:
provision_point_id:
valid_from:
deadline:
eligible_contribution_types:
pledge_form:
collection_or_reservation_method:
activation_rule:
verification_rule:
failure_rule:
refund_or_release_rule:
grace_period:
material_change_rule:
dispute_route:
status:
evidence_ids:

conditional_pledge_id:
actor_id:
resource_type:
amount_or_quantity:
conditions:
withdrawal_rule:
expires_at:
commitment_strength:
related_party_status:
status:
evidence_ids:
```

## 15. Dấu hiệu cảnh báo

- Provision point không có căn cứ.
- Gọi soft pledge là nguồn lực đã có.
- Không có deadline.
- Không công bố ai xác minh.
- Không có rule khi payment fail sau activation.
- Thay đổi scope sau khi đạt ngưỡng.
- Giữ tiền khi điều kiện thất bại mà không có thỏa thuận.
- Đếm related-party pledge để tạo social proof.
- Kích hoạt thiết bị/dữ liệu trước khi đủ điều kiện bảo vệ.
- Gọi assurance contract là bảo đảm dự án sẽ thành công.

## 16. Kết luận cho dự án

> **Assurance contract không bảo đảm outcome; nó bảo đảm rằng một actor không phải thực hiện cam kết đơn độc trước khi điều kiện tập thể đã được xác định và kiểm tra.**

## Khái niệm liên quan

- [[Cơ chế phối hợp tập thể - Bản đồ thuật ngữ]]
- [[Conditional cooperation]]
- [[Provision point và threshold mechanism]]
- [[All-or-nothing và keep-it-all]]
- [[Soft commitment và hard commitment]]
- [[Resource pledge lifecycle]]
- [[Escrow]]
- [[Verification protocol và decision rule]]

## Nguồn tham khảo

- Mark Bagnoli & Barton Lipman — Provision of Public Goods, 1989: https://doi.org/10.2307/2297552
- Alexander Tabarrok — The Private Provision of Public Goods via Dominant Assurance Contracts, 1998: https://doi.org/10.1007/BF02351765
