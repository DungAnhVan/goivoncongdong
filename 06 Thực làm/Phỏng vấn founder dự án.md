---
ai_authored: true
type: giao-thuc
status: chot-tam-cho-pilot
updated: 2026-08-30
review_trigger: sau-3-ca-thuc-hoac-truoc-2026-10-01
tags:
  - goi-von-cong-dong
  - founder
  - phong-van
  - ca-thuc
  - hien-chuong
  - pilot
---

# Phỏng vấn founder dự án

> [!abstract] Địa vị của tài liệu
> Đây là giao thức tiếp nhận **một ca thực** vào Samsti. Trong ngôn ngữ của [[Vai trò và cặp vai bị cấm]], founder là **người mang ca thực**; người phỏng vấn là người thu thập và **soạn dẫn** từ ca thực về tiên đề.
>
> Founder không cần biết mã tiên đề. Rào cản đầu vào phải thấp. Nhưng phía Samsti không được giữ một câu hỏi nếu không chỉ ra được nó được suy từ tiên đề nào.
>
> Toàn bộ tầng hiến chương hiện còn ở trạng thái chờ phê chuẩn, vì vậy giao thức này được **chốt tạm cho pilot** và phải xem lại sau ba ca phỏng vấn thật hoặc trước ngày 01/10/2026, tùy điều kiện nào đến trước.

## 1. Quy tắc vô hiệu

> [!warning] Không truy nguyên được thì bỏ
> Một câu hỏi không chỉ ra được mã **LC-xx**, **TĐ-xx** hoặc một bước cụ thể của [[Giao thức suy dẫn luật]] là câu hỏi tiện tay, không thuộc giao thức này.
>
> Không được nghĩ ra một bộ thẩm định startup thông thường rồi dán mã tiên đề vào sau. Chuỗi đúng phải là:
>
> **tiên đề → kịch bản vi phạm cần ngăn → câu hỏi → bằng chứng → quyết định bị chặn**

Bộ câu hỏi không dùng để chấm founder nói hay, có “máu” hay, học trường nào hoặc làm slide đẹp đến đâu. Nó dùng để xác định Samsti có cơ sở chính đáng cho **quyết định kế tiếp** hay chưa.

## 2. Phân vai trong một ca phỏng vấn

| Chức năng trong ca | Vai theo Hiến chương | Được làm | Không được làm |
|---|---|---|---|
| Founder/chủ dự án | Người mang ca thực | Kể ca, đưa claim, bằng chứng và giới hạn | Tự xác nhận ca của mình đã đạt |
| Người phỏng vấn | Người soạn dẫn | Hỏi, ghi claim, nối câu trả lời về tiên đề, đề xuất bước tiếp | Tự kiểm hợp hiến đề xuất do mình soạn |
| Người phản biện | Người phản biện | Tìm cách bẻ kết luận hoặc pilot được đề xuất | Trùng với người soạn dẫn trong cùng ca |
| Người kiểm | Verifier/người kiểm hợp hiến phù hợp phạm vi | Kiểm claim, evidence requirement hoặc chuỗi suy dẫn | Sửa câu trả lời để giúp ca “đạt” |
| Người giữ hồ sơ | Người giữ sổ | Cấp mã CA-xxx, giữ phiên bản, ghi ai làm vai nào | Ra quyết định về ca |

Một người có thể hỗ trợ nhiều việc, nhưng các cặp vai bị cấm vẫn áp **theo từng ca**. Người phỏng vấn có thể đề xuất “pilot này có thể chạy”, nhưng không được một mình biến đề xuất đó thành kết luận cuối.

## 3. Bản đồ truy nguyên

### 3.1. Sáu lõi cứng — cửa phủ quyết

Lõi cứng không phải sáu chủ đề để cân điểm. Một vi phạm đã xác định là đủ để dừng quyết định liên quan.

