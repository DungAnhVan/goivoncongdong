# Onboarding thang cam kết và tín hiệu

> **Mục tiêu:** Giúp thành viên mới phân loại đúng hành vi tham gia, đánh giá tín hiệu và thiết kế cam kết có điều kiện mà không nhập nhằng với demand validation, evidence verification hoặc outcome.

## 1. Kết quả bắt buộc

Người hoàn thành onboarding phải tạo được:

```text
1. Actor-role map
2. Commitment register
3. Commitment ladder classification
4. Signal interpretation table
5. Authentic social proof display
6. Conditional cooperation rule
7. Overclaim review
```

Không hoàn thành nếu chỉ vẽ funnel hoặc gắn điểm cho từng hành vi.

## 2. Tài liệu phải đọc

```text
1. [[Thang cam kết và tín hiệu - Bản đồ thuật ngữ]]
2. [[Commitment ladder]]
3. [[Soft commitment và hard commitment]]
4. [[Costly signaling và cheap talk]]
5. [[Social proof và authentic social proof]]
6. [[Conditional cooperation]]
7. [[Proof of need và demand validation]]
8. [[Evidence ledger và provenance]]
9. [[Matching fund]]
```

## 3. Bài tập pilot

Giả định dự án công bố:

> “Dự án đã được 12.000 người ủng hộ, có 500 khách hàng, 20 đối tác và huy động được 2 tỷ đồng.”

Dữ liệu thô thực tế:

```text
- 12.000 lượt xem trang;
- 2.300 lượt thích;
- 900 email đăng ký;
- 180 người tham gia demo;
- 60 người ký form nói dự kiến sử dụng;
- 24 người đặt cọc có hoàn lại;
- 8 doanh nghiệp ký pilot trả phí;
- 20 logo xuất hiện trên trang;
- trong 20 logo: 5 nhà tài trợ, 3 nhà cung cấp, 4 mentor,
  2 khách hàng, 6 đơn vị chỉ tham dự sự kiện;
- 2 tỷ gồm 1,2 tỷ investment, 500 triệu grant,
  200 triệu founder contribution và 100 triệu pre-order.
```

Người onboarding phải viết lại toàn bộ tuyên bố mà không phóng đại.

## 4. Ngày 1 — Actor và vai trò

Tạo bảng:

```text
actor_id
actor_name
role
relationship_to_project
target_segment_status
conflict_of_interest
verification_level
```

Phải tách tối thiểu:

- Founder/team.
- Beneficiary.
- User.
- Customer/payer.
- Donor.
- Funder.
- Investor.
- Supplier.
- Verifier.
- Public endorser.

Một actor có thể có nhiều vai trò, nhưng mỗi hành vi phải ghi vai trò liên quan.

## 5. Ngày 2 — Commitment register

Mỗi hành vi phải tạo record:

```text
commitment_id
actor_id
project_id
commitment_stage
commitment_type
resource_type
amount_or_quantity
conditions
withdrawal_rule
withdrawal_cost
offer_version
created_at
expires_at
status
evidence_ids
```

Yêu cầu:

- Không gộp nhiều người vào một record.
- Không gộp nhiều loại tiền vào một dòng.
- Tách promised, activated và fulfilled.
- Ghi điều kiện và ngày hết hạn.

## 6. Ngày 3 — Phân loại ladder và hardness

Với mỗi record, xác định:

```text
Attention / Interest / Endorsement / Trial /
Pre-commitment / Resource contribution /
Transaction-Investment / Continued participation
```

Sau đó mô tả độ cứng:

```text
S0 — expression only
S1 — revocable without consequence
S2 — revocable with friction/reputation cost
S3 — resource reserved or deposit at risk
S4 — contractual/substantial obligation
```

Phải giải thích bằng quyền rút và hậu quả, không chỉ gắn nhãn.

## 7. Ngày 4 — Signal interpretation

Tạo bảng:

