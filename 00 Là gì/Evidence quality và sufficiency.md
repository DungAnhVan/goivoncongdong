---
ai_authored: true
---

# Evidence quality và sufficiency

> **Định nghĩa ngắn:** *Evidence quality* là mức độ một bằng chứng đáng tin, phù hợp và có thể dùng để đánh giá claim. *Evidence sufficiency* là việc tổng thể bằng chứng đã đủ về số lượng, độ phủ và sức nặng để đưa ra kết luận trong phạm vi đã xác định hay chưa.

Nhiều tài liệu không tự động tạo thành bằng chứng đủ mạnh.

```text
Quantity
≠ quality

Quality
≠ sufficiency

Sufficiency
≠ certainty tuyệt đối
```

## 1. Câu hỏi trung tâm

Khi đánh giá một evidence package, cần tách:

```text
Bằng chứng có liên quan không?
→ có đúng nguồn không?
→ có nguyên vẹn không?
→ phương pháp tạo có đáng tin không?
→ có đủ độ phủ không?
→ có nguồn độc lập hoặc đối chiếu không?
→ có bằng chứng mâu thuẫn không?
→ còn thiếu gì trước khi ra quyết định?
```

## 2. Các thuộc tính chất lượng

### Relevance — tính liên quan

Bằng chứng có trực tiếp trả lời claim không?

Ví dụ: hóa đơn liên quan đến claim đã mua vật tư, nhưng không trực tiếp liên quan đến claim outcome đã cải thiện.

### Authenticity — tính xác thực nguồn

Nguồn có đúng là người, tổ chức hoặc hệ thống được khai báo không?

### Integrity — tính toàn vẹn

File hoặc dữ liệu có bị sửa ngoài quy trình, thiếu trang, mất dòng hoặc đổi phiên bản không?

### Reliability — độ tin cậy phương pháp

Cách đo, thu thập và xử lý có nhất quán, có thể lặp lại và phù hợp không?

### Directness — mức trực tiếp

Bằng chứng quan sát trực tiếp claim hay chỉ là proxy?

### Coverage — độ bao phủ

Bằng chứng bao phủ bao nhiêu đối tượng, thời gian, địa điểm và trường hợp?

### Timeliness — tính kịp thời

Bằng chứng có còn phản ánh hiện trạng hoặc claim đã hết hạn không?

### Independence — mức độc lập

Nguồn có lợi ích trực tiếp trong kết luận không? Có lớp kiểm tra khác không?

### Transparency — tính minh bạch

Người review có thể hiểu phương pháp, limitation và bước biến đổi không?

## 3. Sufficiency phụ thuộc quyết định

Cùng một evidence package có thể đủ cho một quyết định nhưng không đủ cho quyết định khác.

```text
10 phỏng vấn
→ có thể đủ để phát hiện giả thuyết mới
→ chưa đủ để tuyên bố tỷ lệ toàn thị trường

5 hóa đơn + giao nhận
→ có thể đủ kiểm tra một tranche nhỏ
→ chưa đủ chứng minh toàn bộ outcome của dự án
```

Do đó phải gắn sufficiency với:

- Claim.
- Phạm vi.
- Mức trọng yếu.
- Rủi ro nếu sai.
- Quyết định dự kiến.

## 4. Evidence hierarchy không cứng nhắc

Không có một bảng xếp hạng duy nhất cho mọi claim. Tuy nhiên có thể dùng thang gợi ý:

```text
L0 — lời kể không có record
L1 — self-report có định danh
L2 — tài liệu/log nội bộ có provenance
L3 — đối chiếu nhiều nguồn hoặc quan sát trực tiếp
L4 — review độc lập tương đối
L5 — kiểm chứng/attestation chuyên môn phù hợp
```

Một bằng chứng L5 nhưng sai chuyên môn vẫn có thể yếu hơn một dataset L3 được thiết kế tốt.

## 5. Triangulation

*Triangulation* là dùng nhiều nguồn hoặc phương pháp khác nhau để kiểm tra cùng claim.

Ví dụ claim “thiết bị đã được sử dụng”:

```text
Phiếu bàn giao
+ ảnh định danh tại địa điểm
+ system log hoạt động
+ xác nhận chọn mẫu từ người dùng
```

Các nguồn nên có lỗi sai khác nhau. Bốn tài liệu đều do cùng một người tạo từ cùng một file gốc không phải triangulation thực chất.

## 6. Negative evidence và contradiction

Một review trung thực phải tìm:

- Trường hợp không đạt.
- Dữ liệu bị thiếu.
- Mẫu bị loại.
- Người dùng bỏ cuộc.
- Khiếu nại.
- Nguồn mâu thuẫn.

Không nên chấm chất lượng bằng cách chỉ đếm tài liệu hỗ trợ. [[Evidence ledger và provenance]] cần lưu cả quan hệ `contradicts`, `limits` và `does_not_address`.

