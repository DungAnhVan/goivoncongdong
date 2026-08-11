---
type: van-de
status: mo
updated: 2026-08-11
tags:
  - chinh-sach-cong
  - project-readiness
  - eligibility
  - startup
  - resource-gap
---

# Khoảng trống từ ý tưởng đến đủ điều kiện nhận hỗ trợ công

**Phát sinh từ:** [[2026-08-11 - Hỗ trợ startup SME đổi mới sáng tạo]]  
**Phân tích liên quan:** [[TP.HCM 2026 - Nhà nước như một nguồn lực trong dự án]]

## 1. Vấn đề

Nhiều chính sách hỗ trợ chỉ có thể xử lý một **đối tượng đã đủ định danh và một dự án đã đủ cấu trúc** để cơ quan quản lý đánh giá.

Trong khi đó, phần lớn ý tưởng đầu nguồn của cộng đồng có thể đang ở trạng thái:

```text
Có vấn đề
→ có ý tưởng
→ nhưng chưa có đội
→ chưa có pháp nhân phù hợp
→ chưa có kế hoạch tài chính
→ chưa có bằng chứng nhu cầu
→ chưa có resource bundle
→ chưa rõ IP / pháp lý
→ chưa có thử nghiệm
→ chưa đủ hồ sơ để bước vào chương trình hỗ trợ
```

Khoảng này có thể được gọi tạm là:

> **project-readiness gap** — khoảng trống giữa một ý tưởng đáng quan tâm và một dự án đủ trưởng thành để đi vào cơ chế chính sách, tài trợ, đầu tư hoặc procurement.

## 2. Vì sao đây là vấn đề của mô hình chúng ta?

Nếu nền tảng chỉ đăng danh sách chính sách, nó trở thành một cổng thông tin.

Nếu nền tảng chỉ giúp viết hồ sơ, nó dễ trở thành dịch vụ “xin grant”.

Nếu nền tảng muốn thực sự tạo ra dự án, nó phải giải một bài toán sâu hơn:

> **Làm sao biến một ý tưởng còn thiếu người, thiếu bằng chứng và thiếu nguồn lực thành một hồ sơ đủ readiness mà không làm giả độ trưởng thành của dự án?**

## 3. Những lớp readiness cần xác định

### Problem readiness

- Vấn đề có được mô tả rõ không?
- Ai đang chịu tác động?
- Có bằng chứng vấn đề tồn tại không?

### Demand readiness

- Ai là user/customer/beneficiary?
- Hành vi nào chứng minh nhu cầu?
- Có commitment thật hay chỉ là sự quan tâm?

### Team readiness

- Có project lead chưa?
- Vai trò thiết yếu nào còn thiếu?
- Năng lực của đội có evidence không?

### Technical readiness

- Giải pháp ở mức ý tưởng, prototype hay pilot?
- Blocking technology là gì?
- Có IP hoặc quyền sử dụng công nghệ không?

### Financial readiness

- Tổng nhu cầu nguồn lực là gì?
- Tiền mặt chỉ chiếm bao nhiêu?
- Có phần đối ứng không?
- Chi phí nào đủ điều kiện?
- Cash-flow trước/sau giải ngân thế nào?

### Compliance readiness

- Pháp nhân nào đứng tên?
- Có giấy phép/tiêu chuẩn/quy chuẩn nào?
- Quyền dữ liệu/IP thế nào?
- Có xung đột lợi ích không?

### Evidence readiness

- Mỗi claim quan trọng có evidence ID không?
- Ai xác minh?
- Dữ liệu có version/history không?
- Bằng chứng nào cần giữ cho hậu kiểm?

### Policy readiness

- Chương trình nào thật sự phù hợp?
- Eligibility là gì?
- Thời hạn và cơ quan có thẩm quyền?
- Hỗ trợ là grant, subsidy, procurement, loan, sandbox hay cơ chế khác?

## 4. Không được biến readiness thành một “điểm đẹp” duy nhất

