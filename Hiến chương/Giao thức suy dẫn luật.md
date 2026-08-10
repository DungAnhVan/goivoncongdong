---
type: giao-thuc
status: cho-phe-chuan
updated: 2026-08-10
tags:
  - goi-von-cong-dong
  - hien-chuong
  - giao-thuc
---

# Giao thức suy dẫn luật

> [!abstract] Văn bản này dùng để làm gì
> Đây là cỗ máy biến một tiên đề trừu tượng thành một luật cụ thể có thể kiểm tra đạt hay không đạt.
>
> Mọi luật đề xuất phải qua **phép kiểm hợp hiến 6 bước**. Không đạt một bước là không ban hành được.

## Quy tắc vô hiệu

> [!warning] Điều kiện tiên quyết
> Một luật không chỉ ra được chuỗi truy nguyên hợp lệ về tiên đề là **luật vô hiệu**, kể cả khi nội dung của nó nghe rất hợp lý.

Đây là cơ chế chính ngăn hệ thống phình ra bằng các quy định tiện tay. Quy định tiện tay là cách hầu hết bộ máy quản trị chết: mỗi quy tắc riêng lẻ đều hợp lý, tổng thể thì không ai vác nổi.

---

## Phép kiểm hợp hiến 6 bước

### B1 — Truy nguyên

> Luật này thực thi tiên đề nào?

Ghi mã cụ thể: `LC-xx` hoặc `TĐ-xx`. Được phép nêu nhiều tiên đề.

```text
Không chỉ ra được → DỪNG. Chưa phải luật.
Chỉ ra được nhưng phải giải thích vòng vo 3 tầng → cảnh báo,
  có thể đây là sở thích cá nhân đang mượn danh tiên đề.
```

**Lỗi thường gặp:** truy nguyên ngược — nghĩ ra luật trước, rồi đi tìm tiên đề nào nghe hợp để dán vào. Cách phát hiện: hỏi người soạn "nếu tiên đề này không tồn tại, anh chị có còn muốn luật này không?" Nếu còn, đó là truy nguyên giả.

### B2 — Cần thiết

> Nếu không có luật này, tiên đề đó bị vi phạm bằng đường nào?

Phải mô tả **kịch bản vi phạm cụ thể**, có nhân vật và hành động. Không chấp nhận mô tả chung chung.

```text
Không đạt:
"Nếu không có quy định này, sẽ có rủi ro về minh bạch."

Đạt:
"Chủ dự án A nhận đủ tiền ở mốc 1, không nộp chứng từ,
 mở mốc 2 bằng cách tự ký biên bản nghiệm thu.
 Người góp không có cách nào biết cho đến khi dự án đóng."
```

### B3 — Không xâm phạm lõi cứng

> Luật này có tạo ra tình huống nào vi phạm `LC-01`…`LC-06` không?

```text
Có → sửa hoặc bỏ. KHÔNG cân đo, không đánh đổi.
```

Chú ý trường hợp vi phạm gián tiếp: một luật buộc công khai toàn bộ chứng từ có thể vô tình vi phạm `LC-05` nếu chứng từ chứa dữ liệu người thụ hưởng.

### B4 — Xâm hại tối thiểu

> Có cách nào đạt cùng mục tiêu mà ràng buộc người tham gia ít hơn không?

Phải liệt kê ít nhất **hai phương án nhẹ hơn** đã xét và nêu vì sao loại. Không liệt kê được là dấu hiệu chưa suy nghĩ đủ.

```text
Thang ràng buộc từ nhẹ đến nặng:
công bố thông tin → mặc định có thể đổi → yêu cầu giải trình
→ cần phê duyệt → cấm
```

Nếu một mức nhẹ hơn đạt được mục tiêu, **bắt buộc** dùng mức đó.

### B5 — Kiểm tra được

> Tiêu chí đạt hay không đạt là gì? Ai kiểm? Bằng chứng nào?

```text
Không đo được → chưa phải Luật, mới là Nguyên tắc.
  Đưa xuống 04 Giải pháp, đừng ép nó thành luật.
```

Đây là chỗ [[Verification protocol và decision rule]] được nối vào: mỗi luật cần chỉ ra protocol kiểm tương ứng, hoặc tạo mới.

**Tối thiểu phải có:** giá trị, đơn vị, cửa sổ thời gian, cách xử lý dữ liệu thiếu, ai kiểm, ai không được kiểm.

### B6 — Tỷ lệ

> Mức độ ràng buộc có tỷ lệ với quy mô, tính khó đảo ngược và mức dễ tổn thương của người chịu tác động không?

Mọi luật phải nêu **ngưỡng áp dụng**. Một luật áp cho mọi chiến dịch bất kể quy mô gần như luôn sai ở một trong hai đầu.

```text
Ví dụ ngưỡng:
- dưới X đồng: chỉ công bố
- X đến Y: cần một người phê duyệt độc lập
- trên Y: cần bên thứ ba xác minh
- mọi mức, nếu người hưởng lợi là nhóm dễ tổn thương:
  áp mức cao hơn một bậc
```

