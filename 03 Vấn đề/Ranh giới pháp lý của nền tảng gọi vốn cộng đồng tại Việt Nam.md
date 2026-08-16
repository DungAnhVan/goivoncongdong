---
ai_authored: true
---

# Ranh giới pháp lý của nền tảng gọi vốn cộng đồng tại Việt Nam

> Trạng thái: vấn đề mở — cần tiếp tục research + legal opinion trước khi vận hành tiền thật.
>
> Cập nhật: 10/08/2026.

**Nguồn chính:** [[Pháp luật Việt Nam - Bản đồ cho mô hình gọi vốn cộng đồng]]

## 1. Vấn đề trung tâm

Việt Nam chưa được nhóm nghiên cứu xác định là có một chế độ pháp lý duy nhất mang tên `crowdfunding` bao trùm mọi mô hình. Vì vậy ranh giới hợp pháp của nền tảng phụ thuộc vào **substance** của từng campaign và chức năng thực tế của platform.

Câu hỏi không phải:

> Nền tảng gọi vốn cộng đồng có được phép không?

Mà là:

> Ở mỗi bước, platform đang cung cấp dịch vụ thông tin, thương mại điện tử, thanh toán, huy động đầu tư, quản lý tài sản, môi giới, tư vấn hay chức năng nào khác?

## 2. Bảy ranh giới chưa được phép vượt bằng giả định

### Ranh giới 1 — Information → Transaction

```text
Đăng ý tưởng / thảo luận
→ người dùng tạo cam kết
→ giao kết hợp đồng
→ thanh toán
```

Khi người dùng bắt đầu tạo quyền và nghĩa vụ, platform không còn chỉ là nơi đăng nội dung.

Liên quan:
- [[Thương mại điện tử và trách nhiệm nền tảng]]
- [[Người tiêu dùng, hợp đồng và giao dịch điện tử]]

### Ranh giới 2 — Donation → Sale

```text
Không có đối ứng kinh tế đáng kể
→ donation

Nhận sản phẩm / dịch vụ như đối tượng chính
→ reward / pre-order / sale cần phân loại
```

Không được dùng từ `ủng hộ` để che một giao dịch bán hàng.

### Ranh giới 3 — Contribution → Investment

Nếu contributor nhận:

- hoàn vốn;
- lãi;
- lợi nhuận;
- doanh thu;
- cổ phần/phần vốn;
- quyền tài chính có thể chuyển nhượng;

→ campaign phải qua legal gate về đầu tư/chứng khoán/doanh nghiệp.

Liên quan: [[Huy động vốn, đầu tư và chứng khoán]].

### Ranh giới 4 — Payment integration → Holding client/project money

```text
Platform gọi API payment provider
≠
Platform tự giữ tiền của contributor
```

Nếu tiền nằm trong tài khoản do platform kiểm soát, phải review riêng về thanh toán, quyền sở hữu, safeguarding, kế toán, AML và insolvency risk.

Liên quan: [[Thanh toán, giữ tiền và phòng chống rửa tiền]].

### Ranh giới 5 — Matching → Investment management

```text
Hiển thị project phù hợp
≠
quyết định đầu tư thay người dùng
≠
gom pool tiền rồi phân bổ
```

Nếu platform bắt đầu tự chọn nơi tiền của người khác được đầu tư, đây là vùng pháp lý khác hẳn matching cộng đồng.

### Ranh giới 6 — Transparency → Personal-data disclosure

Evidence có thể cần verifier xem nhưng không đồng nghĩa phải public toàn bộ.

Liên quan: [[Bảo vệ dữ liệu cá nhân]].

### Ranh giới 7 — Community pool → Fund

Gom tài sản của nhiều người vào một pool rồi tổ chức tự quyết định phân bổ khác với việc mỗi contributor chỉ định một campaign cụ thể.

Phải so với:
- quỹ xã hội/quỹ từ thiện;
- quỹ đầu tư khởi nghiệp sáng tạo;
- quỹ đầu tư chứng khoán;
- các cấu trúc đầu tư/hợp đồng khác.