| Hành vi | Claim có thể hỗ trợ | Claim không được suy ra | Independence | Limitation |
|---|---|---|---|---|
| Đặt cọc | Willingness to pay cho offer | Outcome | ... | ... |
| Investment | Kỳ vọng tài chính | User demand | ... | ... |
| Endorsement | Public support | Năng lực thực hiện | ... | ... |

Phải có ít nhất:

- Một costly signal nhưng evidence yếu.
- Một hard commitment nhưng không phải demand signal.
- Một cheap-talk signal hữu ích cho research.
- Một hành vi của bên liên quan.
- Một tín hiệu đã hết hạn.

## 8. Ngày 5 — Authentic social proof display

Thiết kế khối hiển thị công khai, không dùng tổng “người ủng hộ”.

Ví dụ:

```text
Attention: 12.000 lượt xem đủ điều kiện
Interest: 900 đăng ký nhận cập nhật
Trial: 180 người tham gia demo
Soft pre-commitment: 60 dự kiến sử dụng
Harder pre-commitment: 24 đặt cọc có hoàn lại
Purchase: 8 pilot trả phí

Nguồn vốn:
Investment: 1,2 tỷ
Grant: 500 triệu
Founder contribution: 200 triệu
Pre-order: 100 triệu
```

Phải hiển thị:

- Định nghĩa chỉ số.
- Thời gian.
- Offer version.
- Đếm trùng.
- Bên liên quan.
- Withdrawal/expiry.
- Link evidence summary.

## 9. Conditional cooperation exercise

Thiết kế một cam kết:

> Nhà tài trợ đối ứng 1:1 tối đa 100 triệu nếu cộng đồng đạt đủ điều kiện.

Phải ghi rõ:

```text
eligible contribution
excluded related parties
minimum participant count
concentration cap
threshold
deadline
verification source
activation rule
partial-achievement rule
refund/withdrawal rule
status transitions
```

Sau đó chỉ ra:

```text
Conditional cooperation
→ hành vi phụ thuộc cam kết người khác

Matching fund
→ cơ chế tài chính triển khai sự phụ thuộc đó
```

## 10. Overclaim review

Red team phải tìm tối thiểu mười lỗi:

- Attention bị gọi là demand.
- Follower bị gọi là community member.
- LOI bị gọi là contract.
- Deposit có hoàn lại bị gọi là revenue.
- Investor bị gọi là customer.
- Grant bị gộp vào investment.
- Founder contribution bị hiển thị như independent support.
- Logo không rõ vai trò.
- Commitment hết hạn vẫn được đếm.
- Nhiều hành vi của một actor bị đếm thành nhiều người.
- Social proof bị dùng làm outcome evidence.
- Tổng tiền che mức tập trung.

## 11. Decision memo

Người onboarding phải trả lời:

```text
Dữ liệu hiện tại đủ để quyết định gì?
Dữ liệu chưa đủ để quyết định gì?
Commitment stage nào cần tăng tiếp?
Cần test offer nào?
Cần xác minh record nào?
Social proof nào phải sửa hoặc gỡ?
```

Không được kết luận chung chung “dự án có traction tốt”.

## 12. Tiêu chuẩn hoàn thành

Đạt khi:

- Mỗi hành vi được xếp đúng loại.
- Hardness được giải thích bằng nghĩa vụ thực.
- Claim và signal được liên kết có giới hạn.
- Demand validation không bị thay bằng social proof.
- Evidence verification không bị thay bằng signaling theory.
- Matching fund không bị gọi là conditional cooperation nói chung.
- Có dữ liệu withdrawal, expiry và related parties.
- Tuyên bố công khai được viết lại trung thực.

Không đạt khi:

- Dùng một điểm engagement duy nhất.
- Xếp investment là cấp cao nhất cho mọi mục đích.
- Cho rằng costly signal luôn thật.
- Cho rằng hard commitment luôn tốt.
- Cho rằng nhiều người tham gia nghĩa là dự án có outcome.

## 13. Kết luận

> **Năng lực của thành viên không nằm ở việc biết tên “commitment ladder” hay “social proof”, mà ở khả năng ngăn một hành vi yếu bị kể thành một bằng chứng mạnh hơn bản chất của nó.**
