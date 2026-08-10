---
type: kien-truc-de-xuat
status: cho-duyet
updated: 2026-08-10
tags:
  - goi-von-cong-dong
  - hien-chuong
  - quan-tri
  - kien-truc
---

# Kiến trúc hiến chương và suy dẫn luật

> [!abstract] Vai trò của ghi chú
> Đây là **bản kiến trúc đề xuất**, chưa phải hiến chương đã ban hành.
>
> Nó mô tả cỗ máy: nạp tiên đề vào, ra được luật cụ thể, và có chỗ ghi lại phán quyết của con người khi hai tiên đề va nhau.
>
> Cần được duyệt hoặc sửa trước khi bung thành các file riêng.

## 1. Bài toán

Bộ 12 tiên đề tại [[Khung thiết kê nền tảng cho gọi vốn cộng đồng]] đã trả lời rất tốt câu hỏi *"điều gì đúng"*. Nhưng nó chưa trả lời ba câu hỏi vận hành:

```text
Làm sao đi từ một tiên đề trừu tượng
đến một luật cụ thể có thể kiểm tra pass/fail?

Khi hai tiên đề cùng đúng nhưng chỉ ngược nhau,
ai phán và phán bằng cách nào?

Làm sao để người mới nêu được vấn đề
mà không cần đọc hết 500 dòng whitepaper?
```

Thiếu ba thứ này, bộ tiên đề sẽ đi theo một trong hai hướng hỏng: hoặc trở thành tuyên ngôn đẹp không ai áp dụng được, hoặc trở thành cái cớ để mỗi người diễn giải theo ý mình.

## 2. Phát hiện: cấu trúc hiện tại đã gần đúng

Thư mục hiện có của vault đã trùng khớp với chuỗi suy dẫn của một hệ thống pháp lý:

```text
03 Vấn đề    → điều gì cần xử lý          (issue, question)
04 Giải pháp → nguyên lý xử lý là gì      (nguyên tắc)
05 Phương án → cụ thể làm bằng cách nào   (luật)
06 Thực làm  → áp vào ca thật, kết quả    (ca thực, tiền lệ)
```

Cái thiếu không phải cấu trúc, mà là:

1. **Tầng hiến chương ở trên** — hiện tiên đề đang nằm lẫn trong `02 Mở rộng` như một ghi chú khám phá, không có địa vị ràng buộc.
2. **Kỷ luật truy nguyên bắt buộc** — hiện chưa có quy tắc "luật nào không truy được về tiên đề thì vô hiệu".
3. **Giao thức xử lý xung đột** — hiện chưa có.

> [!important] Hệ quả
> Không cần đập đi xây lại. Chỉ cần thêm một tầng lên trên và một bộ giao thức nối các tầng lại.

## 3. Bốn tầng

| Tầng | Tên | Trả lời | Ai tạo | Sửa được không | Nơi ở |
|---|---|---|---|---|---|
| 0 | **Tiên đề** | Điều gì không bao giờ được vi phạm? | Hội đồng hiến chương | Rất khó; lõi cứng chỉ được thêm | `Hiến chương` |
| 1 | **Nguyên tắc** | Nguyên lý xử lý loại vấn đề này? | Người soạn dẫn | Được, nếu suy dẫn lại | `04 Giải pháp` |
| 2 | **Luật** | Cụ thể buộc/cấm gì, đo bằng gì? | Người soạn dẫn | Được, qua kiểm hợp hiến | `05 Phương án` |
| 3 | **Tiền lệ** | Ca cụ thể này đã được xử ra sao? | Người phân xử | Lật được, phải nêu lý do | `Hiến chương/Tiền lệ` |

Chiều đi xuống là **suy dẫn**. Chiều đi lên là **truy nguyên**.

```text
Tiên đề
  ↓ suy dẫn (phải qua kiểm hợp hiến)
Nguyên tắc
  ↓ suy dẫn
Luật
  ↓ áp dụng
Ca thực
  ↓ khi ca thực làm lộ khoảng trống hoặc xung đột
Tiền lệ ──→ quay lại sửa Luật, hiếm khi sửa Nguyên tắc,
            gần như không bao giờ sửa Tiên đề
```

