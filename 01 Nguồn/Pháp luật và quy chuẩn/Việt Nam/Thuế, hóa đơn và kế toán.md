---
ai_authored: true
---

# Thuế, hóa đơn và kế toán

> Cập nhật: 10/08/2026.

## 1. Không có một “thuế crowdfunding” duy nhất

Thuế phụ thuộc bản chất khoản tiền.

Cần tách:

```text
Donation
Doanh thu bán hàng
Doanh thu dịch vụ
Phí nền tảng
Khoản vay
Tiền góp vốn
Lãi vay
Lợi tức/cổ tức
Grant/subsidy
Khoản hoàn trả
Vendor refund
```

Không được ghi mọi dòng tiền contributor gửi vào là `revenue`.

## 2. Luật Thuế thu nhập doanh nghiệp số 67/2025/QH15

- Ban hành: 14/06/2025.
- Có hiệu lực: 01/10/2025.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?docid=214607&pageid=27160&typegroupid=3)

## 3. Luật Thuế thu nhập cá nhân số 109/2025/QH15

- Ban hành: 10/12/2025.
- Có hiệu lực: 01/07/2026.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?classid=1&docid=216495&pageid=27160&typegroupid=3)

## 4. Luật Quản lý thuế số 108/2025/QH15

- Ban hành: 10/12/2025.
- Có hiệu lực: 01/07/2026.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?classid=1&docid=216541&pageid=27160&typegroupid=3)

Các văn bản triển khai mới đáng chú ý từ 01/07/2026 gồm Nghị định 254/2026/NĐ-CP về hóa đơn điện tử, chứng từ điện tử và Thông tư 91/2026/TT-BTC.

Nguồn: [Cổng TTĐT Chính phủ — Thông tư 91/2026/TT-BTC](https://vanban.chinhphu.vn/?classid=1&docid=219006&orggroupid=4&pageid=27160)

## 5. Luật Thuế giá trị gia tăng

Đến thời điểm nghiên cứu có Luật sửa đổi số 149/2025/QH15, có hiệu lực từ 01/01/2026.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?docid=216588&pageid=27160&typegroupid=3)

## 6. Campaign accounting model

Mỗi transaction nên có classification field:

```text
Transaction ID
Campaign ID
Legal entity
Contributor
Nature: donation / sale / loan / equity / fee / refund
Gross amount
Platform fee
Payment fee
Tax treatment status
Invoice/receipt status
Restriction
Refundability
Recognized revenue?
Liability?
Equity?
```

## 7. Tiền campaign không mặc nhiên là doanh thu nền tảng

Ví dụ:

```text
Contributor trả 1.000.000
Platform fee 50.000
950.000 thuộc campaign/project
```

Hạch toán không thể chỉ ghi:

```text
Doanh thu platform = 1.000.000
```

Phải xác định nền tảng là principal, agent, intermediary hay bên nhận tiền theo cấu trúc thực tế.

## 8. Donation không mặc nhiên được miễn thuế

[VÙNG XÁM — cần tax opinion theo chủ thể và mục đích cụ thể]

Việc gọi khoản tiền là donation không đủ để kết luận về nghĩa vụ thuế. Phải xét người nhận là cá nhân, doanh nghiệp, quỹ xã hội/quỹ từ thiện hay tổ chức khác; mục đích; quyền lợi đối ứng; và luật thuế áp dụng.

## 9. Reward/pre-order

Nếu khoản đóng góp đổi lấy hàng hóa/dịch vụ, cần xem như một giao dịch kinh doanh tiềm năng về:

- doanh thu;
- VAT;
- hóa đơn;
- thời điểm ghi nhận;
- refund;
- fulfilment;
- phí nền tảng.

Không nên marketing là `donation` nếu substance là sale.

## 10. Investment

Tiền mua cổ phần/góp vốn khác doanh thu bán hàng.

Tương tự, khoản vay tạo liability chứ không phải doanh thu.

System ledger phải phân biệt bản chất ngay từ transaction creation, không chờ kế toán sửa cuối tháng.

## 11. Cross-border

Nếu nhận contributor nước ngoài hoặc trả tiền cho service provider ở nước ngoài, cần mở checklist:

- foreign contractor tax nếu áp dụng;
- foreign exchange;
- withholding;
- cross-border e-commerce tax;
- invoice/documentation;
- beneficial owner/AML;
- transfer pricing nếu related party.

## 12. Câu lõi

> **Một đồng tiền đi vào hệ thống phải được gắn bản chất pháp lý và kế toán ngay từ đầu; nếu chỉ biết “đã nhận 1 triệu” thì ledger chưa đủ để vận hành thật.**
