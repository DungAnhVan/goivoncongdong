# In-kind contribution

> **Định nghĩa ngắn:** *In-kind contribution* là đóng góp cho dự án dưới dạng tài sản, hàng hóa, dịch vụ, thời gian, quyền sử dụng hoặc nguồn lực khác thay vì chuyển tiền mặt.

Trong dự án này, `in-kind contribution` là **khái niệm bao trùm**. Các nhóm có rủi ro và cách quản lý riêng được tách sang:

- [[Time and labor contribution]].
- [[Data contribution]].
- [[Asset and access contribution]].

## 1. Điều gì được xem là in-kind?

Ví dụ:

```text
Vật liệu được tặng
Thiết bị được cho mượn
Địa điểm được cấp dùng
Dịch vụ luật sư pro bono
Nhân sự doanh nghiệp được cử sang hỗ trợ
Chi phí vận chuyển được miễn
Quyền sử dụng phần mềm
Quyền tiếp cận cơ sở thử nghiệm
```

Theo cách dùng trong các chương trình tài trợ, đóng góp hiện vật thường bao gồm tài sản hoặc dịch vụ không được chuyển thành một khoản tiền mặt cho bên nhận. Tuy nhiên, việc một chương trình có công nhận nó là cost sharing, eligible cost hay matching hay không phụ thuộc quy định cụ thể.

## 2. Ranh giới với các khái niệm khác

```text
In-kind contribution
→ nguồn lực phi tiền mặt được cung cấp

Donation
→ hành vi cho tặng; có thể là tiền hoặc hiện vật

Procurement
→ dự án mua hàng hóa hoặc dịch vụ

Secondment
→ tổ chức cử nhân sự sang làm việc trong phạm vi xác định

Sweat equity
→ công sức gắn với quyền sở hữu hoặc lợi ích kinh tế

Resource pledge
→ lời hứa cung cấp nguồn lực trong tương lai
```

Không dùng `in-kind contribution` để suy ra:

- Nguồn lực đã được bàn giao.
- Nguồn lực có giá trị đúng như người cung cấp tuyên bố.
- Nguồn lực được phép tính vào matching.
- Dự án đã sử dụng nguồn lực đúng mục đích.

## 3. Sáu thuộc tính phải ghi

```text
Bản chất nguồn lực
→ ai có quyền cung cấp?
→ quyền nào được chuyển hoặc cấp?
→ trong thời gian nào?
→ điều kiện và trách nhiệm gì?
→ tiêu chí nào xác nhận đã nhận?
```

Record tối thiểu:

```text
contribution_id:
provider_id:
project_id:
resource_category:
description:
quantity:
unit:
transfer_type:
ownership_status:
use_rights:
availability_window:
conditions:
restrictions:
estimated_value:
valuation_method:
delivery_evidence_ids:
acceptance_status:
```

`estimated_value` là trường tùy chọn; không được thay thế mô tả nguồn lực thực.

## 4. Transfer type

Cần tách ít nhất:

```text
Donation / title transfer
→ quyền sở hữu được chuyển

Loan / temporary use
→ tài sản phải hoàn trả

Licence / right to use
→ chỉ cấp quyền trong phạm vi xác định

Service contribution
→ một công việc được thực hiện cho dự án

Cost waiver
→ bên cung cấp miễn một khoản phí

Discount
→ giá giảm, không phải toàn bộ giá trị được đóng góp
```

Một khoản giảm giá 20% không được ghi như toàn bộ dịch vụ là in-kind contribution.

## 5. Valuation không phải bước đầu tiên

Một nguồn lực có thể cần định giá để:

- Lập ngân sách.
- Báo cáo matching hoặc co-financing.
- So sánh phương án mua với nhận đóng góp.
- Tính bảo hiểm hoặc trách nhiệm.
- Công bố quy mô hỗ trợ.

Nhưng định giá chỉ có ý nghĩa sau khi xác định:

- Nguồn lực có cần thiết và hợp lý không.
- Điều kiện sử dụng có chấp nhận được không.
- Có bị đếm cho dự án khác không.
- Người cung cấp có phải bên liên quan không.
- Phương pháp định giá có thể kiểm tra không.

Các quy định tài trợ liên bang Hoa Kỳ là một ví dụ rõ: đóng góp in-kind dùng cho cost sharing phải có thể kiểm chứng, cần thiết, hợp lý, không bị tính trùng; dịch vụ, tài sản, không gian và thiết bị cho mượn có quy tắc định giá khác nhau.

## 6. Gross value và usable value

Không nên chỉ lưu giá thị trường danh nghĩa.

```text
Gross value
→ giá trị ước tính trước điều kiện và chi phí tích hợp

Usable value
→ phần nguồn lực thực sự phù hợp và có thể dùng

Net project value
→ usable value trừ chi phí vận chuyển, tích hợp, bảo trì, tuân thủ và hoàn trả
```

Ví dụ:

```text
Máy được cho mượn, giá thuê thị trường 100 triệu
- vận chuyển 20 triệu
- cần kỹ thuật viên 30 triệu
- chỉ dùng được 50% công suất cần thiết
→ không thể công bố đơn giản “đóng góp 100 triệu”
```

## 7. Acceptance

Nguồn lực chỉ nên chuyển sang trạng thái `Accepted` khi:

- Đúng loại và số lượng.
- Đúng chất lượng hoặc thông số.
- Đúng thời gian và địa điểm.
- Quyền sử dụng rõ.
- Không có hạn chế chưa công bố.
- Có người chịu trách nhiệm tiếp nhận.
- Có bằng chứng bàn giao.

Sau acceptance, việc sử dụng được theo dõi bằng [[Proof of use và proof of outcome]].

## 8. Rủi ro

- Định giá phóng đại để làm đẹp quy mô dự án.
- Tặng thứ dự án không cần nhưng vẫn ghi là nguồn lực huy động.
- Đưa hàng tồn kho kém chất lượng vào dự án.
- Không công bố quan hệ lợi ích.
- Không phân biệt tài sản tặng và tài sản mượn.
- Không ghi trách nhiệm hư hỏng hoặc bảo trì.
- Dùng một đóng góp làm matching cho nhiều chương trình.
- Nhận nguồn lực có điều kiện gây lệ thuộc hoặc xung đột mục tiêu.

## 9. Liên hệ với nền tảng

Nền tảng không nên chỉ có trường:

```text
estimated_value: 200.000.000 VND
```

Mà phải lưu:

```text
resource object
→ legal/use basis
→ availability
→ restrictions
→ lifecycle state
→ evidence
→ acceptance
→ proof of use
```

## 10. Kết luận

> **In-kind contribution không phải “tiền được viết dưới hình thức khác”. Nó là một nguồn lực cụ thể với quyền, điều kiện, thời hạn và chi phí tích hợp riêng.**

## Khái niệm liên quan

- [[Nguồn lực ngoài tiền - Bản đồ thuật ngữ]]
- [[Time and labor contribution]]
- [[Data contribution]]
- [[Asset and access contribution]]
- [[Resource pledge lifecycle]]
- [[Matching fund]]
- [[Proof of use và proof of outcome]]

## Nguồn tham khảo

- 2 CFR 200.1 — definition of third-party in-kind contributions: https://www.law.cornell.edu/cfr/text/2/200.1
- 2 CFR 200.306 — cost sharing, valuation and documentation: https://www.law.cornell.edu/cfr/text/2/200.306
- European Commission/CINEA — in-kind contributions in grant implementation: https://cinea.ec.europa.eu/programmes/european-maritime-fisheries-and-aquaculture-fund/faqs-emfaf-calls-proposals_en
