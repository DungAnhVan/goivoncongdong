# Campaign closure, wind-down and dissolution

> **Định nghĩa ngắn:** *Campaign closure* là việc chiến dịch ngừng nhận cam kết mới. *Wind-down* là quá trình đóng dần hoạt động, xử lý nghĩa vụ và bàn giao tài sản/hồ sơ. *Dissolution* là việc giải thể pháp nhân hoặc thiết chế pháp lý, không đồng nhất với việc đóng một chiến dịch.

Node này trả lời:

> Làm sao kết thúc một chiến dịch mà không bỏ lại tiền, tài sản, dữ liệu, lời hứa và khiếu nại trong trạng thái vô chủ?

## 1. Phân biệt các trạng thái

```text
Campaign closed to new commitments
→ không nhận thêm pledge

Campaign completed
→ purpose và nghĩa vụ chính đã hoàn thành

Campaign wound down
→ nghĩa vụ còn lại đã xử lý có trật tự

Project terminated
→ dừng trước khi hoàn thành

Legal entity dissolved
→ pháp nhân chấm dứt tồn tại theo quy trình pháp lý
```

Một campaign có thể closed nhưng chưa completed. Một project có thể terminated nhưng pháp nhân vẫn tồn tại. Một pháp nhân dissolution không tự động xóa nghĩa vụ campaign.

## 2. Closure triggers

- Hết thời hạn huy động.
- Đạt provision point và chuyển sang execution.
- Không đạt threshold.
- Purpose hoàn thành.
- Campaign bị terminate.
- Material change yêu cầu mở campaign mới.
- Pháp nhân hoặc operator không thể tiếp tục.
- Regulatory/legal requirement.
- Governance decision theo charter.

## 3. Closure decision

Quyết định closure phải ghi:

```text
closure_id:
campaign_id:
closure_type:
reason:
effective_at:
new_commitment_rule:
active_obligations:
financial_position:
resource_position:
refund_release_plan:
residual_plan:
data_and_record_plan:
communication_plan:
approved_by:
evidence_ids:
```

## 4. Immediate controls khi đóng

```text
Stop new commitments
Freeze misleading promotion
Lock current charter and versions
Preserve evidence
Reconcile money and resources
Identify outstanding obligations
Notify payment/custody partners
Publish status and next update date
```

Không xóa campaign page hoặc evidence khi xảy ra failure.

## 5. Wind-down workstreams

### Financial

- Reconcile accounts.
- Freeze non-essential disbursement.
- Pay valid outstanding obligations.
- Recover vendor refunds.
- Calculate refund.
- Handle restricted balance.
- Close payment/escrow instructions.

### Resource

- Return borrowed equipment.
- Release reservations.
- Inventory campaign-owned assets.
- Close venue/access rights.
- Resolve partially delivered work.

### Contributor obligations

- Deliver remaining benefits.
- Offer substitute only under valid rule.
- Refund/remedy when fulfilment impossible.
- Close membership/access.

### Beneficiary protection

- Avoid abrupt interruption of essential service.
- Transfer records or operations where appropriate.
- Communicate transition.
- Protect vulnerable groups.

### Data and digital

- Revoke access.
- Export and hand over records.
- Delete/retain data according to purpose and legal basis.
- Secure credentials, domain and accounts.
- Preserve audit trail.

### Governance and legal

- Close conflicts and investigations.
- Resolve grievances.
- Complete reports.
- Transfer contracts if allowed.
- Obtain approvals.

## 6. Wind-down plan

```text
wind_down_id:
scope:
start_date:
target_close_date:
workstreams:
owners:
outstanding_obligations:
priority_order:
resource_inventory:
financial_reconciliation:
refund_release_schedule:
residual_treatment:
beneficiary_transition:
data_plan:
grievance_plan:
final_report_rule:
archive_rule:
```

Mỗi workstream cần owner và deadline.

## 7. Priority order

Thứ tự thực tế phụ thuộc pháp luật và cấu trúc campaign, nhưng governance phải xác định rõ:

```text
Protect people and prevent further harm
→ preserve assets and evidence
→ stop unauthorized spending
→ meet mandatory/legal obligations
→ process valid contributor and vendor obligations
→ refund/release
→ handle residual resources
→ archive and close
```

Không ưu tiên trả founder hoặc related party chỉ vì họ kiểm soát quy trình.

## 8. Outstanding obligation register

```text
obligation_id:
obligation_type:
creditor_or_beneficiary:
source_document:
amount_or_resource:
due_date:
priority:
status:
dispute:
settlement_method:
evidence_ids:
```

Các loại obligation:

- Refund.
- Reward/pre-order delivery.
- Vendor invoice.
- Salary/tax.
- Return of asset.
- Data deletion/return.
- Reporting.
- Warranty.
- Grievance remedy.

## 9. Closure report

Một final report nên gồm:

1. Purpose và scope cuối.
2. Lý do closure.
3. Điều đã hoàn thành và chưa hoàn thành.
4. Tổng commitments theo trạng thái.
5. Tổng nguồn lực nhận, dùng, hoàn và còn lại.
6. Milestone và evidence.
7. Amendments/material changes.
8. Failure và corrective actions.
9. Refund/release status.
10. Residual treatment.
11. Outstanding obligations.
12. Grievance và unresolved issues.
13. Archive location và retention period.

Không dùng final report như bài PR chỉ kể thành công.