---

## Chế độ rút gọn cho pilot

Ở quy mô pilot, chạy đủ 6 bước cho mọi luật là quá tốn. Chế độ rút gọn:

| Bước | Pilot | Ghi chú |
|---|---|---|
| B1 Truy nguyên | **Bắt buộc** | Không bao giờ bỏ |
| B2 Cần thiết | Bắt buộc, có thể ngắn | 3–5 dòng đủ |
| B3 Lõi cứng | **Bắt buộc** | Không bao giờ bỏ |
| B4 Xâm hại tối thiểu | Rút gọn còn 1 phương án thay thế | |
| B5 Kiểm tra được | Bắt buộc | Có thể dùng tiêu chí thô |
| B6 Tỷ lệ | Có thể hoãn | Ghi rõ "áp cho pilot, chưa phân ngưỡng" |

Luật ban hành ở chế độ rút gọn **bắt buộc** mang trạng thái `chốt tạm cho pilot` kèm ngày hết hạn xem lại.

---

## Hồ sơ một luật

```text
rule_id:               # L-xxx
ten_luat:
trang_thai:            # du-thao | dang-phan-bien | ban-hanh
                       # | chot-tam-cho-pilot | hoan-vi-thieu-ca-thuc | bai-bo
che_do:                # day-du | rut-gon

truy_nguyen:           # B1 — mã tiên đề, bắt buộc
kich_ban_vi_pham:      # B2
kiem_loi_cung:         # B3 — kết luận + lý do
phuong_an_nhe_hon:     # B4 — đã xét gì, vì sao loại
tieu_chi_do:           # B5
nguoi_kiem:
bang_chung_yeu_cau:
nguong_ty_le:          # B6

nguoi_soan:
nguoi_phan_bien:       # bắt buộc, KHÔNG được trùng người soạn
nguoi_kiem_hop_hien:   # bắt buộc, KHÔNG được trùng người soạn
ca_thuc_lien_quan:     # CA-xxx
tien_le_lien_quan:     # TL-xxx
nguyen_tac_cha:        # NT-xxx nếu có

phien_ban:
ngay_hieu_luc:
ngay_het_han_xem_lai:  # bắt buộc nếu chốt tạm cho pilot
```

---

## Ví dụ chạy thử

**Vấn đề `VD-001`:** Chủ dự án tự ký biên bản nghiệm thu mốc rồi mở đợt giải ngân tiếp.

**B1 — Truy nguyên:** `LC-03` không tự phán; hỗ trợ bởi `TĐ-10` truy vết từng đơn vị tiền.

**B2 — Kịch bản vi phạm:** Chủ dự án hoàn thành 12/20 sản phẩm thử, tự ký xác nhận đạt, nhận 35% ngân sách đợt hai. Người góp chỉ phát hiện khi dự án đóng và không còn tiền để khắc phục.

**B3 — Lõi cứng:** Luật này *thực thi* `LC-03`, không vi phạm điều nào. Kiểm `LC-05`: yêu cầu bằng chứng có làm lộ dữ liệu cá nhân không? Với sản phẩm thử thì không. Đạt.

**B4 — Xâm hại tối thiểu.** Đã xét:

```text
Phương án A — cấm giải ngân theo mốc, chỉ hoàn ứng sau chi
  → loại: chặn nhóm không có vốn ứng trước, đi ngược mục tiêu hỗ trợ

Phương án B — chỉ yêu cầu công bố biên bản, không cần người thứ hai
  → loại: công bố không giải quyết được vấn đề tự phán,
     người góp không có năng lực kiểm tra kỹ thuật

Phương án C (chọn) — yêu cầu một người xác nhận độc lập với người nhận tiền
  → nhẹ hơn kiểm toán bên thứ ba, đủ để phá thế tự phán
```

**B5 — Tiêu chí đo:** biên bản nghiệm thu phải có chữ ký của một người không nhận lợi ích tài chính từ đợt giải ngân này; danh tính người xác nhận được ghi vào hồ sơ trước khi kiểm, không phải sau.

**B6 — Ngưỡng:** áp cho mọi đợt giải ngân từ mức trung bình trở lên; dưới mức đó chỉ cần công bố kèm quyền yêu cầu kiểm tra sau.

**Kết quả:** đạt 6/6 → chuyển sang phản biện.

---

## Ba dấu hiệu luật hỏng

```text
1. Truy nguyên dài hơn nội dung luật
   → luật đang mượn danh tiên đề

2. Không nêu được ngưỡng áp dụng
   → sẽ chết vì bội thực hoặc vô dụng vì quá nhẹ

3. Người soạn không nghĩ ra được cách lách
   → chưa có phản biện thật, đừng ban hành
```

## Liên kết

- [[Hiến chương - Bản đồ]]
- [[Tiên đề lõi cứng]]
- [[Tiên đề vòng ngoài]]
- [[Giao thức xử lý xung đột]]
- [[Vai trò và cặp vai bị cấm]]
- [[Verification protocol và decision rule]]
- [[Mẫu dự thảo luật]]
