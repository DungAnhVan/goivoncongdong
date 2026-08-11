# Nguồn — Chính sách công

> [!abstract] Vai trò thư mục
> Đây là nơi lưu **dấu vết nguồn và case chính sách**, không phải nơi viết toàn bộ quan điểm chiến lược của dự án.

## 1. Nguyên tắc phân lớp

```text
TIN / VĂN BẢN / THÔNG BÁO
        ↓
01 Nguồn/Chính sách công
→ lưu sự kiện, cơ quan, văn bản, con số, URL, trạng thái hiệu lực
→ tách điều nguồn nói khỏi điều nguồn chưa chứng minh
        ↓
02 Mở rộng/Chính sách công
→ phân tích ý nghĩa với mô hình
→ so sánh cơ chế
→ hình thành giả thuyết chiến lược
        ↓
03 Vấn đề
→ tạo câu hỏi/lỗ hổng cần giải
        ↓
04 Giải pháp / 05 Phương án / 06 Thực làm
→ chỉ đi tiếp khi có một cơ chế hoặc pilot cụ thể
```

## 2. Không trộn ba loại nội dung

### `Nguồn nói`

- văn bản nào;
- cơ quan nào;
- ngày nào;
- đối tượng nào;
- mức hỗ trợ nào;
- quy trình/điều kiện nào được công bố.

### `Phân tích của dự án`

- nó có ý nghĩa gì;
- nó giống/khác [[Matching fund]], [[Public procurement]], [[Grant và subsidy]] thế nào;
- nó mở ra vị trí nào cho nền tảng;
- giả thuyết nào đáng thử.

### `Điều chưa biết`

- chưa có điều khoản;
- chưa rõ thực thi;
- chưa rõ cơ quan xử lý;
- chưa rõ evidence/verification;
- chưa rõ refund/residual/failure rule.

Không được lấp khoảng trống này bằng suy đoán.

## 3. Cấu trúc thư mục

```text
01 Nguồn/Chính sách công/
├─ README.md
├─ Việt Nam/
│  ├─ Chiến lược quốc gia khởi nghiệp sáng tạo
│  ├─ Chiến lược KHCN / công nghệ chiến lược
│  ├─ Khung quốc gia KHCN/ĐMST/startup
│  ├─ Kinh tế tư nhân/SME/vốn khởi nghiệp/scale-up
│  ├─ Quỹ công/NIC/R&D/công nghệ cao
│  ├─ Công nghiệp công nghệ số
│  ├─ Mua sắm công/first-customer
│  ├─ Sandbox/IFC/crowdfunding gap
│  └─ Donation/quỹ xã hội/doanh nghiệp xã hội
├─ TPHCM/
│  ├─ Hỗ trợ startup/SME
│  ├─ NQ98/NQ31/thuế
│  ├─ NQ20/NQ22/NQ23
│  ├─ NQ24/QĐ36/recognition
│  ├─ HCM VIF/kiều hối
│  ├─ Kế hoạch 141/Chương trình 2685
│  └─ Công nghệ chiến lược/IP/TRL/chuyên gia/outcome
├─ Dự thảo và watchlist/
│  └─ draft, consultation, policy gap
└─ Quốc tế/
   └─ ...
```

Phân loại theo **jurisdiction + policy stack + status**, không theo cảm xúc “tin tốt/tin xấu”.

## 4. Template cho một policy source record

```yaml
---
type: nguon-chinh-sach
status: chua-doi-chieu | da-doi-chieu | can-cap-nhat
jurisdiction:
date_event:
updated:
tags: []
---
```

Nội dung tối thiểu:

```text
1. Tin/văn bản khởi phát
2. Nguồn chính thức
3. Đối tượng áp dụng
4. Công cụ chính sách
5. Tiền/nguồn lực
6. Eligibility
7. Quy trình
8. Evidence/verification
9. Điều chưa chứng minh
10. Liên kết repo
11. Câu hỏi nghiên cứu tiếp
```

## 5. Status taxonomy

```text
CURRENT / ĐANG HIỆU LỰC
→ văn bản chính thức đang dùng

OPERATIONAL
→ chương trình/quỹ/thủ tục đã có dấu vết vận hành thực tế

PLAN / STRATEGY
→ kế hoạch, mục tiêu, roadmap; chưa đồng nghĩa mọi công cụ đã mở

DRAFT / CONSULTATION
→ chưa phải quy định cuối

WATCHLIST
→ khoảng trống hoặc thay đổi cần theo dõi

REPLACED / EXPIRED
→ giữ lịch sử nhưng không dùng như quy định hiện hành
```

## 6. Cách gắn với ontology hiện tại

Một case chính sách nên thử phân loại bằng các node:

- [[Public policy]]
- [[Policy instrument]]
- [[Public finance]]
- [[Grant và subsidy]]
- [[Matching fund]]
- [[Public procurement]]
- [[Regulatory sandbox]]
- [[Restricted funds]]
- [[Disbursement]]
- [[Multi-resource matching]]
- [[Proof of use và proof of outcome]]

Nếu không khớp node nào, lúc đó mới cân nhắc tạo thuật ngữ mới.

## 7. Case registry — Việt Nam

