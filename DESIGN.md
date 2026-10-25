# DESIGN.md — Landing page tiệm đồng hồ thủ công Thời Khắc (MSR-41)

> Tài liệu thiết kế chốt cho sprint TEC-311. Dev (task Dev của sprint) dựng đúng tài liệu này, không tự thêm màu, font hay khối ngoài danh sách. QA đối chiếu bản dựng với tài liệu này, kèm kiểm tra đa dạng theo OPERATIONS.md mục 16.5.

## 0. Khác biệt so với các project gần nhất (bắt buộc theo mục 16.5 — đã đọc thật ngày 2026-10-25)

Thứ tự project mới nhất lấy từ mô tả task TEC-312 và đối chiếu trực tiếp DESIGN.md của cả 3 project gần nhất trên GitHub (đọc qua raw.githubusercontent.com ngày 2026-10-25):

1. **An Lạc** (m-software-an-lac, TEC-305) — archetype ghi rõ trong file: **A2 Split (chia đôi)**; cặp font: **Lora + Be Vietnam Pro**; nhiệt màu: **sáng-ấm** (nền kem giấy, chữ xanh rừng, nhấn vàng nghệ).
2. **Lửa Ấm** (m-software-lua-am, TEC-297) — archetype ghi rõ trong file: **A5 Theo chương**; cặp font: **Fraunces + Be Vietnam Pro**; nhiệt màu: **tối-ấm** (nền nâu sẫm, chữ kem, nhấn đất nung).
3. **Lá Xanh** (m-software-la-xanh, TEC-290) — archetype suy ra từ bố cục mô tả (file viết trước luật 16.5 nên không ghi mã): **A1 Editorial dọc**; cặp font: **Playfair Display + Be Vietnam Pro**; nhiệt màu: **sáng-ấm** (nền kem ấm, chữ xanh rừng, nhấn đất nung).

Lựa chọn cho Thời Khắc (đối chiếu trực tiếp với 3 project trên):

