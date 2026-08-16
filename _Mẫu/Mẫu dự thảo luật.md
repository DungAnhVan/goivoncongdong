---
ai_authored: true
type: luat
status: du-thao
updated:
tags:
  - goi-von-cong-dong
  - luat
---

# L-xxx — <tên luật>

> [!abstract] Cách dùng mẫu này
> Chép vào `05 Phương án/`, đổi tên, điền.
>
> Sáu mục B1–B6 là [[Giao thức suy dẫn luật|phép kiểm hợp hiến]]. Thiếu một mục là không đưa ra kiểm được.

## Nội dung luật

> <Viết luật thành một câu buộc hoặc cấm. Nếu cần hơn ba câu, có thể đây là hai luật.>

Xuất phát từ: `VD-xxx` / `CH-xxx`

---

## B1 — Truy nguyên

**Thực thi tiên đề:** `___`

<Giải thích ngắn mối nối. Nếu phải giải thích qua ba tầng trung gian, cảnh báo: có thể đây là sở thích cá nhân đang mượn danh tiên đề.>

> Phép tự kiểm: *nếu tiên đề này không tồn tại, tôi có còn muốn luật này không?* Nếu còn — truy nguyên đang giả.

## B2 — Cần thiết

**Nếu không có luật này, tiên đề bị vi phạm bằng đường nào:**

<Kịch bản cụ thể, có nhân vật và hành động. Không viết "sẽ có rủi ro về…">

## B3 — Kiểm lõi cứng

| Điều | Có vi phạm không | Ghi chú |
|---|---|---|
| `LC-01` Không chiếm dụng | | |
| `LC-02` Không gian lận | | |
| `LC-03` Không tự phán | | |
| `LC-04` Không hồi tố | | |
| `LC-05` Không xâm phạm phẩm giá | | |
| `LC-06` Không lời hứa không phản bác | | |

> Chú ý vi phạm **gián tiếp**. Ví dụ: luật buộc công khai toàn bộ chứng từ có thể vi phạm `LC-05` nếu chứng từ chứa dữ liệu người thụ hưởng.

## B4 — Xâm hại tối thiểu

**Các phương án nhẹ hơn đã xét:**

```text
Phương án A — <mô tả>
  → loại vì: 

Phương án B — <mô tả>
  → loại vì: 

Phương án được chọn — <mô tả>
  → vì: 
```

Thang ràng buộc từ nhẹ đến nặng: `công bố → mặc định có thể đổi → yêu cầu giải trình → cần phê duyệt → cấm`.

Nếu một mức nhẹ hơn đạt được mục tiêu, **bắt buộc** dùng mức đó.

## B5 — Kiểm tra được

```text
tieu_chi_dat:          # giá trị, đơn vị, cửa sổ thời gian
xu_ly_du_lieu_thieu:
nguoi_kiem:
nguoi_KHONG_duoc_kiem:
bang_chung_yeu_cau:
protocol_lien_quan:    # VR-xxx nếu có
```

> Không đo được → chưa phải Luật. Đưa xuống `04 Giải pháp` làm Nguyên tắc.

## B6 — Tỷ lệ

```text
Dưới ngưỡng X:   
Từ X đến Y:      
Trên Y:          
Nhóm dễ tổn thương: nâng một bậc
```

> Luật áp cho mọi chiến dịch bất kể quy mô gần như luôn sai ở một trong hai đầu.

---

## Chữ ký bắt buộc

```text
nguoi_soan:
nguoi_phan_bien:        # KHÔNG được trùng người soạn
nguoi_kiem_hop_hien:    # KHÔNG được trùng người soạn
```

> [!warning] Không có phản biện đứng tên thì không đưa ra kiểm được
> Xem [[Vai trò và cặp vai bị cấm]].

## Trạng thái

```text
che_do:                # day-du | rut-gon
trang_thai:            # du-thao | dang-phan-bien | ban-hanh
                       # | chot-tam-cho-pilot | bai-bo
phien_ban:
ngay_hieu_luc:
ngay_het_han_xem_lai:  # BẮT BUỘC nếu chốt tạm cho pilot
```
