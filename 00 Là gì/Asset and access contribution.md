# Asset and access contribution

> **Định nghĩa ngắn:** *Asset and access contribution* là việc cung cấp tài sản vật chất, quyền sử dụng tài sản, địa điểm, hạ tầng hoặc quyền tiếp cận một mạng lưới, thị trường, cơ sở thử nghiệm hay nhóm đối tượng cho dự án.

Node này gom bốn nhóm thường bị tách vụn nhưng cần quản lý bằng cùng một câu hỏi:

> Dự án được nhận **cái gì**, theo **quyền nào**, trong **thời gian và công suất nào**, với **trách nhiệm nào**?

## 1. Các dạng chính

```text
Asset transfer
→ chuyển quyền sở hữu vật liệu, thiết bị hoặc tài sản

Asset loan
→ cho mượn tài sản và phải hoàn trả

Asset-use access
→ cấp quyền sử dụng theo thời gian/công suất

Venue contribution
→ cấp không gian tổ chức, thử nghiệm, sản xuất hoặc lưu trữ

Infrastructure access
→ cấp quyền dùng phòng lab, dây chuyền, server, kho hoặc hệ thống

Market / distribution access
→ giới thiệu hoặc mở kênh tiếp cận khách hàng, đại lý, cộng đồng

Institutional access
→ quyền tiếp cận chương trình, cơ sở công, chuyên gia hoặc đầu mối thể chế
```

## 2. Access không phải asset

```text
Sở hữu máy
≠ mượn máy
≠ được dùng máy 8 giờ
≠ được ưu tiên lịch máy khi rảnh

Có danh sách khách hàng
≠ được gửi email
≠ được giới thiệu trực tiếp
≠ có hợp đồng phân phối
```

Không ghi chung `equipment contribution` hoặc `market access` nếu chưa mô tả quyền thực tế.

## 3. Các trường quyền phải tách

```text
ownership:
control_right:
access_right:
use_right:
transferability:
exclusivity:
return_obligation:
maintenance_responsibility:
liability:
insurance_requirement:
```

Một tài sản có thể do bên A sở hữu, bên B vận hành và dự án chỉ được sử dụng trong một khung giờ. Ba vai trò này không được gộp.

## 4. Availability và capacity

Nguồn lực vật chất chỉ hữu ích nếu có đúng thời điểm và công suất.

```text
available_from:
available_until:
recurring_schedule:
capacity:
reserved_capacity:
location:
lead_time:
setup_time:
downtime_risk:
operator_requirement:
```

Ví dụ:

```text
Offer: máy CNC miễn phí
Nhưng:
- chỉ rảnh ban đêm;
- không có người vận hành;
- cần jig riêng;
- cách địa điểm dự án 300 km;
- giới hạn vật liệu;
→ matching score có thể thấp
```

## 5. Địa điểm và không gian

Venue contribution phải ghi:

- Diện tích và sức chứa.
- Mục đích được phép.
- Thời gian setup và tháo dỡ.
- Điện, nước, mạng và an toàn.
- Quyền ra vào.
- Bảo vệ và lưu trữ.
- Trách nhiệm hư hỏng.
- Chi phí phụ trợ.
- Quy định thương hiệu hoặc truyền thông.

“Cho địa điểm miễn phí” có thể vẫn kéo theo chi phí vận hành lớn.

## 6. Equipment contribution

Phải phân biệt:

```text
Donated equipment
→ quyền sở hữu chuyển cho dự án/pháp nhân

Loaned equipment
→ hoàn trả sau kỳ sử dụng

Managed service
→ bên cung cấp giữ máy và thực hiện công việc

Capacity slot
→ dự án chỉ được dùng một phần công suất
```

Acceptance cần kiểm tra:

- Model/serial.
- Tình trạng.
- Calibration hoặc chứng nhận nếu cần.
- Phụ kiện.
- Công suất thực.
- Quy trình vận hành.
- Bảo trì.
- Handover và return condition.

