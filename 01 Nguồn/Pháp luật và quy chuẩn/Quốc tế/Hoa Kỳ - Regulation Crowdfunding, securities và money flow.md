# Hoa Kỳ - Regulation Crowdfunding, securities và money flow

> Cập nhật nghiên cứu: 10/08/2026.  
> Trọng tâm: securities crowdfunding, intermediary, investor money, cross-border solicitation và tax.  
> Không phải legal opinion.

## 1. Khung chính

Crowdfunding có yếu tố đầu tư tại Hoa Kỳ nằm trong khung chứng khoán liên bang. `Regulation Crowdfunding (Reg CF)` là một exemption cho phép doanh nghiệp đủ điều kiện huy động vốn từ nhà đầu tư thông qua một intermediary được quản lý.

Nguồn chính thức:

- SEC Regulation Crowdfunding: https://www.sec.gov/resources-small-businesses/exempt-offerings/regulation-crowdfunding
- SEC Small Entity Compliance Guide: https://www.sec.gov/resources-small-businesses/small-business-compliance-guides/regulation-crowdfunding-small-entity-compliance-guide-issuers
- SEC Funding Portal FAQs: https://www.sec.gov/rules-regulations/staff-guidance/trading-markets-frequently-asked-questions/cfportal-faqs
- FINRA Funding Portals: https://www.finra.org/about/entities-we-regulate/funding-portals-we-regulate

## 2. Điểm rất quan trọng với dự án Việt Nam

### Doanh nghiệp Việt Nam không mặc nhiên dùng được Reg CF

Theo SEC, Reg CF chỉ dành cho issuer đủ điều kiện và non-U.S. companies không phải issuer đủ điều kiện theo route này.

Vì vậy:

```text
Vietnamese issuer
≠
đăng lên một U.S. funding portal rồi dùng Reg CF
```

Nếu muốn tiếp cận nhà đầu tư Hoa Kỳ phải phân tích route khác, ví dụ các exemption khác của Securities Act hoặc cấu trúc issuer khác thực sự đủ điều kiện.

SEC overview các offering pathways:
https://www.sec.gov/resources-small-businesses/capital-raising-building-blocks/offering-pathways

## 3. Intermediary là legal gate

Reg CF phải được thực hiện qua **một broker-dealer hoặc funding portal đã đăng ký với SEC**, và funding portal còn chịu FINRA oversight.

Điểm cần học cho kiến trúc platform:

> Securities crowdfunding không được xem như một website listing tự do.

Intermediary có gatekeeping, disclosure, recordkeeping và investor-protection duties.

## 4. Money flow — bài học mạnh nhất

SEC Funding Portal FAQ cho thấy funding portal phải hướng investor gửi tiền trực tiếp đến **qualified third party** phù hợp; funding portal không nên tự giữ tiền đầu tư trong operating account.

Mô hình:

```text
Investor
  ↓
Qualified bank / broker / eligible third party
  ↓
release khi closing conditions đạt
  ↓
Issuer

Funding portal
  └─ instruction + records
```

Đây là benchmark quan trọng cho dự án:

```text
platform-owned omnibus treasury account
→ RED FLAG
```

## 5. No custody không loại bỏ securities law

Ngay cả khi investor trả thẳng issuer, platform vẫn có thể thực hiện các hành vi liên quan đến securities distribution/arranging/solicitation.

Do đó:

```text
Direct-to-issuer payment
≠
platform chắc chắn không bị regulation
```

Phải tách payment role và securities role.

## 6. Cross-border solicitation

Không nên suy luận rằng issuer ở Việt Nam thì U.S. law không liên quan. Nếu offer được hướng đến U.S. persons hoặc U.S. retail investors, cần Securities Act analysis.

Cho giai đoạn đầu, route an toàn về kiến trúc là:

```text
US retail investment campaign
→ BLOCK mặc định
→ chỉ mở khi có U.S.-specific legal route
```

Có thể nghiên cứu riêng các exemption như Regulation D / Regulation S tùy cấu trúc, nhưng không được dùng tên exemption như kết luận trước khi kiểm tra điều kiện cụ thể.

## 7. Investor protection trong Reg CF

Các cơ chế gồm:

- Form C disclosures;
- financial information theo quy mô/circumstances;
- investor limits đối với nhóm nhất định;
- one-platform rule;
- intermediary gatekeeping;
- restrictions on certain advertising/communications;
- resale restrictions trong thời gian nhất định;
- continuing reporting trong trường hợp áp dụng.

Điểm thiết kế cần học:

> High-risk retail finance cần disclosure + friction + gatekeeping, không chỉ Terms of Service.

## 8. AML và money transmission

Nếu platform ngoài securities role còn **accepts and transmits funds**, có thể phát sinh phân tích Bank Secrecy Act / FinCEN money-services-business và state money-transmitter law.

Nguồn:

- FinCEN MSB fact sheet: https://www.fincen.gov/fact-sheet-msb-registration-rule
- FinCEN administrative ruling về money transmission: https://www.fincen.gov/resources/statutes-regulations/administrative-rulings/application-money-services-business
- FinCEN crowdfunding risk advisory: https://www.fincen.gov/resources/advisories/fincen-advisory-fin-2017-a007-0

Không dùng một kết luận MSB chung cho mọi payment processor; classification phụ thuộc facts và exemptions.

## 9. Tax

IRS nêu nguyên tắc chung: một số U.S.-source FDAP income trả cho foreign persons thường chịu withholding 30% trừ khi có exemption/treaty reduction; ECI có framework khác.

Nguồn:
https://www.irs.gov/individuals/international-taxpayers/withholding-on-specific-income

Điểm quan trọng:

```text
Equity subscription
Dividend
Interest
Platform fee
Capital gain
```

là các dòng tiền khác nhau, không có một `U.S. crowdfunding tax rate` duy nhất.

## 10. Risk classification cho dự án

### Lower risk

- reward/pre-order thật sự;
- không financial return;
- platform không giữ tiền;
- không marketing như investment.

Vẫn cần consumer/payment/tax review.

### High risk

- equity/debt/revenue share cho U.S. retail;
- public solicitation;
- platform nhận tiền rồi chuyển cho issuer;
- platform lựa chọn hoặc khuyến nghị investment;
- nominee/custody không có regulated structure.

## 11. Rule đề xuất

```text
US investor detected
  ↓
Is financial return involved?
  ├─ No → consumer/payment/privacy review
  └─ Yes
       ↓
     U.S. securities gate
       ↓
     approved exemption + intermediary + money path
       ↓
     only then permit investment UI
```

## 12. Câu lõi

> **Hoa Kỳ cho thấy rõ nhất rằng securities crowdfunding là một regulated distribution process với intermediary và money-handling rules, không phải chỉ là một website nơi startup đăng dự án và nhận tiền.**