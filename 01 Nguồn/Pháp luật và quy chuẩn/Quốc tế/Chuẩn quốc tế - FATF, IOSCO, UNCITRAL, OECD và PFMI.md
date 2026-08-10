# Chuẩn quốc tế - FATF, IOSCO, UNCITRAL, OECD và PFMI

> Cập nhật nghiên cứu: 10/08/2026.  
> Mục tiêu: phân biệt luật bắt buộc của từng quốc gia với chuẩn quốc tế, soft law và best practice.  
> Không tồn tại một `international crowdfunding license`.

## 1. Phân tầng giá trị pháp lý

```text
Treaty / convention đã có hiệu lực với quốc gia liên quan
→ có thể tạo nghĩa vụ quốc tế và được nội luật hóa theo cơ chế quốc gia

National statute / regulation / regulator rule
→ binding law trong jurisdiction

International standard / recommendation
→ không tự động là luật nhưng ảnh hưởng mạnh đến supervision và domestic rules

Model law
→ mẫu cho quốc gia nội luật hóa; không tự động binding

Guideline / best practice
→ benchmark quản trị/risk, không phải permission để hoạt động
```

Không viết `theo chuẩn quốc tế` mà không nói rõ chuẩn nào và có binding hay không.

## 2. FATF — AML/CFT/PF global standard

FATF Recommendations là chuẩn toàn cầu về AML/CFT và proliferation financing.

Nguồn:
https://www.fatf-gafi.org/en/topics/fatf-recommendations.html

Các concept liên quan trực tiếp:

- risk-based approach;
- customer due diligence;
- beneficial ownership;
- politically exposed persons;
- new technologies;
- wire/payment transparency;
- suspicious transaction reporting;
- recordkeeping;
- beneficial ownership transparency.

Kiến trúc tối thiểu:

```text
Identity
+ beneficial owner
+ PEP / sanctions screening
+ source-of-funds risk
+ transaction monitoring
+ project / recipient due diligence
+ escalation / reporting workflow
```

FATF không cấp license crowdfunding. Nó là standard-setting layer được national regimes phản ánh.

## 3. IOSCO — securities-market principles

IOSCO tập trung vào investor protection, fair/efficient markets, intermediary oversight và cross-border supervisory cooperation.

Nguồn:
https://www.iosco.org/

IOSCO đã có publications về crowdfunding regulation và risks.

Bài học:

> investment crowdfunding phải được xem như capital-market activity với disclosure, conflicts, gatekeeping, default/illiquidity/fraud risk — không chỉ e-commerce.

## 4. CPMI-IOSCO PFMI — không phải chuẩn trực tiếp cho startup platform

Principles for Financial Market Infrastructures (`PFMI`) áp dụng cho systemically important payment, clearing, settlement và related infrastructures; không nên claim `PFMI compliant` cho một crowdfunding startup nếu không thuộc phạm vi.

Nguồn:
https://www.bis.org/cpmi/info_pfmi.htm

Nhưng có thể học design principles:

- legal certainty;
- sound settlement assets;
- segregation;
- operational resilience;
- reconciliation;
- finality;
- credit/liquidity risk controls;
- business continuity;
- wind-down.

Dùng như **engineering benchmark**, không dùng như licensing argument.

## 5. UNCITRAL — electronic commerce và signatures

UNCITRAL Model Law on Electronic Commerce hỗ trợ nguyên tắc functional equivalence giữa electronic và paper communications.

Nguồn:
https://uncitral.un.org/en/texts/ecommerce/modellaw/electronic_commerce

Ranh giới:

```text
Electronic contract enforceability
≠
underlying financial activity lawful
```

Một subscription contract có thể ký điện tử hợp lệ nhưng offering vẫn có thể vi phạm securities/consumer/FX rules.

## 6. OECD — responsible business conduct và tax architecture

OECD Guidelines for Multinational Enterprises on Responsible Business Conduct hữu ích cho due diligence, stakeholder responsibility và corporate conduct.

Nguồn:
https://mneguidelines.oecd.org/

OECD/G20 BEPS framework liên quan khi dùng HoldCo/SPV:

- economic substance;
- permanent establishment;
- transfer pricing;
- beneficial ownership;
- treaty abuse;
- principal-purpose/anti-abuse logic;
- Multilateral Instrument tùy treaty network.

Hard lesson:

```text
Investor
→ shell SPV in treaty jurisdiction
→ Vietnam company
```

không nên được thiết kế chỉ vì headline withholding thấp.

## 7. Cross-border tax transparency — CRS và FATCA

`CRS` và `FATCA` không phải crowdfunding law nhưng có thể ảnh hưởng financial institutions/accounts và reporting structures.

Cần phân biệt:

- FATCA: U.S.-linked statutory/reporting regime;
- CRS: OECD automatic exchange standard implemented through participating jurisdictions.

Không mặc định platform là reporting financial institution; classification phải theo entity/account structure.

## 8. Sanctions screening

Sanctions không phải một standard quốc tế đồng nhất. Screening obligations phụ thuộc jurisdiction, financial partners và applicable sanctions regimes.

Platform policy engine nên tách:

```text
UN sanctions
national sanctions regimes
bank/PSP sanctions requirements
country-specific restrictions
```

Không dùng một vendor list để kết luận `global sanctions compliant`.

## 9. International cooperation

Các cơ chế hợp tác làm cross-border enforcement thực tế hơn:

- IOSCO supervisory/enforcement information sharing;
- FATF-style FIU/supervisory cooperation;
- tax information exchange;
- mutual legal assistance / treaties tùy case;
- regulator-to-regulator MoUs.

Điểm cần nhớ:

> Offshore incorporation không đồng nghĩa offshore invisibility.

## 10. Chuẩn thiết kế tối thiểu cho dự án

Dù chưa regulated financial platform, có thể chủ động áp dụng:

1. verified identity và beneficial-owner map;
2. segregated money architecture;
3. immutable evidence/audit log;
4. conflict disclosure;
5. risk-based due diligence;
6. clear finality/release rules;
7. data minimization và transfer map;
8. incident/wind-down plan;
9. source-of-funds escalation;
10. jurisdiction-specific legal gates.

## 11. Không được suy diễn

```text
FATF aligned
≠ licensed

IOSCO principle aligned
≠ securities offering permitted

UNCITRAL e-signature compatible
≠ investment legal

PFMI-inspired safeguarding
≠ regulated payment institution

OECD-compliant SPV narrative
≠ treaty benefit guaranteed
```

## 12. Câu lõi

> **Chuẩn quốc tế giúp thiết kế một hệ thống đáng tin và tương thích với kỳ vọng regulator; quyền được hoạt động vẫn phải đến từ luật và cơ chế cấp phép/exemption của từng jurisdiction.**