---
ai_authored: true
type: giao-thuc
status: cho-phe-chuan
updated: 2026-08-10
tags:
  - goi-von-cong-dong
  - hien-chuong
  - giao-thuc
  - xung-dot
---

# Giao thức xử lý xung đột

> [!abstract] Văn bản này dùng để làm gì
> Chồng lấn và mâu thuẫn giữa các tiên đề là **không tránh khỏi**. Văn bản này quy định cách xử lý mà không phải hy sinh nguyên tắc "tiên đề không mặc cả".
>
> Cách giải: lõi cứng thì tuyệt đối, vòng ngoài thì cân bằng có ghi lý do — và trước cả hai, phải kiểm xem xung đột có thật không.

## Sơ đồ

```text
Phát hiện mâu thuẫn
        │
        ▼
  B0  Có phải xung đột thật không?
        ├── Không (lỗi phạm vi) → làm rõ miền, ghi chú giải, KẾT THÚC
        └── Có
              ▼
  B1  Có tiên đề lõi cứng liên quan không?
        ├── Có, trực tiếp → lõi cứng thắng, KHÔNG cân đo, KẾT THÚC
        └── Không, hoặc chỉ gián tiếp
              ▼
  B2  Phép cân bằng
        a. Mỗi bên bảo vệ tiên đề nào?
        b. TÌM GIẢI PHÁP THỨ BA  ← bước quan trọng nhất
        c. Nếu không có: chọn phương án hy sinh ít nhất
        d. Lợi ích thu được có xứng cái mất không?
              ▼
  B3  Ghi thành tiền lệ, nêu rõ phạm vi ràng buộc
              ▼
  B4  Tiền lệ có thể bị lật sau, nhưng phải nêu lý do
      và không hồi tố bất lợi (LC-04)
```

---

## B0 — Có phải xung đột thật không?

Phần lớn "mâu thuẫn" là **lỗi xác định phạm vi**: hai bên đang nói về hai tình huống khác nhau mà tưởng là một.

```text
Câu hỏi kiểm:
- Hai tiên đề này áp cho cùng một chủ thể không?
- Cùng một thời điểm trong vòng đời chiến dịch không?
- Cùng một loại quan hệ đóng góp không?
- Cùng một đối tượng thông tin không?
  (công chúng / người góp / bên kiểm toán / cơ quan quản lý)
```

Câu hỏi cuối cùng giải quyết được rất nhiều xung đột về minh bạch: "công khai" với ai là câu hỏi khác hẳn "công khai hay không".

Nếu xung đột tan ở đây: **không tạo tiền lệ**, chỉ ghi một chú giải vào cả hai tiên đề để lần sau không ai vấp lại.

---

## B1 — Lõi cứng có liên quan không?

```text
Có, trực tiếp → lõi cứng thắng. Không cân đo. Kết thúc.
```

> [!warning] Cạm bẫy hay gặp
> **Lõi cứng cấm một hành vi, không bắt buộc một phương pháp.**
>
> Nếu một bên viện dẫn lõi cứng để áp đặt một giải pháp kỹ thuật cụ thể, đó là dùng sai. Ví dụ: `LC-02` cấm tạo người góp giả — nhưng nó **không** bắt buộc phải dùng eKYC. Chọn phương pháp là việc của tầng Luật, và phải qua bước B4 xâm hại tối thiểu.

Khi lõi cứng chỉ liên quan gián tiếp, ghi rõ điều đó rồi đi tiếp B2.

---

## B2 — Phép cân bằng

Chỉ dùng khi **cả hai bên đều là tiên đề vòng ngoài**.

### a. Mỗi bên đang bảo vệ điều gì?

Viết ra giá trị thật sự đang bị đe doạ, không phải tên tiên đề. "TĐ-05" không nói lên gì; "quyền không bị phơi bày của người góp ít tiền" thì có.

### b. Tìm giải pháp thứ ba

> [!important] Đây là bước quan trọng nhất của toàn bộ giao thức
> Đa số xung đột tiên đề tan biến khi **thiết kế cơ chế tốt hơn**, chứ không phải khi chọn bên.
>
> Bắt buộc tìm giải pháp thứ ba trước ngăn hệ thống rơi vào thói quen đánh đổi lười biếng — thói quen sẽ dần bào mòn cả hai tiên đề theo thời gian.

Kỹ thuật hay dùng:

```text
TÁCH THUỘC TÍNH
  Tách "chứng minh là người duy nhất" khỏi "danh tính là ai"

ĐỔI ĐỐI TƯỢNG NHẬN THÔNG TIN
  Không công khai với công chúng, nhưng mở cho bên kiểm toán

DỜI THỜI ĐIỂM
  Không cần lúc đóng góp, cần lúc giải ngân

PHÂN TẦNG THEO RỦI RO
  Áp chặt cho nhóm rủi ro cao, nhẹ cho phần còn lại

ĐỔI HÌNH PHẠT THÀNH ĐỔI TRỌNG SỐ
  Không cấm, nhưng không tính vào trọng số
```

Kỹ thuật cuối là cách giải của `TL-001` và có thể tái dùng rộng.

### c. Nếu thật sự không có giải pháp thứ ba

Chọn phương án **hy sinh ít nhất**. Ghi rõ:

```text
Hy sinh cái gì:
Hy sinh bao nhiêu:
Ai chịu phần hy sinh đó:
Có cách nào bù cho họ không:
Điều kiện nào xuất hiện thì xét lại:
```

Dòng cuối quan trọng: mọi cân bằng đều gắn với điều kiện kỹ thuật và nguồn lực **tại thời điểm đó**. Ghi điều kiện xét lại biến một quyết định vĩnh viễn thành một quyết định có hạn.

### d. Cân xứng hẹp

Lợi ích thu được có xứng với cái mất không? Nếu phải hy sinh nhiều để được ít, quay lại b.

---

## B3 — Ghi thành tiền lệ

Một tiền lệ phải nêu **phạm vi ràng buộc** — ca nào về sau bị buộc theo. Không nêu phạm vi thì tiền lệ hoặc vô dụng hoặc bành trướng.

```text
tien_le_id:            # TL-xxx
ten:
ngay:
xung_dot_giua:         # mã hai tiên đề
tinh_huong_cu_the:
b0_ket_qua:            # xung đột thật hay lỗi phạm vi
b1_ket_qua:            # lõi cứng có liên quan không
giai_phap_thu_ba:      # có hay không, là gì
phuong_an_chon:
ben_bi_hy_sinh:
dieu_kien_xet_lai:     # bắt buộc
pham_vi_rang_buoc:     # bắt buộc — ca nào về sau bị buộc theo
nguoi_phan_xu:
y_kien_thieu_so:       # nếu có, phải ghi
luat_phat_sinh:        # L-xxx nếu tiền lệ dẫn tới luật mới
```

> [!important] Ghi cả ý kiến thiểu số
> Nếu hội đồng không nhất trí, ý kiến thiểu số **phải** được ghi lại. Đây là cách một tiền lệ sai có thể được lật sau này mà không cần tranh cãi lại từ đầu — và là cách người phản đối vẫn ở lại trong hệ thống.

---

## B4 — Lật tiền lệ

Được phép, với hai điều kiện:

```text
1. Nêu lý do: điều kiện đã thay đổi, hoặc lập luận cũ có lỗi
2. Không hồi tố bất lợi (LC-04)
   → ca đã xử theo tiền lệ cũ không bị xử lại theo hướng bất lợi
```

Lật tiền lệ là bình thường và lành mạnh. Lật tiền lệ mà không ghi lý do là vi phạm `LC-04`.

---

## Câu hỏi chưa chốt

> [!warning] Cần hội đồng quyết
> **Tiền lệ có ràng buộc hay chỉ tham khảo?**
>
> - *Ràng buộc:* hệ thống nhất quán hơn, người tham gia dự đoán được, nhưng cứng ở giai đoạn sớm khi tiền lệ đầu tiên có thể sai.
> - *Tham khảo:* linh hoạt, nhưng mở đường cho việc xử hai ca giống nhau theo hai cách.
>
> **Đề xuất trung gian:** tiền lệ ràng buộc, nhưng ở giai đoạn pilot mọi tiền lệ mặc định có hạn 12 tháng và phải được xác nhận lại mới thành vĩnh viễn.

## Liên kết

- [[Hiến chương - Bản đồ]]
- [[Tiên đề lõi cứng]]
- [[Tiên đề vòng ngoài]]
- [[Giao thức suy dẫn luật]]
- [[Vai trò và cặp vai bị cấm]]
- [[Mẫu tiền lệ]]
