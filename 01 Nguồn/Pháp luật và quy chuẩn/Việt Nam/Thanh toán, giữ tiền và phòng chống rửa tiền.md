# Thanh toán, giữ tiền và phòng chống rửa tiền

> Cập nhật: 10/08/2026.

## 1. Câu hỏi phải tách trước

Không dùng chung câu `nền tảng giữ tiền`.

Phải tách:

```text
Ai là chủ sở hữu pháp lý của tiền?
Tài khoản đứng tên ai?
Nền tảng có quyền sử dụng tiền không?
Nền tảng chỉ truyền lệnh hay tự quyết định giải ngân?
Tiền là tiền mua hàng, tiền góp vốn, tiền ký quỹ hay tiền tài trợ?
Có hoàn tiền tự động không?
Có thu hộ/chi hộ không?
Có tạo số dư người dùng không?
Có cho phép chuyển tiền giữa người dùng không?
```

## 2. Nghị định 52/2024/NĐ-CP

Nghị định 52/2024/NĐ-CP quy định về thanh toán không dùng tiền mặt, có hiệu lực từ 01/07/2024.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?classid=0&docid=210262&pageid=27160)

[CHẮC]

Hoạt động cung ứng dịch vụ thanh toán và dịch vụ trung gian thanh toán là lĩnh vực được quản lý. Vì vậy một startup không nên tự gọi mình là `payment intermediary`, `wallet`, `escrow service`, `custodian` hoặc triển khai chức năng có bản chất tương ứng chỉ vì có thể làm được về kỹ thuật.

[PHÂN LOẠI]

Việc một doanh nghiệp nhận tiền theo hợp đồng thương mại không tự động biến doanh nghiệp thành tổ chức trung gian thanh toán. Phải phân loại chức năng thực tế theo Nghị định 52 và quy định của NHNN.

## 3. Thiết kế dòng tiền cho crowdfunding

Ba cấu trúc phải phân biệt:

### A. Tiền đi thẳng đến pháp nhân dự án

```text
Contributor
→ ngân hàng/payment provider
→ tài khoản pháp nhân dự án
```

Nền tảng không trực tiếp giữ tiền nhưng vẫn có thể có trách nhiệm về thông tin, hợp đồng, chứng cứ, điều kiện campaign tùy mô hình.

### B. Tiền đi qua đối tác thanh toán được phép

```text
Contributor
→ payment intermediary/bank
→ điều kiện xử lý
→ project / refund
```

Đây là hướng đáng nghiên cứu nếu muốn AON/refund có kiểm soát.

### C. Tiền vào tài khoản do nền tảng kiểm soát

Đây là cấu trúc phải review pháp lý nghiêm ngặt nhất vì xuất hiện các câu hỏi về quyền sở hữu tiền, tiền của khách hàng, thu hộ/chi hộ, safeguarding, kế toán, insolvency risk và giấy phép.

## 4. Escrow

`Escrow` là thuật ngữ hữu ích về cơ chế nhưng không được giả định rằng pháp luật Việt Nam có một giấy phép chung tên “escrow” cho mọi doanh nghiệp.

Trước khi gọi một cấu trúc là escrow cần xác định:

- ai là bên giữ;
- căn cứ pháp lý của việc giữ;
- tài khoản và quyền kiểm soát;
- điều kiện release;
- điều kiện refund;
- xử lý khi một bên phá sản;
- phí;
- dispute rule.

## 5. Phòng, chống rửa tiền

### Luật số 14/2022/QH15

Luật Phòng, chống rửa tiền có hiệu lực từ 01/03/2023.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?classid=1&docid=207710&pageid=27160&typegroupid=3)

### Nghị định 19/2023/NĐ-CP

Quy định chi tiết một số điều của Luật Phòng, chống rửa tiền.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?classid=1&docid=207830&pageid=27160&typegroupid=4)

### Nghị quyết 66.23/2026/NQ-CP

Ngày 24/07/2026 Chính phủ ban hành cơ chế, chính sách đặc thù nhằm xử lý một số khó khăn, vướng mắc trong pháp luật phòng, chống rửa tiền để đáp ứng cam kết quốc tế về trao đổi thông tin theo yêu cầu về thuế.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?docid=218997&orggroupid=2&pageid=27160)

## 6. Nền tảng có phải đối tượng báo cáo AML không?

[PHÂN LOẠI]

Không được mặc định rằng mọi nền tảng crowdfunding đều là đối tượng báo cáo trực tiếp theo Luật AML. Điều này phụ thuộc ngành nghề và chức năng thực tế.

Tuy nhiên, ngay cả khi nền tảng chưa phải reporting entity, các ngân hàng/payment partners có thể có nghĩa vụ KYC, screening, transaction monitoring và reporting; vì vậy onboarding của nền tảng phải thiết kế để tương thích.

## 7. Control tối thiểu cho pilot

- Không dùng tài khoản cá nhân của founder để nhận tiền campaign.
- Tách tiền vận hành nền tảng và tiền campaign.
- Mỗi transaction có project ID và contributor ID.
- Có ledger đối soát với ngân hàng/payment provider.
- Không giải ngân chỉ dựa trên một người phê duyệt.
- Có rule với refund, chargeback, suspicious transaction và account freeze.
- Lưu evidence cho mọi thay đổi beneficiary bank account.
- Xác minh chủ thể dự án trước khi cho nhận tiền.

## 8. Câu lõi

> **Nếu chưa trả lời được ai sở hữu tiền, ai kiểm soát tài khoản và ai có quyền ra lệnh chuyển tiền thì chưa được gọi đó chỉ là “payment flow”.**
