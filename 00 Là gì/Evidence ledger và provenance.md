---
ai_authored: true
---

# Evidence ledger và provenance

> **Định nghĩa ngắn:** *Evidence ledger* là sổ chỉ mục có cấu trúc ghi nhận các bằng chứng, trạng thái kiểm tra và quyết định liên quan. *Provenance* là thông tin về nguồn gốc, quá trình tạo, biến đổi, chuyển giao và phiên bản của một bằng chứng.

Evidence ledger không phải chính bằng chứng. Nó là lớp giúp trả lời:

```text
Bằng chứng nào tồn tại?
→ hỗ trợ claim nào?
→ đến từ đâu?
→ ai tạo và khi nào?
→ đã bị biến đổi thế nào?
→ ai đã kiểm tra?
→ kết quả kiểm tra là gì?
→ quyết định nào đã dùng nó?
```

## 1. Vì sao cần evidence ledger?

Khi dự án nhỏ, bằng chứng thường nằm rải rác trong:

- Google Drive.
- Zalo, email hoặc chat.
- Ảnh trong điện thoại.
- File kế toán.
- Biên bản giấy.
- Database sản phẩm.
- Báo cáo PDF.

Nếu không có ledger, nhóm có thể có rất nhiều file nhưng vẫn không biết:

- File nào là bản gốc.
- File nào đã hết hiệu lực.
- Claim nào đang thiếu bằng chứng.
- Hai bằng chứng có mâu thuẫn không.
- Ai đã dùng tài liệu nào để phê duyệt giải ngân.

## 2. Evidence ledger tối thiểu

```text
evidence_id:
evidence_type:
title:
linked_claim_ids:
linked_project_id:
source_agent:
created_at:
received_at:
collection_method:
original_location:
current_location:
file_hash_or_version:
access_level:
provenance_status:
review_status:
reviewer:
reviewed_at:
limitations:
contradictions:
linked_decision_ids:
retention_rule:
```

Không nhất thiết mọi trường đều có ngay từ đầu, nhưng `evidence_id`, claim liên quan, nguồn, thời gian, phiên bản và trạng thái kiểm tra là lớp tối thiểu.

## 3. Provenance là gì?

W3C PROV mô hình hóa provenance bằng ba nhóm lõi:

```text
Entity
→ dữ liệu, tài liệu, vật thể hoặc phiên bản

Activity
→ hành động tạo, đo, xử lý, tổng hợp hoặc biến đổi

Agent
→ người, tổ chức hoặc hệ thống chịu vai trò
```

Ví dụ:

```text
Entity: bảng kết quả khảo sát V2
wasGeneratedBy
Activity: lọc phản hồi trùng và loại mẫu không hợp lệ
wasAssociatedWith
Agent: nhóm nghiên cứu A
wasDerivedFrom
Entity: file phản hồi gốc V1
```

Dự án không cần triển khai đầy đủ ontology ngay. Nhưng tư duy này giúp phân biệt file cuối với quá trình tạo ra file đó.

## 4. Provenance của từng loại bằng chứng

### Ảnh và video

- Ai chụp?
- Thời gian và địa điểm?
- Đối tượng nào?
- File gốc hay file đã nén/chỉnh sửa?
- Có định danh liên kết với milestone không?

### Dữ liệu khảo sát

- Câu hỏi và phiên bản form nào?
- Ai được mời và ai trả lời?
- Cách loại phản hồi không hợp lệ?
- File raw có còn không?
- Script hoặc bước xử lý nào tạo bảng kết quả?

### Hóa đơn và chứng từ

- Ai phát hành?
- Giao dịch và hàng hóa nào?
- Có đối soát với ngân hàng và giao nhận không?
- Có sửa đổi, hủy hoặc thay thế không?

### Sensor hoặc system log

- Thiết bị/hệ thống nào tạo log?
- Đồng hồ có đồng bộ không?
- Ai có quyền sửa dữ liệu?
- Có khoảng trống hoặc mất kết nối không?
- Version phần mềm nào đang chạy?

## 5. Ledger không đồng nghĩa blockchain

Một evidence ledger có thể được triển khai bằng:

- Spreadsheet có kiểm soát phiên bản.
- Database quan hệ.
- Document management system.
- Git cho file văn bản và schema.
- Object storage với metadata.
- Append-only event log.

Blockchain chỉ giúp một số thuộc tính về ghi dấu hoặc phân tán niềm tin. Nó không tự giải quyết:

- Dữ liệu đầu vào sai.
- Người tạo bằng chứng có xung đột lợi ích.
- Ảnh không đúng đối tượng.
- Phương pháp đo kém.
- Claim bị diễn giải quá rộng.

> **Dữ liệu sai được ghi bất biến vẫn là dữ liệu sai.**

## 6. Trạng thái bằng chứng

```text
Registered
→ Source checked
→ Integrity checked
→ Content reviewed
→ Accepted / Accepted with limitations / Rejected
→ Superseded / Expired / Withdrawn
```

