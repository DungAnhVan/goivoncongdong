# Campaign failure, recovery and termination

> **Định nghĩa ngắn:** *Campaign failure* là trạng thái chiến dịch không còn đáp ứng một hoặc nhiều điều kiện cốt lõi đã cam kết. *Recovery* là quá trình khắc phục để đưa chiến dịch trở lại trạng thái khả thi và tuân thủ. *Termination* là quyết định chấm dứt thực hiện toàn bộ hoặc một phần chiến dịch khi phục hồi không còn hợp lý, được phép hoặc khả thi.

Node này không coi mọi thất bại là gian lận và không coi mọi khó khăn là lý do để tiếp tục vô thời hạn.

## 1. Vì sao phải phân loại thất bại?

Cùng một biểu hiện `dự án chưa hoàn thành` có thể đến từ:

```text
Không đủ tiền
Mất nguồn lực blocking
Chậm nhà cung cấp
Output không đạt chất lượng
Founder rời dự án
Mất giấy phép
Gian lận
Thiên tai hoặc external shock
Mục đích không còn phù hợp
```

Mỗi nguyên nhân đòi hỏi response khác nhau.

## 2. Funding failure

```text
Không đạt [[Provision point và threshold mechanism|provision point]]
trước deadline
```

Thường xảy ra trước activation.

Response có thể gồm:

- Không collect.
- Refund.
- Release pledge/reservation.
- Gia hạn nếu charter cho phép.
- Chuyển sang fallback scope đã công bố.
- Đóng campaign.

Không được chuyển thành keep-it-all sau deadline nếu ban đầu cam kết all-or-nothing mà chưa có re-consent hợp lệ.

## 3. Execution delay

Dự án vẫn có khả năng hoàn thành nhưng chậm hơn kế hoạch.

Cần phân biệt:

```text
Delay within tolerance
→ xử lý vận hành

Material delay
→ change review, disclosure, có thể re-consent

Indefinite delay
→ xem xét failure/termination
```

Delay không tự động là failure cuối cùng, nhưng delay lặp lại mà không có lịch phục hồi đáng tin là tín hiệu material.

## 4. Partial performance

Một phần output đã hoàn thành, phần còn lại không.

Phải ghi:

- Phần nào đã làm.
- Chất lượng ra sao.
- Nguồn lực nào đã dùng.
- Phần nghĩa vụ còn lại.
- Partial output có giá trị độc lập không.
- Contributor benefit nào đã fulfil.
- Refund/remedy nào khả thi.

Không báo cáo `đã hoàn thành 70%` nếu 30% còn thiếu là thành phần blocking khiến toàn bộ sản phẩm không sử dụng được.

## 5. Quality failure

Output tồn tại nhưng không đạt acceptance criteria.

```text
Delivered
≠ Accepted
```

Response có thể gồm:

- Rework.
- Replacement.
- Partial acceptance.
- Price adjustment.
- Holdback.
- Independent retest.
- Termination nếu lỗi không thể khắc phục.

Không hạ tiêu chí sau khi test thất bại để đổi trạng thái thành đạt.

## 6. Resource failure

Nguồn lực thiết yếu bị mất, rút, hết hạn hoặc không dùng được.

Ví dụ:

- Technical lead rời.
- Venue bị hủy.
- Thiết bị hỏng.
- Dataset không có quyền sử dụng.
- Matching fund bị rút.
- Nhà cung cấp phá sản.

Cần truy dependency:

```text
Resource failure
→ need/match nào bị ảnh hưởng?
→ provision point còn đạt không?
→ milestone nào phải pause?
→ disbursement nào phải dừng?
→ actor nào cần thông báo?
```

Xem [[Resource pledge lifecycle]] và [[Multi-resource matching]].

## 7. Governance failure

Xảy ra khi cấu trúc quyết định hoặc kiểm soát không còn hoạt động đáng tin.

Ví dụ:

- Không còn người đủ thẩm quyền.
- Một người kiểm soát toàn bộ tiền và verification.
- Hội đồng không thể họp hoặc deadlock.
- Conflict of interest không được xử lý.
- Hồ sơ quyết định không tồn tại.
- Người phê duyệt là người hưởng lợi trực tiếp.

Response có thể là:

- Thay người có thẩm quyền.
- Chỉ định interim governance.
- Independent review.
- Freeze disbursement.
- Transfer campaign administration.
- Termination nếu không phục hồi được.

## 8. Compliance failure

Chiến dịch không còn đáp ứng điều kiện pháp lý, giấy phép, hợp đồng hoặc chính sách bắt buộc.

Ví dụ:

- Mất giấy phép.
- Không thể KYC người nhận.
- Dữ liệu được thu sai consent.
- Reward hoặc investment structure không phù hợp.
- Tài sản không được phép sử dụng.

Không tiếp tục chỉ vì mục tiêu xã hội tốt. Phải pause và đánh giá phương án hợp lệ.

## 9. Purpose failure

Mục đích không còn:

- Khả thi.
- Cần thiết.
- Phù hợp với nhóm hưởng lợi.
- Có thể thực hiện trong restriction ban đầu.

Ví dụ, nhu cầu biến mất vì một giải pháp công đã được cung cấp đầy đủ.

Purpose failure không phải thất bại đạo đức. Nhưng giữ tiền để tìm mục đích mới mà không re-consent là governance failure.

## 10. Integrity failure

Bao gồm:

- Gian lận.
- Che giấu xung đột lợi ích.
- Làm giả bằng chứng.
- Chi sai mục đích có chủ ý.
- Tạo contributor giả.
- Thông đồng.
- Ghi đè hồ sơ.