## 10. Archive

Phải lưu tối thiểu:

```text
Campaign charter versions
Commitment records
Contribution and payment records
Resource lifecycle events
Evidence ledger
Verification statements
Decision logs
Amendments and re-consent
Disbursement and reconciliation
Refund/release records
Residual register
Grievances
Final report
```

Archive phải:

- Có integrity.
- Có quyền truy cập phù hợp.
- Có retention rule.
- Bảo vệ dữ liệu cá nhân.
- Không phụ thuộc tài khoản cá nhân của founder.

## 11. Public page sau closure

Nên giữ một public tombstone/status page:

- Campaign status.
- Closure date.
- Completion/termination reason.
- Link final report.
- Refund/release status.
- Contact/grievance route còn hiệu lực.
- Archive reference.

Không redirect âm thầm sang campaign mới.

## 12. Success closure

Ngay cả campaign thành công vẫn cần:

- Xác nhận milestone cuối.
- Reconcile.
- Fulfil benefits.
- Handle residual.
- Transfer sang operations/maintenance.
- Close temporary permissions.
- Publish outcome limitations.

`Đã giao sản phẩm` không tự động nghĩa mọi nghĩa vụ đã đóng.

## 13. Failed closure

Khi terminate:

```text
Stop further loss
→ classify obligations
→ communicate uncertainty honestly
→ recover/refund/release
→ protect beneficiary and data
→ investigate integrity issues
→ publish unresolved items
```

Có thể đóng với unresolved obligations, nhưng phải ghi rõ chứ không gắn status `Completed`.

## 14. Transfer to successor

Wind-down có thể chuyển hoạt động cho tổ chức khác.

Điều kiện:

- Successor identity và năng lực được xác minh.
- Asset/restriction cho phép transfer.
- Contributor rights được xử lý.
- Data transfer có căn cứ.
- Liabilities không bị bỏ lại.
- Handover có inventory và acceptance.

Status `Transferred` khác `Completed`.

## 15. Dissolution của pháp nhân

Nếu legal entity dissolution:

- Campaign obligations có thể trở thành claim đối với pháp nhân.
- Tài sản phải xử lý theo pháp luật, governing document và restriction.
- Data/controller responsibility phải chuyển hoặc đóng.
- Người dùng phải được thông báo.
- Nền tảng không nên tự đưa ra kết luận pháp lý nếu chưa có tư vấn phù hợp.

Node này chỉ giữ khung khái niệm, không thay thế quy trình giải thể tại một quốc gia cụ thể.

## 16. Asset lock và public-benefit restriction

Một số tài sản có thể không được phân cho founder/member khi dissolution mà phải chuyển sang mục đích tương tự.

Cần kiểm tra:

- Charter/constitution.
- Donor restriction.
- Grant terms.
- Asset ownership.
- Applicable law.

Không gọi mọi residual là `surplus distributable`.

## 17. Data closure

```text
What data remains?
Why retain it?
Who controls it?
Who can access?
When delete?
Can it transfer?
What consent applies?
```

Evidence retention không cho phép tiếp tục dùng dữ liệu cho marketing hoặc AI ngoài purpose.

## 18. Grievance closure

Không đóng grievance channel ngay khi campaign terminate.

Cần:

- Thời gian tiếp nhận cuối.
- Người xử lý độc lập.
- Escalation.
- Record outcome.
- Công bố unresolved systemic issue.

## 19. Closure status model

```text
Open
→ Closing announced
→ Closed to new commitments
→ Wind-down in progress
→ Financially reconciled
→ Obligations substantially resolved
→ Closed
→ Archived
```

Nhánh khác:

```text
Transferred
Terminated
Closed with unresolved obligations
Legal dissolution pending
```

## 20. Definition of done

Campaign chỉ được gắn `Closed` khi:

```text
[ ] Không nhận cam kết mới
[ ] Charter/version cuối bị khóa
[ ] Tiền và nguồn lực đã reconcile
[ ] Refund/release đã xử lý hoặc có exception log
[ ] Residual treatment đã phê duyệt
[ ] Outstanding obligations đã đóng hoặc disclosed
[ ] Data/access đã xử lý
[ ] Grievance route và kết quả đã ghi
[ ] Final report được công bố
[ ] Archive được bàn giao
```

## 21. Dấu hiệu cảnh báo

- Xóa page khi thất bại.
- Không có closure owner.
- Vẫn nhận tiền trong wind-down.
- Không kiểm kê asset/data.
- Founder giữ domain, account và records cá nhân.
- Refund chưa xong nhưng status `Closed`.
- Mở campaign mới trước khi công bố nghĩa vụ cũ.
- Dissolution được dùng như cách xóa campaign debt.
- Archive chứa dữ liệu cá nhân nhưng không có retention rule.

## 22. Kết luận

> **Closure là một quyết định; wind-down là công việc; dissolution là sự kiện pháp lý. Một chiến dịch chỉ thực sự kết thúc khi nguồn lực, nghĩa vụ, dữ liệu và hồ sơ đều có nơi đến rõ ràng.**

## Khái niệm liên quan

- [[Campaign failure, recovery and termination]]
- [[Refund and release mechanism]]
- [[Residual funds and unused resources]]
- [[Campaign charter]]
- [[Evidence ledger và provenance]]
- [[Stakeholder engagement và grievance mechanism]]