## 7. Materiality và proportionality

*Mức trọng yếu* là mức sai lệch có thể làm thay đổi quyết định của người dùng thông tin.

Một sai số nhỏ về ngày chụp có thể không trọng yếu với một báo cáo hoạt động, nhưng rất trọng yếu nếu ảnh được dùng để chứng minh milestone hoàn thành trước deadline.

Nguyên tắc:

```text
Rủi ro thấp + quyết định nhỏ
→ review nhẹ nhưng có dấu vết

Rủi ro cao + tiền lớn + claim nhạy cảm
→ evidence mạnh hơn, sampling rõ, verifier độc lập hơn
```

## 8. Scoring rubric gợi ý

Có thể chấm từng thuộc tính 0–3, nhưng điểm số không thay thế judgement.

| Thuộc tính | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| Relevance | không liên quan | gián tiếp yếu | liên quan phần lớn | trực tiếp |
| Provenance | không rõ | nguồn tự khai | có record cơ bản | truy nguyên đầy đủ |
| Reliability | không rõ phương pháp | phương pháp yếu | chấp nhận được | mạnh và tái kiểm tra được |
| Coverage | rất hẹp | thiếu nhóm chính | đủ phần lớn | phù hợp claim |
| Independence | xung đột cao | nội bộ | review tách vai trò | độc lập phù hợp |

Không nên cộng điểm rồi tự động kết luận nếu có một lỗi fatal như giả mạo, sai đối tượng hoặc claim scope không khớp.

## 9. Fatal flaw và limitation

### Fatal flaw

Lỗi làm bằng chứng không thể dùng cho claim:

- Sai đối tượng.
- Không xác định được nguồn.
- Dữ liệu đã bị can thiệp không kiểm soát.
- Phương pháp không đo điều claim nói.
- Xung đột lợi ích nghiêm trọng không xử lý.

### Limitation

Giới hạn làm giảm sức mạnh nhưng không vô hiệu hoàn toàn:

- Mẫu nhỏ.
- Thời gian theo dõi ngắn.
- Một số trường thiếu dữ liệu.
- Chỉ đo ở một địa phương.

Kết luận phải phản ánh limitation thay vì che giấu nó.

## 10. Sufficiency decision

```text
Sufficient
→ đủ cho claim và quyết định trong phạm vi

Sufficient with limitations
→ có thể quyết định nhưng phải ghi giới hạn/holdback

Insufficient
→ cần thêm bằng chứng

Inconclusive
→ bằng chứng mâu thuẫn hoặc phương pháp không cho phép kết luận

Unreliable
→ không nên dùng
```

`Insufficient` không đồng nghĩa claim sai. `Unreliable` nhắm vào bằng chứng, không nhất thiết vào claim.

## 11. Data schema gợi ý

```text
evidence_assessment_id:
evidence_id:
claim_id:
relevance:
authenticity:
integrity:
reliability:
directness:
coverage:
timeliness:
independence:
limitations:
fatal_flaws:
contradictions:
assessment_result:
reviewer:
reviewed_at:
```

Ở package level:

```text
package_id:
claim_id:
required_evidence:
submitted_evidence_ids:
missing_items:
triangulation_notes:
materiality:
sufficiency_result:
decision_allowed:
```

## 12. Những lỗi cần tránh

- Đếm số file rồi gọi là đủ.
- Cho mọi loại bằng chứng cùng trọng lượng.
- Chỉ xem nguồn có uy tín mà bỏ qua phạm vi claim.
- Không kiểm tra raw data.
- Không ghi limitation.
- Dùng score để che judgement khó.
- Đặt burden quá cao khiến nhóm nhỏ không thể tham gia.
- Đặt burden quá thấp cho claim có thể gây thiệt hại lớn.

## 13. Kết luận cho dự án

> **Bằng chứng tốt không phải bằng chứng trông chuyên nghiệp nhất; đó là bằng chứng phù hợp nhất với claim, có provenance đủ rõ và đủ sức nặng cho quyết định đang được cân nhắc.**

## Khái niệm liên quan

- [[Bằng chứng và kiểm chứng - Bản đồ thuật ngữ]]
- [[Claim-evidence mapping]]
- [[Evidence ledger và provenance]]
- [[Verification protocol và decision rule]]
- [[Independent verification và third-party attestation]]
- [[Milestone verification]]

## Nguồn tham khảo

- ISO — ISO/IEC 17029:2019: https://www.iso.org/standard/29352.html
- OECD — Quality Standards for Development Evaluation: https://www.oecd.org/en/publications/dac-quality-standards-for-development-evaluation_9789264083905-en.html
- W3C — PROV-O: https://www.w3.org/TR/prov-o/
