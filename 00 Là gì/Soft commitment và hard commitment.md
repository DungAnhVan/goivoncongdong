---
ai_authored: true
---

# Soft commitment và hard commitment

> **Định nghĩa ngắn:** *Soft commitment* là cam kết có thể rút lại với chi phí hoặc hậu quả thấp. *Hard commitment* là cam kết bị ràng buộc mạnh hơn bởi tiền, thời gian, nghĩa vụ, danh tiếng, quyền lợi bị khóa hoặc hậu quả rõ khi không thực hiện.

Trong dự án này, hai từ dùng để mô tả **độ ràng buộc của một cam kết**, không phải đánh giá đạo đức về người cam kết.

## 1. Trục phân loại

```text
Dễ đưa ra
→ dễ rút
→ ít hậu quả
→ soft commitment

Khó đưa ra
→ khó rút
→ có tài sản/nghĩa vụ đặt vào rủi ro
→ hard commitment
```

Độ cứng không chỉ phụ thuộc vào tiền.

## 2. Những thành phần tạo độ cứng

| Thành phần | Câu hỏi |
|---|---|
| Financial stake | Có tiền đặt cọc, trả trước hay phạt không? |
| Time stake | Đã dành lịch hoặc số giờ cụ thể chưa? |
| Resource reservation | Thiết bị, nhân lực hoặc địa điểm đã được giữ chưa? |
| Reputation stake | Tên hoặc uy tín có được công khai gắn vào cam kết không? |
| Legal obligation | Có hợp đồng hoặc nghĩa vụ pháp lý không? |
| Opportunity cost | Người cam kết có bỏ lựa chọn khác không? |
| Withdrawal friction | Rút lại có cần thông báo, phê duyệt hay chịu phí không? |
| Consequence | Không thực hiện thì điều gì xảy ra? |

## 3. Ví dụ theo phổ cam kết

```text
“Tôi thích ý tưởng này.”
→ rất mềm

“Tôi đăng ký nhận thông tin.”
→ mềm

“Tôi giữ lịch tham gia pilot hai ngày.”
→ mềm–trung bình

“Tôi ký LOI có điều kiện và dành ngân sách dự kiến.”
→ trung bình

“Tôi đặt cọc có điều kiện hoàn tiền rõ.”
→ cứng hơn

“Tôi chuyển giao thiết bị trong ba tháng.”
→ cứng

“Tôi ký hợp đồng mua hoặc đầu tư vốn.”
→ rất cứng về nghĩa vụ kinh tế/pháp lý
```

Không có ranh giới số học phổ quát. Phải mô tả cấu trúc cam kết thực tế.

## 4. Không đồng nhất với Commitment ladder

[[Commitment ladder]] hỏi:

> Hành vi thuộc loại Attention, Trial, Pre-commitment, Resource contribution hay Transaction?

File này hỏi:

> Cam kết đó bị ràng buộc mạnh đến đâu và có thể rút lại với hậu quả gì?

Ví dụ, hai hành vi đều là `Pre-commitment` nhưng độ cứng khác nhau:

```text
LOI không ràng buộc
→ soft pre-commitment

Đặt cọc 10% với điều kiện hoàn tiền xác định
→ harder pre-commitment
```

## 5. Không đồng nhất với costly signaling

Một hard commitment thường tạo tín hiệu mạnh hơn, nhưng không luôn như vậy.

```text
Hard commitment
→ mô tả cấu trúc ràng buộc

Costly signal
→ mô tả giá trị thông tin của hành vi trong bối cảnh bất cân xứng thông tin
```

Khoản đặt cọc có thể cứng nhưng không phải tín hiệu demand độc lập nếu do bên liên quan tài trợ.

Xem [[Costly signaling và cheap talk]].

## 6. Hard commitment không mặc nhiên tốt hơn

Cam kết quá cứng có thể:

- Loại trừ người thu nhập thấp.
- Ép người tham gia chịu rủi ro không cân xứng.
- Tạo rào cản vào pilot.
- Khiến người dùng sợ thử nghiệm.
- Biến đóng góp tự nguyện thành nghĩa vụ mơ hồ.
- Tăng tranh chấp khi điều kiện thay đổi.

Thiết kế phải tương xứng với:

```text
mức rủi ro của dự án
→ giá trị quyết định
→ khả năng hiểu điều kiện
→ quyền rút hợp lý
→ cơ chế hoàn trả
```

## 7. Soft commitment vẫn có giá trị

Soft commitment hữu ích để:

- Đo interest ban đầu.
- Xây cohort nghiên cứu.
- Mời người dùng thử.
- Ghi nhận ý định có điều kiện.
- Cho phép cộng đồng tham gia trước khi dự án đủ rõ.
- Tránh yêu cầu người yếu nguồn lực đặt tiền quá sớm.

Nó chỉ trở thành vấn đề khi bị trình bày như một hard commitment.

## 8. Commitment device khác commitment signal

Trong kinh tế học hành vi, *commitment device* thường là cơ chế một người dùng để ràng buộc hành vi tương lai của chính mình, ví dụ khóa tiền tiết kiệm hoặc đặt hình phạt.

Trong dự án này:

```text
Commitment record
→ ghi một người đã cam kết gì với dự án

Commitment device
→ cơ chế làm việc rút hoặc đổi hành vi trở nên khó hơn
```

Không dùng hai khái niệm thay thế nhau.

## 9. Trường dữ liệu bắt buộc

```text
commitment_id:
commitment_subject:
commitment_object:
conditions:
withdrawal_right:
withdrawal_process:
withdrawal_cost:
penalty_or_forfeiture:
refund_rule:
legal_status:
starts_at:
expires_at:
status:
```

Không nên chỉ lưu `hard = true/false`. Nên lưu các yếu tố tạo độ cứng để người khác đánh giá lại.

## 10. Gợi ý mức phân loại làm việc

```text
S0 — expression only
S1 — revocable without consequence
S2 — revocable with friction or reputation cost
S3 — resource reserved or deposit at risk
S4 — contractual or substantial economic obligation
```

Đây là mức nội bộ để thiết kế hệ thống, không phải chuẩn pháp lý.

## 11. Quy tắc hiển thị

Không viết:

> “500 người đã cam kết mua.”

Khi dữ liệu thực tế là:

```text
350 đăng ký quan tâm
100 LOI không ràng buộc
40 đặt cọc có hoàn lại
10 hợp đồng mua đã ký
```

Nên hiển thị từng lớp và điều kiện hoàn/rút.

## 12. Dấu hiệu cảnh báo

- Điều kiện rút nằm ở phần chữ nhỏ khó thấy.
- Dùng hard commitment trước khi offer đủ rõ.
- Không có refund rule.
- Không xác minh người cam kết có quyền đại diện tổ chức.
- Gọi pledge không ràng buộc là tiền đã huy động.
- Đẩy rủi ro dự án sang người yếu thế để tạo tín hiệu đẹp.
- Phạt rút lui ngay cả khi dự án thay đổi trọng yếu.

## 13. Kết luận cho dự án

> **Độ cứng của cam kết phải được mô tả bằng quyền, nghĩa vụ và hậu quả cụ thể; không được suy từ nhãn “đã cam kết”.**

## Khái niệm liên quan

- [[Thang cam kết và tín hiệu - Bản đồ thuật ngữ]]
- [[Commitment ladder]]
- [[Costly signaling và cheap talk]]
- [[Conditional cooperation]]
- [[Escrow]]
- [[Restricted funds]]

## Nguồn tham khảo

- Bryan, Karlan & Nelson — Commitment Devices, 2010: https://doi.org/10.1146/annurev.economics.102308.124324
- Burke, Luoto & Perez-Arce — Soft versus Hard Commitments, 2018: https://doi.org/10.1111/joca.12170
