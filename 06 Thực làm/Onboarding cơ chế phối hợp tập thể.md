# Onboarding cơ chế phối hợp tập thể

> **Mục tiêu:** Giúp thành viên mới biến một câu chung chung như “đạt đủ người thì triển khai” thành một cơ chế có chẩn đoán vấn đề, provision point, eligibility, activation, allocation, refund/release và verification rule có thể vận hành.

## 1. Kết quả bắt buộc

Người hoàn thành onboarding phải tạo được:

```text
1. Collective action diagnosis
2. Actor–benefit–cost map
3. Provision point specification
4. AON/KIA/hybrid comparison
5. Assurance contract draft
6. Selective incentive register
7. Matching/QF allocation simulation
8. Mechanism risk and control matrix
9. Activation decision log
10. Failure and change-control plan
```

Không hoàn thành nếu chỉ chọn tên cơ chế hoặc vẽ funnel đẹp.

## 2. Tài liệu phải đọc

```text
1. [[Cơ chế phối hợp tập thể - Bản đồ thuật ngữ]]
2. [[Collective action problem và free-rider problem]]
3. [[Provision point và threshold mechanism]]
4. [[All-or-nothing và keep-it-all]]
5. [[Assurance contract và conditional pledge]]
6. [[Selective incentives và contributor benefits]]
7. [[Matching fund]]
8. [[Quadratic funding]]
9. [[Conditional cooperation]]
10. [[Multi-resource matching]]
11. [[Verification protocol và decision rule]]
```

## 3. Case thực hành

Một nhóm tuyên bố:

> “Dự án thư viện công cụ cộng đồng đã đạt 82% mục tiêu và có hơn 300 người ủng hộ, nên có thể bắt đầu ngay.”

Dữ liệu thô:

```text
Mục tiêu công bố: 500 triệu
Tiền đã chuyển: 210 triệu
Pledge có hoàn lại: 120 triệu
Một doanh nghiệp hứa match tối đa 100 triệu
Founder tự góp: 60 triệu
Thiết bị được offer: 8 máy
Thiết bị đã reserved: 2 máy
Giờ kỹ thuật được hứa: 300 giờ
Giờ kỹ thuật đã có scope và lịch: 80 giờ
Venue: có thư bày tỏ quan tâm, chưa có lịch
Bảo hiểm: chưa có
Người đăng ký nhận tin: 300
Người đặt cọc membership: 35
Người dùng pilot xác minh: 18
```

Mô hình thực hiện tối thiểu cần:

```text
250 triệu usable cash
+ 4 máy Accepted/Reserved
+ 160 giờ kỹ thuật Reserved
+ venue 8 tuần
+ bảo hiểm
+ tối thiểu 30 user pilot xác minh
```

## 4. Bài tập 1 — Chẩn đoán collective action problem

Không được mặc định vấn đề là free-rider.

Hãy phân loại:

- Coordination failure.
- Under-provision.
- Fragmentation.
- Holdout/bottleneck.
- Trust problem.
- Demand uncertainty.
- Crowding-out.

Sản phẩm:

```text
problem_id
observed_pattern
affected_actor_groups
alternative_explanations
evidence
mechanism_candidate
what_the_mechanism_cannot_fix
```

## 5. Bài tập 2 — Actor–benefit–cost map

Phải tách:

```text
beneficiary
user
member
contributor
sponsor
founder
resource provider
affected community
verifier
decision-maker
```

Ghi rõ:

- Ai hưởng lợi dù không góp?
- Ai chịu chi phí cố định?
- Ai đang góp ngoài tiền?
- Ai có quyền quyết định?
- Ai bị loại nếu benefit gắn với membership?

## 6. Bài tập 3 — Provision point specification

Không dùng `500 triệu` làm provision point nếu execution model yêu cầu bundle khác.

Phải tạo:

```text
minimum_viable_scope
threshold_bundle
hard_thresholds
soft_thresholds
eligible_lifecycle_statuses
measurement_sources
verifier
deadline
partial_rule
failure_rule
```

Kết luận phải nói rõ:

```text
Đã đạt tiền chưa?
Đã đạt usable cash chưa?
Đã đạt resource bundle chưa?
Resource blocking nào còn thiếu?
Tuyên bố “82%” có ý nghĩa gì và che điều gì?
```

## 7. Bài tập 4 — So sánh AON, KIA và hybrid

Lập bảng:

| Rule | Ai chịu rủi ro thiếu hụt? | Output khi thiếu mục tiêu | Refund/release | Điều kiện áp dụng |
|---|---|---|---|---|
| AON | | | | |
| KIA | | | | |
| Hybrid | | | | |

Phải chọn một rule và nêu lý do dựa trên divisibility và fixed cost, không dựa trên khả năng truyền thông.

## 8. Bài tập 5 — Assurance contract draft

Tạo một bản một trang gồm:

```text
collective_outcome
provision_point
eligible_contributions
conditional_pledge form
collection/reservation method
activation rule
verification rule
failure rule
refund/release rule
grace period
material change rule
dispute route
```

Phải xử lý riêng:

- Tiền.
- Thiết bị.
- Giờ kỹ thuật.
- Venue.
- Matching commitment.

## 9. Bài tập 6 — Selective incentive register

Dự án đề xuất:

```text
Góp 500.000 → badge
Góp 2 triệu → membership 1 năm
Góp 10 triệu → quyền biểu quyết
Góp dữ liệu → access báo cáo
Góp máy → logo “đối tác chiến lược”
```

Người onboarding phải kiểm tra:

- Benefit có đúng bản chất quan hệ không?
- Có biến quyền cơ bản thành đặc quyền không?
- Có làm méo demand signal không?
- Có tạo chi phí fulfilment không?
- Logo có bị hiểu thành endorsement không?
- Quyền biểu quyết có quá phụ thuộc tiền không?

## 10. Bài tập 7 — Matching fund và QF simulation

### Matching fund

Mô phỏng:

```text
1:1
cap 100 triệu
minimum 30 unique contributors
founder và related parties không đủ điều kiện
chỉ tính contribution Fulfilled
```

### Quadratic funding

Dùng ba project giả và tính:

```text
direct contribution
raw quadratic score
raw match
pool scaling
project cap
result sau related-party exclusion
```

Mục tiêu không phải khuyến nghị dùng QF ngay, mà để thấy công thức bị ảnh hưởng thế nào bởi:

- Một whale.
- Nhiều contributor nhỏ.
- Sybil.
- Contribution chéo.
- Project cap.

## 11. Bài tập 8 — Risk and control matrix

Tối thiểu phải có:

| Risk | Trigger | Preventive control | Detective control | Decision owner | Evidence |
|---|---|---|---|---|---|
| Fake contributions | | | | | |
| Related-party funding | | | | | |
| Threshold manipulation | | | | | |
| Resource overbooking | | | | | |
| Payment failure after activation | | | | | |
| Hidden scope change | | | | | |
| Reward over-fulfilment | | | | | |
| Sybil/collusion | | | | | |

## 12. Bài tập 9 — Activation decision log

Tạo record:

```text
snapshot_time:
formula_version:
eligible_contributions:
excluded_contributions:
threshold_component_results:
partial_conditions:
verifier_statement:
approver_decision:
actions_triggered:
refunds_or_releases:
exceptions:
evidence_ids:
```

Không được kết luận `Activated` chỉ từ dashboard tổng tiền.

## 13. Red-team scenarios

Người review sẽ cài ít nhất tám tình huống:

1. Một contributor tạo 20 tài khoản.
2. Founder chuyển tiền cho người khác góp lại.
3. Matching sponsor chưa khóa ngân sách.
4. Venue rút sau khi threshold được công bố đạt.
5. Thiết bị đủ gross value nhưng sai specification.
6. Dự án hạ threshold trước deadline.
7. Reward có chi phí fulfilment lớn hơn contribution.
8. Scope thay đổi nhưng không mở quyền rút.
9. Một nhóm beneficiary không thể góp nhưng vẫn cần được hưởng lợi.
10. QF formula được sửa sau khi round đóng.

## 14. Tiêu chuẩn hoàn thành

Đạt khi người onboarding có thể:

- Chẩn đoán vấn đề mà không đạo đức hóa người không góp.
- Tách provision point khỏi fundraising goal.
- Tách AON/KIA khỏi escrow.
- Tách assurance contract khỏi conditional cooperation.
- Tách matching fund khỏi multi-resource matching.
- Giải thích QF là allocation rule, không phải due diligence.
- Chỉ ra ai chịu rủi ro trong mỗi rule.
- Xác định evidence và decision owner.
- Thiết kế failure/change-control trước khi nhận pledge.

Không đạt nếu:

- Mọi vấn đề đều được gọi là free-rider.
- Mọi contribution đều quy ra tiền.
- Chỉ dùng tổng phần trăm hoàn thành.
- Không có refund/release rule.
- Không xử lý related parties.
- Dùng QF như nhãn dân chủ.
- Đổi ngưỡng sau khi xem kết quả.

## 15. Sản phẩm cuối tuần đầu

```text
Collective Mechanism Pack v0.1/
├─ 01_problem-diagnosis.md
├─ 02_actor-benefit-cost-map.md
├─ 03_provision-point-spec.md
├─ 04_funding-rule-decision.md
├─ 05_assurance-contract-draft.md
├─ 06_incentive-register.md
├─ 07_matching-qf-simulation.xlsx
├─ 08_risk-control-matrix.md
└─ 09_activation-decision-log.md
```

## 16. Câu kết

> **Một cơ chế tập thể tốt không chỉ làm nhiều người góp hơn; nó làm rõ điều kiện để hành động chung xảy ra, phân bổ rủi ro công bằng hơn và để mọi quyết định kích hoạt có thể được kiểm tra lại.**
