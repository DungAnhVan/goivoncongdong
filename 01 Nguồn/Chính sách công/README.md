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

## 3. Cấu trúc thư mục đề xuất

```text
01 Nguồn/Chính sách công/
├─ README.md
├─ TPHCM/
│  ├─ 2026-08-11 - Hỗ trợ startup SME đổi mới sáng tạo.md
│  └─ ...
├─ Việt Nam/
│  └─ ...
└─ Quốc tế/
   └─ ...
```

Phân loại theo **jurisdiction + date + policy event**, không theo cảm xúc “tin tốt/tin xấu”.

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

## 5. Cách gắn với ontology hiện tại

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

## 6. Case registry

| Ngày | Jurisdiction | Case | Source record | Analysis | Problem |
|---|---|---|---|---|---|
| 2026-08-11 | TP.HCM | Hỗ trợ startup/SME đổi mới sáng tạo | [[2026-08-11 - Hỗ trợ startup SME đổi mới sáng tạo]] | [[TP.HCM 2026 - Nhà nước như một nguồn lực trong dự án]] | [[Khoảng trống từ ý tưởng đến đủ điều kiện nhận hỗ trợ công]] |

## 7. Câu hỏi mặc định khi có tin chính sách mới

```text
Đây là chính sách hay chỉ là tuyên bố/định hướng?
Văn bản chính thức ở đâu?
Đang hiệu lực hay dự thảo?
Ai thật sự đủ điều kiện?
Đây là grant, subsidy, procurement, loan, investment hay sandbox?
Nguồn lực đi qua ai?
Ai giữ tiền?
Ai quyết định?
Ai xác minh?
Bằng chứng nào kích hoạt hỗ trợ?
Có đối ứng không?
Nếu thất bại thì hoàn/trả/xử lý thế nào?
Nền tảng có thể tạo giá trị ở upstream, matching, evidence hay downstream?
```

## 8. Liên kết trung tâm

- [[Chính sách công và tài chính công - Bản đồ thuật ngữ]]
- [[Liên kết mô hình khác]]
- [[SIHUB - Tổng quan và bài học]]
