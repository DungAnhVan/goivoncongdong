---
ai_authored: true
---

# All-or-nothing và keep-it-all

> **Định nghĩa ngắn:** *All-or-nothing* là cơ chế chỉ kích hoạt hoặc chuyển giao nguồn lực khi mục tiêu hay provision point được đáp ứng. *Keep-it-all* là cơ chế cho phép dự án giữ phần nguồn lực đã huy động dù chưa đạt mục tiêu ban đầu, theo các điều kiện được công bố trước.

Hai cơ chế trả lời câu hỏi:

> Khi chiến dịch không đạt mục tiêu, ai giữ nguồn lực và ai chịu rủi ro phần thiếu hụt?

## 1. All-or-nothing

```text
Đạt điều kiện trước deadline
→ kích hoạt cam kết
→ chuyển/giải phóng nguồn lực

Không đạt
→ không thu, hoàn lại hoặc release reservation
```

AON phù hợp khi dự án chỉ khả thi nếu đạt một mức tối thiểu rõ.

Ví dụ:

- Sản xuất cần đủ chi phí khuôn.
- Sự kiện chỉ tổ chức được khi đủ người.
- Dự án cần đủ đội vai trò thiết yếu.
- Thiết bị chỉ được cho mượn nếu bảo hiểm và operator đã có.

## 2. Keep-it-all

```text
Đạt mục tiêu
→ dùng theo full scope

Không đạt mục tiêu
→ vẫn nhận/giữ phần đã huy động
→ thực hiện partial scope hoặc mục đích dự phòng đã công bố
```

KIA có thể phù hợp khi mỗi khoản đóng góp vẫn tạo giá trị độc lập.

Ví dụ:

- Cứu trợ khẩn cấp.
- Mua từng bộ vật tư độc lập.
- Tài trợ nội dung theo đơn vị.
- Quỹ vận hành liên tục.
- Dự án có thể chia thành nhiều module không phụ thuộc nhau.

## 3. Ranh giới với provision point

```text
[[Provision point và threshold mechanism|Provision point]]
→ mức nào là đủ để kết quả xảy ra?

All-or-nothing / keep-it-all
→ rule xử lý contribution khi mức đó đạt hoặc không đạt
```

Có thể có threshold mà không dùng AON, và có thể có AON với threshold nhiều chiều.

## 4. Ranh giới với escrow

```text
AON / KIA
→ logic phân bổ rủi ro và xử lý khi thiếu mục tiêu

[[Escrow]]
→ ai giữ tài sản trong thời gian chờ điều kiện
```

Escrow có thể thực hiện AON, nhưng không phải mọi AON đều cần nền tảng tự làm escrow.

## 5. So sánh

| Tiêu chí | All-or-nothing | Keep-it-all |
|---|---|---|
| Rủi ro thiếu vốn | Chủ yếu không chuyển sang dự án | Dự án/người hưởng lợi có thể phải chịu |
| Tín hiệu khả thi | Mạnh hơn nếu ngưỡng hợp lý | Yếu hơn nếu thiếu fallback rõ |
| Tốc độ sử dụng nguồn lực | Chờ ngưỡng | Có thể dùng sớm |
| Hoàn tiền/release | Cần rule rõ | Thường không hoàn chỉ vì thiếu mục tiêu |
| Phù hợp chi phí cố định lớn | Cao | Thấp |
| Phù hợp cứu trợ chia nhỏ | Có thể quá cứng | Thường phù hợp hơn |
| Áp lực đặt ngưỡng sai | Cao | Cao theo hướng overclaim partial scope |

## 6. Ai chịu rủi ro?

### Với AON

Contributor chịu:

- Thời gian chờ.
- Cơ hội bị khóa nếu tiền/reservation bị giữ.
- Rủi ro dự án đạt ngưỡng nhưng vẫn thất bại sau đó.

Dự án chịu:

- Không nhận nguồn lực nếu thiếu ngưỡng.
- Chi phí chuẩn bị chiến dịch không được bù.

### Với KIA

Contributor chịu:

- Dự án có thể thiếu nguồn lực để hoàn thành lời hứa.
- Partial scope có thể ít giá trị hơn kỳ vọng.

Dự án chịu:

- Nghĩa vụ giải thích và thực hiện với nguồn lực không đủ.
- Rủi ro danh tiếng nếu giữ tiền nhưng không tạo output có ý nghĩa.

## 7. Không chọn KIA chỉ vì “dễ gọi vốn”

KIA chỉ hợp lý nếu trả lời được:

```text
Mỗi mức nguồn lực tạo ra output gì?
Phần nào vẫn khả thi nếu thiếu mục tiêu?
Chi phí cố định đã được trang trải chưa?
Có nghĩa vụ nào phải hủy không?
Người góp có hiểu partial scope không?
Phần thiếu sẽ được bù từ đâu?
```

