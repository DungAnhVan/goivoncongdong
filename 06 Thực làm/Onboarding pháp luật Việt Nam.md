---
ai_authored: true
---

# Onboarding pháp luật Việt Nam

> Mục tiêu: giúp thành viên mới đọc khung pháp luật theo đúng thứ tự trước khi đề xuất campaign, money flow hoặc tính năng tài chính.
>
> Cập nhật: 10/08/2026.

## 1. Nguyên tắc đầu tiên

Không bắt đầu bằng câu:

> “Crowdfunding có hợp pháp không?”

Bắt đầu bằng:

```text
Actor nào?
→ thực hiện hành vi gì?
→ với tài sản nào?
→ tạo quyền gì?
→ ai giữ/kiểm soát tiền?
→ ai chịu nghĩa vụ?
→ luật chuyên ngành nào có thể áp dụng?
```

## 2. Lộ trình đọc 90 phút

### 0–15 phút — Bản đồ

Đọc:

1. [[Pháp luật Việt Nam - Bản đồ cho mô hình gọi vốn cộng đồng]]
2. [[Ma trận phân loại mô hình crowdfunding tại Việt Nam]]
3. [[Ranh giới pháp lý của nền tảng gọi vốn cộng đồng tại Việt Nam]]

Kết quả cần đạt:

- hiểu vì sao `góp tiền` không phải một loại giao dịch pháp lý duy nhất;
- biết đâu là legal gate.

### 15–35 phút — Money và investment

Đọc:

1. [[Huy động vốn, đầu tư và chứng khoán]]
2. [[Thanh toán, giữ tiền và phòng chống rửa tiền]]
3. [[Doanh nghiệp, startup và quỹ đầu tư khởi nghiệp sáng tạo]]

Kết quả:

- phân biệt project, legal entity, issuer;
- phân biệt payment, holding money, pooled investment;
- nhận diện financial-return red flags.

### 35–55 phút — Transaction và user rights

Đọc:

1. [[Thương mại điện tử và trách nhiệm nền tảng]]
2. [[Người tiêu dùng, hợp đồng và giao dịch điện tử]]

Kết quả:

- xác định ai là bên hợp đồng;
- biết khi nào `backer` thực chất là consumer/customer;
- hiểu versioning và consent là vấn đề pháp lý, không chỉ UX.

### 55–70 phút — Donation và community money

Đọc:

1. [[Đóng góp tự nguyện, quỹ xã hội và quỹ từ thiện]]
2. [[Restricted funds]]
3. [[Residual funds and unused resources]]

Kết quả:

- không dùng donation để che sale/investment;
- biết cần rule cho purpose, surplus và failure.

### 70–90 phút — Data + tax

Đọc:

1. [[Bảo vệ dữ liệu cá nhân]]
2. [[Thuế, hóa đơn và kế toán]]
3. [[Danh mục nguồn pháp luật Việt Nam hiện hành]]

Kết quả:

- biết evidence không đồng nghĩa public data;
- mỗi transaction cần tax/accounting classification;
- biết cách kiểm tra source sống.

## 3. Bài tập onboarding

Cho campaign giả định:

> “500 người cùng góp tiền để xây một thiết bị xử lý nước. Người góp từ 1 triệu được nhận sản phẩm đầu tiên; từ 20 triệu được chia 5% doanh thu trong 3 năm. Platform nhận tiền vào tài khoản công ty, giữ đến khi đủ 500 triệu rồi tự giải ngân theo milestone.”

Người onboarding phải tách ít nhất:

```text
Pre-order / reward layer
Revenue-share / investment layer
Platform fee
Platform-held money
Threshold/AON
Project legal entity
Consumer relationship
Investment relationship
Payment role
Tax treatment
Personal-data flow
```

Không được kết luận bằng một nhãn chung `crowdfunding`.

## 4. Sản phẩm phải tạo

Mỗi người làm legal/compliance cho một pilot phải tạo:

1. `Actor and legal-role map`.
2. `Transaction classification matrix`.
3. `Money-flow map`.
4. `Contract relationship map`.
5. `Applicable-law register`.
6. `Licensing/registration checklist`.
7. `Consumer-rights checklist`.
8. `Privacy/data-flow map`.
9. `Tax/accounting question memo`.
10. `Open legal questions for counsel`.

## 5. Mẫu Applicable-law register

| ID | Hành vi | Actor | Bản chất | Văn bản | Điều/khoản | Mức chắc chắn | Legal question | Ngày kiểm tra |
|---|---|---|---|---|---|---|---|---|
| LAW-001 | Nhận pre-order | Project company | Sale | ... | ... | [PHÂN LOẠI] | ... | ... |
| LAW-002 | Giữ tiền chờ threshold | Platform | Holding/payment? | ... | ... | [VÙNG XÁM] | ... | ... |

Không ghi `theo luật Việt Nam` chung chung mà không có văn bản và điều/khoản.

## 6. Quy tắc nguồn

Thứ tự ưu tiên:

```text
Luật / Bộ luật
→ Nghị định
→ Quyết định / Thông tư nếu liên quan
→ CSDL quốc gia / website cơ quan quản lý
→ hướng dẫn chính thức
→ án lệ / quyết định / thực tiễn quản lý nếu cần
→ nguồn học thuật / law firm chỉ để diễn giải, không thay source gốc
```

Mỗi source phải lưu:

- số văn bản;
- ngày ban hành;
- ngày hiệu lực;
- cơ quan ban hành;
- tình trạng hiệu lực;
- điều khoản dùng;
- URL nguồn chính thức;
- ngày truy cập.

## 7. Stop rules

Dừng thiết kế và yêu cầu legal review nếu có:

- financial return;
- equity/debt/revenue share;
- platform giữ tiền của nhiều người;
- pooled allocation;
- investment recommendation/management;
- campaign xuyên biên giới;
- beneficiary trẻ em/health/sensitive data;
- thay đổi mục đích tiền sau khi nhận;
- creator không có chủ thể chịu nghĩa vụ rõ;
- terms muốn miễn toàn bộ trách nhiệm cho platform.

## 8. Definition of done

Người onboarding hoàn thành khi có thể nhìn một campaign và không hỏi trước:

> “Đây là loại crowdfunding gì?”

mà có thể lập ngay chuỗi:

```text
Actor
→ transaction
→ right/obligation
→ money/data flow
→ applicable law
→ legal uncertainty
→ control
→ evidence
```

> **Câu lõi:** Legal research tốt không phải tìm một điều luật để hợp thức hóa ý tưởng đã có; nó làm rõ cấu trúc giao dịch trước khi sản phẩm khóa chúng ta vào một kiến trúc sai.
