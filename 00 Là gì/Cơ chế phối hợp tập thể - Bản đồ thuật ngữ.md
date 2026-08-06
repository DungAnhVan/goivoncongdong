# Cơ chế phối hợp tập thể — Bản đồ thuật ngữ

> **Định nghĩa làm việc của dự án:** *Cơ chế phối hợp tập thể* là tập hợp quy tắc dùng để biến nhiều quyết định riêng lẻ, vốn có thể phụ thuộc và dè chừng lẫn nhau, thành một kết quả chung đủ điều kiện để dự án được kích hoạt, phân bổ nguồn lực hoặc tiếp tục thực hiện.

Mảng này không hỏi riêng:

> Một người có muốn tham gia không?

Mà hỏi:

> Những cam kết rời rạc phải được tổ chức theo quy tắc nào để cả nhóm có thể cùng vượt qua điểm không ai muốn đi trước một mình?

## 1. Kiến trúc của mảng

```text
[[Collective action problem và free-rider problem]]
→ chẩn đoán vì sao lợi ích chung không tự tạo ra hành động chung

[[Provision point và threshold mechanism]]
→ xác định mức tối thiểu để dự án hoặc hàng hóa chung khả thi

[[All-or-nothing và keep-it-all]]
→ quy định điều gì xảy ra khi mục tiêu đạt hoặc không đạt

[[Assurance contract và conditional pledge]]
→ đóng gói ngưỡng, cam kết có điều kiện và quy tắc kích hoạt/hoàn trả

[[Selective incentives và contributor benefits]]
→ tạo lợi ích riêng cho người tham gia mà không nhập nhằng bản chất đóng góp

[[Matching fund]]
→ đối ứng nguồn tài chính theo tỷ lệ, trần hoặc điều kiện

[[Quadratic funding]]
→ phân bổ một matching pool giữa nhiều dự án, coi trọng độ rộng đóng góp
```

Các cơ chế trên có thể kết hợp, nhưng không dùng thay thế nhau.

## 2. Ranh giới với các mảng đã có

| Mảng | Câu hỏi chính |
|---|---|
| [[Conditional cooperation]] | Cam kết của một actor phụ thuộc hành vi người khác thế nào? |
| [[Commitment ladder]] | Actor đã thực hiện loại hành vi nào? |
| [[Soft commitment và hard commitment]] | Cam kết khó rút đến đâu? |
| [[Cơ chế phối hợp tập thể - Bản đồ thuật ngữ|Cơ chế phối hợp tập thể]] | Quy tắc nào tổ chức nhiều cam kết thành kết quả chung? |
| [[Multi-resource matching]] | Offer nào ghép được với need nào? |
| [[Resource pledge lifecycle]] | Nguồn lực đang ở trạng thái offered, reserved hay delivered? |
| [[Escrow]] | Ai giữ tài sản và giải phóng theo điều kiện nào? |
| [[Milestone verification]] | Mốc thực hiện đã đạt chưa? |

Ví dụ:

```text
“Tôi góp 20 giờ nếu có đủ đội vận hành.”
→ Conditional cooperation

20 giờ này là pre-commitment hay resource contribution?
→ Commitment ladder

Điều kiện “đủ đội” được đo và kích hoạt thế nào cho toàn nhóm?
→ Collective action mechanism

Nguồn lực đang waiting, reserved hay activated?
→ Resource pledge lifecycle
```

## 3. Chuỗi thiết kế cơ chế

```text
Xác định kết quả chung
→ chẩn đoán collective action problem
→ mô tả nhóm và lợi ích liên quan
→ xác định provision point
→ chọn AON, KIA hoặc hybrid
→ xác định pledge, activation và refund rule
→ quyết định có cần selective incentive không
→ quyết định có matching pool không
→ xác định người giữ tài sản và cách kiểm chứng
→ công bố quy tắc trước khi nhận cam kết
→ theo dõi, kích hoạt, hoàn trả hoặc đóng cơ chế
```

Không nên bắt đầu bằng việc chọn một cơ chế đang phổ biến rồi ép dự án vào cơ chế đó.

## 4. Chẩn đoán trước khi thiết kế

Một cơ chế phải trả lời ít nhất:

```text
Kết quả chung là gì?
Ai hưởng lợi dù không đóng góp?
Ai chịu chi phí?
Dự án có cần mức tối thiểu để khả thi không?
Mức tối thiểu gồm tiền hay một tổ hợp nguồn lực?
Ai đang chờ ai đi trước?
Cam kết có được quan sát và xác minh không?
Nếu không đủ ngưỡng thì nguồn lực còn hữu ích không?
Ai chịu rủi ro thiếu hụt?
Có nhóm nào bị loại trừ bởi cơ chế không?
```

## 5. Ma trận vấn đề → cơ chế

| Vấn đề | Cơ chế có thể cân nhắc | Không tự giải quyết được |
|---|---|---|
| Mọi người chờ nhau | Threshold, assurance contract | Dự án không khả thi hoặc thiếu niềm tin vào đội |
| Người hưởng lợi không góp | Selective incentives, membership rule, matching | Bất bình đẳng khả năng đóng góp |
| Dự án không thể chạy nếu thiếu mức tối thiểu | Provision point + all-or-nothing | Ngưỡng bị tính sai |
| Mỗi khoản nhỏ vẫn tạo giá trị | Keep-it-all hoặc phased funding | Mục đích sử dụng phần thiếu hụt |
| Nhà tài trợ muốn kích hoạt cộng đồng | Matching fund | Demand thực hoặc tính đại diện |
| Nhiều dự án tranh một matching pool | Quadratic funding | Chất lượng dự án, Sybil và thông đồng |
| Thiếu một nguồn lực chặn | Multi-resource threshold | Tính tương thích kỹ thuật của offer |

