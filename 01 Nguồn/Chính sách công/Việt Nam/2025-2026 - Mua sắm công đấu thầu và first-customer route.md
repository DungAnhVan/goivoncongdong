---
type: nguon-chinh-sach
status: da-doi-chieu
jurisdiction: Việt Nam
date_event: 2026-08-11
updated: 2026-08-11
tags:
  - public-procurement
  - first-customer
  - bidding
  - sme
  - market-access
---

# 2025–2026 — Mua sắm công, đấu thầu và `first-customer route`

## 1. Khung Luật Đấu thầu hiện hành dùng trong nghiên cứu

Văn phòng Quốc hội công bố **Văn bản hợp nhất 126/VBHN-VPQH ngày 27/08/2025 — Luật Đấu thầu**.

Nguồn chính thức: https://vanban.chinhphu.vn/?docid=215251&pageid=27160

Luật 90/2025/QH15 đã sửa đổi Luật Đấu thầu cùng một số luật khác, có hiệu lực từ 01/07/2025.

Nguồn: https://vanban.chinhphu.vn/?docid=214558&orggroupid=1&pageid=27160

## 2. Nghị định 214/2025/NĐ-CP

- Ban hành và có hiệu lực: 04/08/2025.
- Quy định chi tiết một số điều và biện pháp thi hành Luật Đấu thầu về lựa chọn nhà thầu.

Nguồn: https://vanban.chinhphu.vn/?classid=1&docid=214821&pageid=27160

### Watch status

Ngày 10/06/2026, Bộ Tài chính có dự thảo sửa đổi Nghị định 214/2025; đợt góp ý đã kết thúc. Tại snapshot 11/08/2026, file này **không tự coi dự thảo là văn bản đã có hiệu lực**.

Nguồn dự thảo: https://vanban.chinhphu.vn/du-thao-vbqppl/du-thao-nghi-dinh-sua-doi-bo-sung-mot-so-dieu-cua-nghi-dinh-so-214-2025-nd-cp-ngay-04-thang-8-na-7851

## 3. Public procurement không phải grant

```text
Grant / subsidy
→ Nhà nước hỗ trợ một activity/project theo mục tiêu chính sách

Public procurement
→ cơ quan công mua hàng hóa/dịch vụ/công trình theo nhu cầu và quy trình áp dụng
```

Vì vậy một startup bán sản phẩm cho cơ quan nhà nước là **supplier/contractor**, không nên ghi thành “nhận tài trợ” nếu bản chất giao dịch là mua sắm.

## 4. `First customer` phải có evidence riêng

Có nhiều mức rất khác nhau:

```text
Public problem statement
→ invitation to pilot
→ unpaid test
→ paid pilot
→ procurement procedure
→ signed contract
→ acceptance
→ payment
→ repeat/scale procurement
```

Không được hiển thị logo cơ quan công như “khách hàng” nếu mới chỉ tham gia sự kiện hoặc thử nghiệm chưa có giao dịch.

Liên kết:

- [[Commitment ladder]]
- [[Costly signaling và cheap talk]]
- [[Social proof và authentic social proof]]
- [[Evidence ledger]]

## 5. SME/startup procurement opportunity

NQ198/2025/QH15 và NĐ20/2026 tạo thêm policy context cho việc hỗ trợ khu vực kinh tế tư nhân/SME tiếp cận thị trường và mua sắm công theo điều kiện áp dụng.

Nguồn chi tiết: [[2025-2026 - Kinh tế tư nhân SME và vốn khởi nghiệp]].

Nhưng:

> `Có ưu tiên/cơ hội tham gia` ≠ `được trao hợp đồng`.

Project vẫn phải đáp ứng điều kiện của gói mua sắm, hồ sơ, năng lực, tiêu chuẩn và quy trình tương ứng.

## 6. Public task / R&D ordering khác procurement thương mại thông thường

Trong KHCN/ĐMST có thể tồn tại các cơ chế:

- đặt hàng nhiệm vụ;
- tuyển chọn;
- giao trực tiếp trong trường hợp luật cho phép;
- tài trợ nhiệm vụ;
- procurement hàng hóa/dịch vụ.

Không gom tất cả thành `government contract`.

Repo liên quan:

- [[2025-2026 - Khung quốc gia KHCN đổi mới sáng tạo và startup]]
- [[2026 - NQ24 QD36 quản lý nhiệm vụ và công nhận actor hệ sinh thái]]
- [[2025-2026 - Công nghệ chiến lược thương mại hóa tài sản trí tuệ và nhân lực]]

## 7. Data object cho procurement opportunity

```yaml
public_market_opportunity:
  authority:
  problem_or_need:
  route: grant | rd_task | pilot | procurement
  legal_basis:
  procurement_method:
  eligibility:
  technical_requirements:
  budget_or_estimate:
  deadline:
  required_evidence:
  contract_status:
  acceptance_status:
  payment_status:
  source_url:
  checked_at:
```

## 8. Ý nghĩa với SAMSTI

Policy routing không nên dừng ở “xin tiền”. Với project đủ trưởng thành, hệ thống có thể route sang:

```text
Grant
OR
R&D task
OR
Corporate pilot
OR
Public paid pilot
OR
Procurement
OR
VC / investment
```

Đây là cách biến **khách hàng đầu tiên** thành một resource route có bằng chứng.

## 9. Không được suy diễn

- Cơ quan công nêu bài toán không phải lời hứa mua.
- Pilot không tự động dẫn đến procurement.
- Procurement không phải grant.
- Dự thảo sửa NĐ214 chưa được dùng như văn bản hiện hành.
- Không dùng quan hệ/giới thiệu để thay thế quy trình mua sắm phải tuân thủ.

## 10. Liên kết repo

- [[Public procurement]]
- [[Grant và subsidy]]
- [[Commitment ladder]]
- [[Evidence ledger]]
- [[Multi-resource matching]]
- [[Bản đồ chính sách công Việt Nam và TP.HCM - 2026]]