> [!warning] Quy tắc vô hiệu
> Một luật không chỉ ra được chuỗi truy nguyên hợp lệ về tiên đề là **luật vô hiệu**, kể cả khi nội dung của nó nghe hợp lý.
>
> Đây là cơ chế chính ngăn hệ thống phình ra bằng các quy định tiện tay.

## 4. Tiên đề: lõi cứng và vòng ngoài

Anh đã chốt mô hình **lõi cứng + cân bằng vòng ngoài**. Cụ thể hóa:

### 4.1. Lõi cứng — tuyệt đối, không cân đo

Vi phạm một điều lõi cứng thì mọi lợi ích thu được đều không cứu được tính chính đáng của hệ thống. Không có ngoại lệ khẩn cấp, không có "lần này thì chấp nhận được".

| Mã | Điều | Nguồn |
|---|---|---|
| **LC-01** | **Không chiếm dụng.** Nguồn lực được giao không bao giờ trở thành tài sản tự do của người đang giữ nó. | Canon 10, 11 |
| **LC-02** | **Không gian lận.** Không làm giả bằng chứng, không tạo người góp giả, không che giấu xung đột lợi ích. | ⚠️ *chưa có trong canon 12* |
| **LC-03** | **Không tự phán.** Người nhận nguồn lực không được là người duy nhất xác nhận điều kiện để nhận nguồn lực đó. | ⚠️ *đang nằm trong [[Custody và safeguarding]], chưa thành tiên đề* |
| **LC-04** | **Không hồi tố bất lợi, không hạ chuẩn sau kết quả.** Không sửa tiêu chí sau khi đã biết kết quả để hợp thức hóa nó. | ⚠️ *đang nằm trong [[Verification protocol và decision rule]], chưa thành tiên đề* |
| **LC-05** | **Không xâm phạm phẩm giá để huy động.** Không dùng xấu hổ, cưỡng ép hay phơi bày để tạo đóng góp. | Canon 5 |
| **LC-06** | **Không lời hứa không thể phản bác.** Tuyên bố nào không thể bị chứng minh sai thì không thể được công nhận là đạt. | Canon 3 |

> [!warning] Phát hiện đáng chú ý
> **Ba trong sáu điều lõi cứng hiện không phải là tiên đề.** Chúng đang sống dưới dạng "thực hành tốt" rải rác trong các note `00 Là gì`.
>
> Tức là những thứ ít có khả năng mặc cả nhất trong toàn hệ thống lại đang có địa vị yếu nhất về mặt văn bản. Đây là lỗ hổng cấu trúc cần vá trước khi gọi vốn.

### 4.2. Vòng ngoài — không thể bị bác bỏ, nhưng có thể được cân bằng khi va nhau

12 tiên đề hiện có (`TĐ-01` … `TĐ-12`) giữ nguyên nội dung, chuyển sang địa vị vòng ngoài.

Phân biệt quan trọng:

```text
Bác bỏ một tiên đề vòng ngoài
→ KHÔNG được phép

Cân bằng một tiên đề vòng ngoài với một tiên đề khác
trong một tình huống cụ thể, có ghi lý do
→ Được phép, và tạo ra tiền lệ
```

### 4.3. Quy tắc sửa hiến chương

| Đối tượng | Được thêm | Được làm rõ | Được thu hẹp / bỏ |
|---|---|---|---|
| Lõi cứng | Có, ngưỡng rất cao | Có | **Không** |
| Vòng ngoài | Có | Có | Chỉ khi chứng minh được nó suy dẫn sai hoặc có ca thực phản bác |
| Nguyên tắc, Luật | Có | Có | Có, qua kiểm hợp hiến lại |

Cơ chế bánh cóc một chiều ở lõi cứng là thứ làm cho câu "tiên đề không thể mặc cả" có hiệu lực thật thay vì chỉ là một lời hứa.

