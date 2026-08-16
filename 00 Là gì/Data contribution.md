---
ai_authored: true
---

# Data contribution

> **Định nghĩa ngắn:** *Data contribution* là việc một cá nhân hoặc tổ chức cung cấp dữ liệu, metadata, quyền truy cập dữ liệu hoặc khả năng tạo dữ liệu cho dự án theo mục đích và điều kiện xác định.

Data contribution không đơn giản là “gửi một file”. Nó phải trả lời đồng thời:

```text
Dữ liệu gì?
→ ai có quyền cung cấp?
→ dự án được phép làm gì?
→ trong thời gian nào?
→ có thể chia sẻ hoặc tái sử dụng không?
→ chất lượng và provenance thế nào?
→ điều gì phải xảy ra khi quyền truy cập kết thúc?
```

## 1. Các dạng đóng góp dữ liệu

```text
Dataset transfer
→ chuyển một bản dữ liệu cho dự án

Data access
→ cấp quyền truy cập mà không chuyển toàn bộ dữ liệu

Data feed / API access
→ cấp dòng dữ liệu định kỳ hoặc thời gian thực

Data collection contribution
→ hỗ trợ thu thập dữ liệu mới

Labeling / annotation
→ đóng góp nhãn, phân loại hoặc metadata

Derived data contribution
→ cung cấp dữ liệu đã tổng hợp, làm sạch hoặc phân tích

Data stewardship
→ duy trì quyền truy cập, chất lượng và quản trị dữ liệu
```

Không phải mọi dạng đều chuyển quyền sở hữu.

## 2. Ranh giới với evidence

```text
Data contribution
→ quyền và điều kiện cung cấp dữ liệu

[[Evidence ledger và provenance]]
→ dữ liệu/bằng chứng đến từ đâu, phiên bản nào và đã biến đổi ra sao

[[Evidence quality và sufficiency]]
→ dữ liệu có đủ chất lượng để hỗ trợ claim không

[[Proof of use và proof of outcome]]
→ dữ liệu được dùng để chứng minh việc sử dụng nguồn lực hay kết quả nào
```

Một dataset có provenance tốt vẫn có thể không được phép sử dụng cho mục đích dự án. Ngược lại, có quyền truy cập hợp lệ không có nghĩa dữ liệu đủ chất lượng để làm bằng chứng.

## 3. Quyền cung cấp và quyền sử dụng

Trước khi nhận data contribution, phải xác định:

- Contributor có sở hữu, kiểm soát hoặc được ủy quyền cung cấp không?
- Có dữ liệu cá nhân, dữ liệu nhạy cảm, bí mật kinh doanh hoặc quyền của bên thứ ba không?
- Dự án được phép lưu, xử lý, kết hợp, công bố hay huấn luyện mô hình không?
- Có giới hạn mục đích, lãnh thổ, thời gian hoặc nhóm người dùng không?
- Có nghĩa vụ xóa, trả lại hoặc chấm dứt truy cập không?

Không dùng từ mơ hồ “dữ liệu thuộc về cộng đồng” để bỏ qua quyền và lợi ích chồng lấn.

## 4. Data access không giống data ownership

```text
Ownership / control
→ ai có quyền quyết định cơ bản đối với dữ liệu?

Access right
→ ai được xem hoặc truy xuất?

Use right
→ được xử lý cho mục đích nào?

Sharing right
→ có được chuyển tiếp cho bên khác không?

Publication right
→ có được công bố dữ liệu hoặc kết quả dẫn xuất không?

Model-training right
→ có được dùng cho huấn luyện AI không?
```

Các quyền này phải được ghi riêng. Không suy từ việc “đã nhận file”.

## 5. Data contribution record

```text
data_contribution_id:
provider_id:
project_id:
data_description:
data_category:
data_subject_or_population:
collection_method:
time_coverage:
geographic_coverage:
format:
volume:
update_frequency:
access_method:
rights_basis:
permitted_purposes:
prohibited_uses:
sharing_rights:
publication_rights:
model_training_rights:
retention_period:
revocation_or_termination_rule:
security_requirements:
quality_summary:
provenance_record_id:
version_or_hash:
status:
```

## 6. Data minimisation theo mục đích

Dự án không nên nhận càng nhiều dữ liệu càng tốt.

Phải hỏi:

```text
Claim hoặc quyết định nào cần dữ liệu này?
→ trường dữ liệu tối thiểu là gì?
→ có thể dùng dữ liệu tổng hợp hoặc ẩn danh hơn không?
→ ai cần truy cập?
→ lưu bao lâu?
```

Nguồn lực dữ liệu càng nhạy cảm thì chi phí bảo vệ, trách nhiệm và nguy cơ gây hại càng lớn.

