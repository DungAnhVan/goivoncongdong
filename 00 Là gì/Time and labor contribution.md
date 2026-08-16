---
ai_authored: true
---

# Time and labor contribution

> **Định nghĩa ngắn:** *Time and labor contribution* là việc một cá nhân hoặc tổ chức cung cấp thời gian, công việc hoặc năng lực chuyên môn cho dự án mà không nhất thiết nhận thanh toán đầy đủ bằng tiền.

Đây là một dạng [[In-kind contribution]], nhưng cần node riêng vì thời gian con người khác tài sản vật chất: nó gắn với năng lực, lịch làm việc, trách nhiệm, chất lượng đầu ra và nguy cơ khai thác lao động không công.

## 1. Các dạng cần phân biệt

```text
Volunteer time
→ thời gian tự nguyện, thường không trả công

Pro bono service
→ dịch vụ chuyên môn được cung cấp miễn phí hoặc dưới giá thị trường

Seconded staff
→ tổ chức cử nhân sự sang hỗ trợ dự án

Deferred compensation
→ công việc được thực hiện nhưng thanh toán bị hoãn

Founder contribution
→ founder tự đóng góp công sức cho dự án

Sweat equity
→ công sức được gắn với quyền sở hữu hoặc lợi ích kinh tế
```

Không được dùng các từ này thay thế nhau.

## 2. Sweat equity là trường hợp đặc biệt

`Sweat equity` không nên dùng để gọi mọi công sức không lương.

Trong cách dùng của dự án:

```text
Time contribution
→ ghi nhận thời gian hoặc công việc được cung cấp

Sweat equity
→ có cơ chế rõ để công sức tạo ra quyền sở hữu,
  quyền lợi kinh tế hoặc phần tham gia trong giá trị tương lai
```

Do đó, một mentor hỗ trợ 10 giờ không mặc nhiên có cổ phần. Một founder làm việc sáu tháng cũng không nên mặc nhiên được tính equity nếu chưa có thỏa thuận rõ.

## 3. Không chỉ đếm số giờ

```text
20 giờ chuyên gia pháp lý
≠ 20 giờ nhập dữ liệu

100 giờ không có đầu ra
≠ 20 giờ tạo sản phẩm được nghiệm thu
```

Record phải mô tả:

- Vai trò.
- Kỹ năng và mức kinh nghiệm.
- Phạm vi công việc.
- Deliverable.
- Thời gian cam kết và thời gian thực tế.
- Người giám sát hoặc nghiệm thu.
- Điều kiện sử dụng kết quả công việc.

## 4. Pledge, reservation và delivery

Cần tách ba việc:

```text
Promised
→ người đó nói sẽ dành 40 giờ

Reserved
→ 40 giờ đã được giữ trong lịch và có điều kiện rõ

Delivered
→ giờ làm và đầu ra đã thực sự phát sinh
```

`Delivered hours` vẫn chưa đồng nghĩa công việc đạt yêu cầu. Cần `Accepted` sau khi kiểm tra deliverable.

Xem [[Resource pledge lifecycle]].

## 5. Data schema gợi ý

```text
labor_contribution_id:
contributor_id:
project_id:
role:
skill_profile:
scope_of_work:
deliverables:
planned_hours:
reserved_hours:
delivered_hours:
rate_reference:
estimated_value:
valuation_method:
start_date:
end_date:
availability_pattern:
supervisor:
acceptance_criteria:
IP_and_confidentiality_terms:
compensation_status:
equity_or_future_rights:
conflict_of_interest:
evidence_ids:
status:
```

Không nên chỉ lưu `hours × market rate`.

## 6. Valuation

Định giá có thể dùng:

- Mức trả cho công việc tương tự trong tổ chức.
- Mức thị trường cho kỹ năng tương đương.
- Đơn giá được chương trình tài trợ quy định.
- Chi phí thực của tổ chức cử nhân sự.
- Một mức quy ước nội bộ phục vụ planning.

Nhưng phải công bố:

```text
rate source
→ skill level
→ địa phương/thị trường
→ có gồm overhead hay không
→ giờ planned hay delivered
→ có được chương trình tài trợ chấp nhận hay không
```

Các quy định cost sharing của Hoa Kỳ là một ví dụ: volunteer services chỉ được tính khi cần thiết cho chương trình và rate phải nhất quán với công việc tương tự hoặc thị trường lao động liên quan.

## 7. Chất lượng và acceptance

Một labor contribution tốt cần kiểm tra:

| Trục | Câu hỏi |
|---|---|
| Competence | Người đó có năng lực phù hợp không? |
| Availability | Có đúng thời gian dự án cần không? |
| Scope | Công việc và giới hạn có rõ không? |
| Output | Deliverable cụ thể là gì? |
| Supervision | Ai điều phối và review? |
| Acceptance | Tiêu chí nào xác nhận hoàn thành? |
| Continuity | Công việc có phụ thuộc một người duy nhất không? |
| Rights | IP, bảo mật và quyền sử dụng kết quả thế nào? |

## 8. Rủi ro đạo đức và vận hành

- Dùng danh nghĩa cộng đồng để yêu cầu lao động miễn phí kéo dài.
- Gọi công việc bắt buộc là tình nguyện.
- Không công bố khả năng có lợi ích kinh tế sau này.
- Founder hứa thời gian nhưng không có lịch hoặc trách nhiệm rõ.
- Đếm giờ họp như giờ tạo đầu ra.
- Định giá cao để làm đẹp social proof.
- Không có quy tắc ghi nhận tác giả hoặc IP.
- Người đóng góp nghỉ giữa chừng nhưng dự án không có handover.

Nguyên tắc:

> **Đóng góp thời gian phải tự nguyện, có phạm vi, có quyền rút hợp lý và không được dùng để che một quan hệ lao động đáng lẽ phải được trả công.**

## 9. Liên hệ với thang cam kết

```text
Commitment ladder
→ hành vi thuộc Pre-commitment hay Resource contribution?

Soft/hard commitment
→ lịch đã được giữ, nghĩa vụ và hậu quả rút thế nào?

Time and labor contribution
→ kỹ năng, giờ, deliverable và acceptance là gì?
```

Một người hứa “sẽ hỗ trợ khi rảnh” là soft pre-commitment. Một tổ chức cử kỹ sư 20% thời gian trong ba tháng với scope rõ là hard hơn. Chỉ phần công việc thực tế được bàn giao mới là delivered contribution.

## 10. Proof of use

Proof of use cho thời gian lao động không chỉ là timesheet. Nó có thể gồm:

- Task log.
- Deliverable và version.
- Review note.
- Biên bản nghiệm thu.
- Quyết định đã sử dụng đầu ra.
- Handover và tài liệu duy trì.

## 11. Kết luận

> **Giờ công chỉ có ý nghĩa khi gắn với đúng năng lực, đúng phạm vi, đúng thời điểm và đầu ra có thể nghiệm thu.**

## Khái niệm liên quan

- [[Nguồn lực ngoài tiền - Bản đồ thuật ngữ]]
- [[In-kind contribution]]
- [[Commitment ladder]]
- [[Soft commitment và hard commitment]]
- [[Resource pledge lifecycle]]
- [[Proof of use và proof of outcome]]

## Nguồn tham khảo

- 2 CFR 200.306(e–f) — valuation of volunteer services and third-party employees: https://www.law.cornell.edu/cfr/text/2/200.306
- Bryan, Karlan & Nelson — Commitment Devices, 2010: https://doi.org/10.1146/annurev.economics.102308.124324