| Tiên đề | Giao thức phải phát hiện | Câu hỏi chính | Quyết định bị chặn nếu chưa rõ |
|---|---|---|---|
| **LC-01 — Không chiếm dụng** | Nguồn lực bị coi thành tài sản tự do của người giữ | Q23–Q25, Q29 | Nhận, giữ hoặc giải ngân nguồn lực |
| **LC-02 — Không gian lận** | Bằng chứng giả, người góp giả, bên liên quan bị che | Q2, Q8, Q20–Q23, Q26 | Gắn nhãn verified, hiển thị social proof, mở rộng huy động |
| **LC-03 — Không tự phán** | Người hưởng lợi tự xác nhận điều kiện có lợi cho mình | Q25–Q27 | Nghiệm thu, giải ngân, kết luận đạt |
| **LC-04 — Không hồi tố bất lợi, không hạ chuẩn sau kết quả** | Đổi ngưỡng hoặc tiêu chí sau khi biết kết quả | Q22, Q27–Q28 | Công nhận test, milestone hoặc amendment |
| **LC-05 — Không xâm phạm phẩm giá để huy động** | Cưỡng ép, gây xấu hổ, phơi bày dữ liệu hoặc nỗi đau | Q11–Q12, Q29 | Công bố câu chuyện, dữ liệu hoặc mở chiến dịch |
| **LC-06 — Không lời hứa không thể phản bác** | Claim không có cách chứng minh sai | Q7–Q8, Q22, Q26–Q27 | Công nhận outcome, milestone hoặc success |

“Chưa rõ” không có nghĩa founder đã vi phạm. Nó có nghĩa Samsti **chưa được phép ra quyết định** dựa trên phần đó.

### 3.2. Mười hai tiên đề vòng ngoài — đường hình thành dự án

| Miền | Tiên đề | Câu hỏi |
|---|---|---|
| Mục đích | **TĐ-01** Nghĩa vụ giải thích trước quyền huy động | Q1–Q4 |
| Mục đích | **TĐ-02** Công ích phải có biên giới | Q5–Q6 |
| Mục đích | **TĐ-03** Lời hứa tác động phải phản bác được | Q7–Q8 |
| Quan hệ | **TĐ-04** Đóng góp là gia nhập một quan hệ | Q9–Q10 |
| Quan hệ | **TĐ-05** Ghi nhận phục vụ phẩm giá | Q11–Q12 |
| Quan hệ | **TĐ-06** Sự đáp lại hữu hạn và xác định | Q13–Q14 |
| Điều phối | **TĐ-07** Thiện chí thành cam kết có điều kiện | Q15–Q16 |
| Điều phối | **TĐ-08** Cơ chế phù hợp cách thiện ích được sản xuất | Q17–Q19 |
| Điều phối | **TĐ-09** Cộng đồng không đồng nhất tổng tiền | Q20–Q21 |
| Quản trị | **TĐ-10** Quỹ là lời hứa được vật chất hóa | Q23–Q24 |
| Quản trị | **TĐ-11** Người giữ tiền là quản thác của mục đích | Q25–Q26 |
| Quản trị | **TĐ-12** Thất bại được quản trị trước khi xảy ra | Q27–Q29 |

Q22 nối miền mục đích với điều phối bằng một pilot có thể phản bác. Q30 dùng bước B4–B6 của giao thức suy dẫn để chọn hành động tiếp theo nhẹ nhất, kiểm tra được và có tỷ lệ.

## 4. Cách nói với founder

Không đọc mã tiên đề trong lúc hỏi, trừ khi founder muốn biết. Người phỏng vấn hỏi bằng ngôn ngữ đời thường và ghi mã ở biên bản nội bộ.

> Buổi hôm nay chưa phải quyết định gọi vốn. Samsti muốn hiểu dự án như một ca thật: trạng thái anh/chị muốn tạo ra, ai chịu tác động, bằng chứng nào đã có, quan hệ nào sẽ hình thành nếu nhận đóng góp và cách xử lý nếu mọi việc không diễn ra như dự kiến. “Chưa biết” là câu trả lời hợp lệ. Phần chưa biết sẽ trở thành việc cần kiểm tra, không bị kể thành điều đã chứng minh.

## 5. Bộ 30 câu hỏi có truy nguyên

### I. Mục đích — TĐ-01 đến TĐ-03

**Q1. Dự án muốn biến trạng thái nào thành trạng thái nào, cho ai, ở đâu và trong khoảng thời gian nào?**

- **Truy nguyên:** TĐ-01.
- **Bằng chứng cần xem:** mô tả hiện trạng, phạm vi, dữ liệu nền hoặc quan sát có ngày.
- **Ngăn/chặn:** tránh xin nguồn lực cho một mục tiêu chỉ có khẩu hiệu; chưa rõ thì chưa bàn ngân sách.

**Q2. Bằng chứng trực tiếp nhất cho thấy nhu cầu này có thật và đủ đáng kể là gì?**

