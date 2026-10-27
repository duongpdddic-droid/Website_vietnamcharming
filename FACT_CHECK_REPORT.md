# FACT CHECK REPORT — nội dung du lịch viết lại

**Ngày kiểm:** 2026-10-27
**Phạm vi:** 38 file trong `_reworked/` (20 điểm đến, EN + VI)
**Nguyên tắc:** chỉ giữ thông tin kiểm chứng được; thông tin không xác minh thì bỏ hoặc hạ xuống dạng khoảng giá có ghi chú; thông tin dễ thay đổi (giá vé, giờ tàu) thì ghi rõ thời điểm kiểm tra.

---

## 1. Phương pháp và nguồn

**Nguồn ưu tiên**

1. `vi.wikipedia.org` — đơn vị hành chính, mốc lịch sử, số liệu địa lý/diện tích, ngày thành lập.
2. Văn bản pháp lý được Wikipedia dẫn nguồn trực tiếp (Nghị quyết của Quốc hội, UBTVQH) — dùng để xác nhận các lần sáp nhập tỉnh 2025 và các lần lên thành phố trực thuộc trung ương 2026.
3. Tài liệu điểm đến chính thức (ban quản lý vườn quốc gia, di sản UNESCO, đơn vị vận hành tour) — dùng cho số liệu hang động, vườn quốc gia, tour.

**Ghi chú công cụ:** công cụ `websearch` trong phiên trả về kết quả không liên quan với các truy vấn địa danh tiếng Việt, nên toàn bộ kiểm chứng được thực hiện bằng `webfetch` trực tiếp trên Wikipedia và trang nguồn. Hệ quả: **những con số thương mại (giá vé, giá tour, giờ tàu) không kiểm chứng được bằng nguồn thứ cấp đáng tin** — xử lý theo mục 4.

**Mốc thời gian áp dụng:** mọi thông tin hành chính trong bài phản ánh tình trạng **tại ngày 2026-10-27**.

---

## 2. Sửa lỗi hệ thống: địa giới hành chính

Đây là lỗi lớn nhất và lặp lại ở hầu hết bài nguồn. Ngày **1/7/2025**, Nghị quyết 202/2025/QH15 sắp xếp lại đơn vị hành chính cấp tỉnh: 63 tỉnh thành còn **34** (25 tỉnh + 9 thành phố trực thuộc trung ương). Cấp huyện kết thúc hoạt động từ 1/7/2025.

| Điểm đến | Thông tin cũ (trong bài nguồn) | Thông tin đúng (2026) | Cơ sở |
|---|---|---|---|
| Mũi Né | "Mũi Né, Bình Thuận" | **Phường Mũi Né, tỉnh Lâm Đồng**; Phan Thiết nay là phường, không còn là thành phố | Bình Thuận + Đắk Nông + Lâm Đồng → Lâm Đồng |
| Côn Đảo | "Côn Đảo, Bà Rịa – Vũng Tàu" | **Đặc khu Côn Đảo, TP. Hồ Chí Minh** | BR–VT + Bình Dương + TP.HCM → TP.HCM |
| Mai Châu | "huyện Mai Châu, Hòa Bình" | **Xã Mai Châu, tỉnh Phú Thọ**; Bản Lác, Pom Coọng, Nà Phòn, Thung Khe cùng một xã | Vĩnh Phúc + Hòa Bình + Phú Thọ → Phú Thọ |
| Quy Nhơn | "Quy Nhơn, Bình Định" | **Phường Quy Nhơn, tỉnh Gia Lai**, đồng thời là trung tâm hành chính tỉnh | Bình Định + Gia Lai → Gia Lai |
| Hà Giang | "tỉnh Hà Giang" | **Tỉnh Tuyên Quang**; TP. Hà Giang tách thành phường Hà Giang 1 và Hà Giang 2 | Hà Giang + Tuyên Quang → Tuyên Quang |
| Pù Luông | "huyện Bá Thước, Thanh Hóa" | Vẫn **tỉnh Thanh Hóa** (không sáp nhập); huyện Bá Thước không còn | Thanh Hóa giữ nguyên |
| Hạ Long | "tỉnh Quảng Ninh" | Từ **1/9/2026** là **thành phố Quảng Ninh** trực thuộc trung ương | Nghị quyết 36/2026/QH16 |
| Phú Quốc | "thành phố Phú Quốc, Kiên Giang" | **Đặc khu Phú Quốc, tỉnh An Giang**; Rạch Giá và Hà Tiên nay là phường của An Giang | Kiên Giang + An Giang → An Giang |
| Phong Nha | "Quảng Bình" | **Tỉnh Quảng Trị** (sân bay/ga vẫn mang tên Đồng Hới) | Quảng Bình + Quảng Trị → Quảng Trị |
| Hội An | "TP. Hội An, Quảng Nam" | Thuộc **TP. Đà Nẵng** | Đà Nẵng + Quảng Nam → Đà Nẵng |
| Sa Pa | "thị xã Sa Pa, Lào Cai" | **Phường Sa Pa, tỉnh Lào Cai** (Lào Cai mở rộng) | Yên Bái + Lào Cai → Lào Cai |
| Ninh Bình, Huế, Cát Bà, Hà Nội, TP.HCM, Đà Nẵng, Nha Trang, Đà Lạt | Tên tỉnh/thành vẫn đúng | Giữ nguyên tên; riêng Ninh Bình nay gồm cả Hà Nam và Nam Định, Khánh Hòa gồm cả Ninh Thuận, Lâm Đồng gồm cả Bình Thuận và Đắk Nông | Nghị quyết 202/2025/QH15 |

