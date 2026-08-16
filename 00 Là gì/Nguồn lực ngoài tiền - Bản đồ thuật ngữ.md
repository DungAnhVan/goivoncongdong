---
ai_authored: true
---

# Nguồn lực ngoài tiền — Bản đồ thuật ngữ

> **Định nghĩa làm việc của dự án:** *Nguồn lực ngoài tiền* là các tài sản, năng lực, thời gian, dữ liệu, quyền sử dụng, quyền tiếp cận hoặc dịch vụ được huy động để giúp một dự án hình thành và triển khai mà không nhất thiết đi qua một khoản thanh toán bằng tiền.

Mảng này tồn tại vì dự án không chỉ hỏi:

> Cần huy động bao nhiêu tiền?

Mà hỏi:

> Dự án cần tổ hợp nguồn lực nào, ai đang có nguồn lực đó, điều kiện sử dụng là gì và làm sao biết nguồn lực đã thực sự được bàn giao, sử dụng và tạo giá trị?

## 1. Kiến trúc của mảng

```text
[[In-kind contribution]]
→ khái niệm bao trùm về đóng góp phi tiền mặt

[[Time and labor contribution]]
→ thời gian, công việc và năng lực con người

[[Data contribution]]
→ dữ liệu hoặc quyền truy cập dữ liệu

[[Asset and access contribution]]
→ tài sản, thiết bị, địa điểm và quyền tiếp cận

[[Multi-resource matching]]
→ ghép nhu cầu dự án với nhiều loại nguồn lực khác nhau

[[Resource pledge lifecycle]]
→ theo dõi nguồn lực từ lời hứa đến bàn giao, nghiệm thu và kết thúc
```

## 2. Ranh giới để tránh chồng lấn

| Khái niệm | Câu hỏi nó trả lời | Không dùng nó để trả lời |
|---|---|---|
| [[Commitment ladder]] | Người đó đã thực hiện hành vi cam kết ở cấp nào? | Không mô tả chi tiết bản chất, chất lượng hay khả năng sử dụng của nguồn lực |
| [[Soft commitment và hard commitment]] | Cam kết khó rút đến đâu và hậu quả là gì? | Không xác định nguồn lực có phù hợp với nhu cầu dự án không |
| [[In-kind contribution]] | Đóng góp phi tiền mặt thuộc loại nào và được ghi nhận ra sao? | Không tự quyết định giá trị kế toán hoặc quyền sở hữu |
| [[Multi-resource matching]] | Offer nguồn lực nào tương thích với need nào? | Không xác minh offer có thật hoặc đã bàn giao |
| [[Resource pledge lifecycle]] | Nguồn lực đang ở trạng thái promised, reserved, delivered hay accepted? | Không thay thế hợp đồng, kế toán hoặc kiểm chứng |
| [[Evidence ledger và provenance]] | Bản ghi và tài liệu về nguồn lực đến từ đâu, phiên bản nào? | Không tự kết luận nguồn lực có hữu ích hoặc đủ điều kiện |
| [[Proof of use và proof of outcome]] | Nguồn lực đã được dùng đúng và tạo kết quả gì? | Không quản lý giai đoạn tìm kiếm và ghép nguồn lực |
| [[Matching fund]] | Một nguồn tài trợ đối ứng theo công thức nào? | Không ghép toàn bộ các loại nguồn lực dị biệt |

## 3. Các họ nguồn lực

```text
Human resources
→ thời gian, kỹ năng, công việc, trách nhiệm vận hành

Physical resources
→ vật liệu, thiết bị, phương tiện, không gian

Data and knowledge resources
→ dataset, tài liệu, IP, phương pháp, dữ liệu vận hành

Access resources
→ khách hàng, kênh phân phối, cơ sở thử nghiệm, mạng lưới, giấy phép tiếp cận

Institutional resources
→ uy tín, xác nhận, chương trình hỗ trợ, quan hệ thể chế

Financial resources
→ tiền, tín dụng, bảo lãnh, đầu tư
```

Mảng này tập trung vào năm nhóm đầu. Tài chính được quản lý trong [[Tài chính và quản lý quỹ - Bản đồ thuật ngữ]].

## 4. Không quy đổi tất cả sang tiền một cách máy móc

Giá trị tiền có thể cần cho ngân sách, matching hoặc báo cáo. Nhưng trước khi định giá, phải ghi giá trị sử dụng thực:

```text
40 giờ kỹ sư cơ khí
≠ 40 giờ nhân sự phổ thông

Quyền dùng máy CNC 2 ngày
≠ được sở hữu máy CNC

Dataset 10.000 dòng
≠ dữ liệu có quyền sử dụng, đủ chất lượng và phù hợp mục đích

Địa điểm miễn phí
≠ địa điểm phù hợp về thời gian, công suất và an toàn
```

Không được dùng một con số `estimated_value` để che:

