# Vương quốc Anh - crowdfunding, financial promotion và client money

> Cập nhật nghiên cứu: 10/08/2026.  
> Trọng tâm: regulated crowdfunding, financial promotion, client money, payment safeguarding và offshore marketing.  
> Không phải legal opinion.

## 1. Khung chung

FCA phân biệt các hình thức crowdfunding có yếu tố tài chính như loan-based/P2P và investment-based crowdfunding khỏi donation/reward models thuần túy.

Nguồn:

- FCA Understanding Crowdfunding: https://www.fca.org.uk/investsmart/understanding-crowdfunding
- FCA Consumer Investments authorisation: https://www.fca.org.uk/firms/authorisation/consumer-investments

Donation/reward không mặc nhiên nằm trong investment-crowdfunding regime, nhưng payment, consumer, charity hoặc financial-promotion rules khác vẫn có thể áp dụng tùy cấu trúc.

## 2. Lending / P2P

Operating an electronic system in relation to lending có thể rơi vào regulated activity, điển hình Article 36H framework.

Nguồn:
https://www.legislation.gov.uk/uksi/2001/544/article/36H

Không nên dùng câu:

> “Platform chỉ kết nối borrower và lender nên không phải financial business.”

Phải phân tích activity thực tế.

## 3. Investment-based crowdfunding

Nếu platform sắp xếp, giới thiệu hoặc tạo điều kiện mua investment products, có thể chạm đến regulated activities và restrictions liên quan.

Điểm chính cho dự án:

```text
Investment return
→ UK regulatory perimeter review
```

đặc biệt khi website hướng đến UK retail investors.

## 4. Financial promotion là gate riêng

UK đặc biệt quan trọng ở lớp **communication/marketing**.

FCA PERG materials giải thích territorial và financial-promotion perimeter.

Nguồn:
https://handbook.fca.org.uk/handbook/perg8

Điểm cần khóa:

```text
Vietnam issuer
+ website accessible from UK
+ targeted investment communication to UK persons
→ không thể mặc định chỉ chịu luật Việt Nam
```

Geo-targeting, investor classification và promotion approval/exemption analysis phải có trước khi mở investment campaign.

## 5. Client money và safeguarding

FCA CASS rules đặt trọng tâm vào segregation và protection của client assets/funds trong các trường hợp thuộc phạm vi.

Nguồn:

- CASS 7: https://handbook.fca.org.uk/handbook/cass7
- CASS 15: https://handbook.fca.org.uk/handbook/cass15

FCA đã đưa strengthened safeguarding regime cho payment/e-money institutions vào hiệu lực ngày 07/05/2026.

Nguồn:
https://www.fca.org.uk/news/press-releases/payment-safeguarding-rules-changes

Bài học:

> Platform-owned operational account không phải nơi hợp lý để trộn campaign money với corporate cash.

## 6. AON / escrow không tự giải quyết licensing

Một cấu trúc all-or-nothing có thể dùng segregated/escrow-style arrangement, nhưng:

```text
AON logic
≠
payment permission
≠
client-money permission
≠
securities permission
```

Cần đọc cùng:

- [[Escrow]]
- [[All-or-nothing và keep-it-all]]
- [[Custody và safeguarding]]

## 7. Offshore platform risk

Đối với platform Việt Nam, các red flags:

- social ads hướng đến UK retail investors;
- UK landing page nói về ROI, return, equity hoặc passive income;
- platform tự nhận subscription money;
- investment promotion không qua regulated/approved route;
- giả định Terms of Service chọn luật Việt Nam là đủ.

## 8. Investor-protection philosophy

UK high-risk investment rules cho thấy product design phải tính đến:

- clear risk warnings;
- investor categorisation;
- promotion restrictions;
- appropriateness/suitability elements tùy product/activity;
- conflicts;
- wind-down planning;
- fair, clear and not misleading communications.

Điểm này nối trực tiếp với:

- [[Campaign charter]]
- [[Material change, pivot and re-consent]]
- [[Campaign failure, recovery and termination]]

## 9. Áp vào dự án

### UK reward/pre-order

Có thể nhẹ hơn securities route, nhưng vẫn cần:

```text
consumer contract
payment
refund
marketing claims
privacy
VAT/tax
```

### UK financial-return campaign

Mặc định:

```text
UK retail detected
→ financial-promotion gate
→ regulated activity gate
→ client money/payment gate
→ instrument/issuer gate
```

Chỉ sau khi pass mới hiển thị invest button.

## 10. Kiến trúc tham chiếu

```text
UK investor
   ↓
FCA-authorized / legally permitted investment pathway
   ↓
regulated client-money / payment actor
   ↓
issuer/SPV
   ↓
Vietnam investment route

Vietnam platform:
UI + records + policy engine + reconciliation
```

## 11. Enforcement lesson

FCA enforcement and failure cases in P2P markets cho thấy regulation không chỉ là giấy phép. Governance, fair communications, due diligence, client-money controls và wind-down plan đều là operational obligations.

Ví dụ nguồn FCA về FundingSecure:
https://www.fca.org.uk/news/statements/fundingsecure-limited-complaints

## 12. Câu lõi

> **UK đặc biệt nhắc chúng ta rằng ngay cả “nói” về một khoản đầu tư với đúng đối tượng cũng có thể là regulated event; marketing jurisdiction phải được kiểm soát như money jurisdiction.**