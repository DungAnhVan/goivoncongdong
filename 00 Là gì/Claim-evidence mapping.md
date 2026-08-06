# Claim–evidence mapping

> **Định nghĩa ngắn:** *Claim–evidence mapping* là việc tách các lời tuyên bố của dự án thành những claim có thể kiểm tra, rồi liên kết từng claim với loại bằng chứng cần có, bằng chứng thực tế đã nộp, kết quả kiểm chứng và quyết định phụ thuộc vào claim đó.

Đây là node cấu trúc trung tâm của cụm [[Bằng chứng và kiểm chứng - Bản đồ thuật ngữ]].

## 1. Vì sao cần mapping?

Một hồ sơ dự án thường trộn nhiều lời tuyên bố trong một đoạn:

> “Đây là một giải pháp rất cần thiết, được cộng đồng ủng hộ, đội ngũ có đủ năng lực, đã hoàn thành pilot và tạo tác động rõ rệt.”

Đoạn này chứa ít nhất năm claim khác nhau:

```text
C1 — vấn đề có thật và đáng giải quyết
C2 — có demand hoặc cam kết cộng đồng
C3 — đội ngũ có năng lực thực hiện
C4 — pilot đã hoàn thành theo tiêu chí
C5 — outcome đã xuất hiện
```

Mỗi claim cần bằng chứng và phương pháp kiểm tra khác nhau. Gộp chúng thành một câu khiến tài liệu nhiều nhưng khả năng kiểm chứng thấp.

## 2. Atomic claim

Một claim tốt nên đủ nhỏ để có thể trả lời:

- Đúng hay sai về phần nào?
- Bằng chứng nào hỗ trợ?
- Phạm vi thời gian và đối tượng nào?
- Ai chịu trách nhiệm?
- Quyết định nào phụ thuộc vào nó?

Ví dụ quá rộng:

```text
“Dự án có nhu cầu thị trường lớn.”
```

Tách tốt hơn:

```text
C-NEED-01:
Ít nhất 30% trong 500 xưởng nhỏ thuộc khu vực X đang quản lý đơn hàng chủ yếu bằng sổ hoặc spreadsheet rời rạc trong quý 2/2026.

C-DEMAND-02:
Ít nhất 10 xưởng thuộc segment trên chấp nhận pilot ba tháng ở mức phí 500.000 đồng/tháng trước ngày Y.
```

## 3. Claim template

```text
claim_id:
claim_text:
claim_type:
subject:
population_or_scope:
geography:
time_period:
measurement_definition:
claim_owner:
materiality:
risk_if_wrong:
status:
```

Các `claim_type` có thể gồm:

- Need.
- Demand.
- Identity.
- Capability.
- Financial use.
- Delivery/output.
- Milestone.
- Outcome.
- Compliance.
- Safety.
- Community impact.

## 4. Evidence requirement khác evidence object

### Evidence requirement

Mô tả **loại bằng chứng cần có trước khi xem hồ sơ thực tế**.

Ví dụ:

```text
- dữ liệu từ tối thiểu 100 xưởng;
- sampling bao phủ ba quy mô;
- raw data và form version;
- ít nhất một nguồn ngoài self-report;
- ngưỡng chấp nhận ≥30%.
```

### Evidence object

Là tài liệu hoặc dữ liệu thực tế được nộp:

```text
E-021 — file khảo sát raw
E-022 — danh sách mời khảo sát
E-023 — script làm sạch dữ liệu
E-024 — biên bản quan sát tại 12 xưởng
```

Tách hai lớp này giúp tránh việc thiết kế tiêu chí theo những tài liệu thuận lợi đã có.

## 5. Claim–evidence matrix

| Claim ID | Claim | Evidence requirement | Evidence IDs | Relationship | Review status | Decision |
|---|---|---|---|---|---|---|
| C-01 | Vấn đề tồn tại ở segment A | survey + observation | E-01, E-02 | supports | accepted with limits | cho pilot |
| C-02 | Có 10 khách trả phí | signed order + payment | E-03 | partially supports | 7/10 | sửa offer |
| C-03 | Mốc kỹ thuật đạt | test report + sample | E-04, E-05 | supports | verified | giải ngân 30% |
| C-04 | Outcome giảm 20% thời gian | baseline + follow-up | E-06 | insufficient | not verified | chưa truyền thông |

Matrix phải hiển thị cả claim chưa có bằng chứng và bằng chứng mâu thuẫn.

## 6. Quan hệ giữa claim và evidence

Không chỉ dùng `supports`.

```text
supports
partially_supports
contradicts
limits
supersedes
context_only
does_not_address
```

Ví dụ:

- Hóa đơn `supports` claim đã mua thiết bị.
- Hóa đơn `does_not_address` claim thiết bị tạo outcome.
- Khiếu nại người dùng có thể `contradicts` claim 100% hài lòng.
- Báo cáo mới có thể `supersedes` báo cáo cũ.

## 7. Direct và indirect evidence

### Direct evidence

Quan sát trực tiếp đối tượng của claim.

Ví dụ: log giao dịch cho claim có thanh toán thật.

### Indirect evidence

Suy ra claim qua dấu hiệu liên quan.

Ví dụ: thư quan tâm là tín hiệu demand, nhưng không bằng thanh toán.

Mapping nên ghi `directness` để tránh một proxy yếu được truyền thông như chứng minh trực tiếp.