Nên tách ít nhất ba lớp:

| Lớp | Ý nghĩa |
|---|---|
| Integrity | File có nguyên vẹn, đúng phiên bản và không bị thay ngoài quy trình không? |
| Authenticity | Nguồn có đúng là người/tổ chức được khai báo không? |
| Evidential value | Nội dung có thực sự hỗ trợ claim đang xét không? |

Một hóa đơn có thể authentic nhưng vẫn không chứng minh outcome.

## 7. Quy tắc versioning

Không ghi đè âm thầm bằng chứng cũ.

```text
E-001 v1
→ file gốc được nộp

E-001 v2
→ bổ sung chữ ký

E-001 v3
→ đính chính số lượng
```

Mỗi phiên bản cần:

- Lý do thay đổi.
- Người thực hiện.
- Thời gian.
- Liên kết phiên bản trước.
- Claim hoặc quyết định nào bị ảnh hưởng.

Nếu bằng chứng đã dùng để giải ngân rồi mới bị sửa, hệ thống phải tạo cảnh báo và review quyết định cũ.

## 8. Contradiction và negative evidence

Evidence ledger không chỉ lưu tài liệu ủng hộ claim. Nó phải lưu:

- Bằng chứng mâu thuẫn.
- Dữ liệu âm tính.
- Mẫu bị loại và lý do.
- Khiếu nại chưa giải quyết.
- Phiên bản đã bị bác bỏ.

Một schema gợi ý:

```text
relationship:
- supports
- partially_supports
- contradicts
- does_not_address
- supersedes
```

Điều này giúp [[Claim-evidence mapping]] không biến thành hồ sơ chỉ chọn bằng chứng thuận lợi.

## 9. Quyền truy cập và bảo vệ dữ liệu

Không phải mọi bằng chứng đều công khai.

```text
Public
→ có thể hiển thị toàn văn

Community-visible
→ thành viên dự án được xem

Reviewer-only
→ chỉ người kiểm chứng được xem

Restricted
→ dữ liệu nhạy cảm, chỉ lưu metadata và quyền truy cập có kiểm soát
```

Nền tảng có thể công khai:

- Evidence ID.
- Loại bằng chứng.
- Người xác nhận.
- Thời gian.
- Trạng thái.
- Tóm tắt và giới hạn.

Trong khi giữ kín dữ liệu cá nhân hoặc bí mật thương mại.

## 10. Liên kết evidence với decision

Mỗi quyết định quan trọng nên chỉ ra bằng chứng đã được dùng:

```text
decision_id: D-042
question: Mở giải ngân đợt 2?
claim_ids: C-17, C-18
accepted_evidence: E-104, E-107, E-110
rejected_evidence: E-108
review_notes: ...
decision_rule: VR-05
result: Approved with holdback
approved_by: ...
```

Khi một bằng chứng bị rút lại, hệ thống có thể truy ngược các quyết định phụ thuộc vào nó.

## 11. Mức triển khai theo giai đoạn

### Pilot rất nhỏ

- Một bảng `evidence_register.csv`.
- Folder bất biến tương đối cho file gốc.
- Mỗi claim có Evidence ID.
- Review note và decision log.

### Pilot nhiều dự án

- Database evidence object.
- Version, hash, role và access control.
- Link trực tiếp với milestone và disbursement.

### Nền tảng quy mô lớn

- Event log.
- Provenance graph.
- API để truy vấn claim → evidence → decision.
- Chính sách retention, privacy và audit.

## 12. Những lỗi cần tránh

- Chỉ lưu link file mà không lưu source và version.
- Cho phép xóa bằng chứng đã dùng cho quyết định.
- Đánh đồng file hash với sự thật của nội dung.
- Không lưu bước làm sạch hoặc tổng hợp dữ liệu.
- Chỉ lưu evidence thuận lợi.
- Không ghi ai đã xem và chấp nhận bằng chứng.
- Dùng một file cho nhiều claim nhưng không mô tả phạm vi hỗ trợ.

## 13. Kết luận cho dự án

> **Evidence ledger biến bằng chứng từ một đống tài liệu thành một mạng lưới có thể truy nguyên và chịu trách nhiệm. Provenance cho biết vì sao ta có thể hoặc không thể tin từng mắt xích của mạng lưới đó.**

## Khái niệm liên quan

- [[Bằng chứng và kiểm chứng - Bản đồ thuật ngữ]]
- [[Claim-evidence mapping]]
- [[Evidence quality và sufficiency]]
- [[Milestone verification]]
- [[Independent verification và third-party attestation]]
- [[Internal financial controls]]
- [[Audit trail]]

## Nguồn tham khảo

- W3C — PROV-O: https://www.w3.org/TR/prov-o/
- W3C — PROV-AQ: https://www.w3.org/TR/prov-aq/
- W3C — PROV Data Model family overview: https://www.w3.org/TR/prov-overview/
