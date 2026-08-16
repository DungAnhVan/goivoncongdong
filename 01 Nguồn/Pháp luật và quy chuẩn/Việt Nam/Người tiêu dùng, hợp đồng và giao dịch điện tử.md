---
ai_authored: true
---

# Người tiêu dùng, hợp đồng và giao dịch điện tử

> Cập nhật: 10/08/2026.

## 1. Ba lớp phải đi cùng nhau

Một campaign reward/pre-order không chỉ là `website`.

Nó có thể tạo đồng thời:

```text
Quan hệ hợp đồng dân sự/thương mại
+ giao dịch điện tử
+ quan hệ người tiêu dùng
```

## 2. Bộ luật Dân sự số 91/2015/QH13

Có hiệu lực từ 01/01/2017.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?classid=1&docid=183188&pageid=27160&typegrou=)

Bộ luật Dân sự là nền chung để phân tích giao dịch, nghĩa vụ, hợp đồng, đại diện, tài sản, hoàn trả và bồi thường khi không có chế độ chuyên ngành thay thế.

## 3. Luật Giao dịch điện tử số 20/2023/QH15

- Ban hành: 22/06/2023.
- Có hiệu lực: 01/07/2024.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?classid=1&docid=208421&pageid=27160&typegroupid=3)

[CHẮC]

Không nên xem click, OTP, checkbox, e-sign hoặc electronic record chỉ là UX. Khi chúng được dùng để biểu thị ý chí, xác nhận giao dịch hoặc lưu chứng cứ, phải thiết kế theo luật giao dịch điện tử và luật chuyên ngành liên quan.

## 4. Luật Bảo vệ quyền lợi người tiêu dùng số 19/2023/QH15

- Ban hành: 20/06/2023.
- Có hiệu lực: 01/07/2024.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?classid=1&docid=208363&orggroupid=1&pageid=27160&previousPage=other+articles)

[PHÂN LOẠI]

Nếu contributor thực chất mua hàng hóa/dịch vụ để tiêu dùng, họ có thể đồng thời là người tiêu dùng; khi đó không được chỉ gọi họ là `backer` để làm mờ quyền tiêu dùng.

## 5. Campaign phải xác định “ai là bên hợp đồng”

Ví dụ:

```text
Contributor ↔ Campaign creator
Platform chỉ cung cấp hạ tầng
```

khác với:

```text
Contributor ↔ Platform
Platform bán reward rồi thuê project fulfil
```

và khác với:

```text
Contributor ↔ Merchant
Platform là marketplace / intermediary
```

UI phải phản ánh đúng cấu trúc, không để người dùng suy đoán.

## 6. Acceptance record

Với mỗi commitment có giá trị pháp lý nên lưu:

- campaign version;
- terms version;
- refund rule version;
- actor identity;
- timestamp;
- action tạo consent;
- amount/resource;
- payment authorization reference;
- material risk disclosure đã hiển thị;
- re-consent record nếu campaign thay đổi trọng yếu.

## 7. Không dùng “im lặng = đồng ý” một cách tùy tiện

Nếu campaign đổi mục đích, reward, timeline, beneficiary hoặc điều kiện hoàn tiền, việc chỉ gửi notification không tự động chứng minh người tham gia đã chấp thuận thay đổi.

Đây là lý do repo đã có node `Material change, pivot and re-consent` và `Commitment versioning`.

## 8. Refund ≠ remedy duy nhất

Khi giao dịch thất bại có thể phát sinh:

```text
Refund
Replacement
Repair
Partial fulfilment
Compensation
Release of authorization
Cancellation
Termination
Dispute resolution
```

Cần xác định theo loại quan hệ pháp lý cụ thể.

## 9. Terms phải tách các statement

Không trộn các câu sau thành một checkbox:

```text
Tôi đồng ý điều khoản sử dụng.
Tôi đồng ý campaign charter.
Tôi đồng ý xử lý dữ liệu.
Tôi đồng ý nhận marketing.
Tôi hiểu rủi ro dự án.
Tôi đặt hàng / donation / đầu tư.
```

Mỗi loại consent có mục đích pháp lý khác nhau.

## 10. Câu lõi

> **Một nút “Ủng hộ ngay” không nói được người dùng vừa donation, mua hàng, ký hợp đồng hay đầu tư; hệ thống phải biết chính xác họ vừa tạo quan hệ pháp lý nào.**