- **Truy nguyên:** TĐ-01; kiểm LC-02.
- **Bằng chứng cần xem:** dữ liệu vận hành, quan sát hiện trường, phỏng vấn có phương pháp, hành vi tự xoay xở, hàng chờ, chi phí hoặc khiếu nại; ghi nguồn và ngày.
- **Ngăn/chặn:** tránh biến trực giác của founder thành nhu cầu của cộng đồng; chưa đủ thì chỉ được quyết định làm proof of need.

**Q3. Người liên quan hiện xử lý vấn đề bằng cách nào, và cách hiện tại thiếu gì?**

- **Truy nguyên:** TĐ-01.
- **Bằng chứng cần xem:** quy trình hiện tại, chi phí, thời gian, thất bại, mức hài lòng và switching cost.
- **Ngăn/chặn:** tránh huy động cho giải pháp không tốt hơn phương án đang có.

**Q4. Founder và đội ngũ hiện có khả năng thực hiện phần nào, phần nào mới là giả định và phần nào chưa có owner?**

- **Truy nguyên:** TĐ-01 — nghĩa vụ giải thích cả năng lực, không chỉ mục tiêu.
- **Bằng chứng cần xem:** việc đã làm, prototype, lịch sử thực hiện, thời gian cam kết, quyền sử dụng công nghệ và khoảng trống năng lực.
- **Ngăn/chặn:** chưa được trình bày một khả năng dự kiến như năng lực đã tồn tại.

**Q5. Ai thuộc cộng đồng hưởng lợi, ai không thuộc, và tiêu chí biên giới là gì?**

- **Truy nguyên:** TĐ-02.
- **Bằng chứng cần xem:** actor map, địa lý, thời gian, tiêu chí eligibility và quy mô sơ bộ.
- **Ngăn/chặn:** không được dùng chữ “cộng đồng” nếu chưa chỉ ra cộng đồng nào.

**Q6. Ai có thể chịu ngoại tác, bị loại khỏi lợi ích hoặc bị ảnh hưởng dù không tham gia, và họ có quyền lên tiếng bằng cách nào?**

- **Truy nguyên:** TĐ-02; kiểm LC-05.
- **Bằng chứng cần xem:** affected-community map, consent/consultation record, grievance route.
- **Ngăn/chặn:** chưa được gọi là công ích nếu chỉ nhìn người hưởng lợi và bỏ người chịu tác động.

**Q7. Dự án đang hứa output và outcome nào; mỗi claim có đơn vị, đối tượng và cửa sổ thời gian gì?**

- **Truy nguyên:** TĐ-03; LC-06.
- **Bằng chứng cần xem:** claim register, baseline, indicator, target, thời gian và phạm vi.
- **Ngăn/chặn:** claim kiểu “nâng cao nhận thức”, “tạo tác động” chưa được dùng làm tiêu chí thành công.

**Q8. Kết quả hoặc bằng chứng nào sẽ khiến anh/chị thừa nhận claim sai, nhỏ hơn dự kiến hoặc cần dừng?**

- **Truy nguyên:** TĐ-03; LC-02; LC-06.
- **Bằng chứng cần xem:** falsification condition, negative evidence, excluded cases và limitation.
- **Ngăn/chặn:** không có điều kiện phản bác thì không được công nhận claim đạt.

### II. Quan hệ — TĐ-04 đến TĐ-06

**Q9. Mỗi loại người tham gia đang làm gì: tặng, đặt trước, mua, cho vay, đầu tư, góp công, góp thiết bị hay cấp quyền tiếp cận?**

- **Truy nguyên:** TĐ-04.
- **Bằng chứng cần xem:** actor-role map và contribution type cho từng nhóm.
- **Ngăn/chặn:** không được gom các quan hệ pháp lý và đạo đức khác nhau vào một nút “ủng hộ”.

**Q10. Với từng loại quan hệ, họ nhận quyền gì, chịu rủi ro gì, được rút khi nào và không có quyền gì?**

- **Truy nguyên:** TĐ-04.
- **Bằng chứng cần xem:** điều khoản, benefit, risk disclosure, withdrawal rule và quyền khiếu nại.
- **Ngăn/chặn:** chưa được nhận cam kết khi bản chất quan hệ chưa được nói rõ.

**Q11. Người góp được lựa chọn hiển thị danh tính, số tiền và hình thức ghi nhận như thế nào?**

