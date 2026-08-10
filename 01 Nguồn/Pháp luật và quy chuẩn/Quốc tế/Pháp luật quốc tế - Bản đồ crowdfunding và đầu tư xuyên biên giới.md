# Pháp luật quốc tế - Bản đồ crowdfunding và đầu tư xuyên biên giới

> Cập nhật nghiên cứu: 10/08/2026.  
> Phạm vi đã nghiên cứu sâu: Hoa Kỳ, Liên minh Châu Âu, Vương quốc Anh, Singapore, Nhật Bản, Trung Quốc và các chuẩn quốc tế liên quan.  
> Đây là bản đồ nghiên cứu pháp lý, không phải legal opinion cho một giao dịch cụ thể.

## 1. Nguyên tắc gốc

Không tồn tại một `luật crowdfunding quốc tế` duy nhất.

Một chiến dịch xuyên biên giới phải được phân loại theo **bản chất giao dịch** và **vai trò của từng actor**:

```text
Donation
Reward
Pre-order
Lending
Equity
Revenue / profit share
Tokenized right
Managed pool
```

Sau đó tách tiếp các chức năng:

```text
Issuance
→ ai phát hành quyền?

Distribution / solicitation
→ ai giới thiệu, môi giới, sắp xếp hoặc chào mời?

Payment
→ ai nhận và chuyển tiền?

Custody / client money
→ ai kiểm soát tài sản trong thời gian chờ?

Management
→ ai quyết định vốn của nhiều người được phân bổ vào đâu?
```

Một website có thể vô tình thực hiện cả năm chức năng trên. Đây là kiến trúc cần tránh.

## 2. Quy tắc xuyên biên giới

Không nên suy luận:

> Công ty ở Việt Nam → chỉ cần tuân luật Việt Nam.

Trong tài chính số, nhiều nước quan tâm đến **nơi nhà đầu tư/người tiêu dùng đang ở**, **nơi hoạt động chào mời hướng đến**, **nơi tiền đi qua**, **nơi dữ liệu được thu và chuyển**, chứ không chỉ nơi platform đăng ký pháp nhân.

Vì vậy phải lập ít nhất sáu bản đồ:

```text
Issuer jurisdiction
Investor jurisdiction
Platform jurisdiction
Money path
Securities / ownership path
Data path
```

và thêm:

```text
Tax residence
FX / capital controls
Exit / repatriation path
```

## 3. Mẫu hình chung từ các nước đã nghiên cứu

Mẫu hình nổi bật nhất là sự **tách chức năng**:

> Platform chỉ cung cấp công nghệ và điều phối dễ bảo vệ hơn platform vừa môi giới đầu tư, vừa giữ tiền, vừa giữ chứng khoán, vừa quyết định phân bổ vốn.

Hoa Kỳ, EU, UK và Singapore đều cho thấy hoạt động đầu tư, thanh toán và custody có thể nằm trong các chế độ cấp phép khác nhau.

Kiến trúc tham chiếu:

```text
Investor
   ↓
Jurisdiction-specific investment gateway
   ↓
Licensed securities / crowdfunding intermediary
   ↓
Licensed bank / PSP / escrow
   ↓
Custodian / nominee nếu cần
   ↓
Eligible issuer / SPV
   ↓
Vietnam project / operating company

Platform technology:
identity + campaign + disclosure + records + reconciliation
```

## 4. Phân loại nhanh theo mô hình

| Mô hình | Lớp pháp lý chính |
|---|---|
| Donation | fundraising/charity tùy nước, AML, fraud, payments, tax |
| Reward | contract, consumer, e-commerce, payments, tax |
| Pre-order | sale/consumer/e-commerce, refund, payments, tax |
| Lending | lending/credit, securities tùy cấu trúc, crowdfunding rules, AML |
| Equity | securities, offering, intermediary licensing, custody |
| Revenue/profit share | thường cần securities/collective-investment analysis |
| Managed pool | fund/CIS/investment management + securities + custody |
| Tokenized | underlying legal category + digital-asset law |