## 7. Access contribution

Quyền tiếp cận là nguồn lực khó định lượng nhưng có thể quyết định thành bại.

Ví dụ:

- Được pilot tại một trường học.
- Được tiếp cận 20 xưởng để phỏng vấn.
- Được đưa sản phẩm vào tám cửa hàng.
- Được dùng mạng lưới chuyên gia.
- Được tham gia một chương trình công.

Cần phân loại mức độ:

```text
Introduction only
→ bên cung cấp chỉ giới thiệu

Facilitated access
→ hỗ trợ sắp xếp và theo dõi

Reserved access
→ có slot hoặc quota được giữ

Contractual access
→ quyền tiếp cận có văn bản và nghĩa vụ rõ
```

Không gọi một lần giới thiệu là “đã có kênh phân phối”.

## 8. Record gợi ý

```text
asset_access_id:
provider_id:
project_id:
resource_subtype:
asset_or_access_description:
ownership_status:
transfer_type:
availability_window:
capacity:
location:
conditions:
restrictions:
operator_or_facilitator:
setup_requirements:
maintenance_responsibility:
insurance_and_liability:
return_rule:
acceptance_criteria:
estimated_value:
valuation_method:
evidence_ids:
status:
```

## 9. Valuation

Có thể tham chiếu:

- Fair market value nếu chuyển tài sản.
- Fair rental value nếu cho mượn hoặc cấp không gian.
- Giá dịch vụ tương đương nếu là managed service.
- Không định giá tiền nếu access quá đặc thù và chưa có benchmark đáng tin.

Quy định cost sharing của Hoa Kỳ là một ví dụ: tài sản tặng, không gian được cấp và thiết bị cho mượn có cơ sở định giá khác nhau. Đây chỉ là nguồn học nguyên lý, không phải quy tắc tự động áp dụng cho dự án tại Việt Nam.

## 10. Proof of delivery và proof of use

Bằng chứng bàn giao có thể gồm:

- Biên bản giao nhận.
- Serial/asset ID.
- Access pass hoặc booking record.
- Hợp đồng cho mượn.
- Lịch công suất.
- Thư xác nhận quyền pilot.
- Log sử dụng.

Proof of use cần ghi:

- Đã dùng bao nhiêu công suất/thời gian.
- Cho activity hoặc milestone nào.
- Có downtime hay hạn chế gì.
- Tài sản đã hoàn trả hay chưa.
- Có hư hỏng hoặc nghĩa vụ phát sinh không.

## 11. Rủi ro

- Công bố logo và lời giới thiệu như quyền tiếp cận thật.
- Thiết bị không phù hợp hoặc không có người vận hành.
- Không ghi trách nhiệm tai nạn và hư hỏng.
- Địa điểm chỉ khả dụng ngoài thời gian dự án cần.
- Quyền access phụ thuộc một cá nhân và mất khi người đó rời đi.
- Tính toàn bộ giá tài sản khi dự án chỉ dùng một phần nhỏ.
- Không ghi chi phí vận chuyển, setup và hoàn trả.
- Nhận tài sản kèm điều kiện thương mại hoặc truyền thông không phù hợp.

## 12. Kết luận

> **Nguồn lực vật chất và quyền tiếp cận chỉ trở thành năng lực dự án khi quyền sử dụng, thời gian, công suất và trách nhiệm đều đủ rõ để vận hành.**

## Khái niệm liên quan

- [[Nguồn lực ngoài tiền - Bản đồ thuật ngữ]]
- [[In-kind contribution]]
- [[Multi-resource matching]]
- [[Resource pledge lifecycle]]
- [[Proof of use và proof of outcome]]
- [[Internal financial controls]]

## Nguồn tham khảo

- 2 CFR 200.306(g–j) — donated property, equipment, space and documentation: https://www.law.cornell.edu/cfr/text/2/200.306
- OECD — data and infrastructure as strategic resources: https://www.oecd.org/en/topics/data-flows-and-governance.html