## 8. Claim scope và overclaiming

Bằng chứng có phạm vi:

```text
50 người tại một xã
trong hai tuần
với một phiên bản sản phẩm
```

Không được tự động suy ra:

```text
người dân Việt Nam
trong dài hạn
đối với mọi phiên bản sản phẩm
```

Các trường bắt buộc:

- Population.
- Time.
- Geography.
- Product/version.
- Conditions.

Nếu truyền thông rút gọn, phải giữ link về full claim scope.

## 9. Claim dependency graph

Một claim có thể phụ thuộc claim khác:

```text
C1: target population được xác định đúng
        ↓
C2: proof of need hợp lệ
        ↓
C3: demand test đại diện cho đúng population
        ↓
C4: quyết định mở pilot
```

Nếu C1 bị bác bỏ, các claim phụ thuộc cần được review lại.

Tương tự:

```text
C-use: tiền đã dùng đúng
+
C-output: output đã giao
+
C-quality: output đạt chuẩn
→
C-milestone: milestone hoàn thành
→
D-disbursement: mở đợt tiếp theo
```

## 10. Claim owner và evidence owner

- **Claim owner** chịu trách nhiệm cho lời tuyên bố.
- **Evidence owner/custodian** chịu trách nhiệm cung cấp hoặc giữ bằng chứng.
- **Reviewer** đánh giá.
- **Decision-maker** ra quyết định.

Bốn vai trò có thể khác nhau. Việc tách vai trò giúp tránh người kể câu chuyện đồng thời tự chọn bằng chứng và tự giải ngân.

## 11. Burden of proof

Không phải mọi claim cần cùng mức bằng chứng.

| Claim | Burden gợi ý |
|---|---|
| Ý tưởng thảo luận | nguồn sơ bộ, ghi rõ giả thuyết |
| Claim marketing nhỏ | bằng chứng nội bộ có provenance |
| Claim dùng để mở giải ngân | tiêu chí và review rõ |
| Claim outcome công khai | phương pháp, baseline, giới hạn |
| Claim an toàn/tài chính trọng yếu | kiểm chứng độc lập phù hợp |

Xem [[Evidence quality và sufficiency]].

## 12. Claim status

```text
Proposed
→ Evidence requirement defined
→ Evidence pending
→ Under review
→ Substantiated
→ Partially substantiated
→ Unsubstantiated
→ Contradicted
→ Superseded
→ Expired
```

`Unsubstantiated` không đồng nghĩa `false`; nó có nghĩa chưa có đủ bằng chứng theo burden đã đặt.

## 13. Quy tắc truyền thông

Nội dung công khai nên được sinh từ claim đã mapping:

```text
Public statement:
“Pilot giúp giảm 18% median thời gian xử lý tại 4 xưởng trong 8 tuần.”

Không viết:
“Giải pháp tăng hiệu suất cho mọi xưởng.”
```

Mỗi claim công khai có thể kèm:

- Status badge.
- Scope.
- Evidence summary.
- Verified by.
- Date.
- Limitations.

## 14. Data schema gợi ý

```text
claim_id:
project_id:
claim_type:
text:
scope:
owner:
requirement_ids:
evidence_links:
contradictory_evidence:
review_ids:
status:
confidence:
limitations:
dependent_claim_ids:
linked_decision_ids:
public_summary:
```

## 15. Quy trình review định kỳ

```text
Extract claims from proposal
→ split atomic claims
→ classify claim type
→ define evidence requirements
→ collect/register evidence
→ map supports/contradictions
→ review sufficiency
→ issue status
→ link decision
→ expire or update over time
```

## 16. Những lỗi cần tránh

- Một claim quá rộng chứa nhiều mệnh đề.
- Chỉ mapping bằng chứng ủng hộ.
- Không nêu scope.
- Evidence requirement được viết sau khi xem kết quả.
- Claim cũ vẫn công khai sau khi evidence hết hạn.
- Một badge verified áp cho toàn dự án.
- Dùng số lượng tài liệu thay cho chất lượng bằng chứng.
- Không nối claim với quyết định thực tế.

## 17. Kết luận cho dự án

> **Claim–evidence mapping là cách biến lời kể của dự án thành một cấu trúc có thể tranh luận, kiểm tra và cập nhật mà không phá hủy toàn bộ câu chuyện.**

Nó cho phép dự án vẫn có tầm nhìn lớn, nhưng mọi claim đang dùng để xin tiền, giải ngân hoặc tuyên bố tác động đều phải có phạm vi và gánh nặng bằng chứng tương xứng.

## Khái niệm liên quan

- [[Bằng chứng và kiểm chứng - Bản đồ thuật ngữ]]
- [[Evidence ledger và provenance]]
- [[Evidence quality và sufficiency]]
- [[Proof of need và demand validation]]
- [[Proof of use và proof of outcome]]
- [[Milestone verification]]
- [[Verification protocol và decision rule]]

## Nguồn tham khảo

- W3C — PROV-O: https://www.w3.org/TR/prov-o/
- OECD — Results-Based Management Glossary: https://www.oecd.org/en/publications/glossary-of-key-terms-in-evaluation-and-results-based-management-for-sustainable-development-second-edition_632da462-en-fr-es.html
- ISO — ISO/IEC 17029:2019: https://www.iso.org/standard/29352.html