## 5. Các vùng tài phán đã có note riêng

- [[Hoa Kỳ - Regulation Crowdfunding, securities và money flow]]
- [[Liên minh Châu Âu - ECSPR, payments, AML và dữ liệu]]
- [[Vương quốc Anh - crowdfunding, financial promotion và client money]]
- [[Singapore - crowdfunding, CMS, payments và dữ liệu]]
- [[Nhật Bản - crowdfunding, FIEA, payments và dữ liệu]]
- [[Trung Quốc - crowdfunding, payments, capital controls và dữ liệu]]
- [[Chuẩn quốc tế - FATF, IOSCO, UNCITRAL, OECD và PFMI]]

## 6. Các note so sánh cần đọc cùng

- [[Ma trận quốc gia x hoạt động crowdfunding]]
- [[FDI và crowdfunding xuyên biên giới vào Việt Nam]]
- [[Kiến trúc tuân thủ quốc tế cho nền tảng Việt Nam]]
- [[Legal gate và risk tiers quốc tế]]
- [[Khoảng trống pháp luật quốc tế cần nghiên cứu tiếp]]

## 7. Hard rules đề xuất cho dự án

### Rule 1 — Không mở worldwide retail investment mặc định

Một campaign có equity, debt, interest, revenue share hoặc profit share phải bị khóa theo jurisdiction.

### Rule 2 — Không dùng tài khoản vận hành của platform để giữ tiền campaign

Ưu tiên:

```text
regulated bank / PSP / escrow
```

Platform chỉ có quyền instruction trong phạm vi được thiết kế, không có quyền dùng tiền cho payroll, cho vay, cầm cố hoặc trộn với corporate cash.

### Rule 3 — Prospectus exemption không đồng nghĩa platform licensing exemption

Ví dụ một đợt chào bán được miễn prospectus vẫn có thể yêu cầu intermediary thực hiện hoạt động phải được cấp phép.

### Rule 4 — No custody ≠ no securities regulation

Tiền đi thẳng investor → issuer không tự loại bỏ quy định về solicitation, arranging, dealing hoặc financial promotion.

### Rule 5 — Data là legal gate độc lập

Một giao dịch đầu tư hợp pháp không đồng nghĩa việc đưa KYC documents từ EU, Nhật, Singapore hay Trung Quốc về database Việt Nam là hợp pháp.

### Rule 6 — Choice of law không loại bỏ mandatory law

Điều khoản `governed by Vietnamese law` không thể tự động vô hiệu hóa luật chứng khoán, AML, consumer, tax, data hoặc financial-promotion bắt buộc của nước nhà đầu tư.

## 8. Source hierarchy

Ưu tiên:

```text
Statute / regulation
→ regulator / central bank
→ official legal database
→ international standard setter
→ official tax authority
→ academic / law-firm commentary chỉ để diễn giải
```

Các nguồn lõi:

- SEC Regulation Crowdfunding: https://www.sec.gov/resources-small-businesses/exempt-offerings/regulation-crowdfunding
- EU ECSPR: https://eur-lex.europa.eu/eli/reg/2020/1503/oj/eng
- FCA crowdfunding: https://www.fca.org.uk/investsmart/understanding-crowdfunding
- MAS CMS licensing: https://www.mas.gov.sg/regulation/capital-markets/apply-for-licensing-or-registration-of-capital-market-entities/cms-licence
- JFSA crowdfunding classification: https://www.fsa.go.jp/en/news/2018/20180717.html
- FATF Recommendations: https://www.fatf-gafi.org/en/topics/fatf-recommendations.html

## 9. Câu lõi

> **Không hỏi “crowdfunding quốc tế có hợp pháp không?”. Hỏi: actor nào đang làm chức năng gì, với loại quyền nào, hướng đến người ở đâu, tiền đi qua ai, tài sản do ai giữ, dữ liệu đi đâu và khi exit thì vốn được chuyển về bằng con đường pháp lý nào.**