Không có cơ chế nào thay thế được [[Proof of need và demand validation]], thẩm định khả thi hoặc [[Bằng chứng và kiểm chứng - Bản đồ thuật ngữ|bằng chứng và kiểm chứng]].

## 6. Provision point không chỉ là tiền

Trong dự án này, provision point có thể là một bundle:

```text
300 triệu tiền mặt
+ 400 giờ kỹ thuật
+ địa điểm đã xác nhận
+ giấy phép cần thiết
+ ít nhất 100 người dùng pilot
```

Đạt 500 triệu nhưng thiếu giấy phép hoặc operator vẫn có thể là **chưa đạt provision point**.

Xem [[Provision point và threshold mechanism]] và [[Multi-resource matching]].

## 7. Ba lớp quyết định phải tách

```text
Eligibility decision
→ ai và loại contribution nào được tính?

Activation decision
→ điều kiện tập thể đã đạt để kích hoạt chưa?

Allocation decision
→ nguồn lực đã kích hoạt được phân cho ai hoặc dự án nào?
```

Ví dụ:

- `Matching fund` cần eligibility và activation rule.
- `All-or-nothing` chủ yếu là activation rule.
- `Quadratic funding` là allocation rule cho matching pool.

Không gộp ba lớp thành một chữ “đã đạt mục tiêu”.

## 8. Cơ chế không phải governance

Cơ chế có thể tự động hóa một phần quy tắc, nhưng vẫn cần governance để xử lý:

- Thay đổi trọng yếu.
- Tranh chấp dữ liệu.
- Ngoại lệ chính đáng.
- Gian lận và bên liên quan.
- Điều kiện bất khả kháng.
- Phần dư và nguồn lực không sử dụng.
- Khiếu nại của [[Affected community|cộng đồng bị ảnh hưởng]].

```text
Mechanism
→ quy tắc áp dụng bình thường

Governance
→ ai có quyền tạo, sửa, giám sát và xử lý ngoại lệ của quy tắc
```

## 9. Hồ sơ thiết kế cơ chế tối thiểu

```text
mechanism_id:
collective_outcome:
target_population:
beneficiary_groups:
contributor_groups:
problem_diagnosis:
provision_point:
eligible_contributions:
measurement_source:
deadline:
activation_rule:
partial_satisfaction_rule:
allocation_rule:
refund_or_release_rule:
change_control:
verifier:
conflict_of_interest_rule:
grievance_route:
status:
evidence_ids:
```

## 10. Quy tắc chống “múa cơ chế”

Không được gọi tên một cơ chế nếu chưa mô tả được:

1. Nó giải quyết thất bại phối hợp nào.
2. Điều kiện đầu vào nào được chấp nhận.
3. Ngưỡng hoặc công thức cụ thể.
4. Ai xác minh dữ liệu.
5. Kết quả nào kích hoạt hành động nào.
6. Ai chịu rủi ro khi thiếu hụt.
7. Cách hoàn trả, giải phóng hoặc xử lý phần dư.
8. Điều kiện sửa hoặc dừng cơ chế.

Ví dụ, viết “dùng quadratic funding” mà chưa có identity rule, matching pool, eligibility và chống thông đồng thì mới là nhãn ý tưởng.

## 11. Áp vào pilot

Pilot đầu tiên không nên dùng tất cả cơ chế. Nên thử một cấu hình có thể giải thích bằng một trang:

```text
Collective problem:
Nhiều bên sẵn sàng góp nhưng không ai muốn đi trước.

Provision point:
100 triệu + 120 giờ kỹ thuật + địa điểm 4 tuần.

Funding rule:
All-or-nothing đối với tiền và nguồn lực blocking.

Pledge rule:
Cam kết chờ điều kiện, chỉ kích hoạt khi đủ bundle.

Verification:
Một người kiểm tra dữ liệu, một người phê duyệt activation.

Failure rule:
Không thu tiền; release mọi reservation; công bố resource gap.
```

## 12. Kết luận cho dự án

> **Một cộng đồng có chung lợi ích chưa chắc tạo được hành động chung. Cơ chế phối hợp tập thể biến sự chờ đợi, phụ thuộc và dè chừng thành các điều kiện cam kết, kích hoạt và phân bổ có thể hiểu, kiểm tra và chịu trách nhiệm.**

## Khái niệm liên quan

- [[Collective action problem và free-rider problem]]
- [[Provision point và threshold mechanism]]
- [[All-or-nothing và keep-it-all]]
- [[Selective incentives và contributor benefits]]
- [[Assurance contract và conditional pledge]]
- [[Quadratic funding]]
- [[Conditional cooperation]]
- [[Matching fund]]
- [[Multi-resource matching]]
- [[Escrow]]
- [[Verification protocol và decision rule]]

## Nguồn tham khảo

- Mancur Olson — *The Logic of Collective Action*, 1965.
- Elinor Ostrom — *Governing the Commons*, 1990.
- Mark Bagnoli & Barton Lipman — Provision of Public Goods: Fully Implementing the Core through Private Contributions, 1989: https://doi.org/10.2307/2297552