### 4.4. Quan hệ với hiến chương chiến dịch

> [!warning] Cần tránh nhầm hai chữ "hiến chương"
> Vault đã có [[Campaign charter]] — hiến chương của **từng chiến dịch**. Cái đang xây ở đây là hiến chương của **nền tảng**.

```text
Hiến chương nền tảng   (tiên đề, áp cho toàn hệ)
        ↓ ràng buộc
Luật nền tảng          (áp cho mọi chiến dịch)
        ↓ ràng buộc
Hiến chương chiến dịch (riêng từng chiến dịch)
```

Một điều khoản trong hiến chương chiến dịch trái với tiên đề nền tảng thì **vô hiệu**, dù người góp đã bấm đồng ý. Điều này cần được viết vào cả hai văn bản.

## 5. Giao thức suy dẫn luật

Mọi luật đề xuất phải qua **phép kiểm hợp hiến 6 bước**. Không đạt một bước là không ban hành được.

```text
B1. TRUY NGUYÊN
    Luật này thực thi tiên đề nào? Ghi mã cụ thể.
    Không chỉ ra được → dừng.

B2. CẦN THIẾT
    Nếu không có luật này, tiên đề đó bị vi phạm bằng đường nào?
    Mô tả kịch bản vi phạm cụ thể, không nói chung chung.

B3. KHÔNG XÂM PHẠM LÕI CỨNG
    Luật này có tạo ra tình huống nào vi phạm LC-01…LC-06 không?
    Có → sửa hoặc bỏ, không cân đo.

B4. XÂM HẠI TỐI THIỂU
    Có cách nào đạt cùng mục tiêu mà ràng buộc người tham gia ít hơn không?
    Có → phải dùng cách đó.

B5. KIỂM TRA ĐƯỢC
    Tiêu chí đạt/không đạt là gì? Ai kiểm? Bằng chứng nào?
    Không đo được → chưa phải luật, mới là nguyên tắc.

B6. TỶ LỆ
    Mức độ ràng buộc có tỷ lệ với quy mô, tính khó đảo ngược
    và mức dễ tổn thương của người chịu tác động không?
```

Bước 6 chính là tiên đề tính tỷ lệ đã có sẵn trong whitepaper, được đưa vào làm bộ lọc bắt buộc — nó ngăn hệ thống áp bộ máy kiểm toán của quỹ đầu tư lên một chiến dịch 5 triệu đồng.

### Hồ sơ một luật

```text
rule_id:
ten_luat:
trang_thai:            # du-thao | dang-phan-bien | ban-hanh | hoan | bai-bo
truy_nguyen:           # mã tiên đề, bắt buộc
kich_ban_vi_pham:      # B2
kiem_loi_cung:         # B3, kết luận + lý do
phuong_an_nhe_hon:     # B4, đã xét những gì, vì sao loại
tieu_chi_do:           # B5
nguoi_kiem:
bang_chung_yeu_cau:
nguong_ty_le:          # B6, áp từ quy mô nào
nguoi_soan:
nguoi_phan_bien:       # bắt buộc, không được trùng người soạn
nguoi_kiem_hop_hien:   # bắt buộc, không được trùng người soạn
ca_thuc_lien_quan:
tien_le_lien_quan:
phien_ban:
ngay_hieu_luc:
```

## 6. Giao thức xử lý xung đột

Chồng lấn và mâu thuẫn là không tránh khỏi — nhưng phần lớn xung đột *biểu kiến* sẽ tan ở bước 0.

