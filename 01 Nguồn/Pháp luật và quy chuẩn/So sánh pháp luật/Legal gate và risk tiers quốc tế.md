# Legal gate và risk tiers quốc tế

> Cập nhật: 10/08/2026.  
> Mục tiêu: tạo stop rules trước khi campaign xuyên biên giới được bật.  
> Không phải legal opinion.

## 1. Bốn mức rủi ro

### GREEN — non-financial, low regulatory complexity

Ví dụ:

- pure information/project collaboration;
- non-cash resource matching;
- genuine donation trong phạm vi cho phép;
- reward/pre-order đơn giản, không financial return;
- platform không giữ tiền.

Vẫn cần contract/consumer/payment/data/tax review phù hợp.

### YELLOW — regulated edges

Ví dụ:

- cross-border pre-order;
- refunds/escrow;
- sensitive KYC data;
- high-value contributions;
- charity/public-interest campaign;
- foreign currency/payment complexity;
- nominee/account structure.

Cần compliance review trước launch.

### ORANGE — financial-return / intermediary risk

Ví dụ:

- lending;
- revenue share;
- profit share;
- convertible right;
- equity to professional/accredited investors;
- platform arranging investments;
- cross-border private placement.

Cần jurisdiction-specific legal memo và regulated-partner architecture.

### RED — default block

- worldwide retail equity/debt;
- mainland China retail investment;
- platform-owned pool/client money;
- discretionary pooled investment allocation;
- unlicensed custody;
- public investment solicitation into a jurisdiction without route;
- unclear beneficial owner/source of funds;
- prohibited/sanctioned person/country transaction;
- attempt to disguise security as donation/membership/reward.

## 2. Gate sequence

```text
GATE 1 — Economic substance
→ contributor receives what?

GATE 2 — Actor roles
→ issuer / platform / intermediary / payment / custodian / manager?

GATE 3 — Jurisdictions
→ investor / issuer / platform / payment / data?

GATE 4 — Offering permission
→ prospectus / exemption / private placement / crowdfunding route?

GATE 5 — Intermediary licensing
→ who solicits/arranges/deals?

GATE 6 — Investor eligibility
→ retail/professional/accredited/sophisticated?

GATE 7 — Money
→ who receives, safeguards, releases and refunds?

GATE 8 — Custody / ownership
→ who legally/practically controls assets?

GATE 9 — AML / beneficial owner
→ identity, PEP, sanctions, source of funds, related parties?

GATE 10 — Data
→ collection, storage, transfer, retention?

GATE 11 — Vietnam inbound
→ FDI/FX/account/ownership/market access?

GATE 12 — Tax
→ instrument/source/withholding/treaty/substance?

GATE 13 — Exit/remittance
→ dividend, interest, sale, redemption, liquidation?

GATE 14 — Failure/wind-down
→ failed closing, refund, insolvency, fraud?
```

## 3. Required evidence by gate

| Gate | Evidence tối thiểu |
|---|---|
| Classification | written transaction classification |
| Jurisdiction | verified investor location/residence as legally relevant |
| Offering | counsel/regulatory memo + exemption conditions |
| Intermediary | license/registration/exemption evidence |
| Investor | eligibility evidence |
| Payment | partner contract + account/safeguarding flow |
| Custody | custody/ownership map + authorization |
| AML | CDD/UBO/PEP/sanctions/source-of-funds record |
| Data | data map + transfer mechanism |
| Vietnam FDI | corporate/investment/FX checklist and bank path |
| Tax | tax memo for instrument and parties |
| Exit | remittance/transfer workflow |
| Wind-down | failure and asset-return plan |

## 4. Stop conditions

### Stop immediately nếu economic label không khớp quyền

```text
“donation” nhưng có revenue share
“reward” nhưng có repayment + interest
“membership” nhưng có transferable profit right
```

### Stop nếu platform giữ tiền mà role chưa rõ

```text
money in platform account
→ payment/client-money/custody review
```

### Stop nếu marketing vượt jurisdiction policy

Một campaign approved cho Singapore professional investors không được tự động chạy ads global.

### Stop nếu investor jurisdiction không xác định

Không cho invest trước rồi KYC sau.

### Stop nếu SPV không có function

Không tạo SPV chỉ để bypass issuer eligibility, ownership limit hoặc tax treaty.

## 5. Country-specific hard gates

### Hoa Kỳ

- Vietnam issuer không dùng Reg CF trực tiếp như eligible U.S. issuer.
- retail financial-return campaign cần U.S. offering route.
- Reg CF money phải qua qualified third-party structure.

### EU

- retail investment/lending crowdfunding cần ECSPR/investment-services route phù hợp.
- payment/custody riêng.
- GDPR transfer riêng.

### UK

- financial promotion là gate trước cả transaction.
- client-money/payment safeguarding riêng.

### Singapore

- offering exemption không loại CMS licensing.
- PSA/payment riêng.

### Nhật Bản

- Japanese retail financial return → FIEA review.

### Mainland China

- retail investment → default block.
- securities + outbound FX + payment + data đều phải pass.

## 6. Risk score không thay legal conclusion

Có thể dùng score để prioritise review, nhưng không được dùng:

```text
Risk score thấp
→ tự kết luận legal
```

Một single prohibited activity có thể override toàn bộ score.

Do đó:

```text
hard gate > weighted score
```

## 7. Product states đề xuất

```text
DRAFT
RESEARCHING
COUNSEL REVIEW
PARTNER REVIEW
APPROVED NON-FINANCIAL
APPROVED PROFESSIONAL-ONLY
APPROVED JURISDICTION-LIMITED
BLOCKED
SUSPENDED
CLOSED
```

Không chỉ `published/unpublished`.

## 8. Câu lõi

> **Legal gate là cơ chế dừng sản phẩm trước khi một giao dịch đi sai đường; nó không phải checklist để hợp thức hóa giao dịch sau khi tiền đã nhận.**