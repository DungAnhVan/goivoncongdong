---
ai_authored: true
---

# Thang cam kết và tín hiệu — Bản đồ thuật ngữ

> **Định nghĩa làm việc của dự án:** *Thang cam kết và tín hiệu* là lớp khái niệm dùng để phân loại hành vi tham gia theo mức độ cam kết, đánh giá thông tin mà hành vi đó truyền đi và xác định mức suy luận mà dự án được phép rút ra.

Đây không phải một thang đo chuẩn duy nhất của một ngành. Nó là **khung làm việc của dự án Gọi vốn cộng đồng**, kết hợp product discovery, kinh tế học thông tin, hành vi tập thể và thiết kế huy động nguồn lực.

## 1. Câu hỏi trung tâm

```text
Người này đã làm gì?
→ hành vi nằm ở cấp cam kết nào?
→ họ đã đặt gì vào rủi ro?
→ tín hiệu đó dễ giả đến đâu?
→ cam kết có điều kiện gì?
→ còn hiệu lực không?
→ được phép dùng để suy luận điều gì?
```

> **Không đếm mọi phản ứng như nhau và không biến mọi phản ứng thành bằng chứng nhu cầu.**

## 2. Kiến trúc của mảng

```text
[[Commitment ladder]]
→ phân loại hành vi theo cấp cam kết

[[Soft commitment và hard commitment]]
→ phân loại độ ràng buộc và chi phí rút lui

[[Costly signaling và cheap talk]]
→ đánh giá tín hiệu đáng tin đến đâu trong điều kiện bất cân xứng thông tin

[[Social proof và authentic social proof]]
→ đánh giá ảnh hưởng của hành vi người khác và chất lượng của bằng chứng xã hội

[[Conditional cooperation]]
→ mô tả cam kết phụ thuộc vào mức tham gia của người khác
```

## 3. Ranh giới để tránh chồng lấn

| Khái niệm | Câu hỏi nó trả lời | Không dùng nó để trả lời |
|---|---|---|
| [[Proof of need và demand validation|Demand validation]] | Một offer cụ thể có tạo hành vi thật ở một nhóm xác định không? | Không tự động xếp mọi hành vi vào cùng một mức cam kết |
| [[Commitment ladder]] | Hành vi nằm ở cấp nào trong chuỗi tham gia? | Không kết luận hành vi đó có thật hoặc đủ đại diện |
| [[Soft commitment và hard commitment]] | Rút lại cam kết khó đến đâu và có hậu quả gì? | Không mặc định hard commitment là tốt hoặc đạo đức hơn |
| [[Costly signaling và cheap talk]] | Hành vi truyền thông tin gì và có khó bắt chước không? | Không kiểm chứng bản ghi hoặc nguồn dữ liệu |
| [[Social proof và authentic social proof]] | Hành vi người khác ảnh hưởng lựa chọn ra sao và proof xã hội có đáng tin không? | Không chứng minh outcome của dự án |
| [[Conditional cooperation]] | Cam kết phụ thuộc hành vi tập thể hoặc ngưỡng nào? | Không thay thế hợp đồng, escrow hoặc matching fund |
| [[Evidence ledger và provenance]] | Bản ghi hành vi có nguồn gốc, phiên bản và dấu vết gì? | Không tự diễn giải ý nghĩa kinh tế–xã hội của hành vi |
| [[Verification protocol và decision rule]] | Ai kiểm tra và kết quả dẫn đến quyết định nào? | Không tạo ra cam kết thay người tham gia |

## 4. Thang cam kết làm việc

```text
Attention
→ Interest
→ Endorsement
→ Trial
→ Pre-commitment
→ Resource contribution
→ Transaction / Investment
→ Continued participation
```

Tên cấp mô tả **loại hành vi**, không phải điểm uy tín cố định.

Một người có thể đi không theo thứ tự:

- Góp chuyên môn mà chưa từng bấm theo dõi.
- Đầu tư nhưng không phải người dùng.
- Dùng thử nhưng không công khai ủng hộ.
- Đồng ý về mục tiêu xã hội nhưng từ chối giải pháp cụ thể.
- Cam kết có điều kiện rồi không kích hoạt vì ngưỡng không đạt.

## 5. Hai chiều không được gộp làm một

### Cấp cam kết

Hỏi người đó **đã thực hiện hành vi gì**.

### Chất lượng tín hiệu

Hỏi hành vi đó **truyền thông tin đáng tin đến đâu**.

Ví dụ:

```text
Một khoản đầu tư lớn từ bên liên quan
→ cấp cam kết tài chính cao
→ nhưng tín hiệu nhu cầu thị trường có thể yếu

Một hợp đồng mua nhỏ từ khách hàng độc lập
→ giá trị tiền thấp hơn
→ nhưng tín hiệu demand có thể mạnh hơn
```

Không xây một điểm tổng hợp duy nhất trước khi xác định mục đích phân tích.

## 6. Phân loại theo loại nguồn lực

Cam kết không chỉ là tiền:

```text
Money
Time
Skill
Equipment
Data
Reputation
Access / distribution
Physical space
Purchase commitment
Legal obligation
Governance responsibility
```

Hai cam kết cùng giá trị tiền không nhất thiết tương đương nếu khác:

- Khả năng thay thế.
- Thời hạn.
- Điều kiện.
- Chi phí cơ hội.
- Khả năng thu hồi.
- Rủi ro pháp lý.
- Mức phụ thuộc của dự án.