Không nên chấm:

```text
Project Readiness Score = 82/100
→ đủ điều kiện
```

vì có thể tồn tại **blocking condition**:

```text
Đội rất mạnh
+ prototype tốt
+ demand rõ
+ tài chính ổn
BUT
không có quyền sử dụng dataset
→ không thể triển khai
```

hoặc:

```text
đủ mọi thứ
BUT
không thuộc đối tượng của chương trình
→ không đủ eligibility
```

Do đó readiness phải gồm:

```text
Strength
Gap
Blocking condition
Required evidence
Owner
Deadline
Status
```

## 5. Câu hỏi thiết kế cho nền tảng

1. Khi nào một ý tưởng được phép chuyển sang trạng thái `Project`?
2. Khi nào một project được gắn `Policy-ready`?
3. Ai có quyền xác nhận readiness?
4. Những claim nào bắt buộc phải có verifier độc lập?
5. Làm sao cập nhật eligibility khi chính sách thay đổi?
6. Nếu dự án không đạt một điều kiện, hệ thống gợi ý nguồn lực hay gợi ý đổi chương trình?
7. Có cho phép người dùng thấy “thiếu gì để đủ điều kiện” thay vì chỉ hiện “không đạt” không?
8. Làm sao chống việc chỉnh mô tả dự án chỉ để khớp tiêu chí grant?
9. Làm sao phân biệt `eligible`, `likely eligible`, `needs review`, `not eligible`?
10. Ai chịu trách nhiệm khi thông tin chính sách trên nền tảng đã lỗi thời?

## 6. Một object có thể cần trong sản phẩm

```yaml
policy_readiness:
  program_id:
  authority:
  policy_version:
  eligibility_status:
  assessed_at:
  assessed_by:

  criteria:
    - criterion:
      status: met | partial | unmet | unknown
      evidence_ids: []
      blocking: true | false
      note:

  resource_gap_ids: []
  compliance_gap_ids: []
  next_actions: []
```

Điểm quan trọng là **policy version**. Một dự án đủ điều kiện hôm nay có thể không còn đủ điều kiện khi chính sách thay đổi.

## 7. Pilot đề xuất

Chọn một dự án thật chưa nộp hồ sơ hỗ trợ và chạy quy trình:

```text
Raw idea
→ Project profile
→ Actor map
→ Demand evidence
→ Resource needs
→ Compliance gaps
→ Policy inventory
→ Eligibility mapping
→ Blocking gaps
→ Action plan
→ Evidence package
→ Handoff sang chương trình phù hợp
```

Đo các chỉ số:

- mất bao lâu để phát hiện đúng chương trình;
- bao nhiêu điều kiện ban đầu còn `unknown`;
- bao nhiêu gap được lấp bằng nguồn lực ngoài tiền;
- bao nhiêu claim phải sửa sau verification;
- hồ sơ cuối cùng có dễ thẩm định hơn không;
- sau khi hỗ trợ, có theo dõi được proof of use và outcome không.

## 8. Liên kết

- [[Chính sách công và tài chính công - Bản đồ thuật ngữ]]
- [[Proof of need và demand validation]]
- [[Commitment ladder]]
- [[Multi-resource matching]]
- [[Resource pledge lifecycle]]
- [[Evidence ledger]]
- [[Verification protocol]]
- [[Grant và subsidy]]
- [[Matching fund]]
- [[Public procurement]]
- [[Restricted funds]]
- [[Disbursement]]
- [[Proof of use và proof of outcome]]
- [[Campaign charter]]

## 9. Câu lõi

> **Chính sách có thể đã có nguồn lực, nhưng nguồn lực đó không tự tìm được một ý tưởng còn thô. Khoảng trống cần giải là biến ý tưởng thành một dự án đủ rõ, đủ bằng chứng và đủ trách nhiệm để một cơ chế hỗ trợ có thể tiếp nhận mà không phải giả vờ rằng dự án đã trưởng thành hơn thực tế.**