- **Truy nguyên:** TĐ-05; kiểm LC-05.
- **Bằng chứng cần xem:** lựa chọn opt-in/opt-out, chế độ ẩn danh/nhóm/công khai và cách đổi lựa chọn.
- **Ngăn/chặn:** không được dùng công khai mặc định hoặc bảng xếp hạng để tạo áp lực.

**Q12. Câu chuyện hoặc bằng chứng nào liên quan người thụ hưởng là nhạy cảm; ai đồng ý cho sử dụng và có cách nhẹ hơn để chứng minh claim không?**

- **Truy nguyên:** TĐ-05; LC-05; bước B4 xâm hại tối thiểu.
- **Bằng chứng cần xem:** consent, data minimization, access level, redaction và phương án thay thế.
- **Ngăn/chặn:** không được đổi phẩm giá và riêng tư lấy sức mạnh truyền thông.

**Q13. Dự án hứa đáp lại người góp điều gì, với phạm vi và giới hạn nào?**

- **Truy nguyên:** TĐ-06.
- **Bằng chứng cần xem:** reward/benefit schedule, nghĩa vụ, điều kiện fulfil và giới hạn quyền lực của người góp.
- **Ngăn/chặn:** quà tặng không được âm thầm tạo quyền chi phối dự án hoặc người nhận.

**Q14. Quan hệ đó kết thúc khi nào; sau khi đóng dự án còn nghĩa vụ báo cáo, giao hàng, bảo hành, dữ liệu hoặc quyền biểu quyết nào?**

- **Truy nguyên:** TĐ-06; hỗ trợ TĐ-12.
- **Bằng chứng cần xem:** thời hạn, closure condition, surviving obligations và record retention.
- **Ngăn/chặn:** không để nghĩa vụ hoặc quyền lực tồn tại vô thời hạn vì chưa ai viết điểm kết thúc.

### III. Điều phối — TĐ-07 đến TĐ-09

**Q15. Sau khi thấy một offer đủ cụ thể, người thuộc đúng nhóm mục tiêu đã thực hiện hành vi gì?**

- **Truy nguyên:** TĐ-07.
- **Bằng chứng cần xem:** offer version, giá/nghĩa vụ, hành vi, ngày, quyền rút và evidence record.
- **Ngăn/chặn:** lượt thích, lời khen và đăng ký nhận tin không được kể thành cam kết giao dịch.

**Q16. Cam kết chỉ được kích hoạt khi điều kiện nào đạt; trước thời điểm đó người tham gia còn quyền gì?**

- **Truy nguyên:** TĐ-07.
- **Bằng chứng cần xem:** conditional pledge, activation event, withdrawal/release rule, deadline và người xác minh.
- **Ngăn/chặn:** thiện chí chưa đạt điều kiện không được biến sớm thành nguồn lực không thể đảo ngược.

**Q17. Thiện ích của dự án được sản xuất liên tục, chia nhỏ được hay chỉ có giá trị khi đủ một chi phí cố định?**

- **Truy nguyên:** TĐ-08.
- **Bằng chứng cần xem:** cost structure, minimum viable scope, dependency và partial-delivery value.
- **Ngăn/chặn:** chưa được chọn cơ chế huy động trước khi hiểu công nghệ sản xuất của dự án.

**Q18. Tổ hợp nguồn lực tối thiểu để dự án tạo được giá trị là gì?**

- **Truy nguyên:** TĐ-08; hỗ trợ TĐ-07.
- **Bằng chứng cần xem:** provision point gồm tiền, người, thiết bị, địa điểm, dữ liệu, access, giấy phép, deadline và blocking conditions.
- **Ngăn/chặn:** không được chỉ đặt một con số tiền nếu thiếu một nguồn lực khác vẫn làm dự án bất khả thi.

**Q19. All-or-nothing, keep-it-all hay hybrid phù hợp hơn, và rủi ro thiếu nguồn lực được đặt lên ai?**

- **Truy nguyên:** TĐ-08.
- **Bằng chứng cần xem:** mechanism rationale, fallback scope, partial-achievement rule và phân bổ rủi ro.
- **Ngăn/chặn:** không được chọn cơ chế chỉ vì nó dễ truyền thông hoặc giữ được nhiều tiền hơn.

**Q20. Dự án có bao nhiêu người độc lập tham gia, thay vì chỉ có tổng bao nhiêu tiền?**