## 7. Chất lượng dữ liệu

Trước khi matching hoặc acceptance, cần ghi:

| Trục | Câu hỏi |
|---|---|
| Relevance | Dữ liệu có phù hợp nhu cầu dự án không? |
| Coverage | Bao phủ nhóm, thời gian và địa bàn nào? |
| Completeness | Thiếu trường hoặc kỳ dữ liệu nào? |
| Accuracy | Có kiểm tra sai lệch hoặc lỗi đo không? |
| Timeliness | Dữ liệu còn đủ mới không? |
| Consistency | Định nghĩa và cách thu thập có ổn định không? |
| Bias | Nhóm nào bị bỏ sót hoặc đại diện quá mức? |
| Traceability | Có raw source và lịch sử biến đổi không? |

## 8. Revocation và dữ liệu dẫn xuất

Cần làm rõ trước:

```text
Contributor chấm dứt quyền truy cập
→ dữ liệu gốc có phải xóa không?
→ bản sao lưu xử lý thế nào?
→ kết quả tổng hợp có được giữ không?
→ model đã huấn luyện xử lý ra sao?
→ quyết định cũ dùng dữ liệu đó có cần review không?
```

Không phải mọi quyền đều có thể rút lại theo cùng một cách. Vì vậy cần quyết định pháp lý và kỹ thuật trước khi triển khai, không hứa chung chung “có thể xóa bất cứ lúc nào”.

## 9. Data contribution như một nguồn lực cộng đồng

Ví dụ:

```text
Nông dân đóng góp nhật ký mùa vụ
→ viện nghiên cứu đóng góp dữ liệu thời tiết
→ doanh nghiệp đóng góp log máy
→ địa phương cấp dữ liệu hạ tầng
→ cộng đồng gắn nhãn và phát hiện lỗi
```

Giá trị có thể xuất hiện khi nhiều nguồn được ghép. Nhưng việc ghép dữ liệu làm tăng:

- Khả năng tái định danh.
- Xung đột quyền.
- Bias.
- Rủi ro sử dụng ngoài mục đích.

Do đó [[Multi-resource matching]] chỉ xác định khả năng phù hợp; acceptance vẫn cần review quyền, chất lượng và bảo vệ dữ liệu.

## 10. Proof of contribution và proof of use

Bằng chứng bàn giao có thể là:

- Access grant hoặc API key record.
- Data sharing agreement.
- Hash/version của dataset.
- Transfer log.
- Schema và data dictionary.
- Security review.

Proof of use cần ghi:

- Ai truy cập.
- Dùng cho claim, activity hoặc decision nào.
- Phiên bản nào.
- Kết quả dẫn xuất nào.
- Có sự cố hoặc sử dụng ngoài phạm vi không.

## 11. Rủi ro

- Contributor không có quyền cung cấp.
- Consent hoặc mục đích không phù hợp.
- Dataset cũ nhưng được quảng bá như dữ liệu hiện tại.
- Đếm số dòng thay cho chất lượng.
- Dữ liệu của nhóm dễ tổn thương bị dùng làm social proof.
- Cho phép bên thứ ba truy cập ngoài điều kiện ban đầu.
- Huấn luyện AI khi chưa có quyền rõ.
- Không có quy trình chấm dứt và xóa.
- Công khai metadata khiến cá nhân vẫn có thể bị nhận diện.

## 12. Kết luận

> **Đóng góp dữ liệu là cấp quyền có điều kiện đối với một nguồn lực có thể sao chép và tái sử dụng; vì vậy giá trị của nó luôn đi cùng trách nhiệm quản trị.**

## Khái niệm liên quan

- [[Nguồn lực ngoài tiền - Bản đồ thuật ngữ]]
- [[In-kind contribution]]
- [[Evidence ledger và provenance]]
- [[Evidence quality và sufficiency]]
- [[Multi-resource matching]]
- [[Resource pledge lifecycle]]
- [[Proof of use và proof of outcome]]

## Nguồn tham khảo

- OECD — Recommendation on Enhancing Access to and Sharing of Data: https://www.oecd.org/en/publications/access-to-public-research-data-toolkit_a12e8998-en/oecd-recommendation-on-enhancing-access-to-and-sharing-of-data-2021_cd69b13a-en.html
- OECD — Enhancing Access to and Sharing of Data: https://www.oecd.org/en/publications/enhancing-access-to-and-sharing-of-data_276aaca8-en.html
- OECD — Going Digital Guide to Data Governance Policy Making: https://www.oecd.org/en/publications/going-digital-guide-to-data-governance-policy-making_40d53904-en.html
