---
ai_authored: true
---

# Ma trận quốc gia x hoạt động crowdfunding

> Cập nhật: 10/08/2026.  
> Ma trận định hướng nghiên cứu, không thay thế legal opinion theo facts cụ thể.

## 1. Ma trận lõi

| Jurisdiction | Investment/equity | Lending/P2P | Reward/donation/pre-order | Platform giữ tiền | Data cross-border | Đánh giá sơ bộ cho Vietnam platform |
|---|---|---|---|---|---|---|
| Hoa Kỳ | Reg CF/other Securities Act routes; issuer/intermediary limits | securities/credit/MSB tùy structure | thường ngoài securities nếu thật sự non-investment | Reg CF funding portal dùng qualified third party | federal/state sectoral review | U.S. retail investment = high gate |
| EU | ECSPR cho investment/lending business crowdfunding | ECSPR | ngoài ECSPR nhưng consumer/e-commerce/payment vẫn áp dụng | payment/custody authorization riêng | GDPR Chapter V | retail investment cần EU regulated pathway |
| UK | FCA-regulated investment crowdfunding | FCA/Article 36H environment | thường ngoài investment regime nếu non-financial | CASS/payment safeguarding tùy perimeter | UK data rules | financial promotion là gate mạnh |
| Singapore | SFA/CMS + offering exemption analysis | capital-markets analysis | contract/consumer/payment | PSA + safeguarding; custody riêng | PDPA transfer limitation | ứng viên tốt cho regional/private hub |
| Nhật Bản | FIEA / FIB registration route | structure-dependent | JFSA phân biệt donation/purchasing | Payment Services Act + custody review | APPI | Japanese retail investment = legal review |
| Mainland China | public/private securities fundraising bị kiểm soát chặt | P2P history rất restrictive | e-commerce/payment/consumer | fund pools/payment licensing là red flag | PIPL/CAC cross-border rules | retail investment = RED ZONE |

## 2. Theo chức năng platform

| Function | US | EU | UK | SG | JP | CN |
|---|---|---|---|---|---|---|
| Listing information only | thấp hơn nhưng vẫn phải xem marketing/fraud | thấp hơn | financial-promotion risk nếu investment | thấp hơn | thấp hơn | solicitation risk |
| Arrange investment | regulated gate | ECSPR/MiFID perimeter | FCA perimeter | CMS perimeter | FIEA perimeter | securities/private fundraising gate |
| Receive/transmit money | MSB/state/payment analysis | PSD2/payment | payment/CASS | PSA | Payment Services Act | non-bank payment rules |
| Hold client assets | custody/client-money analysis | custody authorization | CASS/custody | custody/securities permissions | custody review | high risk |
| Allocate pooled capital | fund/adviser/CIS analysis | AIF/CIS/investment management analysis | fund management/CIS | fund management/CMS analysis | fund/investment management | very high risk |

## 3. Theo loại campaign

### Donation

Không nên mặc định `không regulated`.

Check:

```text
fundraising/charity rules
fraud/misrepresentation
AML/payment
tax
consumer where benefits promised
```

### Reward / pre-order

Check:

```text
sale/consumer contract
refund/withdrawal
e-commerce/marketing
payment
tax
product regulation
data
```

### Lending

Check:

```text
credit/lending
securities depending instrument
intermediary/platform licensing
AML
payment/client money
collections/default
```

### Equity

Check:

```text
issuer eligibility
offering exemption/prospectus
intermediary licensing
investor class
custody/ownership
secondary transfer
AML
payment
FDI/FX
```

### Revenue/profit share

Mặc định treat as **financial-return red flag** cho đến khi counsel phân loại.

### Managed pool

Mặc định `highest risk` vì platform có thể trở thành investment manager/fund/CIS operator.

## 4. Investor-location policy sơ bộ

```text
US retail financial return
→ BLOCK unless approved U.S. route

EU retail financial return
→ EU-authorized pathway

UK retail financial return
→ FCA + financial-promotion route

Singapore retail financial return
→ SFA/CMS route

Japan retail financial return
→ FIEA route

Mainland China retail financial return
→ BLOCK; dedicated PRC opinion required
```

## 5. Money flow scorecard

Legend:

```text
✓ structurally favorable
△ possible but regulated/conditional
✕ poor default architecture
```

| Framework | Platform custody | External escrow/PSP | Direct-to-issuer | Full regulated stack |
|---|:---:|:---:|:---:|:---:|
| U.S. securities crowdfunding | ✕ | ✓ | △ | ✓ |
| EU ECSPR | ✕/△ | ✓ | △ | ✓ |
| UK | △ | ✓ | △ | ✓ |
| Singapore | △ | ✓ | △ | ✓ |
| Japan | △ | ✓ | △ | ✓ |
| Mainland China retail investment | ✕ | △ | △ | △ only after dedicated review |

## 6. Điểm hội tụ quốc tế

Các jurisdiction khác nhau về ngưỡng và hình thức, nhưng cùng hội tụ ở các nguyên tắc:

1. Investment-like return kéo activity vào financial regulation.
2. Platform/intermediary không chỉ là website trung lập khi tham gia arranging/distribution.
3. Client money cần segregation/safeguarding và regulated actor phù hợp.
4. Custody là chức năng riêng.
5. Investor classification và disclosure quan trọng.
6. AML/KYC/beneficial owner là lớp bắt buộc khi financial perimeter tăng.
7. Cross-border data là gate riêng.
8. Marketing jurisdiction có thể quan trọng như incorporation jurisdiction.

## 7. Điểm không được đơn giản hóa

```text
One country license
≠ global license

One payment provider
≠ global investment permission

One SPV
≠ treaty/FDI solution

Accredited investor
≠ no AML/no securities law

No custody
≠ no intermediary regulation
```

## 8. Liên kết

- [[Pháp luật quốc tế - Bản đồ crowdfunding và đầu tư xuyên biên giới]]
- [[FDI và crowdfunding xuyên biên giới vào Việt Nam]]
- [[Kiến trúc tuân thủ quốc tế cho nền tảng Việt Nam]]
- [[Legal gate và risk tiers quốc tế]]

## 9. Câu lõi

> **Jurisdiction policy phải được quyết định từ loại quyền + investor location + platform function, không chỉ từ nơi công ty đăng ký.**