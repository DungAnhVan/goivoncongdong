---
ai_authored: true
---

# Milestone verification

> **Định nghĩa ngắn:** *Milestone verification* là quy trình kiểm tra có cấu trúc để xác định một mốc dự án đã đạt, đạt một phần hay chưa đạt theo tiêu chí được xác định trước.

Milestone verification không phải việc “xem qua rồi xác nhận”. Nó phải kết nối:

```text
Milestone claim
→ acceptance criteria
→ required evidence
→ verification method
→ verifier
→ decision rule
→ release consequence
```

## 1. Claim được kiểm tra là gì?

Ví dụ:

> “Dự án đã hoàn thành lô 20 sản phẩm thử đạt yêu cầu V3 và đủ điều kiện nhận đợt giải ngân tiếp theo.”

Claim này chứa nhiều phần:

- Đúng số lượng.
- Đúng phiên bản.
- Đúng tiêu chuẩn chất lượng.
- Hoàn thành trong phạm vi thời gian.
- Bằng chứng đủ tin cậy.
- Không có ngoại lệ trọng yếu chưa xử lý.

Nếu chỉ kiểm tra một phần, kết luận phải nói rõ phạm vi.

## 2. Milestone tốt phải được thiết kế trước

Một milestone verification plan tối thiểu gồm:

```text
milestone_id:
claim:
due_date:
deliverables:
acceptance_criteria:
required_evidence:
sampling_method:
verification_method:
verifier_role:
independence_requirements:
threshold:
partial_completion_rule:
exception_rule:
decision_consequence:
```

Điểm quan trọng nhất là **pre-specification**: tiêu chí và ngưỡng phải được xác định trước khi xem kết quả, trừ khi có variation được ghi dấu vết.

## 3. Activity không phải milestone

Các câu sau quá mơ hồ:

- “Bắt đầu nghiên cứu.”
- “Triển khai truyền thông.”
- “Phát triển hệ thống.”
- “Kết nối cộng đồng.”

Milestone cần chuyển thành đối tượng kiểm tra được:

```text
Activity:
Triển khai khảo sát nhu cầu.

Milestone:
Thu được tối thiểu 120 phản hồi hợp lệ từ ba nhóm mục tiêu,
không nhóm nào dưới 25 phản hồi,
tỷ lệ câu trả lời thiếu dưới 10%,
file raw và quy tắc loại mẫu được lưu trong evidence ledger.
```

## 4. Các loại milestone

### Deliverable milestone

Kiểm tra một sản phẩm hoặc tài liệu đã được tạo.

Ví dụ: bản vẽ, prototype, báo cáo, module phần mềm.

### Process milestone

Kiểm tra một quy trình bắt buộc đã được hoàn thành.

Ví dụ: tham vấn cộng đồng, kiểm tra an toàn, phê duyệt thiết kế.

### Performance milestone

Kiểm tra chỉ số vận hành.

Ví dụ: uptime, thời gian xử lý, tỷ lệ lỗi.

### Outcome milestone

Kiểm tra thay đổi ở nhóm hưởng lợi.

Ví dụ: tỷ lệ tiếp tục sử dụng sau ba tháng.

### Compliance milestone

Kiểm tra điều kiện pháp lý, tài chính hoặc quản trị.

Ví dụ: hoàn thành đối soát, công bố xung đột lợi ích, cấp phép cần thiết.

Không nên dùng cùng một phương pháp kiểm chứng cho mọi loại.

## 5. Verification method

### Document review

Phù hợp với hợp đồng, hóa đơn, báo cáo, log và hồ sơ pháp lý.

Rủi ro: tài liệu có thể đầy đủ nhưng hoạt động thực tế không xảy ra.

### Physical inspection

Kiểm tra trực tiếp vật thể, địa điểm hoặc hoạt động.

Rủi ro: chỉ nhìn được thời điểm và mẫu được chọn.

### Testing hoặc measurement

Đo hiệu năng, chất lượng hoặc thông số.

Rủi ro: phương pháp đo, thiết bị và sampling có thể không phù hợp.

### User confirmation

Người nhận hoặc người dùng xác nhận đã nhận và sử dụng.

Rủi ro: self-report, selection bias và áp lực quan hệ.

### System data review

Dùng log, transaction hoặc sensor data.

Rủi ro: quyền sửa dữ liệu và provenance không rõ.

Một milestone trọng yếu thường cần **triangulation** từ nhiều phương pháp.

## 6. Sampling

Không phải lúc nào cũng kiểm tra 100%.

Sampling plan phải nêu:

- Population là gì.
- Chọn mẫu ngẫu nhiên, rủi ro hay thuận tiện.
- Kích thước mẫu.
- Sai lệch nào được chấp nhận.
- Nếu mẫu lỗi thì mở rộng kiểm tra ra sao.

Ví dụ:

```text
Lô 200 sản phẩm
→ chọn ngẫu nhiên 20 sản phẩm
→ đo 5 kích thước trọng yếu
→ nếu quá 2 sản phẩm không đạt, mở rộng mẫu thêm 30
→ nếu tổng tỷ lệ lỗi vượt 8%, milestone không đạt
```