| Policy stack | Source record | Status 11/08/2026 |
|---|---|---|
| NQ86 — Chiến lược quốc gia khởi nghiệp sáng tạo | [[2026 - Chiến lược quốc gia về khởi nghiệp sáng tạo NQ86]] | Strategy / current |
| QĐ604 + QĐ21 + QĐ808 — chiến lược KHCN và công nghệ chiến lược | [[2026 - Chiến lược KHCN 2030 và giao nhiệm vụ công nghệ chiến lược]] | Strategy + current task framework |
| Luật 93 + NĐ264/265/267/268 + TT36 + NQ193/NĐ88 | [[2025-2026 - Khung quốc gia KHCN đổi mới sáng tạo và startup]] | Current / cần kiểm tra chuyển tiếp theo cơ chế cụ thể |
| NQ198 + NĐ20 + NĐ80 + NĐ38/210 + QĐ631 scale-up | [[2025-2026 - Kinh tế tư nhân SME và vốn khởi nghiệp]] | Current / scale-up program current |
| NĐ77 + NĐ229 + NĐ182 + NĐ97 + NĐ125 + NĐ260 + QĐ21 | [[2024-2026 - Các quỹ công NIC và nguồn lực R&D công nghệ cao]] | Current / một số call operational |
| Luật Công nghiệp công nghệ số 71/2025 | [[2025-2026 - Công nghiệp công nghệ số và hỗ trợ startup số]] | Current |
| Luật Đấu thầu hợp nhất + NĐ214/2025 | [[2025-2026 - Mua sắm công đấu thầu và first-customer route]] | Current; draft sửa NĐ214 đang watch |
| IFC + banking sandbox + crowdfunding legal gap | [[2025-2026 - Sandbox tài chính IFC và khoảng trống crowdfunding]] | Current + watchlist |
| NĐ93 + NĐ03/2026 + doanh nghiệp xã hội | [[2021-2026 - Donation quỹ xã hội từ thiện và doanh nghiệp xã hội]] | Current / theo phạm vi từng lane |

## 8. Case registry — TP.HCM

| Policy stack | Source record | Status 11/08/2026 |
|---|---|---|
| NQ98 sửa bởi NQ260 + NQ31 + ưu đãi thuế | [[2023-2026 - NQ98 NQ260 NQ31 và ưu đãi thuế đổi mới sáng tạo]] | Current |
| NQ20 + NQ22 + NQ23 | [[2023-2026 - NQ20 NQ22 NQ23 và hỗ trợ dự án đổi mới sáng tạo]] | Current; NQ20 có draft reform đang theo dõi |
| NQ24 + QĐ36 + recognition theo NĐ268 | [[2026 - NQ24 QD36 quản lý nhiệm vụ và công nhận actor hệ sinh thái]] | Current / operational |
| HCM VIF + Kế hoạch 90 kiều hối | [[2026 - HCM VIF kiều hối và các kênh tài chính mới cho KHCN]] | VIF operational; Kế hoạch 90 = plan |
| Kế hoạch 141 + QĐ2685 | [[2026 - Kế hoạch 141 và Chương trình 2685 hệ sinh thái đổi mới sáng tạo]] | Plan / program implementation |
| Kế hoạch 122 + QĐ3053 + QĐ05 + QĐ18 | [[2025-2026 - Công nghệ chiến lược thương mại hóa tài sản trí tuệ và nhân lực]] | Plan + operational pilots/procedures |
| Tin 11/08 về hỗ trợ startup/SME | [[2026-08-11 - Hỗ trợ startup SME đổi mới sáng tạo]] | Source event |

## 9. Watchlist registry

- [[2026 - Dự thảo hỗ trợ startup và policy watchlist]]
  - dự thảo hỗ trợ không hoàn lại 3 stage TP.HCM;
  - local sandbox;
  - investment/equity crowdfunding framework;
  - sửa Luật Hỗ trợ DNNVV;
  - HCM VIF investment rules/portfolio data;
  - dự thảo sửa NĐ214/2025 về lựa chọn nhà thầu.

## 10. Analysis registry

- [[TP.HCM 2026 - Nhà nước như một nguồn lực trong dự án]]
- [[Bản đồ chính sách công Việt Nam và TP.HCM - 2026]]
- [[Khoảng trống từ ý tưởng đến đủ điều kiện nhận hỗ trợ công]]

## 11. Câu hỏi mặc định khi có tin chính sách mới

```text
Đây là chính sách hay chỉ là tuyên bố/định hướng?
Văn bản chính thức ở đâu?
Đang hiệu lực hay dự thảo?
Ai thật sự đủ điều kiện?
Đây là grant, subsidy, procurement, loan, investment, donation hay sandbox?
Nguồn lực đi qua ai?
Ai giữ tiền/tài sản/quyền?
Ai quyết định?
Ai xác minh?
Bằng chứng nào kích hoạt hỗ trợ?
Có đối ứng không?
Có IP/data/right restriction không?
Nếu thất bại thì hoàn/trả/xử lý thế nào?
Nền tảng có thể tạo giá trị ở upstream, matching, evidence hay downstream?
```

## 12. Quy tắc chống overclaim

```text
Có văn bản
≠ có call đang mở

Có chương trình
≠ project đủ điều kiện

Đủ điều kiện
≠ được duyệt

Được duyệt
≠ đã giải ngân

Đã giải ngân
≠ đã tạo outcome

Có quỹ
≠ quỹ đã đầu tư project này

Có sandbox
≠ mô hình của ta được phép thử

Có strategic-tech tag
≠ được ưu đãi tự động

Có donation button
≠ transaction thuộc donation law

Có public problem/pilot
≠ có procurement contract
```

## 13. Liên kết trung tâm

- [[Chính sách công và tài chính công - Bản đồ thuật ngữ]]
- [[Bản đồ chính sách công Việt Nam và TP.HCM - 2026]]
- [[Danh mục nguồn pháp luật Việt Nam hiện hành]]
- [[Liên kết mô hình khác]]
- [[SIHUB - Tổng quan và bài học]]