Không được dùng KIA để nhận tiền cho một dự án vốn không thể bắt đầu nếu thiếu ngưỡng.

## 8. Không chọn AON chỉ để tạo khẩn cấp

AON có thể bị lạm dụng để:

- Tạo countdown tâm lý.
- Đặt ngưỡng giả thấp để “thành công”.
- Đặt ngưỡng giả cao rồi hạ sau.
- Gọi mọi pledge là cam kết chắc chắn.
- Che việc provision point thực sự cao hơn.

Ngưỡng phải bắt nguồn từ execution model, không phải marketing.

## 9. Cơ chế hybrid

### Minimum viable tranche

```text
T0 đạt
→ mở scope tối thiểu

T1 đạt
→ mở module bổ sung

T2 đạt
→ full scope
```

### Phased all-or-nothing

Mỗi giai đoạn có provision point riêng, thay vì huy động toàn bộ dự án một lần.

### Flex funding với fallback đã công bố

Nếu không đạt full target, dự án chuyển sang một fallback scope xác định trước và cho contributor quyền rút khi thay đổi trọng yếu.

### Mixed resource activation

```text
Tiền
→ AON

Giờ mentor
→ reserve có điều kiện

Dữ liệu khảo sát
→ vẫn được ghi nhận nếu consent cho phép
```

Không mặc định mọi loại nguồn lực dùng cùng một rule.

## 10. AON với nguồn lực ngoài tiền

AON không chỉ là hoàn tiền:

```text
Không đạt provision point
→ release lịch chuyên gia
→ trả thiết bị về available
→ hủy venue reservation
→ đóng quyền truy cập dữ liệu tạm thời
→ không kích hoạt matching
```

Xem [[Resource pledge lifecycle]].

## 11. Rule khi đạt một phần

Một cơ chế phải nói rõ:

```text
Nếu đạt 90% thì sao?
Nếu đủ tiền nhưng thiếu giấy phép thì sao?
Nếu đủ người nhưng thiếu role blocking thì sao?
Nếu một nguồn lực rút sau deadline thì sao?
Có grace period không?
Có substitute rule không?
```

Không dùng một tổng phần trăm để che điều kiện hard threshold chưa đạt.

## 12. Refund và release

AON cần phân biệt:

```text
Authorization only
→ chưa thu tiền, chỉ hủy authorization

Funds held
→ hoàn tiền từ bên giữ

Resource reserved
→ release reservation

Resource delivered early
→ return, compensate hoặc xử lý theo agreement
```

Phải nói rõ phí, thời gian, chênh lệch tỷ giá và trường hợp hoàn một phần.

## 13. Change control

Sau khi nhận cam kết, thay đổi các yếu tố sau có thể cần tái đồng ý:

- Provision point.
- Scope.
- Deadline.
- Funding rule.
- Refund rule.
- Người giữ tiền.
- Loại reward hoặc contributor benefit.
- Bên nhận nguồn lực.

Không được đổi từ AON sang KIA âm thầm khi chiến dịch sắp hết hạn.

## 14. Data schema gợi ý

```text
funding_rule_id:
rule_type: AON | KIA | HYBRID
provision_point_id:
activation_time:
collection_method:
held_by:
partial_rule:
fallback_scope:
refund_rule:
release_rule:
fee_rule:
grace_period:
change_control:
status:
evidence_ids:
```

## 15. Checklist chọn cơ chế

1. Dự án có minimum viable scope không?
2. Thiếu bao nhiêu thì dự án mất khả thi?
3. Output có chia nhỏ độc lập không?
4. Ai chịu chi phí cố định?
5. Contributor đang mua, tặng, cho vay hay đầu tư?
6. Nguồn lực có bị giữ trong lúc chờ không?
7. Partial scope có được công bố rõ không?
8. Có nguồn lực blocking ngoài tiền không?
9. Refund/release có khả thi về vận hành và pháp lý không?
10. Có quyền rút khi thay đổi trọng yếu không?

## 16. Kết luận cho dự án

> **AON và KIA không chỉ là lựa chọn giao diện thanh toán. Chúng là cách phân bổ rủi ro thiếu nguồn lực giữa contributor, dự án và người hưởng lợi.**

## Khái niệm liên quan

- [[Cơ chế phối hợp tập thể - Bản đồ thuật ngữ]]
- [[Provision point và threshold mechanism]]
- [[Assurance contract và conditional pledge]]
- [[Conditional cooperation]]
- [[Escrow]]
- [[Resource pledge lifecycle]]
- [[Restricted funds]]
- [[Disbursement]]

## Nguồn tham khảo

- Mark Bagnoli & Barton Lipman — Provision of Public Goods, 1989: https://doi.org/10.2307/2297552
- Douglas Cumming, Gaël Leboeuf & Armin Schwienbacher — Crowdfunding Models: Keep-it-All vs. All-or-Nothing, 2020: https://doi.org/10.1111/fima.12262
