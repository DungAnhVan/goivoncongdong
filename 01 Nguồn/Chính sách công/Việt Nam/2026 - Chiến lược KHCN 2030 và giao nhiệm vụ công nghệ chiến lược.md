---
ai_authored: true
type: nguon-chinh-sach
status: da-doi-chieu
jurisdiction: Việt Nam
date_event: 2026-05-06
updated: 2026-08-11
tags:
  - science-technology-strategy
  - strategic-technology
  - public-task
  - rd
  - commercialization
---

# 2026 — Chiến lược KHCN 2030 và giao nhiệm vụ công nghệ chiến lược

## 1. Quyết định 604/QĐ-TTg ngày 02/04/2026

Thủ tướng phê duyệt **điều chỉnh, bổ sung Chiến lược phát triển khoa học, công nghệ và đổi mới sáng tạo đến năm 2030**.

Nguồn chính thức: https://vanban.chinhphu.vn/?classid=0&docid=217503&pageid=27160

Đây là national S&T/innovation strategy layer, chạy song song nhưng khác vai với [[2026 - Chiến lược quốc gia về khởi nghiệp sáng tạo NQ86]].

```text
NQ86
→ startup ecosystem strategy

QĐ604
→ broader S&T / innovation development strategy
```

Một project có thể nằm ở giao điểm hai chiến lược, nhưng strategy không phải funding approval.

## 2. Quyết định 21/2026/QĐ-TTg ngày 30/04/2026

- Có hiệu lực từ 01/07/2026.
- Ban hành Danh mục công nghệ chiến lược và Danh mục sản phẩm công nghệ chiến lược.
- Thay thế QĐ1131/QĐ-TTg năm 2025.

Nguồn: https://vanban.chinhphu.vn/?classid=1&docid=218002&orggroupid=3&pageid=27160

Danh mục hiện hành là một **priority taxonomy** để tập trung nguồn lực, không phải một grant list.

Nguồn chi tiết repo: [[2024-2026 - Các quỹ công NIC và nguồn lực R&D công nghệ cao]].

## 3. Quyết định 808/QĐ-TTg ngày 06/05/2026

Thủ tướng ban hành Quyết định 808/QĐ-TTg về **giao nhiệm vụ phát triển công nghệ chiến lược**.

Nguồn chính thức: https://vanban.chinhphu.vn/?classid=0&docid=218045&pageid=27160

### Ý nghĩa

Chuỗi này chuyển policy từ taxonomy sang execution:

```text
National strategy
→ strategic-tech list
→ assigned development tasks
→ programs/calls/projects
→ R&D / infrastructure / product development
→ measurable outputs
```

Đây là bằng chứng rằng `strategic technology` không nên chỉ là tag marketing. Tag đó có thể route project vào những **nhiệm vụ/chương trình cụ thể** khi có call và tiêu chí phù hợp.

## 4. Dấu vết operational năm 2026

Bộ KH&CN đã công bố kế hoạch tài trợ nhiệm vụ nghiên cứu phát triển công nghệ năm 2026 và viện dẫn QĐ604, QĐ21 cùng NĐ267/2025 làm căn cứ.

Nguồn: https://mst.gov.vn/thong-bao-ke-hoach-tai-tro-nhiem-vu-nghien-cuu-phat-trien-cong-nghe-nam-2026-197260714093009277.htm

NAFOSTED cũng công bố kế hoạch tài trợ nghiên cứu cơ bản năm 2026, ưu tiên một số lĩnh vực công nghệ lõi/chiến lược.

Nguồn: https://mst.gov.vn/thong-bao-ke-hoach-tai-tro-nghien-cuu-co-ban-nam-2026-197260714092003683.htm

## 5. Project taxonomy nên có version

```yaml
technology_priority:
  taxonomy_id: QD21-2026
  category:
  product_category:
  matched_at:
  source:
  taxonomy_effective_from: 2026-07-01
```

Không chỉ lưu:

```yaml
strategic_technology: true
```

vì danh mục có thể được cập nhật/thay thế theo thời gian.

## 6. Policy routing

```text
Project technology
→ classify under current QĐ21 taxonomy
→ check assigned task / national program
→ check R&D funding call
→ check university/NIC/lab resource
→ check local strategic-tech program
→ check commercialization / VC route
```

TP.HCM tương ứng:

- [[2025-2026 - Công nghệ chiến lược thương mại hóa tài sản trí tuệ và nhân lực]]
- [[2026 - Kế hoạch 141 và Chương trình 2685 hệ sinh thái đổi mới sáng tạo]]

## 7. Không được suy diễn

- Strategic-tech classification không tự tạo eligibility.
- QĐ808 giao nhiệm vụ cấp nhà nước không đồng nghĩa startup bất kỳ có thể nhận nhiệm vụ.
- Strategy/call/task phải lưu riêng state.
- Dự án dùng công nghệ chiến lược nhưng không có lợi thế/TRL/evidence phù hợp vẫn có thể không match chương trình.

## 8. Liên kết repo

- [[2026 - Chiến lược quốc gia về khởi nghiệp sáng tạo NQ86]]
- [[2025-2026 - Khung quốc gia KHCN đổi mới sáng tạo và startup]]
- [[2024-2026 - Các quỹ công NIC và nguồn lực R&D công nghệ cao]]
- [[Multi-resource matching]]
- [[Evidence ledger]]
- [[Bản đồ chính sách công Việt Nam và TP.HCM - 2026]]