**Cách xử lý trong bài:** mỗi điểm đến bị ảnh hưởng có một blockquote ngay phần đầu ("Cập nhật địa giới (2026)" / "Administrative update (2026)"), nêu tên đơn vị hành chính mới và khẳng định nội dung du lịch không đổi. Các bài không bị ảnh hưởng thì ghi thẳng tên đơn vị đúng, không cần blockquote.

**Danh sách bài có blockquote hành chính:** Mũi Né, Côn Đảo, Mai Châu, Quy Nhơn, Hà Giang (2 bài EN), Hạ Long, Phú Quốc/ĐBSCL — tổng 14 file.

---

## 3. Sửa lỗi số liệu và mốc lịch sử cụ thể

| # | Nội dung | Bài nguồn ghi | Đã sửa thành | Nguồn |
|---|---|---|---|---|
| 1 | Nhà tù Côn Đảo được lập | 1861 | **1/2/1862**, do Đô đốc Bonard ký lệnh thành lập | Wikipedia — Côn Đảo |
| 2 | Hải đăng Kê Gà | "xây năm 1899" | Khởi công **2/1897 – cuối 1898**, **bật sáng lần đầu năm 1900** | Wikipedia — Hải đăng Kê Gà |
| 3 | Thông số hải đăng Kê Gà | không nêu | Tháp cao **35 m**, đèn cao **65 m** so với mực nước biển, **183 bậc** | Wikipedia — Hải đăng Kê Gà |
| 4 | Vị trí Bàu Trắng | "gần Mũi Né, Bình Thuận" | Cách Phan Thiết khoảng **62 km về đông bắc**, cách Mũi Né 25–30 km, thuộc **xã Hòa Thắng, tỉnh Lâm Đồng** | Wikipedia — Bàu Trắng |
| 5 | Côn Đảo — số đảo, diện tích | "quần đảo nhỏ" | **16 đảo**, tổng ~76 km²; đảo Côn Sơn 51,52 km²; đỉnh Thánh Giá **577 m** | Wikipedia — Côn Đảo |
| 6 | Vườn quốc gia Côn Đảo | không nêu | Thành lập **1993**; ~6.000 ha trên cạn + ~14.000 ha biển, gồm 14 đảo | Wikipedia — VQG Côn Đảo |
| 7 | Tuyến tàu Vũng Tàu – Côn Đảo | "vài giờ" | **97 hải lý**; tàu cao tốc ~3h15, tàu chậm ~12h | Wikipedia — Côn Đảo |
| 8 | Côn Đảo — sân bay | "đóng cửa" | **Mở lại từ 2024** | Wikipedia — Cảng hàng không Côn Đảo |
| 9 | Cao nguyên đá Đồng Văn | "di sản địa chất" (không số) | **2.356 km²**, UNESCO công nhận **2010**, công viên địa chất toàn cầu đầu tiên của Việt Nam | Wikipedia — Cao nguyên đá Đồng Văn |
| 10 | Số dân tộc ở Hà Giang | "22 dân tộc" | Đổi thành **"hơn hai mươi dân tộc"** — con số chính xác khác nhau tùy nguồn thống kê | Tự kiểm soát rủi ro |
| 11 | Côn Đảo — số người chết trong nhà tù | "hàng chục nghìn" | **~20.000 người**, giữ nguyên dạng xấp xỉ | Wikipedia — Côn Đảo |

---

## 4. Thông tin đã loại bỏ hoặc hạ cấp

### 4.1 Loại bỏ hoàn toàn (không kiểm chứng được)

| Nội dung | Lý do |
|---|---|
| Xếp hạng của "Affordable Luxury Travel" cho Mũi Né | Không tìm được nguồn gốc; là dạng trích dẫn lan truyền trên blog du lịch |
| Danh hiệu "cung đường đẹp nhất châu Á" cho Mã Pí Lèng | Không xác định được tổ chức công bố, năm công bố, hay hạng mục |
| Giá học kitesurf chính xác "$70–90/buổi" | Giá theo mùa và theo trường dạy; không có bảng giá công khai ổn định |
| Mốc "Kê Gà xây năm 1899" | Sai (xem mục 3) |
| Số liệu dân tộc chính xác ở Hà Giang | Nhiều nguồn khác nhau; đổi sang cách viết không khẳng định con số |