- **Truy nguyên:** TĐ-09.
- **Bằng chứng cần xem:** unique actor count, distribution, concentration và top-contributor share.
- **Ngăn/chặn:** một khoản lớn từ một người không được kể thành sự đồng thuận của cộng đồng.

**Q21. Có người liên quan, tài khoản chia nhỏ, cam kết được hoàn lại ngầm hoặc lợi ích nào làm méo tín hiệu không?**

- **Truy nguyên:** TĐ-09; LC-02.
- **Bằng chứng cần xem:** related-party disclosure, identity/uniqueness control có tỷ lệ, benefit received và source of contribution.
- **Ngăn/chặn:** chưa được hiển thị social proof hoặc matching theo số người khi chưa kiểm soát tính độc lập phù hợp.

**Q22. Pilot nhỏ nhất nào sẽ kiểm tra giả định trọng yếu, với ngưỡng tiếp tục/sửa/dừng được viết trước?**

- **Truy nguyên:** TĐ-01, TĐ-03, TĐ-07, TĐ-08; LC-04; LC-06.
- **Bằng chứng cần xem:** protocol có population, intervention/offer, thời gian, threshold, exclusions, evidence và decision rule.
- **Ngăn/chặn:** không được đổi tiêu chí sau kết quả hoặc gọi một hoạt động không thể phản bác là pilot thành công.

### IV. Quản trị — TĐ-10 đến TĐ-12

**Q23. Với mỗi nguồn lực, có truy được nguồn, trạng thái, quyền sử dụng, đích đến và bằng chứng không?**

- **Truy nguyên:** TĐ-10; kiểm LC-01 và LC-02.
- **Bằng chứng cần xem:** resource/fund ledger, provenance, trạng thái promised–reserved–received–used–returned và evidence ID.
- **Ngăn/chặn:** không nhận hoặc hiển thị một nguồn lực không truy được bản chất và trạng thái.

**Q24. Ngân sách được tính sau khi xác định nhu cầu và cơ chế như thế nào; khoản nào được chi, không được chi, phí và dự phòng ra sao?**

- **Truy nguyên:** TĐ-10, TĐ-11, trở lại trình tự TĐ-01.
- **Bằng chứng cần xem:** budget line, basis/quote, restriction, contingency, fee treatment và biên độ điều chỉnh.
- **Ngăn/chặn:** không bắt đầu bằng số tiền muốn gọi rồi tìm câu chuyện để hợp thức hóa.

**Q25. Ai giữ tiền hoặc tài sản, và điều gì chứng minh người giữ chỉ quản thác mục đích chứ không sở hữu tự do?**

- **Truy nguyên:** TĐ-11; LC-01.
- **Bằng chứng cần xem:** custody/safeguarding arrangement, account ownership, restriction source, reconciliation và residual rule.
- **Ngăn/chặn:** chưa được chuyển nguồn lực nếu quyền kiểm soát kỹ thuật có thể biến thành quyền đổi mục tiêu.

**Q26. Ai đề nghị chi, ai phê duyệt, ai chuyển, ai ghi sổ và ai xác nhận milestone?**

- **Truy nguyên:** TĐ-11; LC-03; [[Vai trò và cặp vai bị cấm]].
- **Bằng chứng cần xem:** role matrix, prohibited overlaps, conflict disclosure, verification protocol và disbursement rule.
- **Ngăn/chặn:** founder/người nhận nguồn lực không được là người duy nhất tự xác nhận điều kiện nhận tiếp nguồn lực.

**Q27. Tiêu chí, bằng chứng yêu cầu và người kiểm đã được ghi trước khi xem kết quả chưa?**

- **Truy nguyên:** TĐ-03; LC-04; LC-06.
- **Bằng chứng cần xem:** timestamped protocol, version, acceptance criteria, missing-data rule và reviewer identity.
- **Ngăn/chặn:** tiêu chí viết sau hoặc hạ sau kết quả không được dùng để công nhận milestone.

**Q28. Thay đổi nào là nhỏ, thay đổi nào là trọng yếu; ai đánh giá và khi nào phải xin re-consent?**

- **Truy nguyên:** TĐ-04, TĐ-12; LC-04.
- **Bằng chứng cần xem:** material-change rule, amendment/version history, notification, re-consent và withdrawal route.
- **Ngăn/chặn:** không được dùng quyền vận hành để đổi mục đích hoặc quan hệ đã cam kết.

**Q29. Nếu không đạt ngưỡng, chậm, thất bại, còn dư nguồn lực hoặc phát sinh tranh chấp thì điều gì xảy ra?**

