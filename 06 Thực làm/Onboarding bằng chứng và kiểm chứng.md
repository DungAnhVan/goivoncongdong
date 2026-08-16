---
ai_authored: true
---

# Onboarding bằng chứng và kiểm chứng

> **Mục tiêu:** Giúp thành viên mới hiểu và sử dụng được lớp bằng chứng–kiểm chứng của dự án trong một tuần đầu, thay vì chỉ biết thuật ngữ.

## 1. Kết quả bắt buộc

Người hoàn thành onboarding phải tạo được sáu sản phẩm:

```text
1. Claim register
2. Claim–evidence matrix
3. Evidence ledger
4. Verification protocol
5. Verification statement
6. Decision log
```

Không hoàn thành nếu chỉ gửi bản tóm tắt lý thuyết.

## 2. Tài liệu phải đọc

```text
1. [[Bằng chứng và kiểm chứng - Bản đồ thuật ngữ]]
2. [[Claim-evidence mapping]]
3. [[Proof of need và demand validation]]
4. [[Proof of use và proof of outcome]]
5. [[Evidence ledger và provenance]]
6. [[Evidence quality và sufficiency]]
7. [[Verification protocol và decision rule]]
8. [[Milestone verification]]
9. [[Independent verification và third-party attestation]]
10. [[Disbursement]]
```

## 3. Bài tập pilot

Giả định một dự án tuyên bố:

> “Cộng đồng cần một hệ thống minh bạch quỹ địa phương. Pilot đã được 100 người ủng hộ, dùng đúng 100 triệu đồng, hoàn thành phần mềm và giúp giảm 30% tranh chấp.”

Người onboarding phải tách câu này thành các claim độc lập.

Tối thiểu:

```text
C-01: có nhu cầu thật ở một population xác định
C-02: có demand/cam kết hành vi
C-03: 100 triệu được dùng đúng mục đích
C-04: milestone phần mềm hoàn thành
C-05: outcome giảm tranh chấp 30%
```

## 4. Ngày 1 — Tách claim

Tạo `claim_register.md` hoặc bảng dữ liệu gồm:

```text
claim_id
claim_text
claim_type
scope
population
period
owner
risk_if_wrong
materiality
status
```

Yêu cầu:

- Không claim nào chứa nhiều mệnh đề độc lập.
- Mọi claim có phạm vi thời gian và đối tượng.
- Claim marketing phải tách khỏi claim dùng để giải ngân.

## 5. Ngày 2 — Định nghĩa evidence requirement

Trước khi xem tài liệu giả định, viết yêu cầu bằng chứng cho từng claim:

```text
claim_id
required evidence
minimum provenance
sampling
threshold
reviewer competence
independence level
decision consequence
```

Mục tiêu là tránh thiết kế tiêu chuẩn theo tài liệu thuận lợi đang có.

## 6. Ngày 3 — Dựng evidence ledger

Đăng ký tối thiểu 12 evidence object, gồm cả:

- Bằng chứng hỗ trợ.
- Bằng chứng mâu thuẫn.
- Bằng chứng không đủ phạm vi.
- Một file bị thay phiên bản.
- Một nguồn có xung đột lợi ích.
- Một dữ liệu nhạy cảm không được công khai toàn văn.

Mỗi record cần:

```text
evidence_id
source
created_at
method
version/hash
linked claims
relationship
review status
limitations
access level
```

## 7. Ngày 4 — Viết verification protocol

Chọn claim milestone hoặc outcome và viết protocol trước khi kết luận.

Protocol phải có:

- Criteria.
- Evidence requirement.
- Sampling.
- Materiality.
- Result categories.
- Decision rules.
- Conflict rule.
- Appeal.

Sau đó thực hiện review theo đúng protocol.

## 8. Ngày 5 — Phát hành verification statement

Statement phải trả lời:

```text
Claim nào được kiểm tra?
Tiêu chí nào được dùng?
Bằng chứng nào được xem?
Công việc nào đã thực hiện?
Điều gì không được kiểm tra?
Ngoại lệ nào được phát hiện?
Kết luận thuộc trạng thái nào?
Kết luận cho phép quyết định gì?
```

Không được viết:

> “Dự án đã được xác minh minh bạch.”

Phải viết theo phạm vi, ví dụ:

> “Khoản chi thuộc budget line B-03 trong giai đoạn 01/08–31/08 đã được đối soát với 12 payment reference và 10 phiếu giao nhận. Hai giao dịch tổng trị giá 8 triệu đồng chưa đủ bằng chứng occurrence; claim sử dụng đúng toàn bộ 100 triệu chưa được xác minh đầy đủ.”

## 9. Decision log

Người khác đóng vai decision-maker, không phải verifier.

```text
decision_id
question
claim_ids
verification_result
rule applied
decision
exceptions/holdback
approved_by
date
```

Verifier xác nhận sự kiện; governance quyết định hành động.

## 10. Red-team overclaim review

Một thành viên khác phải tìm ít nhất năm lỗi:

- Claim rộng hơn evidence.
- Hóa đơn bị dùng như outcome evidence.
- Thiếu provenance.
- Threshold đổi sau khi thấy kết quả.
- Người kiểm tra có xung đột lợi ích.
- Không có negative evidence.
- Verification statement che limitation.

Kết quả red-team phải được lưu, không sửa âm thầm bản cũ.

## 11. Tiêu chuẩn hoàn thành

Đạt khi:

- Claim được tách rõ.
- Requirement được viết trước evidence review.
- Ledger truy được evidence → claim → decision.
- Có ít nhất một bằng chứng bị từ chối với lý do đúng.
- Có ít nhất một claim `partially substantiated` hoặc `insufficient`, không ép mọi claim thành verified.
- Verification statement nêu scope và limitation.
- Decision-maker áp rule có dấu vết.

Không đạt khi:

- Chỉ tạo dashboard đẹp.
- Mọi claim đều `verified`.
- Không có bằng chứng mâu thuẫn.
- Không phân biệt proof of use với proof of outcome.
- Bên nhận tiền tự xác nhận và tự giải ngân.

## 12. Bộ câu hỏi phỏng vấn thành viên mới

1. Một hóa đơn chứng minh được claim nào và không chứng minh được claim nào?
2. `Not verified` khác `false` thế nào?
3. Bên thứ ba có luôn độc lập không?
4. Khi nào proof of need không tạo demand?
5. Nếu milestone đạt 90%, ai có quyền quyết định giải ngân và dựa trên rule nào?
6. Một file hash giúp gì và không giúp gì?
7. Khi outcome cải thiện, làm sao tránh tuyên bố attribution quá mức?
8. Bằng chứng nào có thể bác bỏ claim của chính anh/chị?

## 13. Definition of done cho pilot thật

Trước khi pilot đầu tiên nhận hoặc giải ngân tiền, dự án cần tối thiểu:

```text
[ ] claim register
[ ] proof-of-need package
[ ] demand test protocol
[ ] milestone definitions
[ ] evidence ledger schema
[ ] verification roles
[ ] disbursement decision rules
[ ] exception and appeal process
[ ] public claim format
[ ] data/privacy rules
```

## 14. Kết luận

> **Năng lực bằng chứng không được đánh giá bằng số thuật ngữ một người biết, mà bằng việc họ có thể biến một claim mơ hồ thành tiêu chí, bằng chứng, kiểm chứng và quyết định có thể xem xét lại hay không.**
