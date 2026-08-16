---
ai_authored: true
---

# Kiến trúc tuân thủ quốc tế cho nền tảng Việt Nam

> Cập nhật: 10/08/2026.  
> Mục tiêu: chuyển kết quả so sánh pháp luật thành kiến trúc sản phẩm và vận hành.  
> Không phải legal opinion.

## 1. Không xây một `global crowdfunding product`

Kiến trúc đúng hơn là:

> **jurisdiction-aware orchestration layer**.

Platform không giả định một campaign hợp pháp ở Việt Nam sẽ tự động hợp pháp với mọi investor trên thế giới.

## 2. Target architecture

```text
GLOBAL PLATFORM
   │
   ├─ Identity / KYC orchestration
   ├─ Campaign + disclosure records
   ├─ Evidence / audit ledger
   ├─ Jurisdiction policy engine
   ├─ Compliance / AML engine
   ├─ Data policy engine
   └─ Reconciliation
          │
          ↓
Jurisdiction gateway
   ├─ U.S. regulated route
   ├─ EU ECSPR / investment route
   ├─ UK FCA-compatible route
   ├─ Singapore MAS-compatible route
   ├─ Japan FIEA-compatible route
   └─ China route = blocked unless dedicated approval
          │
          ↓
Licensed payment / escrow
          ↓
Custodian if required
          ↓
Eligible issuer / genuine SPV
          ↓
Vietnam entity
```

## 3. Bốn money-flow models

### Model A — platform custody

```text
Investor
→ platform operating/omnibus account
→ project
```

**Không khuyến nghị.**

Rủi ro:

- payment licensing;
- client money/custody;
- AML concentration;
- insolvency;
- misappropriation;
- reconciliation;
- trust.

### Model B — external regulated escrow / PSP

```text
Investor
→ licensed bank / PSP / escrow
→ issuer/project khi conditions đạt

Platform
→ instruction + records
```

**Baseline khuyến nghị.**

Phù hợp nhất với philosophy từ U.S. Reg CF, EU/UK/Singapore safeguarding.

### Model C — direct to issuer

```text
Investor
→ regulated payment rail
→ issuer
```

Tốt cho non-investment/simple transaction, nhưng không giải quyết securities distribution.

### Model D — full regulated investment stack

```text
Investor
→ licensed securities/crowdfunding intermediary
→ escrow/payment actor
→ custodian/nominee if needed
→ eligible issuer/SPV
→ Vietnam OpCo
```

**Long-term investment architecture.**

## 4. Platform role boundary

Platform nên ưu tiên giữ các chức năng:

- project/campaign workflow;
- identity orchestration;
- evidence and verification records;
- disclosure versioning;
- matching;
- jurisdiction policy;
- compliance workflow;
- milestone/release instruction;
- reconciliation/reporting.

Không mặc định tự làm:

- deposit taking;
- money transmission;
- investment brokerage;
- custody;
- discretionary investment management;
- pooled fund allocation.

## 5. Jurisdiction-aware user account

Mỗi financial user phải có policy inputs:

```text
Residence
Nationality where relevant
Current location where relevant
Tax residence
Investor type
Entity type
Beneficial ownership
Sanctions/PEP status
```

Không chỉ `country` dropdown tự khai.

## 6. Campaign eligibility engine

Input:

```text
Contributor receives what?
Issuer jurisdiction?
Investor jurisdiction?
Is financial return present?
Platform function?
Money holder?
Custody actor?
Data destinations?
```

Output:

```text
ALLOW
ALLOW WITH CONDITIONS
COUNSEL REVIEW
BLOCK
```

## 7. Suggested rollout

### Phase A — non-investment

```text
donation / reward / genuine pre-order
→ external PSP
→ no investment return
→ clear consumer/refund/purpose rules
```

### Phase B — professional/private investment

```text
professional/accredited investors
→ jurisdiction-specific permitted route
→ licensed intermediary partner
→ escrow
→ Vietnam FDI/FX close
```

### Phase C — Singapore regional layer

Chỉ nếu SG entity có real function và regulatory architecture hợp lý.

### Phase D — retail by jurisdiction

```text
EU
U.S.
UK
Japan
```

mỗi nơi là một regulated product/module riêng.

### Mainland China retail

Separate project; default block.

## 8. Data architecture

Không copy mọi KYC document vào một database trung tâm mặc định.

Thiết kế:

```text
Data source jurisdiction
→ collection purpose
→ controller/processor
→ minimal fields
→ storage location
→ transfer basis
→ retention
→ deletion/rights
```

Có thể dùng token/reference to regulated KYC provider thay vì duplicate documents nếu pháp lý và technical design cho phép.

## 9. Money architecture

Hard rules:

1. Client/campaign money không vào operating treasury của platform.
2. Platform không được use/pledge/lend funds.
3. Release conditions machine-readable và versioned.
4. Refund path xác định trước.
5. Reconciliation độc lập với campaign UI.
6. Bank/PSP ledger là source of truth cho cash movement.
7. Evidence ID cho every release/refund.

Đọc cùng:

- [[Custody và safeguarding]]
- [[Escrow]]
- [[Disbursement]]
- [[Internal financial controls]]
- [[Refund and release mechanism]]

## 10. Investment architecture

Trước khi bật investment UI phải có:

```text
Instrument classification
Issuer eligibility
Offering route
Intermediary permission
Investor eligibility
Disclosure pack
Custody/ownership path
Payment path
AML
Tax
Vietnam FDI/FX
Exit path
```

## 11. Marketing architecture

Content cũng cần jurisdiction gate.

Một campaign có thể:

```text
visible globally as project information
```

nhưng investment terms/button chỉ hiển thị ở permitted jurisdictions/users.

Không dùng social media unrestricted cho financial promotion trước khi policy engine kiểm tra.

## 12. Failure architecture

Cross-border investment cần:

- campaign cancellation;
- failed closing;
- refund;
- platform insolvency;
- intermediary failure;
- PSP failure;
- issuer failure;
- fraud/integrity failure;
- sanctions freeze;
- data breach;
- wind-down.

Đọc cùng [[Campaign failure, recovery and termination]].

## 13. Partner architecture

Thay vì tự xin mọi license từ đầu:

```text
Platform
→ partner with licensed securities actors
→ partner with licensed payment/escrow actors
→ partner with custodian/nominee if needed
→ use local counsel by jurisdiction
```

Platform cạnh tranh ở **orchestration + evidence + project quality + multi-resource coordination**, không cần biến thành bank/broker/custodian cùng lúc.

## 14. Câu lõi

> **Mục tiêu không phải sở hữu tiền của đám đông; mục tiêu là điều phối đúng actor được phép để tiền, quyền đầu tư, dữ liệu và bằng chứng đi qua đúng kênh.**