- **Truy nguyên:** TĐ-12; hỗ trợ TĐ-06; kiểm LC-01 và LC-05.
- **Bằng chứng cần xem:** pause, recovery, termination, refund/release, residual, closure và grievance rules.
- **Ngăn/chặn:** chưa mở huy động nếu chỉ có success path mà không có failure path tương xứng.

**Q30. Quyết định nhỏ nhất Samsti nên đưa ra sau buổi này là gì, và có phương án nhẹ hơn đạt cùng mục tiêu không?**

- **Truy nguyên:** TĐ-01; bước B4 xâm hại tối thiểu, B5 kiểm tra được và B6 tỷ lệ.
- **Bằng chứng cần xem:** next test, owner, deadline, output, decision rule, quy mô tiền, khả năng đảo ngược và mức dễ tổn thương.
- **Ngăn/chặn:** không biến khoảng trống thông tin nhỏ thành yêu cầu hồ sơ quá mức; cũng không dùng pilot nhỏ để hợp thức hóa quyết định lớn.

## 6. Chạy phép kiểm suy dẫn sau phỏng vấn

Người phỏng vấn không được kết luận chỉ bằng cảm giác. Mọi đề xuất tiếp theo phải chạy sáu bước:

### B1 — Truy nguyên

Liệt kê các tiên đề thực sự bị kích hoạt bởi ca. Không cần kéo đủ 18 tiên đề nếu ca chưa chạm tới chúng.

### B2 — Cần thiết

Viết một kịch bản cụ thể cho từng yêu cầu mới:

~~~text
Nếu không yêu cầu ___,
actor ___ có thể làm ___,
khiến actor ___ chịu ___,
và chỉ bị phát hiện khi ___.
~~~

Không viết “để tăng minh bạch” hoặc “để chuyên nghiệp hơn”.

### B3 — Kiểm sáu lõi cứng

Với từng LC, ghi **không kích hoạt / chưa rõ / đạt / có dấu hiệu vi phạm / vi phạm đã xác định**.

- “Chưa rõ” → chặn quyết định liên quan, yêu cầu bằng chứng có tỷ lệ.
- “Có dấu hiệu” → nâng mức kiểm tra, chưa kết tội.
- “Vi phạm đã xác định” → dừng; không cân lợi ích để cho qua.

### B4 — Xâm hại tối thiểu

Tìm ít nhất một cách nhẹ hơn để giảm cùng rủi ro.

Ví dụ: nếu cần xác nhận có nhu cầu, trước tiên chạy một demand test nhỏ; không bắt founder làm ngay bộ hồ sơ gọi vốn đầy đủ. Nếu cần kiểm một milestone kỹ thuật nhỏ, dùng một reviewer độc lập phù hợp; không mặc định thuê kiểm toán toàn diện.

### B5 — Kiểm tra được

Bước tiếp theo phải có:

- giá trị hoặc trạng thái cần quan sát;
- đơn vị;
- cửa sổ thời gian;
- bằng chứng;
- người kiểm;
- người không được kiểm;
- kết quả nào dẫn tới quyết định nào.

### B6 — Tỷ lệ

Xét đồng thời:

1. Quy mô nguồn lực.
2. Khả năng đảo ngược.
3. Mức dễ tổn thương của người chịu tác động.
4. Bất cân xứng thông tin.
5. Mức trọng yếu nếu claim sai.

Không áp bộ máy của chiến dịch lớn lên một pilot nhỏ; không hạ chuẩn cho một quyết định lớn chỉ vì founder là người quen hoặc kể chuyện thuyết phục.

## 7. Kết quả hợp lệ của một ca

| Kết quả | Khi dùng | Ý nghĩa |
|---|---|---|
| **Hoãn vì thiếu ca thực/bằng chứng** | Chưa đủ dữ liệu để suy dẫn | Không bác bỏ dự án; ghi điều kiện kích hoạt lại |
| **Đề xuất test** | Có một bất định chính và cách kiểm nhẹ | Chưa nhận nguồn lực cho triển khai rộng |
| **Đề xuất pilot chốt tạm** | B1–B5 đạt, B6 đủ cho pilot | Phải có phạm vi và ngày hết hạn xem lại |
| **Chuyển phản biện độc lập** | Đã có đề xuất pilot/quy tắc cụ thể | Người soạn dẫn không tự phản biện |
| **Hold** | Rủi ro integrity, pháp lý, an toàn hoặc phẩm giá chưa đủ rõ | Dừng quyết định có thể gây hại, không kết tội khi chưa xác minh |
| **Dừng do vi phạm lõi cứng** | Có bằng chứng xác định một LC bị vi phạm | Không cân bằng bằng lợi ích hoặc tiềm năng |

