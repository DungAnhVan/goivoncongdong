# Ma trận phân loại mô hình crowdfunding tại Việt Nam

> Cập nhật: 10/08/2026.
>
> Mục tiêu: dùng trước khi thiết kế campaign để xác định cụm luật cần mở.

## 1. Ma trận nhanh

| Mô hình | Người góp nhận gì? | Cụm luật chính cần kiểm tra | Rủi ro trọng tâm |
|---|---|---|---|
| Donation | Không có quyền tài chính; có thể chỉ recognition | Dân sự; đóng góp tự nguyện; quỹ xã hội/từ thiện tùy cấu trúc; thuế; dữ liệu | sai mục đích, phần dư, công khai, thuế |
| Reward | Quà/quyền lợi phi tài chính | Dân sự; TMĐT; người tiêu dùng; thuế | reward thực chất là hàng hóa/dịch vụ |
| Pre-order | Sản phẩm/dịch vụ tương lai | TMĐT; người tiêu dùng; giao dịch điện tử; thuế | giao trễ, không giao, refund |
| Lending | Hoàn vốn + lãi hoặc quyền đòi nợ | Dân sự; tín dụng/ngân hàng tùy cấu trúc; thuế; AML | kinh doanh cho vay, lãi, thu hồi nợ |
| Revenue share | Quyền hưởng % doanh thu/lợi nhuận | Dân sự; doanh nghiệp; đầu tư; có thể chứng khoán tùy cấu trúc | sản phẩm đầu tư trá hình |
| Equity | Cổ phần/phần vốn | Doanh nghiệp; chứng khoán; đầu tư; thuế | chào bán, ghi nhận sở hữu, phân phối |
| Bond/debt security | Chứng khoán nợ | Chứng khoán; trái phiếu doanh nghiệp | phát hành/chào bán trái luật |
| Investment pool | Nền tảng/quản lý chọn tài sản thay cộng đồng | Chứng khoán; quản lý quỹ; AML; thanh toán | hoạt động quản lý đầu tư không phép |
| Social/charity fund | Tài sản vào quỹ không vì lợi nhuận | Nghị định 03/2026/NĐ-CP; thuế; kế toán | lập/quản lý quỹ sai cấu trúc |
| Disaster/medical appeal | Đóng góp tự nguyện cho mục tiêu thuộc phạm vi | Nghị định 93/2021/NĐ-CP | tiếp nhận, phân phối, công khai |

## 2. Decision tree trước khi campaign được publish

```text
1. Người góp có quyền nhận lại tiền không?
   ├─ Không
   │   ├─ Có hàng/dịch vụ đối ứng?
   │   │   ├─ Có → Reward / Pre-order
   │   │   └─ Không → Donation / Sponsorship / Grant
   │   └─ Có quyền sở hữu hoặc lợi nhuận?
   │       └─ Nếu có → không còn donation thuần
   │
   └─ Có
       ├─ Hoàn đúng số tiền?
       │   → Loan / refundable advance / deposit
       ├─ Hoàn kèm lãi?
       │   → Lending / debt
       ├─ Hưởng doanh thu/lợi nhuận?
       │   → Investment / revenue share
       └─ Có cổ phần/phần vốn?
           → Equity
```

Sau đó hỏi tiếp:

```text
2. Ai nhận tiền?
3. Ai giữ tiền trong thời gian chờ?
4. Nền tảng có quyền quyết định phân bổ không?
5. Có chào mời rộng rãi ra công chúng không?
6. Có nhiều project nằm trong một pool đầu tư không?
7. Contributor là consumer, donor hay investor?
8. Campaign có yếu tố nước ngoài không?
```

## 3. Mức rủi ro theo chức năng nền tảng

### Mức thấp hơn — Information layer

- đăng ý tưởng;
- thảo luận;
- matching chuyên gia;
- lưu evidence;
- không nhận tiền;
- không hứa lợi nhuận.

### Mức trung bình — Campaign layer

- host campaign;
- pre-order/reward/donation;
- tích hợp payment provider;
- milestone/refund;
- platform fee.

Cần TMĐT, consumer, tax, payment, data review.

### Mức cao — Investment layer

- cổ phần;
- debt;
- revenue share;
- investment agreement;
- pooled capital;
- platform recommends/allocates investments.

Cần securities/investment/legal opinion trước khi build.

## 4. Rule engine gợi ý

Mỗi campaign nên có các field bắt buộc:

```yaml
campaign_legal_type:
  - donation
  - reward
  - pre_order
  - loan
  - revenue_share
  - equity
  - debt_security
  - grant
  - other_review_required

return_of_principal: true/false
financial_return: true/false
ownership_right: true/false
goods_or_services: true/false
public_offer: true/false
platform_holds_funds: true/false
platform_allocates_funds: true/false
cross_border: true/false
beneficiary_type: individual/company/fund/other
```

Nếu:

```text
financial_return = true
OR ownership_right = true
OR platform_allocates_funds = true
```

→ **LEGAL GATE: không publish trước khi legal review hoàn thành.**

## 5. Không cho creator tự chọn nhãn tùy ý

Creator có thể nghĩ campaign là donation nhưng mô tả lại hứa chia lợi nhuận.

Do đó cần rule-based review:

```text
Label do creator chọn
≠ legal classification cuối cùng
```

Nền tảng phải đối chiếu offer, rights và money flow.

## 6. Ví dụ

### Case A

> Góp 500.000 để nhận áo kỷ niệm trị giá nhỏ; không hoàn vốn, không lợi nhuận.

Khả năng: donation + recognition/reward. Kiểm tra TMĐT/consumer nếu reward mang bản chất hàng hóa bán cho contributor.

### Case B

> Góp 10 triệu, sau 18 tháng được nhận lại 10 triệu + 12%.

Không được gọi donation. Đây là giao dịch có principal + return; phải mở legal review lending/debt/investment.

### Case C

> Góp 50 triệu nhận 0,5% công ty.

Equity. Phải có legal entity, cấu trúc phát hành/chuyển nhượng và kiểm tra luật doanh nghiệp/chứng khoán.

### Case D

> Người dùng nạp tiền vào ví trên nền tảng, nền tảng tự chia vào 20 dự án rồi trả lợi nhuận.

Rủi ro rất cao: payment + pooled investment + investment management + AML + securities.

## 7. Câu lõi

> **Classification trước, fundraising sau. Nếu chưa biết một đồng tiền tạo ra quyền gì thì chưa được mở campaign.**
