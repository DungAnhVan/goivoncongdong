# Proof of use và proof of outcome

> **Định nghĩa ngắn:** *Proof of use* là bằng chứng cho thấy tiền, vật tư, thời gian hoặc nguồn lực đã được sử dụng theo mục đích và quy trình đã cam kết. *Proof of outcome* là bằng chứng cho thấy một thay đổi có ý nghĩa đã xuất hiện ở người hưởng lợi, hệ thống hoặc môi trường mục tiêu.

Hai loại bằng chứng trả lời hai câu khác nhau:

```text
Proof of use
→ nguồn lực đã đi đâu và được dùng làm gì?

Proof of outcome
→ sau việc sử dụng đó, điều gì thực sự thay đổi?
```

## 1. Vì sao phải tách?

Một dự án có thể:

- Chi đúng ngân sách nhưng không tạo kết quả.
- Tạo đủ sản phẩm nhưng người dùng không sử dụng.
- Có nhiều hoạt động nhưng vấn đề không cải thiện.
- Đạt outcome nhưng không thể chứng minh tiền nào tạo ra phần nào.

Do đó:

> Hóa đơn chứng minh giao dịch; nó không tự động chứng minh output, outcome hay tác động.

## 2. Results chain

```text
Inputs
→ Activities
→ Outputs
→ Outcomes
→ Impacts
```

| Lớp | Ví dụ | Bằng chứng thường gặp |
|---|---|---|
| Input | 100 triệu, 2 kỹ sư, 500 kg vật liệu | sao kê, hợp đồng, timesheet, phiếu nhập |
| Activity | đào tạo, sản xuất, khảo sát, lắp đặt | lịch, log, biên bản, ảnh hiện trường |
| Output | 20 bộ thiết bị, 10 lớp học, 1 phần mềm | nghiệm thu, kiểm thử, danh sách bàn giao |
| Outcome | giảm thời gian chờ, tăng tỷ lệ sử dụng | dữ liệu trước–sau, khảo sát, log hành vi |
| Impact | thay đổi dài hạn hoặc hệ thống | đánh giá sâu, dữ liệu nhiều kỳ, phân tích đóng góp/nhân quả |

Proof of use chủ yếu nằm ở input–activity–một phần output. Proof of outcome nằm ở outcome và có thể mở rộng đến impact.

## 3. Proof of use gồm những gì?

### Financial use evidence

- Sao kê và payment reference.
- Hóa đơn, hợp đồng, phiếu giao nhận.
- Budget line và eligible expenditure.
- Đối soát giữa ledger, ngân hàng và chứng từ.

### Physical use evidence

- Vật tư đã nhận và đưa vào đâu.
- Thiết bị có tồn tại, định danh và đang ở vị trí nào.
- Sản phẩm đã bàn giao cho ai.
- Ảnh, video, sensor log hoặc biên bản có provenance.

### Non-financial resource use evidence

Nguồn lực ngoài tiền cần bằng chứng theo bản chất riêng:

```text
Time and labor
→ giờ thực tế + task/deliverable + acceptance

Data
→ version/quyền truy cập + mục đích sử dụng + access log

Equipment and venue
→ asset/booking ID + thời gian/công suất sử dụng + tình trạng

Access contribution
→ introduction/slot/quyền tiếp cận đã thực sự được kích hoạt
```

Không dùng `estimated_value` của nguồn lực thay cho bằng chứng nó đã được dùng.

Xem [[Nguồn lực ngoài tiền - Bản đồ thuật ngữ]], [[Time and labor contribution]], [[Data contribution]] và [[Asset and access contribution]].

### Process evidence

- Ai đề nghị, kiểm tra, phê duyệt và thực hiện.
- Phiên bản kế hoạch hoặc bản vẽ nào được dùng.
- Có variation hay ngoại lệ nào.
- Có xung đột lợi ích hay bên liên quan nào.

## 4. Proof of outcome gồm những gì?

Một outcome claim cần ít nhất:

```text
Target population
→ outcome definition
→ indicator
→ baseline
→ target hoặc expected direction
→ measurement method
→ time window
→ data source
→ limitations
→ result
```

Ví dụ:

```text
Claim: hệ thống giúp giảm thời gian xử lý hồ sơ.

Không đủ:
- đã cài phần mềm;
- đã đào tạo 30 người;
- đã tạo 500 tài khoản.

Outcome evidence tốt hơn:
- median thời gian xử lý trước pilot: 4,8 ngày;
- sau 3 tháng: 2,9 ngày;
- cùng định nghĩa hồ sơ hoàn tất;
- nêu số lượng hồ sơ, tỷ lệ thiếu dữ liệu và thay đổi quy trình khác.
```

## 5. Outcome không đồng nghĩa attribution

Quan sát thấy thay đổi không tự động chứng minh dự án là nguyên nhân duy nhất.

Có ba mức tuyên bố:

```text
Descriptive
→ outcome đã thay đổi trong giai đoạn dự án

Contribution
→ có bằng chứng hợp lý rằng dự án góp phần tạo thay đổi

Causal attribution
→ thiết kế đánh giá đủ mạnh để ước lượng phần thay đổi do dự án gây ra
```

Dự án nhỏ thường nên dùng ngôn ngữ **contribution** trung thực thay vì tuyên bố causal impact quá mức.

## 6. Proof of use không chỉ là kiểm tra chống gian lận

Nó còn giúp:

- Học chi phí thực tế của từng hoạt động.
- So sánh kế hoạch với triển khai.
- Xác định bottleneck.
- Tạo dữ liệu cho vòng gọi vốn sau.
- Phân biệt thất bại do thiết kế với thất bại do thực thi.

Ví dụ:

```text
Outcome không đạt
├─ nguồn lực chưa dùng đủ
├─ hoạt động triển khai sai
├─ output kém chất lượng
├─ người dùng không tiếp nhận
└─ theory of change sai
```

Không có proof of use thì khó biết thất bại nằm ở đâu.

## 7. Pledge, delivery, acceptance và use

Nguồn lực chỉ nên đi vào proof of use sau khi tách được:

```text
Promised
→ lời hứa

Reserved / Activated
→ nguồn lực đã được giữ hoặc điều kiện đã đạt

Delivered
→ đã bàn giao

Accepted
→ đã đạt yêu cầu tiếp nhận

In use
→ đang được dùng cho activity/milestone
```

Xem [[Resource pledge lifecycle]]. Một pledge chưa activated không phải input đã có; một delivery chưa accepted chưa chắc dùng được.

## 8. Bộ kiểm tra proof of use

| Kiểm tra | Câu hỏi |
|---|---|
| Existence | Giao dịch, vật tư hoặc hoạt động có thật không? |
| Eligibility | Có thuộc mục đích và ngân sách được phép không? |
| Authorization | Có đúng người phê duyệt không? |
| Occurrence | Hàng hóa/dịch vụ đã thực sự được nhận chưa? |
| Acceptance | Nguồn lực có đạt specification và quyền sử dụng không? |
| Accuracy | Số lượng, giá và thông tin có đúng không? |
| Period | Có thuộc đúng kỳ và milestone không? |
| Related party | Có xung đột lợi ích không? |
| Reconciliation | Ledger có khớp ngân hàng và chứng từ không? |

## 9. Bộ kiểm tra proof of outcome

| Kiểm tra | Câu hỏi |
|---|---|
| Relevance | Chỉ số có thực sự phản ánh outcome không? |
| Baseline | Có điểm xuất phát đáng tin không? |
| Coverage | Dữ liệu bao phủ ai và bỏ sót ai? |
| Consistency | Cách đo trước và sau có giống nhau không? |
| Timing | Đã đủ thời gian để outcome xuất hiện chưa? |
| Alternative explanations | Có thay đổi khác cùng lúc không? |
| Distribution | Nhóm nào hưởng lợi và nhóm nào không? |
| Adverse effects | Có outcome tiêu cực hoặc [[Externality|ngoại tác]] không? |

## 10. Áp vào giải ngân

Không phải mọi đợt giải ngân đều nên đợi outcome dài hạn.

```text
Đợt sớm
→ proof of use + output/milestone verification

Đợt giữa
→ proof of use + early outcome indicators

Đợt cuối hoặc mở rộng
→ outcome evidence + báo cáo giới hạn
```

World Bank PforR là ví dụ về cơ chế liên kết giải ngân trực tiếp với kết quả xác định, nhưng dự án phải thiết kế mức kiểm chứng tương xứng và không sao chép máy móc một cơ chế tài chính công quy mô lớn.

## 11. Data schema gợi ý

```text
use_evidence_id:
resource_id:
resource_pledge_id:
resource_type:
lifecycle_status_at_use:
budget_line:
amount_or_quantity:
purpose:
recipient_or_location:
document_ids:
provenance_record:
review_result:
exceptions:
linked_milestone:

outcome_claim_id:
population:
outcome_definition:
indicator:
baseline:
target:
measurement_method:
data_source_ids:
period:
result:
confidence:
limitations:
verification_status:
```

## 12. Những lỗi cần tránh

- Dùng total money spent như chỉ số thành công.
- Dùng tổng giá trị in-kind ước tính như proof of use.
- Tính giờ planned hoặc pledged như giờ delivered.
- Gọi quyền tiếp cận chưa kích hoạt là resource used.
- Dùng số người tham dự như outcome mặc định.
- Chụp ảnh sự kiện nhưng không có danh sách, thời gian hoặc đối tượng.
- Đo outcome chỉ ở người trả lời thuận tiện.
- Thay định nghĩa chỉ số sau khi thấy kết quả.
- Chỉ báo cáo trung bình, che mất nhóm không hưởng lợi.
- Gộp output, outcome và impact vào từ “tác động”.
- Dùng một câu chuyện thành công để đại diện toàn bộ dữ liệu.

## 13. Kết luận cho dự án

> **Proof of use bảo vệ tính toàn vẹn của nguồn lực; proof of outcome bảo vệ tính trung thực của lời hứa giá trị.**

Một dự án đáng tin cần cả hai:

```text
Nguồn lực được bàn giao và accepted đúng
+ được dùng đúng
+ hoạt động được thực hiện đúng
+ kết quả được đo đúng
+ giới hạn được công bố đúng
```

## Khái niệm liên quan

- [[Bằng chứng và kiểm chứng - Bản đồ thuật ngữ]]
- [[Restricted funds]]
- [[Disbursement]]
- [[Milestone verification]]
- [[Evidence ledger và provenance]]
- [[Distributional impact]]
- [[Claim-evidence mapping]]
- [[Nguồn lực ngoài tiền - Bản đồ thuật ngữ]]
- [[Resource pledge lifecycle]]
- [[Multi-resource matching]]

## Nguồn tham khảo

- OECD — Glossary of Key Terms in Evaluation and Results-Based Management: https://www.oecd.org/en/publications/glossary-of-key-terms-in-evaluation-and-results-based-management-for-sustainable-development-second-edition_632da462-en-fr-es.html
- UNDP — Handbook on Planning, Monitoring and Evaluating for Development Results: https://www.undp.org/turkiye/publications/undp-handbook-planning-monitoring-and-evaluating-development-results
- World Bank — Program-for-Results Financing: https://www.worldbank.org/en/programs/program-for-results-financing