- **Archetype: A7 Typography-first (chữ làm chủ đạo)** — KHÁC A2 của project liền trước (An Lạc) và KHÁC A5 của project liền trước nữa (Lửa Ấm), thỏa luật "không dùng lại archetype của 2 project liền trước"; cũng khác A1 của Lá Xanh.
- **Cặp font: Noto Serif Display + Be Vietnam Pro** — KHÁC nguyên cặp của project liền trước An Lạc (Lora + Be Vietnam Pro): font tiêu đề đổi sang Noto Serif Display; cũng khác Fraunces + Be Vietnam Pro của Lửa Ấm và Playfair Display + Be Vietnam Pro của Lá Xanh.
- **Nhiệt màu: tối-trung tính** — nền than chì lạnh-trung tính, nhấn vàng đồng ấm chỉ làm điểm nhấn. KHÔNG tạo chuỗi 3 project liên tiếp cùng nhiệt màu: chuỗi gần nhất là Lá Xanh sáng-ấm → Lửa Ấm tối-ấm → An Lạc sáng-ấm (đã đứt quãng), và Thời Khắc tối-trung tính khác hẳn cả sáng-ấm lẫn tối-ấm của hai project liền trước.
- **Điểm nhấn đặc sắc riêng:** chữ số khổng lồ kiểu mặt số + vạch phút làm dải phân cách (mô tả cụ thể ở mục 7).
- **Không đổi so với công thức gợi ý trong yêu cầu:** bảng màu (nền #0F1419, chữ #ECE7DD, nhấn #C9A86A), cặp font (Noto Serif Display + Be Vietnam Pro) và không khí (nhiếp ảnh studio đồng hồ cao cấp tối giản) đều giữ nguyên, vì không vi phạm luật chống trùng nào — chỉ mở rộng bảng màu từ 3 mã gợi ý thành 6 mã đủ vai trò (thêm nền khối phụ, chữ phụ, nhấn phụ).

## 1. Tổng quan và phong cách tham chiếu (duy nhất)

- Sản phẩm: landing page 1 trang cho tiệm đồng hồ thủ công Thời Khắc — xưởng nhỏ làm và bảo dưỡng đồng hồ cơ, bán 3 dòng đồng hồ, nhận đặt lịch bảo dưỡng.
- Phong cách tham chiếu duy nhất: **nhiếp ảnh studio đồng hồ cao cấp tối giản kiểu Hodinkee** — nền tối phẳng, một nguồn sáng mềm rọi từ một phía, macro mặt số và bộ máy lộ rõ từng chi tiết; chữ serif cao, ít chữ, nhiều khoảng thở; không khí sang trọng lặng lẽ, không ồn ào kiểu quảng cáo giảm giá.
- CẤM: template bán hàng (giỏ hàng, nút mua ngay, banner khuyến mãi), icon stock đủ màu, ảnh sáng phẳng ban ngày kiểu sàn thương mại điện tử, lưới thẻ đều tăm tắp không có chữ khổng lồ dẫn nhịp.

## 2. Bảng màu (chỉ dùng đúng 6 mã dưới đây, không dùng màu ngoài bảng)

| Mã | Vai trò |
|---|---|
| `#0F1419` | Nền chính toàn trang (than chì tối-trung tính) |
| `#1A2129` | Nền khối phụ, nền thẻ đồng hồ, nền form |
| `#ECE7DD` | Chữ chính (tiêu đề + nội dung), chữ trên nền nhấn |
| `#9AA3AB` | Chữ phụ: mô tả, ghi chú, nhãn nhỏ, placeholder trong form |
| `#C9A86A` | Nhấn chính (vàng đồng): nút CTA, giá mẫu, số bước quy trình, vạch phút trang trí |
| `#3A4750` | Nhấn phụ (xám thép): đường kẻ mảnh ngăn khối, viền thẻ, nền khối ảnh khi ảnh lỗi/chưa tải |

Quy tắc dùng màu:

- Nền tối chiếm đa số diện tích; chữ kem trên nền than chì phải đọc rõ, không dùng chữ phụ cho đoạn văn chính.
- Nhấn chính chỉ dùng cho nút CTA, giá, số bước và điểm nhấn nhỏ — không làm nền khối lớn.
- Ảnh lỗi tải thì hiện nền nhấn phụ kèm tên dòng đồng hồ bằng chữ kem, không để khung ảnh trống vỡ.

## 3. Chữ (typography)

- Font tiêu đề: **Noto Serif Display** (serif cao, dùng cho H1/H2/H3, tên dòng đồng hồ và chữ số khổng lồ).
- Font nội dung: **Be Vietnam Pro** (dùng cho đoạn văn, nút, form, ghi chú, bảng giá).
- Nạp font từ Google Fonts, khai báo `font-display: swap`.

Thang kích thước:

| Cấp | Desktop | Mobile (≤768px) | Ghi chú |
|---|---|---|---|
| H1 | 72px / dòng 1.05 | 44px / dòng 1.1 | Chỉ 1 H1 ở hero, kèm chữ số khổng lồ |
| Chữ số khổng lồ | 160px / dòng 1 | 96px / dòng 1 | Số hiệu khối (01–06) kiểu mặt số, màu nhấn phụ, không đè lên H2 |
| H2 | 40px / dòng 1.2 | 30px / dòng 1.25 | Tiêu đề mỗi khối |
| H3 | 24px / dòng 1.3 | 20px / dòng 1.35 | Tên dòng đồng hồ, tên bước quy trình |
| Nội dung | 17px / dòng 1.6 | 16px / dòng 1.6 | Đoạn văn chính |
| Nhỏ/ghi chú | 14px / dòng 1.5 | 14px / dòng 1.5 | Giá mẫu, nhãn, chân trang |

## 4. Quy tắc hình ảnh

- Tông ảnh: tối và sang — nền tối, ánh sáng mềm một phía, chi tiết kim loại và da rõ nét; ảnh sáng phẳng ban ngày hoặc nền trắng sáng là lệch tông.
- Khung ảnh: hero là ảnh macro mặt đồng hồ **toàn màn hình, tỉ lệ 16:9 trở lên phủ kín viewport**; ảnh bộ sưu tập **tỉ lệ 4:5 dọc** (kiểu ảnh catalogue đồng hồ); ảnh xưởng và người thợ **tỉ lệ 3:2 ngang**; ảnh quy trình bảo dưỡng **tỉ lệ 1:1 vuông**.
- Ảnh mẫu: dùng ảnh mẫu chất lượng cao, đồng tông tối và sang ngay từ bản đầu tiên (theo OPERATIONS.md mục 16.3); ghi rõ là ảnh mẫu trong comment kết quả của Dev.
- Ảnh lỗi tải thì hiện nền nhấn phụ kèm tên khối bằng chữ kem, không để khung trống vỡ.

## 5. Bố cục (archetype A7 Typography-first)

Trang 1 cột, chữ dẫn nhịp: mỗi khối mở đầu bằng một chữ số khổng lồ kiểu mặt số (01–06) đặt lệch trái, H2 ngay sau đó; ảnh đi sau chữ, không tranh vai trò dẫn dắt. Thứ tự khối:

1. **Hero** — ảnh macro mặt đồng hồ toàn màn hình; H1 "Thời Khắc" + 1 câu giới thiệu xưởng; nút CTA "Đặt lịch bảo dưỡng" (nhấn chính).
2. **Bộ sưu tập** — chữ số 01; 3 thẻ dọc 4:5: Cổ điển, Thể thao, Dây da thủ công — mỗi thẻ: ảnh, tên dòng, 1 câu mô tả, giá mẫu.
3. **Câu chuyện xưởng và người thợ** — chữ số 02; ảnh xưởng 3:2 + đoạn văn về người thợ (không bịa tên thật: ghi [CẦN BỔ SUNG] nếu chưa có tên).
4. **Quy trình bảo dưỡng 4 bước** — chữ số 03; 4 bước đánh số bằng nhấn chính, mỗi bước 1 câu + ảnh vuông 1:1.
5. **Bảng giá mẫu** — chữ số 04; bảng 1 cột giá theo hạng mục, ghi rõ "giá mẫu".
6. **Form đặt lịch (chỉ giao diện)** — chữ số 05; form họ tên, số điện thoại, dòng đồng hồ, ghi chú; nút gửi chỉ hiển thị, chưa cần gửi thật.
7. **Chân trang** — chữ số 06 thu nhỏ; địa chỉ, điện thoại, giờ mở cửa, người phụ trách đều để **[CẦN BỔ SUNG]**, không bịa.

## 6. Thành phần (components)

- Nút CTA: nền nhấn chính `#C9A86A`, chữ nền chính `#0F1419`, bo góc 2px, chữ in hoa cỡ 15px, giãn cách chữ 1px.
- Thẻ đồng hồ: nền khối phụ `#1A2129`, viền 1px nhấn phụ `#3A4750`, ảnh 4:5 phủ kín đầu thẻ, tên dòng bằng Noto Serif Display 24px, giá bằng nhấn chính.
- Dải vạch phút: hàng 60 vạch mảnh (dài 12px, cách nhau đều, màu nhấn phụ) ngăn giữa các khối, vạch ở vị trí 12h–3h–6h–9h dài gấp đôi và màu nhấn chính.
- Form: nền khối phụ, ô nhập viền 1px nhấn phụ, placeholder màu chữ phụ, nhãn nhỏ in hoa 13px.

## 7. Điểm nhấn đặc sắc riêng

**Chữ số khổng lồ kiểu mặt số + vạch phút làm dải phân cách:** mỗi khối mở đầu bằng một con số 160px (desktop) set bằng Noto Serif Display, màu xám thép `#3A4750`, đặt lệch trái và hơi tràn ra lề như kim số trên mặt đồng hồ; giữa các khối là một dải 60 vạch phút mảnh — 4 vạch ở vị trí giờ chính dài gấp đôi và mạ vàng đồng `#C9A86A`, còn lại màu xám thép. Người xem lướt trang như đang đọc một mặt số kéo dài: số dẫn đường, vạch phút đếm nhịp, ảnh và chữ đi sau.