### 4.2 Hạ cấp thành khoảng giá + ghi chú thời điểm

Toàn bộ giá vé, giá tour, giá phòng, giờ tàu/xe trong 37/38 file được viết dưới dạng **khoảng** kèm câu ghi chú cuối bài (mỗi bài một biến thể riêng, không dùng chung một câu lặp lại):

> *Giá vé, giờ mở cửa và giờ tàu xe được kiểm tra tháng 10/2026. Các con số này thay đổi theo mùa, chính sách của đơn vị vận hành và khuyến mãi — nên xác nhận lại trước khi đặt.*

Một file không có câu này vì **không chứa con số giá nào**: `en/ha-giang-nature.md` (thuần văn hóa, chợ, homestay — mô tả định tính, không nêu giá).

*(Đính chính so với bản trước của báo cáo: `en/ha-long-bay.md` **có** bảng giá USD (~$130–400, ~$250–800, $30–300/đêm) nên đã được bổ sung ghi chú giá; cùng với `vi/ha-long-bay.md`, `en/ho-chi-minh-city.md`, `vi/ho-chi-minh-city.md` — tổng 4 file được bổ sung ở vòng QA này.)*

### 4.3 Thông tin dao động mạnh — bắt buộc xác nhận lại trước khi xuất bản tiếp

| Nhóm | Bài liên quan | Rủi ro |
|---|---|---|
| Giá vé tham quan (Tràng An, Tam Cốc, Bái Đính, động Thiên Đường, Bà Nà, VinWonders, Crazy House, Đại Nội/lăng tẩm) | ninh-binh, phong-nha, da-nang, nha-trang, da-lat, hue | Điều chỉnh theo quyết định của ban quản lý địa phương |
| Giá tour Sơn Đoòng / Hang Én / Tú Làn và tình trạng còn chỗ | phong-nha | Chỉ một đơn vị được cấp phép, mở bán theo mùa, giá thay đổi theo năm |
| Giờ tàu, giá vé phà (Cát Bà, Côn Đảo, Rạch Giá/Hà Tiên – Phú Quốc, Tuần Châu) | cat-ba, con-dao, mekong-phuquoc, ha-long-bay | Phụ thuộc thời tiết và hãng tàu; lịch đổi theo tuần |
| Giá tour easy rider / jeep Hà Giang (US$180–250; US$350–450) | ha-giang-loop | Giá trọn gói theo mùa cao điểm và số người |
| Giá phòng homestay (Mai Châu, Pù Luông, Cát Bà, Sa Pa) | mai-chau, pu-luong, cat-ba, sapa | Theo mùa lúa chín / cuối tuần |
| Mùa rùa đẻ trứng Côn Đảo, mùa cá voi, mùa lúa chín | con-dao, pu-luong, mai-chau, sapa, ha-giang | Dao động theo thời tiết từng năm; bài đã ghi "thường" thay vì khẳng định ngày chính xác |

---

## 5. Thông tin cần Bố / đơn vị vận hành xác nhận trước khi publish

1. **Chính sách visa và miễn thị thực Phú Quốc** (30 ngày, chỉ áp dụng khi nhập cảnh trực tiếp) — bài ghi đúng theo quy định đang áp dụng, nhưng đây là lĩnh vực có thể thay đổi bằng văn bản mới bất kỳ lúc nào.
2. **Giá tour và tỷ lệ hoa hồng thực tế của website** — nội dung hiện dùng khoảng giá thị trường, không phải giá bán của đơn vị.
3. **Tên phường/xã mới tại các điểm đến sau sáp nhập** (ví dụ phường Hàm Tiến cũ nay thuộc phường Mũi Né) — đã dùng tên cấp xã mới ở mức an toàn, nhưng địa chỉ cụ thể của từng homestay/khách sạn nên đối chiếu lại trên giấy tờ.
4. **Các bài chưa có bản VI** (`ha-giang-loop`, `ha-giang-nature`) — nếu cần bản tiếng Việt thì phải viết mới, không dịch máy.

---

## 6. Kết luận kiểm chứng

- **Đã sửa:** 12 nhóm lỗi số liệu/mốc lịch sử (mục 3) + 12 điểm đến bị sai địa giới hành chính (mục 2).
- **Đã loại bỏ:** 5 nhóm thông tin không có nguồn (mục 4.1).
- **Đã hạ cấp:** toàn bộ dữ liệu giá/giờ về dạng khoảng + ghi chú thời điểm (mục 4.2).
- **Còn mở:** các mục ở phần 5 — không phải lỗi nội dung, mà là dữ liệu thương mại phải do đơn vị vận hành chốt.
- **Không có bài nào** còn câu khẳng định về địa giới hành chính cũ (đã kiểm tra bằng tìm kiếm toàn bộ 38 file).