- Chất lượng.
- Khả năng thay thế.
- Thời hạn.
- Điều kiện sử dụng.
- Chi phí tích hợp.
- Trách nhiệm và rủi ro.
- Quyền sở hữu hoặc quyền truy cập.

## 5. Resource need và resource offer

### Resource need

Mô tả điều dự án thật sự cần:

```text
need_id:
project_id:
resource_category:
specification:
quantity:
unit:
quality_or_skill_level:
location:
availability_window:
duration:
dependencies:
acceptable_substitutes:
acceptance_criteria:
priority:
needed_by:
```

### Resource offer

Mô tả điều một actor có thể cung cấp:

```text
offer_id:
provider_id:
resource_category:
description:
quantity_or_capacity:
availability_window:
location:
conditions:
withdrawal_rule:
ownership_or_access_type:
restrictions:
related_party_status:
evidence_ids:
status:
```

Không ghép một offer với một need chỉ vì cùng tên loại nguồn lực. Phải kiểm tra mức tương thích thực tế.

## 6. Bốn câu hỏi trước khi chấp nhận nguồn lực

```text
Nó có thật và người cung cấp có quyền cung cấp không?
→ Nó có phù hợp với nhu cầu kỹ thuật và thời gian không?
→ Điều kiện, trách nhiệm và chi phí ẩn là gì?
→ Bằng chứng nào xác nhận bàn giao và sử dụng?
```

Ví dụ, thiết bị miễn phí có thể không phù hợp nếu:

- Thiếu người vận hành.
- Chi phí vận chuyển cao.
- Chỉ có trong thời gian không đúng tiến độ.
- Không có bảo hiểm hoặc trách nhiệm hư hỏng.
- Công suất thấp hơn yêu cầu.

## 7. Giá trị đối với mô hình dự án

Mảng này biến dự án từ một cơ chế gọi tiền thành một cơ chế điều phối năng lực:

```text
Vấn đề
→ hồ sơ dự án
→ resource needs
→ resource offers
→ compatibility review
→ commitment
→ reservation
→ delivery
→ acceptance
→ proof of use
→ outcome
```

Đây là một ranh giới chiến lược quan trọng với các nền tảng chỉ tập trung vào chiến dịch và thanh toán.

## 8. Cách hiển thị công khai

Không viết:

> Dự án đã huy động được 3 tỷ đồng nguồn lực.

Khi dữ liệu thực tế gồm nhiều thứ không tương đương.

Nên tách:

```text
Tiền đã nhận: 500 triệu
Giờ chuyên môn đã xác nhận: 420 giờ
Thiết bị được cho mượn: 3 máy / 18 ngày-máy
Không gian thử nghiệm: 240 m² trong 6 tuần
Dataset được cấp quyền dùng: 2 bộ
Kênh phân phối pilot: 8 điểm
```

Mỗi số cần ghi:

- Promised hay delivered.
- Điều kiện và thời hạn.
- Bên liên quan.
- Phương pháp định lượng.
- Evidence ID.
- Phần đã được chấp nhận sử dụng.

## 9. Các lỗi cần tránh

- Tính toàn bộ lời hứa nguồn lực như nguồn lực đã có.
- Quy mọi giờ lao động theo một đơn giá.
- Gọi mọi dữ liệu được gửi là dữ liệu có thể sử dụng hợp pháp.
- Nhầm cho mượn thiết bị với chuyển quyền sở hữu.
- Nhầm giới thiệu một đầu mối với quyền tiếp cận thị trường.
- Đếm nguồn lực trùng cho nhiều dự án cùng lúc.
- Không ghi availability window và dependency.
- Nhận nguồn lực miễn phí nhưng bỏ qua chi phí tích hợp, bảo trì và hoàn trả.
- Dùng giá trị ước tính làm social proof mà không công bố phương pháp.

## 10. Kết luận cho dự án

> **Tiền chỉ là nguồn lực có tính chuyển đổi cao. Nền tảng phải nhìn thấy cả những nguồn lực khó thay thế hơn: đúng người, đúng dữ liệu, đúng thiết bị, đúng quyền tiếp cận và đúng thời điểm.**

## Khái niệm liên quan

- [[Thang cam kết và tín hiệu - Bản đồ thuật ngữ]]
- [[Commitment ladder]]
- [[Soft commitment và hard commitment]]
- [[Matching fund]]
- [[Evidence ledger và provenance]]
- [[Proof of use và proof of outcome]]
- [[Internal financial controls]]

## Nguồn tham khảo

- 2 CFR 200.1 và 200.306 — third-party in-kind contributions, valuation and documentation: https://www.law.cornell.edu/cfr/text/2/200.1 và https://www.law.cornell.edu/cfr/text/2/200.306
- OECD — Enhancing Access to and Sharing of Data: https://www.oecd.org/en/publications/enhancing-access-to-and-sharing-of-data_276aaca8-en.html
- Shen et al. — Ecosystem orchestration practices, 2024: https://arxiv.org/abs/2401.04526
