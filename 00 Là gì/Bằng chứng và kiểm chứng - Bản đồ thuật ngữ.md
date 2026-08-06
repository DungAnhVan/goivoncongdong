# Bằng chứng và kiểm chứng — Bản đồ thuật ngữ

> **Định nghĩa làm việc của dự án:** *Bằng chứng và kiểm chứng* là lớp cơ chế biến một lời tuyên bố về nhu cầu, việc sử dụng nguồn lực, tiến độ hoặc kết quả thành một đối tượng có thể truy nguồn, kiểm tra và dùng để ra quyết định.

Đây không phải tên một ngành hay tiêu chuẩn pháp lý duy nhất. Đây là **cụm khái niệm làm việc của dự án Gọi vốn cộng đồng**, được xây từ quản trị dự án, monitoring & evaluation, provenance, assurance và kiểm soát giải ngân.

## 1. Vì sao đây là bản sắc của dự án?

Nền tảng gọi vốn thông thường thường dừng ở:

```text
Câu chuyện hấp dẫn
→ mục tiêu tiền
→ lượt ủng hộ
→ chiến dịch thành công
```

Dự án này muốn đi sâu hơn:

```text
Claim — lời tuyên bố
→ Evidence requirement — cần bằng chứng gì?
→ Evidence object — bằng chứng cụ thể nào được nộp?
→ Provenance — bằng chứng đến từ đâu và đã biến đổi thế nào?
→ Verification — ai kiểm tra bằng phương pháp nào?
→ Decision rule — kết quả kiểm tra dẫn đến quyết định gì?
→ Decision — giải ngân, sửa, tiếp tục, tạm dừng hoặc bác bỏ
```

> **Một claim không trở nên đúng chỉ vì được kể hay, có nhiều người tin hoặc đi kèm nhiều tài liệu.**

## 2. Sáu lớp bằng chứng theo vòng đời dự án

```text
1. Vấn đề có thật không?
   → [[Proof of need và demand validation|Proof of need]]

2. Có người thật sự muốn dùng, trả tiền hoặc cam kết không?
   → [[Proof of need và demand validation|Demand validation]]

3. Nguồn lực có được dùng đúng và hoạt động có diễn ra không?
   → [[Proof of use và proof of outcome|Proof of use]]

4. Mốc đã đạt theo tiêu chí định trước chưa?
   → [[Milestone verification]]

5. Kết quả thực tế có xuất hiện ở người hưởng lợi không?
   → [[Proof of use và proof of outcome|Proof of outcome]]

6. Ta có thể tin chuỗi bằng chứng và người xác nhận đến mức nào?
   → [[Evidence ledger và provenance]]
   → [[Independent verification và third-party attestation]]
```

## 3. Kiến trúc claim–evidence–decision

```text
Project
├─ Claim 01: vấn đề tồn tại
│  ├─ evidence requirement
│  ├─ evidence objects
│  ├─ provenance records
│  ├─ verification result
│  └─ decision consequence
│
├─ Claim 02: có nhu cầu sử dụng/trả tiền
│  └─ ...
│
├─ Claim 03: milestone đã hoàn thành
│  └─ ...
│
└─ Claim 04: outcome đã xuất hiện
   └─ ...
```

Cấu trúc này được triển khai bằng [[Claim-evidence mapping]].

## 4. Quy tắc chống “múa thuật ngữ”

Một thuật ngữ chỉ được coi là **đã có ứng dụng trong dự án** khi trả lời đủ tám câu:

| Câu hỏi bắt buộc | Ví dụ |
|---|---|
| Claim nào đang được kiểm tra? | “Đã giao 20 bộ thiết bị đạt chuẩn.” |
| Đối tượng nào được đo? | 20 bộ thiết bị, phiên bản bản vẽ V3 |
| Bằng chứng nào được chấp nhận? | Biên bản đo, ảnh định danh, phiếu giao nhận |
| Ai tạo bằng chứng? | Nhà gia công + kỹ thuật viên đo |
| Xuất xứ được lưu thế nào? | Thời gian, thiết bị, file gốc, phiên bản |
| Ai kiểm tra? | Người không trực tiếp nhận khoản giải ngân |
| Tiêu chí đạt là gì? | Ít nhất 18/20 bộ đạt năm kích thước trọng yếu |
| Kết quả kích hoạt quyết định gì? | Mở 35% ngân sách đợt tiếp theo |

Nếu chỉ có tên gọi nhưng thiếu các trường trên, đó mới là **nhãn ý tưởng**, chưa phải cơ chế vận hành.

## 5. Phân biệt validation và verification

Trong dự án, hai từ này nên dùng có chủ đích:

- **Validation** hỏi một claim về dự kiến, thiết kế hoặc tương lai có hợp lý và phù hợp mục đích không.
- **Verification** hỏi một claim về điều đã xảy ra hoặc kết quả đã có có được trình bày đúng không.

Ví dụ:

```text
Trước pilot:
“Thiết kế khảo sát này có đủ khả năng kiểm tra nhu cầu không?”
→ validation

Sau pilot:
“Có đúng 82 người hoàn thành khảo sát hợp lệ không?”
→ verification
```

ISO/IEC 17029 dùng sự phân biệt gần như vậy trong conformity assessment: validation liên quan tính hợp lý của claim cho mục đích tương lai; verification liên quan tính trung thực của claim về sự kiện hoặc kết quả đã xảy ra.

## 6. Các trạng thái của một claim

