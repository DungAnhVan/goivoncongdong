# Onboarding pháp luật quốc tế và FDI

> Mục tiêu: giúp thành viên mới phân tích một campaign có investor/người dùng/nguồn vốn nước ngoài mà không nhảy thẳng từ `quốc gia` sang `được phép/không được phép`.  
> Cập nhật: 10/08/2026.

## 1. Nguyên tắc đầu tiên

Không hỏi:

> “Nước X có cho crowdfunding không?”

Hỏi theo thứ tự:

```text
Investor ở đâu?
Issuer ở đâu?
Contributor nhận quyền gì?
Ai chào mời?
Ai nhận tiền?
Ai giữ tài sản?
Dữ liệu đi đâu?
Vốn đi vào Việt Nam bằng route nào?
Exit/remittance bằng route nào?
```

## 2. Lộ trình đọc 120 phút

### 0–15 phút — Bản đồ

1. [[Pháp luật quốc tế - Bản đồ crowdfunding và đầu tư xuyên biên giới]]
2. [[Ma trận quốc gia x hoạt động crowdfunding]]
3. [[Legal gate và risk tiers quốc tế]]

Kết quả:

- hiểu không có global crowdfunding license;
- biết investor jurisdiction có thể kéo mandatory law vào transaction.

### 15–45 phút — Các jurisdiction ưu tiên

Đọc nhanh:

1. [[Hoa Kỳ - Regulation Crowdfunding, securities và money flow]]
2. [[Liên minh Châu Âu - ECSPR, payments, AML và dữ liệu]]
3. [[Vương quốc Anh - crowdfunding, financial promotion và client money]]
4. [[Singapore - crowdfunding, CMS, payments và dữ liệu]]
5. [[Nhật Bản - crowdfunding, FIEA, payments và dữ liệu]]
6. [[Trung Quốc - crowdfunding, payments, capital controls và dữ liệu]]

Không học thuộc threshold. Học **regulatory architecture**.

### 45–65 phút — International standards

Đọc:

1. [[Chuẩn quốc tế - FATF, IOSCO, UNCITRAL, OECD và PFMI]]
2. [[KYC và AML]] nếu có
3. [[Beneficial owner]] nếu có

Mục tiêu:

- phân biệt binding law và soft law;
- hiểu AML/UBO/safeguarding là common design language.

### 65–90 phút — Vietnam connection

Đọc:

1. [[FDI và crowdfunding xuyên biên giới vào Việt Nam]]
2. [[Huy động vốn, đầu tư và chứng khoán]]
3. [[Thanh toán, giữ tiền và phòng chống rửa tiền]]
4. [[Thuế, hóa đơn và kế toán]]

Mục tiêu:

```text
home-jurisdiction permission
+
Vietnam inbound permission
```

đều phải pass.

### 90–120 phút — Architecture

1. [[Kiến trúc tuân thủ quốc tế cho nền tảng Việt Nam]]
2. [[Custody và safeguarding]]
3. [[Escrow]]
4. [[Campaign failure, recovery and termination]]
5. [[Khoảng trống pháp luật quốc tế cần nghiên cứu tiếp]]

## 3. Bài tập onboarding

Case:

> Một công ty Việt Nam muốn huy động 2 triệu USD. Website cho bất kỳ ai trên thế giới mua một quyền nhận 4% doanh thu trong 5 năm. Platform nhận USD vào tài khoản Singapore của chính platform, giữ đến khi đủ threshold, sau đó chuyển cho công ty Việt Nam. Có investor từ Mỹ, Đức, Anh, Singapore, Nhật và Trung Quốc. KYC được lưu chung ở server Việt Nam.

Người onboarding phải xác định ít nhất:

```text
Revenue-share = financial-return red flag
US investor gate
EU investor gate
UK financial-promotion gate
SG CMS/payment gate
Japan FIEA gate
China securities/FX/payment/data gate
Platform custody/client money
Singapore entity role
Vietnam FDI/FX route
Tax
Cross-border KYC data
Refund/failed closing
Exit/remittance
```

Không được kết luận:

> “Công ty Việt Nam nên mở một Singapore SPV là xong.”

## 4. Sản phẩm bắt buộc

1. `Jurisdiction map`.
2. `Actor-role map`.
3. `Instrument classification memo`.
4. `Country x activity matrix`.
5. `Offering/intermediary permission register`.
6. `Money-flow map`.
7. `Custody/ownership map`.
8. `AML/UBO/source-of-funds map`.
9. `Cross-border data map`.
10. `Vietnam FDI/FX closing checklist`.
11. `Tax and treaty question memo`.
12. `Exit/repatriation map`.
13. `Legal gate decision log`.
14. `Open questions for local counsel`.

## 5. Mẫu jurisdiction register

| Jurisdiction | Actor/user | Activity | Rule/source | Permission/exemption | Partner/license | Status | Counsel question |
|---|---|---|---|---|---|---|---|
| US | retail investor | revenue-share offer | Securities Act route | unresolved | unresolved | BLOCK | ... |
| SG | platform/PSP | receive/hold money | SFA/PSA | unresolved | ... | REVIEW | ... |

Status chỉ dùng:

```text
UNKNOWN
RESEARCHING
COUNSEL REVIEW
PARTNER REVIEW
ALLOWED WITH CONDITIONS
BLOCKED
```

Không dùng `probably okay`.

## 6. Money-flow exercise

Người onboarding phải vẽ từng account:

```text
Investor
→ Bank/PSP
→ Escrow/client-money account
→ Intermediary/SPV
→ Vietnam capital account
→ Issuer
→ Vendor
```

Với mỗi mũi tên ghi:

- legal basis;
- account owner;
- currency;
- instruction authority;
- AML actor;
- tax event;
- evidence;
- refund/reversal path.

## 7. Data-flow exercise

Không chỉ ghi `GDPR compliant`.

Phải vẽ:

```text
User device
→ KYC provider
→ regulated intermediary
→ platform
→ Vietnam database
→ analytics/vendor
→ archive/deletion
```

và xác định jurisdiction/legal basis ở từng transfer.

## 8. Stop rules

Dừng ngay nếu:

- worldwide retail financial return;
- investor jurisdiction unknown;
- platform giữ client money;
- pooled discretionary allocation;
- intermediary permission chưa rõ;
- nominee/custodian role chưa rõ;
- sanctions/UBO/source-of-funds unresolved;
- Vietnam capital-account route chưa rõ;
- mainland China retail investment;
- KYC data transfer chưa có legal basis;
- SPV chỉ được đề xuất vì “thuế thấp”.

## 9. Definition of done

Người onboarding hoàn thành khi nhìn một campaign quốc tế và có thể tạo chuỗi:

```text
Economic right
→ actor function
→ jurisdiction
→ mandatory rule
→ regulated partner
→ money/custody
→ AML/data
→ Vietnam inbound
→ tax
→ exit
→ failure path
```

## 10. Câu lõi

> **Cross-border legal design không phải chọn một nước “dễ” để đặt công ty; nó là việc ghép nhiều jurisdiction và regulated actors thành một đường giao dịch mà mỗi mắt xích đều có căn cứ.**