```text
B0. CÓ PHẢI XUNG ĐỘT THẬT KHÔNG?
    Phần lớn "mâu thuẫn" là lỗi xác định phạm vi:
    hai bên đang nói về hai tình huống khác nhau.
    Làm rõ miền áp dụng trước. Tan → kết thúc, ghi làm chú giải.

B1. CÓ LÕI CỨNG LIÊN QUAN KHÔNG?
    Có → lõi cứng thắng. Không cân đo. Kết thúc.
    Lưu ý: lõi cứng cấm một HÀNH VI, không bắt buộc một PHƯƠNG PHÁP.
    Nếu chỉ liên quan gián tiếp, đi tiếp B2.

B2. PHÉP CÂN BẰNG (chỉ dùng khi cả hai đều vòng ngoài)
    a. Mỗi bên đang bảo vệ tiên đề nào?
    b. TÌM GIẢI PHÁP THỨ BA trước khi hy sinh bên nào.
    c. Nếu không có: chọn phương án hy sinh ít nhất.
    d. Lợi ích thu được có xứng với cái mất không?

B3. GHI THÀNH TIỀN LỆ
    Nêu rõ phạm vi áp dụng: ca nào về sau bị ràng buộc.

B4. LẬT TIỀN LỆ
    Được, nhưng phải nêu lý do và không hồi tố bất lợi (LC-04).
```

> [!important] Bước 2b là bước quan trọng nhất
> Đa số xung đột tiên đề tan biến khi thiết kế cơ chế tốt hơn, chứ không phải khi chọn bên. Bắt buộc tìm giải pháp thứ ba trước ngăn hệ thống rơi vào thói quen đánh đổi lười biếng.

### Ví dụ chạy thử: ẩn danh vs chống Sybil

**Xung đột:** `TĐ-05` danh dự tự nguyện (người góp được chọn ẩn danh hoàn toàn) chọi `TĐ-12` chống giả mạo cộng đồng (cơ chế thưởng theo số người phải kiểm soát danh tính duy nhất).

**B0 — Xung đột thật không?**
`TĐ-05` nói về *hiển thị công khai*. Chống Sybil nói về *xác minh nội bộ*. Hai miền khác nhau → phần lớn xung đột tan. Phần còn lại thật sự: người góp không muốn để lại dấu vết định danh cho **cả nền tảng**.

**B1 — Lõi cứng?**
`LC-02` có liên quan (người góp giả là gian lận). Nhưng LC-02 cấm *hành vi tạo người góp giả*, không quy định *phải xác minh bằng phương pháp nào*. Chưa kết thúc, đi tiếp.

**B2a — Mỗi bên bảo vệ gì?**
`TĐ-05` bảo vệ quyền không bị phơi bày. `TĐ-12` bảo vệ tính toàn vẹn của tín hiệu "độ rộng ủng hộ" — thứ mà matching và quadratic funding dựa vào.

**B2b — Giải pháp thứ ba:**
Tách *chứng minh là người duy nhất* khỏi *danh tính*. Bên thứ ba xác minh tính duy nhất và cấp một token không liên kết ngược được; nền tảng đếm token mà không biết ai. Thỏa cả hai tiên đề.

**B2c — Khi chưa có bên thứ ba (giai đoạn pilot):**
Chọn phương án xâm hại ít nhất — người ẩn danh vẫn góp được bình thường, nhưng khoản của họ không được tính vào trọng số độ rộng. Hy sinh một phần hiệu lực của `TĐ-12` thay vì tước quyền ẩn danh.

**B3 — Tiền lệ `TL-001`:**
> Ẩn danh là quyền đối với công chúng, không phải quyền đối với hệ thống kiểm toán. Khi hệ thống chưa thể xác minh tính duy nhất, hãy loại khoản ẩn danh khỏi trọng số thay vì cấm ẩn danh.

**Phạm vi ràng buộc:** mọi cơ chế thưởng hoặc matching tính theo số người.

## 7. Vai trò

Vai trò được định nghĩa theo **chức năng trong cỗ máy suy dẫn**, không theo chức danh. Một người có thể giữ nhiều vai, trừ các cặp bị cấm.

