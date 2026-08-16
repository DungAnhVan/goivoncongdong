---
ai_authored: true
type: nguon-chinh-sach
status: da-doi-chieu
jurisdiction: TP.HCM
date_event: 2026-03-30
updated: 2026-08-11
tags:
  - tphcm
  - tax
  - startup
  - innovation
  - nq98
---

# 2023–2026 — NQ98, NQ260, NQ31 và ưu đãi thuế đổi mới sáng tạo TP.HCM

## 1. Nghị quyết 98/2023/QH15 và Nghị quyết 260/2025/QH15

Nghị quyết 98 là khung thí điểm cơ chế, chính sách đặc thù phát triển TP.HCM. CSDL quốc gia về VBQPPL ghi nhận Nghị quyết 98 là văn bản hiện thời và Nghị quyết 260/2025/QH15 là văn bản sửa đổi Nghị quyết 98.

Nguồn CSDL quốc gia: https://vbpl.moj.gov.vn/TW/Pages/vbpq-luocdo.aspx?ItemID=179317

Nghị quyết 260/2025/QH15 được Quốc hội ban hành ngày 11/12/2025 và sửa đổi, bổ sung Nghị quyết 98. Khi dùng một điều cụ thể phải đọc **NQ98 sau sửa đổi**, không dùng bản 2023 như văn bản đóng băng.

## 2. Nghị quyết 31/2024/NQ-HĐND

- Ban hành: 11/12/2024.
- Hiệu lực: 01/01/2025.
- Tình trạng trên Công báo TP.HCM tại ngày kiểm tra: **đang hiệu lực**.
- Quy định các lĩnh vực ưu tiên; tiêu chí, điều kiện và nội dung hoạt động khởi nghiệp đổi mới sáng tạo có thu nhập phát sinh trên địa bàn Thành phố được miễn thuế TNCN/TNDN theo cơ chế đặc thù.

Nguồn Công báo: https://congbao.hochiminhcity.gov.vn/cong-bao/van-ban/nghi-quyet/so/31-2024-nq-hdnd/ngay/11-12-2024/47450

## 3. Hướng dẫn thực tế của Sở KH&CN và Thuế TP.HCM năm 2026

Ngày 30/03/2026, Sở KH&CN phối hợp Thuế TP.HCM tổ chức hướng dẫn chính sách miễn thuế theo Nghị quyết 98, Nghị quyết 198/2025/QH15 và Nghị quyết 31/2024/NQ-HĐND.

Nguồn Sở KH&CN: https://dost.hochiminhcity.gov.vn/hoat-dong-so-khcn/go-diem-nghen-chinh-sach-thue-tphcm-tang-toc-he-sinh-thai-doi-moi-sang-tao/

Điểm cần giữ khi thiết kế hệ thống:

```text
NQ98/NQ31
→ local/special HCMC tax lane

NQ198/NĐ20
→ national private-economy tax lane
```

Một startup có thể phải kiểm tra **cả hai lane** và xác định chính xác căn cứ nào áp dụng; không cộng cơ học các ưu đãi nếu pháp luật không cho phép.

## 4. Policy eligibility phải trở thành dữ liệu cấu trúc

Hồ sơ project/company nên có:

- địa điểm/trụ sở;
- ngày thành lập;
- loại hình actor;
- lĩnh vực hoạt động;
- hoạt động tạo doanh thu;
- tỷ lệ doanh thu từ hoạt động đổi mới sáng tạo nếu tiêu chí yêu cầu;
- tình trạng công nhận startup/doanh nghiệp KHCN nếu liên quan;
- kỳ tính thuế;
- thời điểm bắt đầu hưởng ưu đãi;
- chứng từ/kế toán làm căn cứ.

Nền tảng chỉ nên hiển thị:

```text
Potentially eligible
→ cần kiểm tra

Verified eligible
→ có căn cứ/cơ quan/hồ sơ xác nhận
```

Không hiển thị “được miễn thuế” chỉ dựa trên tag `startup`.

## 5. Giá trị chiến lược

Ưu đãi thuế là **resource** nhưng không phải cash inflow:

```text
Cash grant
→ tăng tiền hiện có

Tax relief
→ giảm outflow/nghĩa vụ thuế nếu đủ điều kiện
```

Khi tính runway/resource bundle cần tách hai loại này.

## 6. Không được suy diễn

- Có hoạt động đổi mới sáng tạo không đồng nghĩa tự động thuộc lĩnh vực ưu tiên.
- Nghị quyết 31 không phải giấy chứng nhận startup.
- Miễn thuế không thay thế nghĩa vụ khai thuế, kế toán, hóa đơn và hồ sơ chứng minh.
- NQ260 đã sửa NQ98; khi viện dẫn điều khoản phải kiểm tra phiên bản hợp nhất/hiện hành.

## 7. Liên kết repo

- [[Public policy]]
- [[Policy instrument]]
- [[Public finance]]
- [[Multi-resource matching]]
- [[Khoảng trống từ ý tưởng đến đủ điều kiện nhận hỗ trợ công]]
