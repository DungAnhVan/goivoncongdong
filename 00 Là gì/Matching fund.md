# Matching fund

> **Định nghĩa ngắn:** *Matching fund* là cơ chế trong đó một nhà tài trợ cam kết đóng góp thêm khi dự án hoặc cộng đồng đã huy động được một phần nguồn lực khác theo tỷ lệ hoặc công thức xác định.

Ví dụ:

```text
Cộng đồng góp 1 đồng
→ nhà tài trợ góp thêm 1 đồng
→ tổng cộng 2 đồng
```

Tỷ lệ có thể là 1:1, 1:2, có trần tối đa hoặc áp dụng theo điều kiện khác.

## 1. Matching fund dùng để làm gì?

- Khuyến khích cộng đồng tham gia.
- Giảm rủi ro tài trợ một dự án không có nhu cầu thật.
- Buộc dự án huy động thêm nguồn lực thay vì phụ thuộc một nguồn.
- Tăng hiệu ứng đòn bẩy của ngân sách công hoặc quỹ tài trợ.
- Kiểm tra mức cam kết của địa phương, doanh nghiệp hoặc người hưởng lợi.

## 2. Các dạng thường gặp

### Dollar-for-dollar match

Mỗi đơn vị đóng góp hợp lệ được đối ứng bằng một đơn vị.

### Capped match

Nhà tài trợ chỉ đối ứng đến một mức trần.

### Challenge grant

Khoản tài trợ chỉ được giải ngân nếu dự án đạt một mục tiêu huy động trước thời hạn.

### Tiered match

Tỷ lệ thay đổi theo mức huy động hoặc loại người đóng góp.

### In-kind match

Phần đối ứng có thể gồm công sức, thiết bị, dữ liệu hoặc địa điểm nếu quy định cho phép.

## 3. Matching khác co-financing thế nào?

- **Co-financing** chỉ yêu cầu nhiều nguồn cùng chia sẻ chi phí.
- **Matching** gắn khoản tài trợ với công thức hoặc điều kiện huy động từ nguồn khác.

Mọi matching đều là một dạng co-financing, nhưng không phải mọi co-financing đều là matching.

## 4. Ranh giới với conditional cooperation

[[Conditional cooperation]] mô tả hành vi:

> Một người hoặc tổ chức sẵn sàng đóng góp khi đủ người khác cũng đóng góp hoặc khi một điều kiện tập thể được đáp ứng.

`Matching fund` là **một cơ chế tài chính cụ thể** có thể khai thác hành vi đó.

```text
Conditional cooperation
→ động lực và sự phụ thuộc giữa các cam kết

Matching fund
→ công thức đối ứng, trần, điều kiện hợp lệ và giải ngân
```

Không dùng hai thuật ngữ thay thế nhau. Conditional cooperation còn áp dụng cho thời gian, vai trò, thiết bị và tuân thủ, ngay cả khi không có matching fund.

## 5. Tại sao liên quan đến dự án?

Đây là cơ chế rất gần với mô hình gọi vốn cộng đồng:

```text
Cộng đồng xác nhận nhu cầu bằng cam kết thật
→ quỹ công hoặc doanh nghiệp đối ứng
→ dự án có thêm nguồn lực
→ cả hai bên chia sẻ rủi ro
```

Nền tảng có thể ghi nhận:

- Ai đã đóng góp.
- Khoản nào đủ điều kiện matching.
- Tỷ lệ và trần đối ứng.
- Thời điểm khóa sổ.
- Bằng chứng nguồn tiền.
- Điều kiện giải ngân.
- Cấp cam kết theo [[Commitment ladder]].
- Điều kiện kích hoạt theo [[Conditional cooperation]].

## 6. Matching không tự chứng minh demand

Một khoản matching lớn có thể cho thấy ưu tiên của nhà tài trợ nhưng không tự động chứng minh người dùng cần hoặc sẵn sàng trả tiền.

Phải tách:

```text
Cam kết của cộng đồng
→ thuộc nhóm nào, ở cấp nào, có độc lập không?

Cam kết của nhà tài trợ
→ tỷ lệ, trần và điều kiện là gì?

Demand validation
→ offer có tạo hành vi thật ở target segment không?
```

Xem [[Proof of need và demand validation]] và [[Thang cam kết và tín hiệu - Bản đồ thuật ngữ]].

## 7. Rủi ro thiết kế

- Dự án tự tạo giao dịch giả để mở khóa matching.
- Nhà tài trợ lớn đóng góp thay cộng đồng, làm mất ý nghĩa xác nhận nhu cầu.
- Quy tắc quá phức tạp khiến người tham gia không hiểu.
- Khoản match được công bố nhưng chưa có ngân sách thật.
- Chỉ đo số tiền, không đo độ rộng và tính đại diện của người tham gia.
- Nhóm giàu huy động dễ hơn nhóm nghèo dù nhu cầu thấp hơn.
- Một whale contributor kích hoạt match nhưng che mức tham gia cộng đồng thấp.
- Gộp pledge mềm với khoản đóng góp đã chuyển giao.

## 8. Kiểm soát tối thiểu

```text
Cam kết matching có văn bản
→ xác định tỷ lệ và trần
→ định nghĩa khoản đóng góp hợp lệ
→ phân loại soft/hard commitment
→ xác minh giao dịch và bên liên quan
→ khóa sổ
→ tính khoản match
→ phê duyệt
→ [[Disbursement|giải ngân]]
→ báo cáo và kiểm tra
```

Cam kết matching phải ghi:

```text
matching_commitment_id:
sponsor:
ratio:
cap:
eligible_sources:
excluded_related_parties:
minimum_participant_count:
valid_from:
expires_at:
activation_rule:
withdrawal_rule:
evidence_ids:
status:
```

## 9. Áp vào pilot

Một pilot có thể thử:

```text
Mục tiêu cộng đồng: 100 triệu
Nhà tài trợ: match 1:1, tối đa 100 triệu
Điều kiện:
- tối thiểu 50 người xác minh;
- không một người góp quá 20% phần cộng đồng;
- chỉ tính commitment đã Activated/Fulfilled;
- đạt milestone hồ sơ trước khi nhận match;
- match giải ngân theo từng mốc.
```

Như vậy số tiền huy động không phải tín hiệu duy nhất; độ rộng cộng đồng, mức cam kết và bằng chứng dự án cũng được tính.

## 10. Kết luận cho dự án

> Matching fund có thể nối nguồn lực cộng đồng với nguồn lực công hoặc doanh nghiệp, nhưng chỉ có giá trị nếu phần đóng góp ban đầu là thật, đại diện, còn hiệu lực và được xác minh.

## Khái niệm liên quan

- [[Grant và subsidy]]
- [[Public finance]]
- [[Crowdfunding]]
- [[Co-financing]]
- [[Challenge grant]]
- [[Additionality]]
- [[Disbursement]]
- [[Restricted funds]]
- [[Conditional cooperation]]
- [[Commitment ladder]]
- [[Soft commitment và hard commitment]]
- [[Evidence ledger và provenance]]

## Nguồn tham khảo

- European Commission — grants commonly use co-financing: https://commission.europa.eu/strategy-and-policy/eu-budget/how-it-works/annual-lifecycle/implementation/grants-and-procurement_en
- World Bank — community and matching grant materials: https://documents.worldbank.org/
