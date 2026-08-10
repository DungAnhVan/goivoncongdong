# Pháp luật Việt Nam — Bản đồ cho mô hình gọi vốn cộng đồng

> Cập nhật nghiên cứu: 10/08/2026.
>
> Đây là **bản đồ nghiên cứu pháp lý**, không phải ý kiến pháp lý chính thức. Mỗi chiến dịch thật cần được phân loại theo bản chất giao dịch và kiểm tra lại văn bản có hiệu lực tại thời điểm triển khai.

## 1. Kết luận nền tảng

Trong phạm vi rà soát nguồn chính thức đến 10/08/2026, chưa tìm thấy một luật hoặc nghị định chuyên biệt điều chỉnh toàn bộ mô hình `crowdfunding` dưới một chế độ pháp lý duy nhất.

Vì vậy không nên hỏi:

> “Crowdfunding có hợp pháp ở Việt Nam không?”

mà phải hỏi:

> “Người A chuyển tài sản gì cho ai, để đổi lấy quyền gì, ai giữ tiền, ai quyết định sử dụng, có hoàn trả/lợi nhuận/quyền sở hữu hay không, và nền tảng đang làm chức năng gì?”

Một từ `góp tiền` có thể che ít nhất các giao dịch khác nhau:

```text
Donation / tài trợ
Pre-order / mua trước
Reward crowdfunding
Cho vay
Hợp tác đầu tư
Góp vốn vào doanh nghiệp
Mua cổ phần
Mua trái phiếu / chứng khoán
Đóng góp vào quỹ xã hội, quỹ từ thiện
```

Mỗi loại kích hoạt một cụm luật khác nhau.

## 2. Bản đồ các điểm chạm pháp lý

```text
Ý tưởng / dự án
        ↓
Công bố chiến dịch
        ├─ Luật Thương mại điện tử
        ├─ Luật Bảo vệ quyền lợi người tiêu dùng
        └─ Luật Giao dịch điện tử
        ↓
Nhận cam kết / nhận tiền
        ├─ Bộ luật Dân sự
        ├─ Nghị định thanh toán không dùng tiền mặt
        └─ AML / KYC tùy chủ thể
        ↓
Đổi lại quyền lợi gì?
        ├─ Không nhận lợi ích tài chính → donation/reward
        ├─ Nhận hàng/dịch vụ → thương mại
        ├─ Quyền đòi nợ/lãi → debt
        └─ Quyền sở hữu/lợi nhuận → doanh nghiệp/chứng khoán/đầu tư
        ↓
Giữ và giải ngân tiền
        ├─ thanh toán
        ├─ hợp đồng
        ├─ kiểm soát nội bộ
        └─ quy định chuyên ngành nếu có
        ↓
Thu thập danh tính, hành vi, payment data
        └─ Luật Bảo vệ dữ liệu cá nhân
        ↓
Thuế, hóa đơn, kế toán
        └─ luật thuế + quản lý thuế hiện hành
```

## 3. Các cụm tài liệu trong thư mục này

- [[Huy động vốn, đầu tư và chứng khoán]]
- [[Thanh toán, giữ tiền và phòng chống rửa tiền]]
- [[Thương mại điện tử và trách nhiệm nền tảng]]
- [[Người tiêu dùng, hợp đồng và giao dịch điện tử]]
- [[Bảo vệ dữ liệu cá nhân]]
- [[Đóng góp tự nguyện, quỹ xã hội và quỹ từ thiện]]
- [[Doanh nghiệp, startup và quỹ đầu tư khởi nghiệp sáng tạo]]
- [[Thuế, hóa đơn và kế toán]]
- [[Ma trận phân loại mô hình crowdfunding tại Việt Nam]]
- [[Danh mục nguồn pháp luật Việt Nam hiện hành]]

## 4. Ba vùng pháp lý phải đặc biệt tránh nhập nhằng

### A. `Cộng đồng góp tiền` ≠ mặc nhiên donation

Nếu người góp có quyền nhận lãi, chia lợi nhuận, hoàn vốn, cổ phần hoặc quyền tài chính khác thì phải kiểm tra luật doanh nghiệp, đầu tư, chứng khoán, cho vay và thuế.

### B. `Nền tảng giữ hộ tiền` ≠ chỉ là tính năng kỹ thuật

Phải xác định chính xác tiền thuộc về ai, tài khoản đứng tên ai, nền tảng có quyền định đoạt hay chỉ truyền lệnh, và hoạt động có rơi vào dịch vụ thanh toán/trung gian thanh toán được quản lý hay không.

### C. `Hợp đồng hợp tác đầu tư` ≠ tự động được bảo vệ như chứng khoán

Ngày 26/03/2026, UBCKNN cảnh báo về một số doanh nghiệp huy động vốn qua app/website bằng hợp đồng hợp tác đầu tư; UBCKNN nêu hoạt động được cảnh báo đó không do UBCKNN quản lý, cấp phép và nhà đầu tư có thể không được pháp luật chứng khoán bảo vệ khi tranh chấp.

Nguồn: [UBCKNN — Khuyến cáo nhà đầu tư về hoạt động hợp tác đầu tư trên môi trường mạng](https://ssc.gov.vn/webcenter/portal/ubck/pages_r/l/chitit?dDocName=APPSSCGOVVN1620165260)

## 5. Nguyên tắc thiết kế cho dự án

Trước khi cho phép một campaign nhận tiền, hồ sơ pháp lý tối thiểu phải trả lời:

1. Ai là bên nhận tiền theo pháp luật?
2. Người đóng góp nhận quyền gì?
3. Quyền đó là contractual right, consumer right, debt claim, ownership right hay security?
4. Tiền nằm ở tài khoản của ai?
5. Ai được ra lệnh giải ngân?
6. Nếu campaign thất bại, nghĩa vụ hoàn tiền thuộc về ai?
7. Nền tảng chỉ cung cấp hạ tầng thông tin hay còn trung gian thanh toán, đại diện, quản lý tài sản hoặc chào mời đầu tư?
8. Ai chịu nghĩa vụ thuế/hóa đơn?
9. Dữ liệu nào được thu và căn cứ xử lý là gì?
10. Cơ quan quản lý chuyên ngành nào có thể có thẩm quyền?

## 6. Mức độ kết luận

Các ghi chú dùng ba nhãn:

```text
[CHẮC]
→ văn bản hiện hành điều chỉnh trực tiếp vấn đề đã nêu.

[PHÂN LOẠI]
→ luật áp dụng phụ thuộc bản chất giao dịch; cần fact pattern cụ thể.

[VÙNG XÁM]
→ chưa đủ cơ sở để khẳng định từ văn bản tổng quát; phải xin legal opinion hoặc ý kiến cơ quan quản lý trước khi triển khai thật.
```

## 7. Câu lõi

> **Không thiết kế pháp lý bằng tên gọi của tính năng. Thiết kế pháp lý bằng quyền, nghĩa vụ, dòng tiền và quyền kiểm soát thực tế của từng actor.**
