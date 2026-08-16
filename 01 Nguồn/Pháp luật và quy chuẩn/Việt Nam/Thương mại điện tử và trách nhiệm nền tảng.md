---
ai_authored: true
---

# Thương mại điện tử và trách nhiệm nền tảng

> Cập nhật: 10/08/2026.

## 1. Khung pháp luật mới đã có hiệu lực

### Luật Thương mại điện tử số 122/2025/QH15

- Ban hành: 10/12/2025.
- Có hiệu lực: 01/07/2026.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?classid=1&docid=216503&pageid=27160&typegroupid=3)

### Nghị định 248/2026/NĐ-CP

- Ban hành: 30/06/2026.
- Có hiệu lực: 01/07/2026.
- Quy định chi tiết một số điều của Luật Thương mại điện tử.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?docid=218747&orggroupid=2&pageid=27160)

Bộ Công Thương đã tổ chức phổ biến Luật và Nghị định này ngay đầu tháng 7/2026.

Nguồn: [Bộ Công Thương](https://moit.gov.vn/tin-tuc/bo-cong-thuong-pho-bien-luat-thuong-mai-dien-tu-va-nghi-dinh-so-248-2026-nd-cp.html)

## 2. Tại sao crowdfunding có thể chạm thương mại điện tử?

Nếu nền tảng chỉ đăng nội dung ý tưởng để thảo luận, chưa chắc đã là một giao dịch thương mại điện tử.

Nhưng khi xuất hiện:

- đặt trước sản phẩm;
- reward đổi theo mức tiền;
- bán dịch vụ;
- campaign creator là thương nhân/tổ chức kinh doanh;
- nền tảng hỗ trợ giao kết;
- thanh toán trực tuyến;
- xếp hạng/hiển thị seller/campaign;
- xử lý complaint/refund;

thì phải kiểm tra Luật Thương mại điện tử và Nghị định 248/2026.

## 3. Không gọi tất cả campaign là “community project”

Một campaign có thể đồng thời là:

```text
Trang nội dung
+ hoạt động quảng bá
+ nơi giao kết hợp đồng
+ marketplace
+ nền tảng trung gian
+ payment integration
```

Nghĩa vụ pháp lý của nền tảng phụ thuộc vào chức năng thực tế, không chỉ tên gọi sản phẩm.

## 4. Reward crowdfunding và pre-order

[PHÂN LOẠI]

Nếu người đóng tiền nhận một sản phẩm/dịch vụ xác định, cần kiểm tra bản chất mua bán/cung ứng dịch vụ.

Các field campaign phải ghi rõ:

```text
Đây là donation hay purchase/pre-order?
Giá đã gồm thuế/phí chưa?
Khi nào giao?
Điều kiện campaign thành công là gì?
Nếu không đạt threshold thì xử lý tiền thế nào?
Nếu dự án đạt threshold nhưng giao trễ thì quyền người mua ra sao?
Reward là hàng hóa, dịch vụ hay chỉ recognition?
Ai là người bán/cung cấp?
Nền tảng có phải bên hợp đồng không?
```

## 5. Trách nhiệm thông tin

Thiết kế an toàn nên buộc campaign creator công khai tối thiểu:

- danh tính/pháp nhân;
- đầu mối liên hệ;
- bản chất campaign;
- giá/đóng góp;
- phí nền tảng;
- điều kiện activation;
- timeline;
- refund rule;
- rủi ro;
- quyền lợi contributor;
- hạn chế của nền tảng;
- xử lý khi campaign thay đổi trọng yếu.

Thông tin này phải versioned, không được sửa mất dấu vết sau khi người dùng đã cam kết.

## 6. Dark patterns và social proof

[VÙNG XÁM — cần đối chiếu điều khoản cụ thể của Luật/Nghị định khi thiết kế UI]

Các pattern nên tránh ngay từ đầu:

- countdown giả;
- “chỉ còn 2 suất” không có dữ liệu;
- số contributor không phân biệt test/internal/related party;
- đánh dấu “verified” khi chỉ xác minh email;
- tự động chọn thêm donation/reward;
- che điều kiện refund;
- nút cancel khó thấy hơn nút pay;
- dùng logo cơ quan/tổ chức khiến người dùng tưởng có endorsement.

## 7. Phân vai pháp lý trên nền tảng

Mỗi campaign cần machine-readable role:

```text
Platform operator
Campaign creator
Merchant / seller
Project legal entity
Payment provider
Contributor
Customer / consumer
Beneficiary
Verifier
Sponsor
Investor
```

Không dùng một field chung `partner` hoặc `project owner` cho nhiều vai trò.

## 8. Giao dịch xuyên biên giới

Nếu campaign creator, contributor, payment provider hoặc seller ở ngoài Việt Nam, cần mở thêm workstream:

- thương mại điện tử xuyên biên giới;
- thuế nhà thầu/thuế nền tảng;
- ngoại hối;
- chuyển dữ liệu ra nước ngoài;
- luật áp dụng và giải quyết tranh chấp;
- sanctions/AML nếu có.

## 9. Câu lõi

> **Khi nền tảng chuyển từ “nơi nói về dự án” sang “nơi người dùng giao kết và trả tiền”, trách nhiệm pháp lý cũng chuyển tầng.**