| Vai | Việc phải làm | Ai vào được |
|---|---|---|
| **Người nêu vấn đề** | Nêu tình huống chưa có luật, hoặc luật đang hỏng | Bất kỳ ai |
| **Người đặt câu hỏi** | Nêu điều chưa rõ trong hiến chương | Bất kỳ ai |
| **Người mang ca thực** | Mang dự án hoặc tình huống thật vào để thử luật | Bất kỳ ai có ca thật |
| **Người soạn dẫn** | Nối vấn đề về tiên đề, viết dự thảo luật kèm chuỗi truy nguyên | Cần hiểu hiến chương |
| **Người phản biện** | Nhiệm vụ bắt buộc là **tìm cách bẻ** dự thảo | Cần độc lập với người soạn |
| **Người kiểm hợp hiến** | Chạy phép kiểm 6 bước, kết luận đạt hoặc không | Cần độc lập với người soạn |
| **Người phân xử** | Chỉ vào cuộc khi có xung đột tiên đề; ra tiền lệ | Hội đồng, không phải cá nhân |
| **Người giữ sổ** | Đánh mã, giữ phiên bản, không cho sửa lén | Cần kỷ luật, không cần chuyên môn sâu |

### Các cặp vai bị cấm trùng

```text
Người soạn dẫn ≠ Người kiểm hợp hiến   (cùng một luật)
Người soạn dẫn ≠ Người phản biện        (cùng một luật)
Người mang ca thực ≠ Người phân xử      (cùng một ca)
Người giữ sổ ≠ mọi vai ra quyết định
```

> [!important] Hệ thống tự áp tiên đề lên chính nó
> Các cặp cấm trùng ở trên chính là `LC-03` (không tự phán) áp dụng cho bộ máy quản trị nội bộ, không chỉ cho người gây quỹ.
>
> Một hệ thống đòi hỏi người khác tách biệt vai trò nhưng tự mình gộp hết vào một người sẽ mất tính chính đáng ngay từ đầu.

### Không có phản biện thì không có luật

Một dự thảo không có người phản biện đứng tên **không được đưa ra kiểm hợp hiến**. Phản biện phải ghi lại được:

```text
Cách tôi sẽ lách luật này nếu tôi là người xấu:
Trường hợp luật này ra kết quả vô lý:
Chi phí mà luật này áp lên người trung thực:
Tiên đề nào có thể bị luật này vi phạm gián tiếp:
```

## 8. Vòng đời một issue

```text
Nêu
 → Phân loại
 → Truy nguyên
 → Dự thảo
 → Phản biện (bắt buộc)
 → Kiểm hợp hiến
 → Ban hành
 → Thử trong ca thực
 → Ổn định
```

Bốn loại phân loại, đi bốn đường khác nhau:

| Loại | Nghĩa | Đi về đâu |
|---|---|---|
| **Câu hỏi hiến chương** | Chưa rõ một tiên đề nghĩa là gì | Chú giải, hoặc đề xuất làm rõ tiên đề |
| **Khoảng trống** | Có tình huống mà chưa có luật | Soạn luật mới |
| **Luật hỏng** | Có luật nhưng ra kết quả sai | Sửa luật |
| **Xung đột** | Hai tiên đề hoặc hai luật chỉ ngược nhau | Giao thức mục 6 |

### Hai trạng thái đặc biệt cần có

```text
HOÃN VÌ THIẾU CA THỰC
→ Câu hỏi hợp lệ nhưng không thể chốt khi chưa có dự án thật.
  Không đóng, không ép trả lời. Chờ ca thực kích hoạt lại.

CHỐT TẠM CHO PILOT
→ Luật đủ dùng cho quy mô pilot, có ngày hết hạn bắt buộc xem lại.
  Ngăn quy tắc tạm thời âm thầm trở thành vĩnh viễn.
```

> [!important] Vì sao hai trạng thái này quan trọng ở giai đoạn hiện tại
> Anh đang ở giai đoạn luận giải rất sớm. Không có "hoãn vì thiếu ca thực", nhóm sẽ hoặc chốt bừa bằng suy đoán, hoặc để câu hỏi rơi mất. Trạng thái này cho phép ghi nhận một câu hỏi tốt mà chưa cần trả lời nó.

