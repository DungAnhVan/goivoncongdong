---
ai_authored: true
---

# Singapore - crowdfunding, CMS, payments và dữ liệu

> Cập nhật nghiên cứu: 10/08/2026.  
> Trọng tâm: securities/lending crowdfunding, Capital Markets Services licensing, offering exemptions, payment safeguarding, AML, data transfer và vai trò Singapore như regional hub.  
> Không phải legal opinion.

## 1. Vì sao Singapore quan trọng với dự án

Singapore thường là một trong các nguồn FDI lớn vào Việt Nam và là trung tâm vốn/tài chính quan trọng trong khu vực. Vì vậy nó có thể là jurisdiction thực tế cho:

- investor onboarding;
- regional holding/SPV;
- securities intermediary;
- payment/escrow;
- governance;
- private/accredited fundraising.

Nhưng:

> Singapore không phải “nơi đặt công ty để thoát luật Việt Nam và luật nước nhà đầu tư”.

## 2. Securities and Futures Act + CMS licensing

MAS quản lý regulated capital-markets activities theo Securities and Futures Act (`SFA`).

Nguồn:
https://www.mas.gov.sg/regulation/capital-markets/apply-for-licensing-or-registration-of-capital-market-entities/cms-licence

Nguyên tắc:

```text
Conduct regulated SFA activity
→ CMS licence unless exemption applies
```

Crowdfunding có equity hoặc lending có thể chạm trực tiếp vào capital-markets regulation.

## 3. Offering exemption ≠ intermediary exemption

Singapore có các prospectus exemptions thường được dùng trong startup/private fundraising, gồm small-offer, private-placement và accredited-investor pathways trong điều kiện luật định.

MAS đã từng hướng dẫn crowdfunding và prospectus exemptions, trong đó small-offer route có ngưỡng S$5m/12 tháng và private-placement route có giới hạn số người theo điều kiện áp dụng.

Nguồn:

- MAS lending-based crowdfunding FAQs: https://www.mas.gov.sg/regulation/faqs/faqs-on-lending-based-crowdfunding
- MAS securities crowdfunding materials: https://www.mas.gov.sg/news/media-releases/2016/mas-to-improve-access-to-crowdfunding-for-startups-and-smes

Hard rule:

> **Miễn prospectus không đồng nghĩa bất kỳ website nào cũng được môi giới/chào mời mà không cần xem xét licensing.**

## 4. Payment Services Act là lớp riêng

Payment activity chịu Payment Services Act (`PSA`) và MAS requirements.

Nguồn:

- PSA: https://sso.agc.gov.sg/Act/PSA2019
- MAS payment provider ongoing requirements: https://www.mas.gov.sg/regulation/payments/ongoing-requirements-for-payment-service-providers

Major payment institutions có safeguarding obligations trong phạm vi áp dụng.

Kiến trúc cần tách:

```text
CMS / securities intermediary
≠
payment institution
≠
custodian
```

## 5. AML/KYC

MAS AML notices cho regulated payment services yêu cầu risk-based controls, CDD và các biện pháp liên quan.

Nguồn:
https://www.mas.gov.sg/regulation/notices/psn01-aml-cft-notice---specified-payment-services

Cho dự án, Singapore layer không chỉ là KYC form. Cần:

```text
identity
beneficial owner
PEP/sanctions
source-of-funds risk
transaction monitoring
project/recipient due diligence
records
escalation
```

## 6. Data transfer

PDPA có Transfer Limitation Obligation đối với overseas transfers.

Nguồn:
https://www.pdpc.gov.sg/organisations/resources/guidance-by-topic/guide-to-cross-border-data-transfers

Nếu SG intermediary thu KYC rồi đồng bộ về Việt Nam:

```text
Singapore data controller/organization
→ overseas transfer to Vietnam
→ protection requirement
→ contractual/organizational controls
```

Không được xem API sync là chuyện technical thuần túy.

## 7. Tax

IRAS xác nhận Singapore hiện không áp withholding tax trên dividends, nhưng một số khoản như interest và specified payments có thể phát sinh withholding tùy circumstances.

Nguồn:

- https://www.iras.gov.sg/taxes/withholding-tax/payments-to-non-resident-company/payments-that-are-not-subject-to-withholding-tax
- https://www.iras.gov.sg/taxes/withholding-tax/payments-to-non-resident-company/payments-that-are-subject-to-withholding-tax

Một Singapore HoldCo/SPV vẫn phải phân tích:

```text
substance
corporate residence
beneficial ownership
treaty anti-abuse
transfer pricing
Vietnam withholding/FDI
investor residence taxation
```

## 8. Singapore regional hub — khi nào có ý nghĩa

Cấu trúc có thể hợp lý nếu entity Singapore có **real function**, ví dụ:

- regional governance;
- contracting;
- regulated intermediary relationship;
- treasury;
- holding company;
- fundraising;
- IP/regional management.

Không nên tạo shell chỉ để đi vòng luật hoặc treaty shopping.

## 9. Kiến trúc tham chiếu

```text
Foreign / ASEAN investor
   ↓
Singapore licensed intermediary nếu regulated activity
   ↓
Singapore licensed PSP / bank / escrow
   ↓
SG issuer / genuine HoldCo / direct Vietnam route
   ↓
Vietnam OpCo / project entity
```

Platform technology có thể giữ:

```text
campaign UI
identity orchestration
records
disclosure
policy engine
reconciliation
```

nhưng không tự động nhận quyền custody/payment/securities intermediation.

## 10. Giai đoạn triển khai hợp lý

### Phase đầu

Professional/accredited/private capital qua regulated partners phù hợp thường thực tế hơn worldwide retail.

### Retail sau

Chỉ mở khi đã xác định rõ:

- issuer;
- offering route;
- intermediary permission;
- payment/custody;
- disclosure;
- investor class;
- data;
- Vietnam FDI/FX path.

## 11. Red flags

- quảng bá exemption như “không cần license”;
- platform Singapore entity chỉ là paper conduit;
- nhận investor money vào operating account;
- pooling rồi platform tự chọn project;
- đưa KYC về Việt Nam không có PDPA transfer design;
- không xác định repatriation/exit path về sau.

## 12. Câu lõi

> **Singapore là ứng viên mạnh cho regional capital infrastructure, nhưng giá trị nằm ở regulated actors, governance và real substance — không phải ở việc đăng ký một công ty Singapore rồi coi mọi giao dịch xuyên biên giới là hợp pháp.**