## 7. Commitment record tối thiểu

```text
commitment_id:
actor_id:
project_id:
actor_role:
commitment_stage:
commitment_type:
resource_type:
amount_or_quantity:
unit:
offer_version:
conditions:
withdrawal_right:
withdrawal_cost:
created_at:
starts_at:
expires_at:
status:
conflict_of_interest:
evidence_ids:
verification_status:
```

### Trạng thái gợi ý

```text
Proposed
→ Confirmed
→ Conditional
→ Activated
→ Partially fulfilled
→ Fulfilled
→ Withdrawn
→ Expired
→ Breached
→ Superseded
```

`Withdrawn` không đồng nghĩa gian lận. Cần lưu lý do, điều kiện thay đổi và quyền rút đã được thỏa thuận.

## 8. Quy tắc diễn giải

### Không cộng thẳng các cấp

```text
10.000 lượt thích
+ 100 đăng ký
+ 10 đặt cọc
≠ 10.110 người cam kết
```

Có thể trùng người, khác offer, khác thời điểm và khác mức ràng buộc.

### Không quy tiền thành demand một cách máy móc

- Donation có thể thể hiện đồng cảm, không phải nhu cầu sử dụng.
- Investment thể hiện kỳ vọng tài chính, không nhất thiết xác nhận beneficiary demand.
- Grant thể hiện ưu tiên của funder, không nhất thiết là willingness to pay của end user.
- Purchase order từ khách hàng độc lập thường gần demand thương mại hơn lượt bình chọn.

### Không coi chi phí cao là trung thực tuyệt đối

Một tín hiệu có thể tốn kém nhưng vẫn bị thao túng bởi:

- Bên liên quan.
- Người có ngân sách quảng bá lớn.
- Whale contributor.
- Tài trợ chéo.
- Giao dịch hoàn lại sau hậu trường.
- Cam kết không có khả năng thực hiện.

## 9. Hiển thị dữ liệu trên nền tảng

Không hiển thị một con số “ủng hộ” tổng hợp duy nhất. Nên tách:

```text
Attention: 12.400 lượt xem đủ điều kiện
Interest: 1.250 người theo dõi
Endorsement: 320 xác nhận công khai
Trial: 86 người dùng thử hợp lệ
Pre-commitment: 34 cam kết có điều kiện
Resource contribution: 12 người góp 280 giờ + 3 thiết bị
Purchase: 8 đơn vị ký pilot
Investment: 2 khoản đầu tư
```

Mỗi số cần có:

- Khoảng thời gian.
- Offer/version liên quan.
- Quy tắc chống đếm trùng.
- Quan hệ lợi ích.
- Trạng thái còn hiệu lực.
- Đường dẫn sang [[Evidence ledger và provenance|evidence records]].

## 10. Kết nối với quyết định

| Quyết định | Tín hiệu phù hợp hơn |
|---|---|
| Có đáng nghiên cứu vấn đề? | Attention có ngữ cảnh + proof of need sơ bộ |
| Có nên thiết kế pilot? | Interest + trial willingness + nhóm mục tiêu rõ |
| Có demand cho offer? | Trial, pre-commitment, purchase hoặc hành vi thay đổi |
| Có đủ nguồn lực khởi động? | Resource commitments đã xác minh và còn hiệu lực |
| Có nên giải ngân? | Cam kết không đủ; cần [[Milestone verification]] và decision rule |
| Có outcome? | Không suy từ social proof; cần [[Proof of use và proof of outcome]] |

## 11. Dấu hiệu cảnh báo

- Dùng lượt xem hoặc lượt thích làm “số người có nhu cầu”.
- Gọi thư quan tâm không ràng buộc là hợp đồng.
- Gộp donation, pre-order và investment thành một tổng vốn.
- Hiển thị logo đối tác nhưng không nêu loại cam kết.
- Đếm người trong đội dự án như người dùng độc lập.
- Dùng tổng tiền để thay cho số người tham gia và mức tập trung.
- Không ghi điều kiện kích hoạt hoặc ngày hết hạn.
- Giữ lại social proof cũ sau khi offer đã thay đổi trọng yếu.

## 12. Kết luận cho dự án

> **Dự án không hỏi “có bao nhiêu người ủng hộ?” trước; dự án hỏi “họ đã làm gì, đặt gì vào rủi ro, trong điều kiện nào và hành vi đó cho phép ta tin điều gì?”**

Mảng này nối:

```text
Cộng đồng và stakeholder
→ hành vi cam kết
→ tín hiệu
→ bằng chứng và provenance
→ kiểm chứng
→ quyết định nguồn lực
```

## Khái niệm liên quan

- [[Proof of need và demand validation]]
- [[Bằng chứng và kiểm chứng - Bản đồ thuật ngữ]]
- [[Evidence ledger và provenance]]
- [[Verification protocol và decision rule]]
- [[Matching fund]]
- [[Stakeholder]]
- [[Consumer, customer và end user]]

## Nguồn tham khảo

- Michael Spence — Job Market Signaling, 1973: https://doi.org/10.2307/1882010
- Bryan, Karlan & Nelson — Commitment Devices, 2010: https://doi.org/10.1146/annurev.economics.102308.124324
- Fischbacher, Gächter & Fehr — Are People Conditionally Cooperative?, 2001: https://doi.org/10.1016/S0165-1765(01)00394-9
