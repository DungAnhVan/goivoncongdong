# Quadratic funding

> **Định nghĩa ngắn:** *Quadratic funding* là một quy tắc phân bổ matching pool giữa nhiều dự án, trong đó độ rộng của sự ủng hộ từ nhiều contributor độc lập được coi trọng hơn việc chỉ cộng tổng số tiền trực tiếp.

Trong dạng cơ bản, điểm của một dự án được tính gần như:

```text
score_j = (Σ_i √contribution_ij)²
```

Khoản matching trước điều chỉnh có thể được hiểu là:

```text
score_j - direct_contributions_j
```

Nếu tổng nhu cầu matching vượt matching pool, các khoản được scale theo rule công bố trước.

## 1. Trực giác

So sánh hai dự án cùng nhận 100 đơn vị:

```text
Dự án A:
1 người góp 100
→ score = (√100)² = 100

Dự án B:
100 người, mỗi người góp 1
→ score = (100 × √1)² = 10.000
```

Quadratic funding xem dự án B có độ rộng ủng hộ lớn hơn và vì vậy có thể nhận nhiều matching hơn.

Đây là ví dụ trực giác; hệ thống thật phải áp dụng matching pool, cap, eligibility và chống thao túng.

## 2. QF là allocation rule

```text
[[Matching fund]]
→ matching pool đến từ đâu, quy mô và điều kiện gì?

Quadratic funding
→ pool đó được chia giữa nhiều dự án như thế nào?
```

QF không phải cơ chế giữ tiền, không phải assurance contract và không phải demand validation.

## 3. Ranh giới với quadratic voting

```text
Quadratic funding
→ phân bổ nguồn matching dựa trên contribution

Quadratic voting
→ phân bổ sức biểu đạt preference bằng chi phí tăng theo bình phương số phiếu
```

Hai cơ chế liên quan về toán học nhưng không dùng thay thế nhau.

## 4. Ranh giới với crowdfunding thông thường

Crowdfunding thông thường có thể xếp dự án theo:

- Tổng tiền.
- Tỷ lệ đạt mục tiêu.
- Số contributor.

QF kết hợp độ lớn và độ phân tán đóng góp trong một công thức matching. Nó không thay thế funding rule AON/KIA của từng dự án.

Một dự án có thể:

```text
Dùng AON để kích hoạt campaign
+ dùng QF để nhận phần matching pool
```

## 5. Điều kiện tối thiểu trước khi dùng

QF chỉ có ý nghĩa khi có:

1. Matching pool thật và bị ràng buộc.
2. Danh sách dự án đủ điều kiện.
3. Contributor identity/uniqueness đủ đáng tin.
4. Related-party rule.
5. Contribution hợp lệ và truy nguyên được.
6. Công thức, cap và scaling rule công bố trước.
7. Thời gian khóa sổ.
8. Verification và dispute process.

Thiếu identity rule, việc chia một contributor thành nhiều tài khoản có thể tạo matching giả.

## 6. Sybil attack

*Sybil attack* trong bối cảnh này là việc một actor kiểm soát nhiều danh tính để làm contribution trông như đến từ nhiều người độc lập.

Ví dụ:

```text
Một người có 100 đơn vị
→ chia thành 100 tài khoản, mỗi tài khoản góp 1
→ công thức hiểu nhầm là 100 contributor độc lập
```

Kiểm soát có thể gồm:

- Identity verification tương xứng.
- Uniqueness check.
- Payment instrument analysis.
- Device/network signals, có giới hạn và bảo vệ privacy.
- Related-party disclosure.
- Review pattern bất thường.
- Challenge period.

Không tuyên bố “one human one identity” khi chưa chứng minh được.

## 7. Collusion

Các nhóm có thể trao đổi contribution chéo:

```text
Nhóm A góp cho B
Nhóm B góp cho A
→ cả hai mở rộng matching giả
```

Cần xem xét:

- Quan hệ tổ chức.
- Cùng beneficial owner.
- Dòng tiền quay vòng.
- Contribution hoàn lại bí mật.
- Cụm actor luôn góp chéo.
- Tài khoản mới tạo cùng thời điểm.

QF nhạy với độ rộng đóng góp nên provenance và related-party review là lớp bắt buộc.

## 8. Contribution đủ điều kiện

Không mặc định mọi khoản đều đi vào công thức.

Có thể loại:

- Self-funding.
- Founder và bên liên quan.
- Khoản đã được hoàn.
- Contribution được bù lại ngoài hệ thống.
- Nguồn không xác minh.
- Khoản vượt cap.
- Contribution sau deadline.
- Incentivized transaction làm sai lệch preference.

Rule phải công bố trước.

## 9. Contributor caps và project caps

Có thể áp dụng:

```text
per-contributor eligible cap
per-project matching cap
minimum direct contribution
minimum unique contributors
maximum related-party share
```

Cap giảm một số dạng chi phối nhưng cũng thay đổi incentive. Không mô tả kết quả là “thuần quadratic” nếu đã dùng nhiều adjustment mà không công bố.

## 10. Scaling khi pool không đủ

Nếu tổng matching theo công thức là 10 tỷ nhưng pool chỉ có 1 tỷ, cần scaling.

