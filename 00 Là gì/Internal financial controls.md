---
ai_authored: true
---

# Internal financial controls

> **Định nghĩa ngắn:** *Internal financial controls* là các quy tắc, phân quyền, bước kiểm tra và bằng chứng được thiết kế để bảo vệ tiền và tài sản, giúp số liệu đáng tin, ngăn một người kiểm soát toàn bộ giao dịch và phát hiện sai sót hoặc gian lận đủ sớm.

Có thể dịch là **kiểm soát tài chính nội bộ**.

## 1. Kiểm soát không đồng nghĩa với không tin nhau

Một hệ thống tốt không dựa trên giả định rằng mọi người xấu. Nó dựa trên thực tế rằng:

- Người tốt vẫn có thể nhầm.
- Tài khoản có thể bị chiếm quyền.
- Chứng từ có thể thất lạc.
- Áp lực tiến độ có thể khiến nhóm bỏ quy trình.
- Xung đột lợi ích có thể không được nhận ra.
- Một người nắm quá nhiều quyền có thể trở thành điểm thất bại duy nhất.

> Kiểm soát bảo vệ cả người góp, dự án và chính người đang giữ trách nhiệm tài chính.

## 2. Bốn mục tiêu chính

```text
Bảo vệ tài sản
+ số liệu chính xác và kịp thời
+ giao dịch đúng thẩm quyền, mục đích
+ sai lệch được phát hiện và xử lý
```

Theo Charity Commission của Anh, financial controls giúp bảo vệ tiền và tài sản, cung cấp thông tin để ra quyết định, quản lý rủi ro, giữ hồ sơ kế toán tốt và duy trì niềm tin công chúng.

## 3. Segregation of duties — phân tách nhiệm vụ

Nguyên tắc cốt lõi:

```text
Người tạo giao dịch
≠ người phê duyệt
≠ người thực hiện chuyển tiền
≠ người ghi sổ
≠ người đối soát
```

Trong tổ chức nhỏ, không phải lúc nào cũng tách được năm người. Khi đó cần **compensating controls** — kiểm soát bù trừ:

- Hai thành viên xem báo cáo giao dịch hằng tháng.
- Mọi khoản trên ngưỡng phải có hai phê duyệt.
- Người ngoài giao dịch kiểm tra bank reconciliation.
- Công khai chứng từ và số dư theo dự án.
- Kiểm tra đột xuất.
- Đổi người rà soát theo kỳ.

## 4. Authorization — thẩm quyền phê duyệt

Mỗi hành động phải có giới hạn rõ:

| Hành động | Ai được làm? | Ai phê duyệt? |
|---|---|---|
| Tạo/chỉnh tài khoản ngân hàng | Người được ủy quyền | Hội đồng hoặc hai người |
| Thêm người thụ hưởng | Nhân sự vận hành | Người độc lập xác minh |
| Đề nghị chi | Chủ ngân sách | Người có authority limit |
| Chuyển tiền | Người vận hành ngân hàng | Người phê duyệt thứ hai |
| Thay đổi ngân sách | Chủ dự án | Hội đồng theo ngưỡng |
| Xóa/điều chỉnh giao dịch | Kế toán | Có log và người duyệt |
| Hoàn tiền | Hỗ trợ/vận hành | Theo chính sách và đối soát |

[[Delegation of authority]] nên ghi ngưỡng theo giá trị, loại giao dịch và mức rủi ro.

## 5. Dual authorization — hai bước phê duyệt

Online banking nên có cấu trúc:

```text
Maker
→ tạo lệnh

Checker/Approver
→ kiểm tra người nhận, số tiền, mục đích và bằng chứng
→ phê duyệt
```

Hai người dùng chung mật khẩu không phải dual authorization. Mỗi người phải dùng danh tính và quyền truy cập riêng.

## 6. Reconciliation — đối soát

[[Reconciliation]] là việc so sánh các nguồn dữ liệu độc lập để tìm sai lệch.

### Bank reconciliation

```text
Số dư ngân hàng
↔ sổ kế toán
↔ danh sách giao dịch nền tảng
↔ số dư từng project/fund
```

Phải giải thích được:

- Giao dịch đang chờ.
- Phí ngân hàng/thanh toán.
- Hoàn tiền.
- Khoản thu chưa gắn dự án.
- Thanh toán bị thất bại.
- Chênh lệch tỷ giá.
- Sai mã giao dịch.

Người thực hiện đối soát không nên là người duy nhất kiểm soát tài khoản; nên có người thứ hai rà soát.

## 7. Audit trail — dấu vết kiểm toán

Mỗi giao dịch cần trả lời được:

```text
Ai đề nghị?
Ai kiểm tra?
Ai duyệt?
Ai thực hiện?
Khi nào?
Dựa vào ngân sách nào?
Mục đích và restriction nào?
Chứng từ ở đâu?
Dữ liệu đã bị sửa lần nào?
Kết quả cuối cùng là gì?
```

Hệ thống không nên cho sửa lịch sử mà không lưu phiên bản. “Đã xóa giao dịch sai” làm mất dấu vết; cách tốt hơn là reversal/adjustment có lý do và người phê duyệt.

## 8. Kiểm soát thu tiền