## 3. Legal gates đề xuất

### Gate A — trước khi publish campaign

Phải xác định:

```text
legal type
campaign creator
legal entity / recipient
rights of contributor
money flow
refund rule
platform role
consumer status
personal-data flow
cross-border status
```

### Gate B — trước khi bật payment

Phải xác định:

```text
Ai nhận tiền?
Ai đứng tên tài khoản?
Ai có quyền release?
Platform fee được tách thế nào?
Ai hoàn tiền?
Payment provider nào?
Ledger và reconciliation ra sao?
```

### Gate C — trước khi cho phép financial return

Nếu có bất kỳ:

```text
return of principal
interest
profit share
revenue share
ownership
security/token with financial right
pooled allocation
```

→ **không tự động triển khai**; yêu cầu legal opinion bằng văn bản.

### Gate D — trước khi mở cross-border

Review tối thiểu:

- ngoại hối;
- thuế;
- AML/sanctions;
- dữ liệu xuyên biên giới;
- luật áp dụng;
- tranh chấp;
- payment provider;
- securities rules ở nước contributor nếu investment.

## 4. Các câu hỏi cần luật sư Việt Nam trả lời bằng văn bản

1. Với donation/reward/pre-order, vai trò pháp lý tối ưu của platform là gì?
2. Platform có thể thiết kế all-or-nothing bằng payment authorization hoặc account structure nào mà không tự trở thành nhà cung ứng dịch vụ thanh toán?
3. Có cấu trúc nào cho phép giữ tiền có điều kiện qua ngân hàng/payment partner phù hợp pháp luật Việt Nam?
4. Khi platform thu phí theo % campaign, nghĩa vụ thuế/hóa đơn và trách nhiệm với giao dịch gốc thay đổi thế nào?
5. Ngưỡng nào khiến `revenue share`, `conditional return`, `investment cooperation` hoặc quyền tương tự phải xử lý như sản phẩm đầu tư/chứng khoán?
6. Nếu project chưa có pháp nhân, chủ thể nào được phép nhận tiền và chịu nghĩa vụ?
7. Cấu trúc `community matching fund` có thể dùng doanh nghiệp bình thường hay cần pháp nhân/quỹ riêng?
8. Khi beneficiary là cá nhân, donation campaign phát sinh nghĩa vụ thuế và chứng từ thế nào?
9. Platform phải thực hiện KYC đến mức nào khi bản thân chưa phải reporting entity AML nhưng payment partner là reporting entity?
10. Những nghĩa vụ cụ thể nào của Luật TMĐT 122/2025/QH15 và NĐ 248/2026/NĐ-CP áp trực tiếp cho kiến trúc dự kiến?

## 5. Giả thuyết vận hành tạm thời

Cho pilot đầu, hướng ít tạo rủi ro pháp lý mới nhất để nghiên cứu tiếp là:

```text
Platform = project-development + evidence + matching layer

Campaign loại đầu:
→ donation / reward / pre-order đã phân loại
→ không financial return
→ không equity/debt
→ không pooled investment
→ tiền qua ngân hàng/payment partner phù hợp
→ project/recipient rõ chủ thể
→ refund/change rule rõ
→ platform không tự đầu tư tiền thay user
```

Đây **không phải kết luận hợp pháp cuối cùng**, chỉ là giả thuyết kiến trúc để thu hẹp số vùng pháp lý phải mở cùng lúc.

## 6. Tiêu chuẩn đóng vấn đề này

Node chỉ được chuyển khỏi `03 Vấn đề` khi có:

- legal classification matrix hoàn chỉnh;
- money-flow diagram được luật sư review;
- platform role memo;
- campaign contract map;
- privacy/data map;
- tax/accounting memo;
- danh sách giấy phép/đăng ký/thông báo cần thiết;
- legal opinion cho pilot;
- change log theo phiên bản pháp luật.

> **Câu lõi:** Platform không nên hỏi “lách luật thế nào để làm crowdfunding”; phải chia mô hình thành các hành vi pháp lý nhỏ đến mức biết chính xác luật nào điều chỉnh từng hành vi.
