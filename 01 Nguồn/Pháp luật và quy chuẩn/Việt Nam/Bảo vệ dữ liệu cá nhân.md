# Bảo vệ dữ liệu cá nhân

> Cập nhật: 10/08/2026.

## 1. Khung pháp luật hiện hành

### Luật Bảo vệ dữ liệu cá nhân số 91/2025/QH15

- Ban hành: 26/06/2025.
- Có hiệu lực: 01/01/2026.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?classid=1&docid=214590&pageid=27160&typegroup=)

### Nghị định 356/2025/NĐ-CP

- Ban hành: 31/12/2025.
- Có hiệu lực: 01/01/2026.
- Quy định chi tiết một số điều và biện pháp thi hành Luật Bảo vệ dữ liệu cá nhân.

Nguồn: [Cổng TTĐT Chính phủ](https://vanban.chinhphu.vn/?classid=0&docid=216387&pageid=27160)

## 2. Vì sao dự án này thu nhiều dữ liệu rủi ro?

Nền tảng có thể xử lý:

- họ tên;
- số điện thoại/email;
- định danh/KYC;
- tài khoản ngân hàng;
- lịch sử đóng góp;
- dự án quan tâm;
- vị trí;
- dữ liệu nghề nghiệp;
- đánh giá uy tín;
- mối quan hệ giữa contributor và project;
- complaint/grievance;
- dữ liệu người hưởng lợi;
- dữ liệu trẻ em hoặc nhóm yếu thế trong một số dự án xã hội.

Không được xem toàn bộ là `profile data` chung chung.

## 3. Data map bắt buộc

Trước pilot cần bảng:

| Data | Chủ thể | Mục đích | Ai truy cập | Thời gian giữ | Chia sẻ với ai | Căn cứ xử lý | Xóa/ẩn danh |
|---|---|---|---|---|---|---|---|
| KYC | contributor | xác minh | compliance | ... | payment partner | ... | ... |
| Payment ref | contributor | đối soát | finance | ... | bank | ... | ... |
| Beneficiary evidence | beneficiary | thẩm định | verifier | ... | ... | ... | ... |

## 4. `Public campaign` không có nghĩa mọi dữ liệu đều công khai

Ví dụ:

```text
Tên project creator
→ có thể cần public

CCCD của project creator
→ dùng để verify, không mặc nhiên public

Số tiền contributor
→ có thể public theo lựa chọn/chính sách

Tài khoản ngân hàng
→ không được công khai chỉ vì campaign minh bạch
```

Transparency phải được thiết kế theo nguyên tắc data minimization, không phải dump toàn bộ evidence ra cộng đồng.

## 5. Evidence ledger và privacy

Repo muốn giữ dấu vết bằng chứng dài hạn. Điều này tạo xung đột cần giải quyết giữa:

```text
Auditability
↔ privacy
↔ retention limit
↔ right to correction/deletion where applicable
↔ legal hold
```

Giải pháp kiến trúc nên tách:

```text
Public evidence metadata
Private evidence vault
Hash / evidence ID
Access log
Retention rule
Legal hold flag
```

Không đưa tài liệu định danh thô vào public GitHub hoặc public campaign page.

## 6. Consent không phải cái cớ dùng cho mọi thứ

Không thiết kế một checkbox kiểu:

> “Tôi đồng ý cho nền tảng sử dụng dữ liệu cho mọi mục đích.”

Mỗi mục đích phải được phân loại và kiểm tra căn cứ xử lý phù hợp.

Marketing, KYC, fraud prevention, fulfilment, analytics và public attribution là các mục đích khác nhau.

## 7. Dữ liệu của beneficiary

Đây là vùng đặc biệt nhạy cảm.

Một campaign y tế/xã hội có thể muốn công bố câu chuyện, bệnh án, hoàn cảnh gia đình để tăng donation. Không vì mục tiêu tốt mà bỏ qua quyền dữ liệu và phẩm giá của beneficiary.

Bắt buộc tách:

```text
Thông tin cần để verifier kiểm chứng
≠ thông tin cần public
≠ thông tin donor muốn xem
```

## 8. Chuyển dữ liệu ra nước ngoài

Nếu dùng cloud, analytics, AI API, CRM hoặc payment provider ở nước ngoài, phải mở checklist riêng theo Luật 91/2025 và Nghị định 356/2025.

Không chỉ hỏi server đặt ở đâu; phải hỏi ai nhận dữ liệu, mục đích gì, có onward transfer không và trách nhiệm của các bên.

## 9. AI và scoring

Nếu sau này nền tảng chấm `trust score`, `project risk score`, `beneficiary credibility` hoặc dùng AI để ra quyết định, phải thiết kế:

- provenance của dữ liệu;
- explainability phù hợp;
- quyền sửa dữ liệu sai;
- chống discrimination;
- human review;
- log phiên bản model/rule;
- giới hạn sử dụng dữ liệu ban đầu.

Ngoài khung dữ liệu cá nhân, Việt Nam còn có Luật Trí tuệ nhân tạo số 134/2025/QH15 có hiệu lực từ 01/03/2026; cần mở nghiên cứu riêng khi AI trở thành chức năng quyết định chứ không chỉ hỗ trợ nội bộ.

## 10. Câu lõi

> **Minh bạch dự án không đồng nghĩa công khai dữ liệu cá nhân; bằng chứng phải truy nguyên được nhưng quyền truy cập phải có mục đích và giới hạn.**
