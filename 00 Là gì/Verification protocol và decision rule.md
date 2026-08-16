---
ai_authored: true
---

# Verification protocol và decision rule

> **Định nghĩa ngắn:** *Verification protocol* là kế hoạch quy định trước cách một claim sẽ được kiểm tra. *Decision rule* là quy tắc chuyển kết quả kiểm tra thành hành động cụ thể như chấp nhận, yêu cầu bổ sung, giữ lại tiền, sửa phạm vi hoặc dừng dự án.

Đây là lớp ngăn dự án thay đổi tiêu chuẩn sau khi đã thấy kết quả.

```text
Claim
→ protocol
→ evidence
→ verification result
→ decision rule
→ action
```

## 1. Vì sao cần viết protocol trước?

Nếu không có protocol, reviewer có thể:

- Chọn bằng chứng thuận lợi sau khi xem hồ sơ.
- Thay ngưỡng để một milestone được tính là đạt.
- Áp tiêu chuẩn khác nhau cho các dự án giống nhau.
- Kết luận theo cảm giác hoặc quan hệ.
- Không giải thích được vì sao giải ngân hoặc từ chối.

Protocol tạo **pre-commitment**: nhóm thống nhất trước điều gì sẽ được kiểm tra và kết quả nào dẫn đến quyết định gì.

## 2. Thành phần tối thiểu

```text
protocol_id:
claim_id_or_type:
purpose:
criteria:
evidence_requirements:
collection_method:
verification_method:
sampling_plan:
reviewer_role:
independence_requirement:
materiality:
thresholds:
exception_rules:
result_categories:
decision_rules:
appeal_process:
version:
effective_date:
```

## 3. Criteria và indicator

### Criteria

Điều kiện định tính hoặc định lượng dùng để đánh giá.

### Indicator

Biến quan sát dùng để đại diện cho trạng thái hoặc kết quả.

Ví dụ:

```text
Criterion:
Prototype hoạt động ổn định trong điều kiện pilot.

Indicators:
- uptime ≥ 98% trong 14 ngày;
- không có lỗi an toàn loại A;
- median recovery time < 30 phút.
```

Không nên dùng một indicator duy nhất nếu nó không bao phủ đầy đủ criterion.

## 4. Threshold

Threshold phải gồm:

- Giá trị.
- Đơn vị.
- Cửa sổ thời gian.
- Population hoặc mẫu.
- Cách xử lý missing data.
- Quy tắc làm tròn.
- Trường hợp ngoại lệ.

Ví dụ không đủ:

```text
“Phần lớn người dùng hài lòng.”
```

Ví dụ tốt hơn:

```text
Ít nhất 70% trong số người dùng đủ điều kiện trả lời
chọn mức 4 hoặc 5 trên thang 5 điểm,
tỷ lệ phản hồi tối thiểu 60%,
không nhóm quy mô nào dưới 20 phản hồi.
```

## 5. Decision rule

Decision rule không chỉ là pass/fail.

```text
Nếu A và B đạt, C không có fatal flaw
→ Approved

Nếu A đạt, B thiếu dưới materiality threshold
→ Approved with holdback

Nếu dữ liệu thiếu nhưng có thể bổ sung
→ Evidence request

Nếu claim bị contradict hoặc có dấu hiệu gian lận
→ Freeze and escalate
```

Bảng gợi ý:

| Verification result | Decision |
|---|---|
| Verified | chấp nhận/mở bước tiếp |
| Verified with minor exceptions | chấp nhận có điều kiện/holdback |
| Partially verified | chia nhỏ phạm vi hoặc sửa kế hoạch |
| Insufficient evidence | yêu cầu bổ sung, chưa kết luận |
| Not verified | không mở bước tiếp |
| Contradicted | xem xét dừng, hoàn tiền hoặc điều tra |
| Unable to verify | xử lý theo contingency rule |

## 6. Materiality

Protocol phải xác định sai lệch nào có thể bỏ qua và sai lệch nào thay đổi quyết định.

Ví dụ:

```text
Mốc giao 100 bộ
- thiếu 1 bộ nhưng không ảnh hưởng pilot: minor exception
- thiếu 20 bộ: material
- có lỗi an toàn ở 1 bộ: fatal dù tỷ lệ nhỏ
```

Không dùng tỷ lệ phần trăm duy nhất cho mọi loại sai lệch.

## 7. Sampling plan

Một protocol sampling cần nêu:

```text
population:
sampling frame:
selection method:
sample size:
risk strata:
replacement rule:
error tolerance:
expansion rule:
```

Ví dụ:

- Random sample để ước lượng tỷ lệ chung.
- Risk-based sample để tìm giao dịch bất thường.
- Stratified sample để bảo đảm các nhóm được đại diện.
- 100% review cho giao dịch bên liên quan hoặc sự kiện an toàn.

## 8. Evidence request và admissibility

Protocol nên quy định:

- Loại file hoặc record được chấp nhận.
- File gốc có bắt buộc không.
- Metadata tối thiểu.
- Thời hạn nộp.
- Cách xử lý tài liệu bổ sung muộn.
- Bằng chứng do chính bên hưởng lợi tạo có cần đối chiếu không.
- Ngôn ngữ, chữ ký hoặc xác minh danh tính cần thiết.

Không nên từ chối bằng chứng chỉ vì định dạng khác nếu nội dung và provenance vẫn kiểm tra được; nhưng phải giữ nguyên tiêu chuẩn substantive.

## 9. Protocol versioning

```text
VR-03 v1
→ áp dụng từ ngày X

VR-03 v2
→ thay sampling do quy mô tăng
→ áp dụng cho claim nộp sau ngày Y
```

Nếu đổi protocol giữa một claim đang review:

- Nêu lý do.
- Đánh giá ảnh hưởng.
- Có phê duyệt.
- Không áp hồi tố bất lợi hoặc thuận lợi tùy tiện.
- Lưu cả hai version trong [[Evidence ledger và provenance]].

## 10. Blind review và separation of roles

Tùy rủi ro, có thể:

- Ẩn danh người tạo bằng chứng ở bước chấm kỹ thuật.
- Tách reviewer kỹ thuật khỏi decision-maker tài chính.
- Tách người hỗ trợ dự án chuẩn bị hồ sơ khỏi người kết luận.
- Dùng reviewer thứ hai cho claim trọng yếu.

Protocol phải nói ai được quyền:

```text
collect
review
request clarification
issue finding
approve exception
make decision
execute payment
```

## 11. Clarification khác bổ sung evidence

### Clarification

Giải thích nội dung đã tồn tại tại thời điểm cutoff.

### New evidence

Tài liệu hoặc dữ liệu mới được tạo sau cutoff.

Hai loại cần được đánh dấu khác nhau để tránh dự án sửa kết quả sau deadline rồi trình bày như bằng chứng ban đầu.

## 12. Appeal và dispute

Một cơ chế tối thiểu:

```text
Notification of finding
→ factual correction window
→ appeal with stated grounds
→ independent reviewer
→ final decision
→ publish record and version
```

Appeal không phải vòng thương lượng để giảm tiêu chuẩn. Nó dùng để xử lý:

- Sai sự kiện.
- Sai áp dụng protocol.
- Xung đột lợi ích.
- Bằng chứng bị bỏ sót.
- Kết luận vượt phạm vi.

## 13. Ví dụ protocol ngắn

```text
Protocol: Verify paid pilot demand
Claim:
Ít nhất 10 xưởng đã cam kết pilot trả phí.

Evidence requirement:
- hợp đồng/đơn đăng ký định danh;
- payment hoặc deposit reference;
- không tính giao dịch hoàn tiền trước cutoff;
- không quá 30% từ bên liên quan.

Review:
- kiểm tra 100% danh tính và payment reference;
- đối soát ngân hàng;
- công bố related parties.

Decision rule:
- ≥10 hợp lệ: mở pilot;
- 7–9: sửa offer và test thêm;
- <7: không gọi là demand validated;
- có giả mạo: freeze và review toàn bộ.
```

## 14. Protocol registry của nền tảng

Nền tảng có thể duy trì thư viện:

```text
VR-NEED-01  Proof of need sơ bộ
VR-DEM-01   Demand test trả phí
VR-USE-01   Kiểm tra sử dụng ngân sách
VR-MILE-01  Milestone vật lý
VR-OUT-01   Early outcome
VR-COM-01   Tham vấn affected community
```

Mỗi protocol có template chung nhưng cho phép cấu hình theo ngành và rủi ro.

## 15. Những lỗi cần tránh

- Protocol viết sau khi evidence đã nộp.
- Threshold không có đơn vị hoặc thời gian.
- Không nêu cách xử lý missing data.
- Reviewer có toàn quyền thay tiêu chí không ghi record.
- Decision-maker bỏ qua finding mà không giải thích.
- Một protocol dùng cho mọi ngành.
- Không có appeal hoặc exception rule.
- Đánh đồng `insufficient evidence` với gian lận.

## 16. Kết luận cho dự án

> **Verification protocol bảo vệ tính nhất quán của kiểm chứng; decision rule bảo vệ tính có thể giải thích của quyết định.**

Nếu không có hai lớp này, evidence ledger chỉ là kho tài liệu và milestone verification dễ trở thành phán xét tùy ý.

## Khái niệm liên quan

- [[Bằng chứng và kiểm chứng - Bản đồ thuật ngữ]]
- [[Claim-evidence mapping]]
- [[Evidence quality và sufficiency]]
- [[Milestone verification]]
- [[Independent verification và third-party attestation]]
- [[Disbursement]]
- [[Internal financial controls]]

## Nguồn tham khảo

- ISO — ISO/IEC 17029:2019: https://www.iso.org/standard/29352.html
- OECD — Quality Standards for Development Evaluation: https://www.oecd.org/en/publications/dac-quality-standards-for-development-evaluation_9789264083905-en.html
- World Bank — Program-for-Results Financing: https://www.worldbank.org/en/programs/program-for-results-financing