Response đầu tiên thường là:

```text
Freeze affected transactions
→ preserve evidence
→ separate implicated actors
→ independent investigation
→ protect whistleblower and data
→ notify required parties
→ decide recovery, remedy or termination
```

Không để người bị nghi ngờ tự kiểm tra chính mình.

## 11. External shock

Sự kiện ngoài khả năng kiểm soát hợp lý:

- Thiên tai.
- Dịch bệnh.
- Chiến sự.
- Đứt chuỗi cung ứng lớn.
- Thay đổi chính sách bất ngờ.
- Mất hạ tầng thiết yếu.

External shock không tự động miễn mọi nghĩa vụ. Cần đánh giá:

- Nghĩa vụ nào còn thực hiện được.
- Bảo hiểm hoặc contingency.
- Tác động lên beneficiary.
- Alternative performance.
- Refund/release.
- Thời hạn phục hồi hợp lý.

## 12. Failure status model

```text
At risk
→ Under review
→ Paused
→ Corrective action
→ Recovery monitoring
→ Recovered
```

Các nhánh khác:

```text
Transferred
Partially completed
Terminated
Closed with unresolved obligations
Closed
```

Không dùng một status `failed` duy nhất cho mọi trạng thái.

## 13. Early-warning indicators

- Milestone liên tục trễ.
- Burn rate cao hơn plan.
- Evidence quality giảm.
- Resource blocking sắp hết hạn.
- Team turnover ở vai trò cốt lõi.
- Grievance tăng.
- Vendor concentration.
- Dữ liệu outcome không xuất hiện.
- Reconciliation chậm.
- Founder tránh công bố thay đổi.
- Repeated amendment để hạ scope.

Chỉ báo không tự chứng minh failure; nó kích hoạt review.

## 14. Corrective action plan

```text
failure_or_risk_id:
root_cause:
affected_commitments:
affected_actor_groups:
immediate_controls:
corrective_actions:
owner:
deadline:
required_resources:
verification_criteria:
next_decision_date:
escalation_rule:
evidence_ids:
```

Corrective action phải có tiêu chí kết thúc. Không dùng “đang xử lý” vô thời hạn.

## 15. Recovery test

Trước khi resume, phải xác nhận:

```text
Root cause đã được xử lý?
Provision point còn đạt?
Nguồn lực blocking đã thay thế?
Charter có cần amendment?
Actor có cần re-consent?
Milestone và budget còn khả thi?
Risk mới đã disclosed?
Governance có độc lập đủ?
```

Resume là một quyết định, không phải hệ quả tự động của việc nhóm nói đã ổn.

## 16. Transfer

Có thể chuyển dự án hoặc nghĩa vụ cho actor khác khi:

- Charter cho phép.
- Actor nhận có năng lực.
- Restriction cho phép.
- Rights và data obligations được xử lý.
- Contributor được thông báo hoặc re-consent khi cần.
- Tài sản và hồ sơ được bàn giao có kiểm kê.

Transfer không phải cách để founder cũ trốn nghĩa vụ.

## 17. Termination decision

Termination cần ghi:

```text
termination_id:
scope:
reason:
failure_classification:
recovery_attempts:
alternatives_considered:
affected_commitments:
financial_position:
unused_resources:
refund_release_obligations:
beneficiary_protection:
records_and_data_plan:
approved_by:
effective_at:
evidence_ids:
```

Có thể terminate:

- Toàn campaign.
- Một module.
- Một milestone.
- Một contributor benefit.
- Một supplier relationship.

## 18. Termination không xóa nghĩa vụ

Sau termination vẫn có thể còn:

- Refund.
- Vendor debt.
- Payroll.
- Tax.
- Return of equipment.
- Data deletion/return.
- IP obligations.
- Reporting.
- Grievance.
- Record retention.

Đó là lý do phải có [[Campaign closure, wind-down and dissolution]].

## 19. Communication khi thất bại

Thông báo phải nói:

1. Điều gì xảy ra.
2. Điều gì đã biết và chưa biết.
3. Cam kết nào bị ảnh hưởng.
4. Nguồn lực nào đã dùng.
5. Việc gì đang tạm dừng.
6. Corrective action hoặc termination process.
7. Quyền refund/release.
8. Ngày cập nhật tiếp theo.
9. Grievance route.

Không nên:

- Chỉ xin lỗi chung chung.
- Đổ lỗi cho “thị trường”.
- Xóa campaign page.
- Mở campaign mới để bù campaign cũ mà không disclosure.

## 20. Dấu hiệu cảnh báo

- Delay không có next decision date.
- Corrective action không có owner.
- Founder tự xác nhận recovery.
- Gian lận bị gọi là “sai sót truyền thông”.
- External shock được dùng cho vấn đề đã có từ trước.
- Termination nhưng vẫn nhận contribution mới.
- Không kiểm kê nguồn lực đã dùng.
- Không phân biệt failure của dự án và dissolution của pháp nhân.
- Không có public final status.

## 21. Kết luận

> **Xử lý thất bại tốt không phải là bảo đảm mọi dự án thành công; đó là khả năng nhận diện đúng loại thất bại, giới hạn tổn thất, bảo vệ các bên và đóng hoặc phục hồi dự án bằng quyết định có dấu vết.**

## Khái niệm liên quan

- [[Campaign charter]]
- [[Material change, pivot and re-consent]]
- [[Refund and release mechanism]]
- [[Residual funds and unused resources]]
- [[Campaign closure, wind-down and dissolution]]
- [[Milestone verification]]
- [[Evidence ledger và provenance]]
- [[Stakeholder engagement và grievance mechanism]]