Không gọi việc chọn vài trường hợp đẹp nhất là sampling.

## 7. Kết quả verification

Nên có nhiều trạng thái hơn đạt/không đạt:

```text
Verified
Partially verified
Verified with exceptions
Not verified
Unable to verify
Contradicted
```

- **Not verified** không luôn có nghĩa claim sai; có thể bằng chứng chưa đủ.
- **Unable to verify** cần dùng khi dữ liệu mất, verifier không thể tiếp cận hoặc phương pháp không thực hiện được.
- **Verified with exceptions** phải ghi ngoại lệ và ảnh hưởng đến quyết định.

## 8. Liên kết với giải ngân

```text
Milestone submitted
→ evidence registered
→ verification performed
→ result issued
→ decision rule applied
→ [[Disbursement|giải ngân]], holdback, correction hoặc stop
```

Ví dụ decision rule:

| Kết quả | Hành động |
|---|---|
| Verified | Mở 100% tranche kế tiếp |
| Verified with minor exceptions | Mở 80%, giữ 20% đến khắc phục |
| Partially verified | Chia nhỏ hoặc sửa phạm vi |
| Not verified | Tạm dừng và yêu cầu corrective action |
| Contradicted/fraud indication | Escalate, freeze và điều tra |

Không để verifier tự quyết tiền nếu vai trò của họ chỉ là xác nhận sự kiện. Quyết định giải ngân thuộc cơ chế governance đã định.

## 9. Variation và thay đổi milestone

Dự án thật luôn có thay đổi. Nhưng thay đổi phải tạo dấu vết:

```text
original milestone
→ reason for change
→ impact on budget/time/outcome
→ approval
→ revised criteria
→ version effective date
```

Không được hạ tiêu chí sau khi dự án thất bại mà vẫn gọi đó là milestone ban đầu đã đạt.

## 10. Conflict of interest

Verifier không nên là người:

- Trực tiếp nhận khoản giải ngân phụ thuộc vào kết luận.
- Tạo toàn bộ bằng chứng và tự kiểm tra duy nhất.
- Có quan hệ tài chính chưa công bố với nhà cung cấp.
- Chịu KPI chỉ dựa trên tỷ lệ dự án được duyệt.

Mức độc lập cần tỷ lệ với rủi ro. Xem [[Independent verification và third-party attestation]].

## 11. Verification record

```text
verification_id:
milestone_id:
claim_version:
criteria_version:
evidence_ids:
method:
sample:
reviewer:
conflict_declaration:
work_performed:
findings:
exceptions:
result:
confidence_or_limitations:
issued_at:
linked_decision_id:
```

Record này phải được lưu trong [[Evidence ledger và provenance]].

## 12. Ví dụ hoàn chỉnh

```text
Milestone M-03:
Hoàn thành 20 prototype theo drawing V3.

Acceptance criteria:
- đủ 20 sản phẩm định danh;
- ít nhất 18/20 đạt 5 kích thước trọng yếu;
- không có lỗi an toàn loại A;
- hồ sơ vật liệu và giao nhận đầy đủ.

Evidence:
- E-112 phiếu giao nhận;
- E-113 ảnh định danh từng sản phẩm;
- E-114 bảng đo raw;
- E-115 chứng chỉ vật liệu.

Method:
- đối chiếu 100% số lượng;
- chọn ngẫu nhiên 10 sản phẩm đo lại;
- kiểm tra provenance của bảng đo.

Decision:
- verified: mở 35%;
- minor exception: mở 25%, giữ 10%;
- not verified: tạm dừng.
```

## 13. Những lỗi cần tránh

- Viết milestone chỉ bằng động từ hoạt động.
- Không chỉ rõ phiên bản tài liệu hoặc sản phẩm.
- Chọn mẫu sau khi biết trường hợp nào tốt.
- Verifier chỉ kiểm tra file PDF tổng hợp, không thấy raw evidence.
- Kết luận rộng hơn phạm vi đã kiểm tra.
- Không có quy tắc partial completion.
- Không nối verification với quyết định cụ thể.
- Dùng “đã nghiệm thu” như một nhãn không có record.

## 14. Kết luận cho dự án

> **Milestone verification là chiếc bản lề nối bằng chứng với dòng tiền.**

Nếu milestone mơ hồ, giải ngân theo mốc chỉ là giải ngân theo lịch được trang trí bằng ngôn ngữ kiểm soát.

## Khái niệm liên quan

- [[Bằng chứng và kiểm chứng - Bản đồ thuật ngữ]]
- [[Disbursement]]
- [[Proof of use và proof of outcome]]
- [[Evidence ledger và provenance]]
- [[Verification protocol và decision rule]]
- [[Independent verification và third-party attestation]]
- [[Public procurement]]

## Nguồn tham khảo

- World Bank — Program-for-Results Financing: https://www.worldbank.org/en/programs/program-for-results-financing
- ISO — ISO/IEC 17029:2019: https://www.iso.org/standard/29352.html
- OECD — Results-Based Management Glossary: https://www.oecd.org/en/publications/glossary-of-key-terms-in-evaluation-and-results-based-management-for-sustainable-development-second-edition_632da462-en-fr-es.html
