---
ai_authored: true
---

# Liên minh Châu Âu - ECSPR, payments, AML và dữ liệu

> Cập nhật nghiên cứu: 10/08/2026.  
> Trọng tâm: investment/lending crowdfunding, payment safeguarding, custody, retail investor protection, AML và cross-border data.  
> Không phải legal opinion.

## 1. ECSPR là khung crowdfunding chuyên biệt

Regulation (EU) 2020/1503 — European Crowdfunding Service Providers Regulation (`ECSPR`) tạo khung thống nhất cho **investment-based và lending-based crowdfunding cho business**.

Nguồn:

- EUR-Lex ECSPR: https://eur-lex.europa.eu/eli/reg/2020/1503/oj/eng
- ESMA Investment Services and Crowdfunding: https://www.esma.europa.eu/esmas-activities/investors-and-issuers/investment-services-and-crowdfunding

ECSPR không phải luật chung cho mọi crowdfunding.

```text
Donation / reward / ordinary pre-order
→ thường nằm ngoài ECSPR
→ nhưng vẫn chịu consumer, contract, e-commerce, payment, charity và tax rules liên quan
```

## 2. Passporting chỉ là nội bộ EU

Một ECSP được authorization phù hợp có thể dùng cơ chế cross-border trong thị trường EU theo ECSPR.

Nhưng:

```text
EU passport
≠
passport vào Việt Nam

Vietnam platform
≠
tự được EU passport chỉ vì có user EU
```

Nếu regulated crowdfunding service được cung cấp cho EU market, cần EU authorization/third-country analysis phù hợp.

## 3. Payment là lớp riêng

Crowdfunding authorization không tự động cấp quyền làm payment institution.

Payment services hiện được neo vào PSD2 và các quy định triển khai.

Nguồn:

- PSD2: https://eur-lex.europa.eu/eli/dir/2015/2366/oj/eng
- EBA safeguarding Q&A: https://www.eba.europa.eu/single-rule-book-qa/qna/view/publicId/2020_5264

Điểm kiến trúc:

```text
Crowdfunding provider
≠
Payment institution
≠
Custodian
```

Nếu money flow cần giữ tiền investor, dùng licensed payment/banking actor và safeguarding structure phù hợp.

## 4. Custody cũng là lớp riêng

Việc nắm giữ financial instruments hoặc quyền kiểm soát tài sản có thể cần một appropriately authorized entity.

Đổi tên thành `nominee` không tự loại bỏ custody analysis.

```text
Nominee label
≠
unregulated custody permission
```

Đối với dự án, cần hỏi:

- ai là legal owner trên register?
- ai có quyền chuyển nhượng?
- ai có authority để withdraw/transfer?
- tài sản tách khỏi insolvency estate thế nào?

## 5. Retail investor protection

ECSPR thể hiện triết lý bảo vệ nhà đầu tư bằng nhiều lớp chứ không chỉ disclosure:

- phân biệt sophisticated và non-sophisticated investors;
- standardized investor information;
- risk warnings;
- knowledge/appropriateness-related protections;
- cooling-off/reflection protections trong phạm vi áp dụng;
- conflict-of-interest controls.

Điểm học cho platform:

> Investment UI phải có legal friction theo mức rủi ro; checkbox `I agree` không đủ để thay thế investor-protection architecture.

## 6. Data — GDPR là gate độc lập

GDPR có territorial reach ngoài EU trong một số trường hợp khi tổ chức ở nước ngoài offer goods/services hoặc monitor individuals trong EU.

Nguồn:
https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng

Cross-border transfer sang Việt Nam là câu hỏi riêng:

```text
EU investor KYC
→ collected lawfully?
→ controller/processor roles?
→ transfer basis?
→ SCC/BCR/other safeguard nếu cần?
→ retention?
→ data subject rights?
```

Một transaction hợp pháp về securities không chữa được data-transfer non-compliance.

## 7. AML đang chuyển sang khung mới

Regulation (EU) 2024/1624 là thành phần quan trọng của EU AML package và nhìn chung bắt đầu áp dụng từ 10/07/2027 theo lộ trình của Regulation.

Nguồn:
https://eur-lex.europa.eu/eli/reg/2024/1624/oj/eng

Vì nghiên cứu tại 10/08/2026, phải phân biệt:

```text
Current law in force
vs
rules adopted but not yet generally applicable
```

Không viết như thể toàn bộ AMLR đã áp dụng đầy đủ từ 2026.

## 8. Thuế

EU không có một income-tax code duy nhất cho crowdfunding.

Phải xác định:

```text
Member State of investor
Member State / country of issuer
Instrument
Income source
Withholding
Treaty
Beneficial owner
SPV substance
```

Nếu dùng EU SPV/holding vehicle, cần tax and treaty analysis riêng; `EU company` không phải lời giải thuế.

## 9. Áp vào platform Việt Nam

### Reward/pre-order vào EU

Cần:

- consumer/e-commerce terms;
- payment provider;
- refund/withdrawal analysis;
- GDPR/data-transfer architecture;
- VAT/tax analysis tùy transaction.

### Equity/lending vào EU retail

Mặc định:

```text
EU retail financial return
→ ECSPR / investment-services legal gate
→ regulated EU pathway
→ payment/custody pathway
→ data pathway
```

Không mở bằng website Việt Nam unrestricted.

## 10. Kiến trúc tham chiếu

```text
EU investor
  ↓
EU-authorized crowdfunding / investment actor
  ↓
EU licensed PSP / bank
  ↓
Custodian nếu instrument cần
  ↓
Eligible issuer / SPV
  ↓
Vietnam entity theo FDI/FX rules
```

Platform Việt Nam có thể là technology/orchestration layer nếu hợp đồng và operational reality đúng với vai trò đó.

## 11. Red flags

- EU retail offer nhưng không có EU regulatory route;
- platform Việt Nam tự collect investor money;
- gọi nominee nhưng platform vẫn có practical control;
- KYC docs của EU users được copy về Việt Nam không có data-transfer basis;
- SPV chỉ là shell để lấy treaty benefits;
- marketing cross-border không kiểm soát jurisdiction.

## 12. Câu lõi

> **EU cho thấy crowdfunding authorization, payment safeguarding, custody và data protection phải được thiết kế như các module độc lập; một license không tự bao trùm toàn bộ stack.**