## 9. Hệ mã số

```text
LC-01…LC-06   Tiên đề lõi cứng
TĐ-01…TĐ-12   Tiên đề vòng ngoài
NT-xxx        Nguyên tắc          → 04 Giải pháp
L-xxx         Luật                → 05 Phương án
TL-xxx        Tiền lệ             → Hiến chương/Tiền lệ
VD-xxx        Vấn đề              → 03 Vấn đề
CH-xxx        Câu hỏi             → 03 Vấn đề
CA-xxx        Ca thực             → 06 Thực làm
```

Mã số là điều kiện để truy nguyên hoạt động được. Không có mã, chuỗi suy dẫn không kiểm tra được và cả kiến trúc này sụp.

### Thư mục cần thêm

```text
Hiến chương/
    Tiên đề lõi cứng.md
    Tiên đề vòng ngoài.md
    Giao thức suy dẫn luật.md
    Giao thức xử lý xung đột.md
    Vai trò và cặp vai bị cấm.md
    Tiền lệ/
        TL-001 ….md
_Mẫu/
    Mẫu vấn đề.md
    Mẫu câu hỏi.md
    Mẫu dự thảo luật.md
    Mẫu phản biện.md
    Mẫu tiền lệ.md
```

Thư mục `Hiến chương` đặt ngoài dãy `00`–`06` vì nó nằm **trên** dây chuyền, không phải một khâu trong dây chuyền.

## 10. Kiến trúc này không giải quyết điều gì

> [!warning] Giới hạn phải nói trước
> - **Không thay pháp luật.** Một luật hợp hiến nội bộ vẫn có thể bất hợp pháp. Cần một bước kiểm tra pháp lý song song, đặc biệt với Nghị định 93/2021, quy định trung gian thanh toán và phòng chống rửa tiền.
> - **Không bảo đảm phán quyết đúng.** Nó chỉ bắt phán quyết phải có dấu vết và có thể bị kiểm tra lại.
> - **Tốn công.** Mỗi luật cần truy nguyên và phản biện. Ở pilot nhỏ nên có chế độ rút gọn, nhưng bước B1 truy nguyên và bước phản biện thì không được bỏ.
> - **Rủi ro lớn nhất là nghi lễ giấy tờ** — người ta viết chuỗi suy dẫn cho có. Cách chống duy nhất là người phản biện phải đứng tên và phản biện phải được lưu công khai cùng luật.

## 11. Những gì cần anh chốt

1. **Danh sách lõi cứng 6 điều** — đặc biệt ba điều em bổ sung ngoài canon 12 (`LC-02`, `LC-03`, `LC-04`). Có nâng chúng lên thành tiên đề không?
2. **Cơ chế bánh cóc ở mục 4.3** — lõi cứng chỉ được thêm, không được thu hẹp. Có chấp nhận ràng buộc này không?
3. **Tiền lệ có ràng buộc hay chỉ tham khảo?** Ràng buộc thì hệ thống nhất quán hơn nhưng cứng hơn ở giai đoạn sớm.
4. **Ngưỡng phản biện ở pilot** — đề xuất tối thiểu một người phản biện đứng tên cho mỗi luật.
5. **Điều khoản vô hiệu ở mục 4.4** — hiến chương chiến dịch trái tiên đề nền tảng thì vô hiệu, kể cả khi người góp đã đồng ý.

## Liên kết

- [[Khung thiết kê nền tảng cho gọi vốn cộng đồng]] — nguồn của 12 tiên đề
- [[Gọi vốn cộng đồng]] — ý tưởng gốc và nguyên tắc tạm thời
- [[Campaign charter]] — hiến chương cấp chiến dịch, chịu ràng buộc của tầng này
- [[Verification protocol và decision rule]] — nguồn của `LC-04`
- [[Custody và safeguarding]] — nguồn của `LC-03`
- [[Các câu hỏi cần được trả lời]] — kho issue đầu vào hiện có