Ví dụ đơn giản:

```text
raw_match_j
→ chia theo tỷ lệ chung để tổng = pool
```

Có thể có phương án khác như cap theo project hoặc matching round nhiều tầng. Rule phải được mô phỏng trước để thấy ai được lợi và ai bị thiệt.

## 11. QF không chứng minh chất lượng dự án

Một dự án có matching score cao chỉ cho thấy mẫu contribution theo rule, không tự chứng minh:

- Need có thật.
- Solution khả thi.
- Team đủ năng lực.
- Outcome sẽ xuất hiện.
- Beneficiary đại diện.
- Không có ngoại tác.

Eligibility và due diligence phải xảy ra trước allocation.

Xem [[Proof of need và demand validation]], [[Milestone verification]] và [[Affected community]].

## 12. QF và social proof

QF có thể tạo social proof mạnh, nhưng social proof chỉ đáng tin nếu:

- Actor thật.
- Không đếm trùng.
- Quan hệ lợi ích được công bố.
- Contribution còn hiệu lực.
- Incentive không làm méo hành vi.

Xem [[Social proof và authentic social proof]].

## 13. QF với nguồn lực ngoài tiền

Không nên đưa giờ lao động, thiết bị và dữ liệu vào cùng công thức tiền tệ một cách trực tiếp.

Lý do:

- Khó chuẩn hóa value.
- Dễ khai khống.
- Khả năng sử dụng khác gross value.
- Một resource blocking không thể thay bằng nhiều resource không liên quan.

Cách an toàn hơn:

```text
QF
→ phân bổ financial matching pool

[[Multi-resource matching]]
→ ghép nguồn lực phi tiền với nhu cầu

Provision point
→ kiểm tra bundle cuối có đủ không
```

Có thể nghiên cứu non-financial matching riêng, nhưng không gọi đó là QF nếu không có mô hình và giả định rõ.

## 14. Ví dụ mô phỏng tối thiểu

```text
Matching pool: 100 triệu

Project A:
- 2 contributor lớn
- direct total: 100 triệu

Project B:
- 80 contributor nhỏ
- direct total: 80 triệu

Project C:
- 30 contributor
- direct total: 40 triệu
```

Trước khi chạy thật, phải mô phỏng:

- Raw score.
- Raw match.
- Scaling.
- Project cap.
- Related-party exclusions.
- Kết quả sau loại contribution bất thường.

Không chỉ hiển thị con số cuối.

## 15. Staged adoption

### Giai đoạn 1 — simulation only

- Dùng dữ liệu lịch sử hoặc dữ liệu giả.
- Không phân tiền thật.
- Red-team Sybil và collusion.

### Giai đoạn 2 — small capped pool

- Số dự án ít.
- Matching cap thấp.
- Identity review thủ công.
- Công bố đầy đủ calculation.

### Giai đoạn 3 — production round

- Audit formula.
- Monitoring bất thường.
- Dispute and recalculation rule.
- Public result ledger.

QF không nên là cơ chế pilot đầu tiên khi identity và contribution data chưa ổn định.

## 16. Data schema gợi ý

```text
qf_round_id:
matching_pool_id:
eligible_project_ids:
valid_from:
closes_at:
eligible_contribution_rule:
identity_rule:
related_party_rule:
contributor_cap:
project_cap:
formula_version:
scaling_rule:
calculation_snapshot:
challenge_period:
recalculation_rule:
verifier:
status:
evidence_ids:

qf_contribution_record:
actor_id:
project_id:
amount:
eligible_amount:
related_party_status:
identity_status:
transaction_status:
included_in_snapshot:
exclusion_reason:
```

## 17. Dấu hiệu cảnh báo

- Gọi QF là “dân chủ tuyệt đối”.
- Không có identity/uniqueness rule.
- Không công bố scaling.
- Không loại self-funding.
- Một nhóm tổ chức chia contribution qua nhiều pháp nhân.
- Reward lớn làm contribution không còn phản ánh preference.
- Công thức thay đổi sau khi round đóng.
- Dùng QF để thay thẩm định dự án.
- Dùng gross matching score như tiền chắc chắn nhận.
- Không có quyền challenge và recalculation.

## 18. Kết luận cho dự án

> **Quadratic funding là quy tắc phân bổ matching pool nhạy với độ rộng đóng góp; nó chỉ đáng tin khi danh tính, quan hệ lợi ích, contribution và công thức đều có thể kiểm tra.**

## Khái niệm liên quan

- [[Cơ chế phối hợp tập thể - Bản đồ thuật ngữ]]
- [[Matching fund]]
- [[Collective action problem và free-rider problem]]
- [[Social proof và authentic social proof]]
- [[Costly signaling và cheap talk]]
- [[Evidence ledger và provenance]]
- [[Proof of need và demand validation]]
- [[Multi-resource matching]]

## Nguồn tham khảo

- Vitalik Buterin, Zoë Hitzig & E. Glen Weyl — Liberal Radicalism: A Flexible Design for Philanthropic Matching Funds, 2019: https://doi.org/10.2139/ssrn.3243656
- Gitcoin — Quadratic Funding documentation: https://www.gitcoin.co/mechanisms