- Xác định kênh nhận tiền được phép.
- Xác minh tài khoản và cổng thanh toán.
- Ghi nhận gross amount, fee và net amount riêng.
- Đối soát danh sách người góp với settlement của cổng thanh toán.
- Hai người cùng kiểm đếm tiền mặt nếu có.
- Có policy nhận, từ chối và hoàn lại khoản đóng góp.
- Kiểm tra donor hoặc nguồn tiền khi rủi ro yêu cầu.
- Không dùng tiền thu được trước khi biết nó thuộc fund nào.

## 9. Kiểm soát chi tiền

Mô hình kiểm tra ba chiều (*three-way match*) đáng học:

```text
Đơn đặt hàng/hợp đồng
↔ bằng chứng đã nhận hàng/dịch vụ
↔ hóa đơn
```

Chỉ có hóa đơn chưa đủ. Cần biết:

- Có thực sự đặt hàng không?
- Hàng/dịch vụ đã nhận chưa?
- Giá và số lượng có khớp không?
- Người bán có phải bên liên quan không?
- Khoản chi có thuộc ngân sách và [[Restricted funds|restriction]] không?

## 10. Related-party transaction

Giao dịch với founder, thành viên hội đồng, người thân hoặc công ty liên quan không mặc nhiên bị cấm, nhưng phải:

- Khai báo quan hệ.
- Ghi vào register of interests.
- Người có lợi ích không tham gia quyết định.
- So sánh giá hoặc chứng minh tính hợp lý.
- Lưu biên bản.
- Công bố khi trọng yếu.

Xem: [[Conflict of interest]], [[Related-party transaction]].

## 11. Kiểm soát quyền truy cập số

- Mỗi người có tài khoản riêng.
- Bật MFA.
- Không chia sẻ mật khẩu/PIN.
- Quyền tối thiểu cần thiết.
- Thu hồi quyền ngay khi người rời nhóm.
- Danh sách người có quyền được rà soát định kỳ.
- Thiết bị truy cập ngân hàng phải được bảo vệ.
- Thay đổi thông tin người nhận cần xác minh ngoài kênh email nếu giá trị lớn.
- Log truy cập và thay đổi phải được giữ.

## 12. Kiểm soát tối thiểu cho dự án pilot

```text
1 tài khoản hoặc cơ chế nhận tiền được công bố
+ ledger riêng cho từng dự án
+ ngân sách được duyệt
+ hai bước cho thanh toán trọng yếu
+ chứng từ tập trung
+ bank reconciliation hằng tháng
+ một người thứ hai rà soát
+ báo cáo thu, chi, số dư và milestone
+ register of interests
+ quy tắc hoàn tiền và tiền dư
```

Không cần dựng bộ máy ngân hàng ngay, nhưng không được để một người nhận tiền, tự chi, tự ghi sổ và tự báo cáo.

## 13. Control matrix cho nền tảng

| Rủi ro | Kiểm soát phòng ngừa | Kiểm soát phát hiện |
|---|---|---|
| Chuyển sai tài khoản | Xác minh payee, whitelist | Rà soát settlement/bank |
| Chi sai mục đích | Budget + restriction check | Báo cáo variance |
| Tạo nhà cung cấp giả | Due diligence, dual approval | Phân tích giao dịch bất thường |
| Chi trùng | Mã hóa đơn duy nhất | Duplicate check |
| Founder tự trả cho mình | Conflict declaration | Related-party report |
| Tiền chiến dịch bị dùng vận hành | Segregation + ledger | Fund balance reconciliation |
| Sửa lịch sử | Append-only audit log | Review change log |
| Milestone giả | Người xác nhận độc lập | Kiểm tra mẫu/đột xuất |

## 14. Khi nào phải nâng cấp kiểm soát?

- Tổng tiền tăng mạnh.
- Bắt đầu nhận tiền công chúng.
- Có nhiều dự án đồng thời.
- Hoạt động qua nhiều quốc gia/tiền tệ.
- Có khoản vay hoặc đầu tư.
- Có nhân viên được trả lương từ quỹ.
- Xuất hiện giao dịch bên liên quan.
- Từng có sai lệch hoặc gần xảy ra mất tiền.
- Bắt đầu tích hợp cổng thanh toán/API tự động.

Kiểm soát phải được rà soát ít nhất theo kỳ và sau thay đổi lớn hoặc sự cố.

## 15. Kết luận cho dự án

> **Minh bạch là cho người khác nhìn thấy; kiểm soát nội bộ là làm cho giao dịch sai khó xảy ra và dễ bị phát hiện.**

Nền tảng cần cả hai. Công khai ảnh hóa đơn sau khi tiền đã bị dùng sai không thay thế một quy trình phê duyệt, tách quyền và đối soát tốt.

## Khái niệm liên quan

- [[Tài chính và quản lý quỹ - Bản đồ thuật ngữ]]
- [[Fund management]]
- [[Custody và safeguarding]]
- [[Restricted funds]]
- [[Disbursement]]
- [[Delegation of authority]]
- [[Reconciliation]]
- [[Audit trail]]
- [[Conflict of interest]]
- [[Related-party transaction]]
- [[Independent audit]]

## Nguồn tham khảo

- Charity Commission — Internal financial controls for charities: https://www.gov.uk/government/publications/internal-financial-controls-for-charities-cc8/internal-financial-controls-for-charities
- FCA Handbook — client money: https://handbook.fca.org.uk/glossary/G160