Không dùng một tổng điểm để cho phép một điểm mạnh bù một vi phạm lõi cứng.

## 8. Biên bản ca thực

~~~text
case_id: CA-xxx
project:
case_carrier:
interviewer_drafter:
independent_critic:
constitutional_checker_or_verifier:
record_keeper:
interviewed_at:
protocol_version:

plain_language_summary:

axioms_triggered:
  - code:
    reason:

claims:
  - claim_id:
    claim_text:
    status: da-biet | co-dau-hieu | gia-dinh | chua-biet
    supporting_evidence:
    contradictory_evidence:
    provenance:
    limitations:
    decision_currently_allowed:

core_checks:
  LC-01:
  LC-02:
  LC-03:
  LC-04:
  LC-05:
  LC-06:

derivation:
  B1_truy_nguyen:
  B2_kich_ban_vi_pham:
  B3_kiem_loi_cung:
  B4_phuong_an_nhe_hon:
  B5_tieu_chi_kiem:
  B6_nguong_ty_le:

proposed_next_action:
owner:
deadline:
review_date:
decision_after_result:
status:
~~~

Người giữ sổ không sửa âm thầm bản cũ. Bản mới thay thế phải giữ liên kết tới phiên bản trước.

## 9. Bản rút gọn 30 phút

Bản rút gọn không được bỏ B1, B3 và B5. Hỏi 12 câu sau:

1. Trạng thái nào cần được tạo ra, cho ai? — TĐ-01.
2. Bằng chứng nhu cầu mạnh nhất và phản chứng là gì? — TĐ-01, TĐ-03.
3. Ai hưởng lợi, ai chịu ngoại tác? — TĐ-02.
4. Các claim thành công bị chứng minh sai bằng cách nào? — TĐ-03, LC-06.
5. Người tham gia đang tặng, mua, đặt trước, cho vay, đầu tư hay góp nguồn lực gì? — TĐ-04.
6. Có dữ liệu hoặc cách ghi nhận nào xâm phạm phẩm giá không? — TĐ-05, LC-05.
7. Cam kết kích hoạt khi điều kiện nào đạt? — TĐ-07.
8. Thiện ích chia nhỏ được không và provision point là gì? — TĐ-08.
9. Có bao nhiêu actor độc lập, bên liên quan và mức tập trung ra sao? — TĐ-09, LC-02.
10. Nguồn lực được truy vết, giữ và chi theo mục đích thế nào? — TĐ-10, TĐ-11, LC-01.
11. Ai kiểm milestone; tiêu chí có được đặt trước kết quả không? — LC-03, LC-04, LC-06.
12. Failure, refund/release và bước thử nhỏ nhất tiếp theo là gì? — TĐ-12, B4–B6.

Sau đó chỉ được đưa ra một trong các kết quả tại mục 7.

## 10. Definition of done

Một buổi phỏng vấn chỉ hoàn thành khi:

- Có mã CA-xxx hoặc đã giao người giữ sổ cấp mã.
- Mỗi yêu cầu tiếp theo có mã tiên đề truy nguyên.
- Có ít nhất một phản chứng hoặc ghi rõ chưa tìm phản chứng.
- Sáu lõi cứng đều được ghi trạng thái, không để trống.
- Không có người vừa soạn dẫn vừa tự kết luận hợp hiến.
- Bước tiếp theo nhẹ nhất đã được cân nhắc.
- Bước tiếp theo có evidence requirement và decision rule.
- Mức kiểm tra được giải thích theo tính tỷ lệ.
- Có owner, deadline và ngày xem lại.
- Bản cũ được giữ nếu biên bản được sửa.

## 11. Liên kết

- [[Hiến chương - Bản đồ]]
- [[Tiên đề lõi cứng]]
- [[Tiên đề vòng ngoài]]
- [[Giao thức suy dẫn luật]]
- [[Giao thức xử lý xung đột]]
- [[Vai trò và cặp vai bị cấm]]
- [[Proof of need và demand validation]]
- [[Campaign charter]]
- [[Verification protocol và decision rule]]