```text
Draft
→ Evidence required
→ Evidence submitted
→ Under review
→ Verified / Partially verified / Not verified
→ Contradicted / Superseded / Expired
```

Không nên dùng một cờ nhị phân `verified = true/false` cho mọi trường hợp.

Một claim có thể:

- Đúng một phần.
- Đúng ở thời điểm trước nhưng đã hết hạn.
- Có bằng chứng nhưng bằng chứng yếu.
- Có hai nguồn mâu thuẫn.
- Được kiểm tra đúng phạm vi nhưng bị diễn giải rộng hơn phạm vi đó.

## 7. Ma trận quyết định theo độ trọng yếu

| Quyết định | Mức bằng chứng gợi ý |
|---|---|
| Hiển thị một ý tưởng để thảo luận | Bằng chứng sơ bộ, ghi rõ chưa xác minh |
| Cho phép mở chiến dịch pilot nhỏ | Proof of need tối thiểu + kiểm tra danh tính/năng lực |
| Giải ngân đợt nhỏ | Proof of use hoặc milestone evidence do nội bộ kiểm tra |
| Giải ngân lớn/trọng yếu | [[Milestone verification]] có người kiểm tra độc lập tương đối |
| Tuyên bố outcome công khai | Dữ liệu kết quả + phương pháp + giới hạn + provenance |
| Tuyên bố nhạy cảm hoặc giá trị cao | [[Independent verification và third-party attestation]] |

Nguyên tắc là **proportional assurance**: độ nghiêm ngặt của kiểm chứng phải tương xứng với rủi ro, số tiền và hệ quả của claim.

## 8. Bộ hồ sơ bằng chứng tối thiểu của một dự án

```text
01_need/
  need_claim.md
  target_population.md
  source_data/
  interviews/
  demand_tests/

02_plan/
  claim_evidence_map.md
  milestone_verification_plan.md
  decision_rules.md

03_execution/
  evidence_ledger.csv
  use_evidence/
  milestone_evidence/
  exception_log.md

04_outcomes/
  baseline.md
  outcome_data/
  method.md
  limitations.md

05_assurance/
  reviewer_notes/
  verification_statements/
  conflicts_of_interest.md
```

Đây là logic cấu trúc; công cụ triển khai có thể là database, object storage, Git, hệ thống quản lý tài liệu hoặc kết hợp nhiều lớp.

## 9. Những điều hệ thống không nên làm

- Gắn nhãn “verified” mà không công bố phạm vi được kiểm tra.
- Xem hóa đơn là bằng chứng outcome.
- Xem ảnh là bằng chứng đầy đủ nếu không rõ thời gian, địa điểm và đối tượng.
- Cho người nhận tiền tự xác nhận milestone duy nhất.
- Chọn tiêu chí sau khi đã xem kết quả.
- Xóa bằng chứng cũ khi dự án thay đổi claim.
- Dùng blockchain như thay thế cho chất lượng nguồn dữ liệu.
- Dùng bên thứ ba có tên tuổi nhưng không công bố xung đột lợi ích hoặc phương pháp.

## 10. Liên hệ với các lớp hiện có của dự án

```text
[[Proof of need và demand validation]]
→ nối với [[Beneficiary và target population]] và [[Affected community]]

[[Milestone verification]]
→ nối với [[Disbursement]] và [[Public procurement]]

[[Proof of use và proof of outcome]]
→ nối với [[Restricted funds]], outcome và báo cáo tác động

[[Evidence ledger và provenance]]
→ nối với [[Internal financial controls]] và audit trail

[[Independent verification và third-party attestation]]
→ tăng độ tin cậy cho claim trọng yếu

[[Claim-evidence mapping]]
→ là cấu trúc liên kết toàn bộ các lớp trên
```

## 11. Thứ tự đọc cho thành viên mới

```text
1. [[Claim-evidence mapping]]
2. [[Proof of need và demand validation]]
3. [[Proof of use và proof of outcome]]
4. [[Evidence ledger và provenance]]
5. [[Milestone verification]]
6. [[Evidence quality và sufficiency]]
7. [[Verification protocol và decision rule]]
8. [[Independent verification và third-party attestation]]
```

## 12. Kết luận cho dự án

> **Dự án không chỉ huy động niềm tin; dự án thiết kế cách niềm tin được tạo ra, kiểm tra, cập nhật và rút lại dựa trên bằng chứng.**

Điểm khác biệt không nằm ở việc sử dụng nhiều thuật ngữ chuyên môn. Nó nằm ở khả năng biến mỗi thuật ngữ thành:

```text
một trường dữ liệu
→ một trách nhiệm
→ một quy trình
→ một tiêu chí
→ một quyết định có dấu vết
```

## Nguồn tham khảo

- W3C — PROV-O, mô hình biểu diễn provenance: https://www.w3.org/TR/prov-o/
- W3C — PROV-AQ, truy cập và truy vấn provenance: https://www.w3.org/TR/prov-aq/
- ISO — ISO/IEC 17029:2019, validation và verification bodies: https://www.iso.org/standard/29352.html
- OECD — Glossary of Key Terms in Evaluation and Results-Based Management: https://www.oecd.org/en/publications/glossary-of-key-terms-in-evaluation-and-results-based-management-for-sustainable-development-second-edition_632da462-en-fr-es.html
- World Bank — Program-for-Results Financing: https://www.worldbank.org/en/programs/program-for-results-financing
