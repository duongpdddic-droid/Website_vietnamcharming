# SEO QA REPORT — nội dung du lịch viết lại

**Ngày kiểm:** 2026-10-27
**Phạm vi:** 38 file trong `_reworked/` (20 EN + 18 VI, 20 điểm đến)
**Trạng thái:** 38/38 file đạt toàn bộ kiểm tra tự động; 7 cảnh báo còn lại đã được xác minh là **dương tính giả của script**, không phải lỗi nội dung (giải thích ở mục 5).
**Kiểm chứng nội dung/số liệu:** xem `FACT_CHECK_REPORT.md` (báo cáo riêng).

---

## 1. Cách kiểm và mức độ tin cậy

| Hạng mục | Cách kiểm | Tin cậy |
|---|---|---|
| Front matter, heading, độ dài, CTA | Script đọc trực tiếp file (`qa4.js`) | Cao — đếm chính xác |
| Trùng lặp đoạn văn giữa các bài | So khớp từng đoạn >120 ký tự trên toàn bộ 38 file | Cao |
| Ký tự lạ, HTML sót, placeholder | Regex trên toàn bộ nội dung | Cao |
| Vị trí từ khóa | Đếm vị trí từ đầu tiên của cụm từ khóa trong thân bài | Cao (theo nghĩa "vị trí", không phải "chất lượng") |
| Số liệu, giá, địa giới | Đọc Wikipedia bản tiếng Việt + văn bản nghị quyết được dẫn nguồn | Trung bình-cao, xem `FACT_CHECK_REPORT.md` |
| Search volume / độ khó từ khóa | **Chưa kiểm** — không có quyền truy cập công cụ keyword | Thấp |
| Hiển thị thực tế trên Google | **Chưa kiểm** — cần site chạy thật | — |

Toàn bộ kiểm tra dưới đây chạy trên nội dung trong repo, **không** chạy trên site đã render.

---

## 2. Quy ước YAML front matter (chuẩn hoá 38/38 file)

Mọi file dùng đúng 7 trường, cùng thứ tự, cùng kiểu giá trị:

```yaml
---
title: "Du lịch Ninh Bình 2026: Tràng An, Hang Múa và lịch trình 2 ngày"
description: "Kinh nghiệm du lịch Ninh Bình 2026: giá vé Tràng An, Tam Cốc, Hang Múa, chùa Bái Đính, mùa lúa chín, lịch trình 2 ngày và những khoản cần trả tiền mặt."
slug: "/vi/ninh-binh"
primary_keyword: "du lịch Ninh Bình"
secondary_keywords: ["kinh nghiệm du lịch Ninh Bình", "Tràng An hay Tam Cốc", "Hang Múa", "chùa Bái Đính", "lịch trình Ninh Bình 2 ngày"]
language: "vi"
updated: "2026-10-27"
---
```

| Trường | Quy ước | Kiểm |
|---|---|---|
| `title` | Chuỗi trong ngoặc kép, 49–66 ký tự | 38/38 đạt |
| `description` | Chuỗi trong ngoặc kép, 136–164 ký tự | 38/38 đạt |
| `slug` | Bắt đầu bằng `/`, dạng `/{lang}/{tên-file}` | 38/38 khớp tên file |
| `primary_keyword` | Một cụm duy nhất, ngôn ngữ khớp `language` | 38/38 có |
| `secondary_keywords` | Mảng flow `[...]`, tối thiểu 3 phần tử (thực tế 5–7) | 38/38 đạt |
| `language` | `en` hoặc `vi`, khớp thư mục | 38/38 đạt |
| `updated` | `"2026-10-27"` | 38/38 đạt |

**Đã chuẩn hoá:** 35 file trước đó dùng biến thể front matter cũ (`seo_title`, `meta_description`, `lang`, `last_updated`, danh sách keyword kiểu block `- item`, giá trị không có ngoặc kép). Nay tất cả về một schema, nên template render chỉ cần đọc một dạng.

---

## 3. Bảng QA từng file

Cột **Title** / **Desc** = số ký tự (giới hạn 66 / 120–165). Cột **FAQ** = số câu hỏi trong mục FAQ.

| # | File | Từ | Title | Desc | H2 | FAQ | CTA |
|---|---|---|---|---|---|---|---|
| 1 | `_reworked/en/cat-ba.md` | 1509 | 56 | 146 | 10 | 5 | ✓ |
| 2 | `_reworked/en/con-dao.md` | 1612 | 58 | 156 | 10 | 5 | ✓ |
| 3 | `_reworked/en/da-lat.md` | 1540 | 57 | 148 | 11 | 5 | ✓ |
| 4 | `_reworked/en/da-nang.md` | 1583 | 64 | 154 | 9 | 6 | ✓ |
| 5 | `_reworked/en/ha-giang-loop.md` | 1876 | 51 | 162 | 11 | 6 | ✓ |
| 6 | `_reworked/en/ha-giang-nature.md` | 1740 | 49 | 162 | 10 | 6 | ✓ |
| 7 | `_reworked/en/ha-long-bay.md` | 1637 | 61 | 146 | 10 | 5 | ✓ |
| 8 | `_reworked/en/hanoi.md` | 1987 | 63 | 149 | 10 | 5 | ✓ |
| 9 | `_reworked/en/ho-chi-minh-city.md` | 1765 | 64 | 150 | 9 | 5 | ✓ |
| 10 | `_reworked/en/hoi-an.md` | 1813 | 60 | 142 | 9 | 5 | ✓ |
| 11 | `_reworked/en/hue.md` | 1723 | 65 | 158 | 10 | 6 | ✓ |
| 12 | `_reworked/en/mai-chau.md` | 1515 | 55 | 159 | 9 | 5 | ✓ |
| 13 | `_reworked/en/mekong-phuquoc.md` | 1878 | 64 | 161 | 11 | 6 | ✓ |
| 14 | `_reworked/en/mui-ne.md` | 1859 | 50 | 164 | 10 | 5 | ✓ |
| 15 | `_reworked/en/nha-trang.md` | 1837 | 61 | 159 | 11 | 5 | ✓ |
| 16 | `_reworked/en/ninh-binh.md` | 1698 | 60 | 149 | 11 | 5 | ✓ |
| 17 | `_reworked/en/phong-nha.md` | 1547 | 64 | 146 | 10 | 5 | ✓ |
| 18 | `_reworked/en/pu-luong.md` | 1492 | 57 | 160 | 9 | 5 | ✓ |
| 19 | `_reworked/en/quy-nhon.md` | 1532 | 55 | 157 | 9 | 5 | ✓ |
| 20 | `_reworked/en/sapa.md` | 2279 | 61 | 158 | 12 | 7 | ✓ |
| 21 | `_reworked/vi/cat-ba.md` | 1691 | 63 | 138 | 10 | 5 | ✓ |
| 22 | `_reworked/vi/con-dao.md` | 1948 | 60 | 162 | 10 | 5 | ✓ |
| 23 | `_reworked/vi/da-lat.md` | 1832 | 62 | 139 | 11 | 5 | ✓ |
| 24 | `_reworked/vi/da-nang.md` | 1671 | 55 | 147 | 9 | 6 | ✓ |
| 25 | `_reworked/vi/ha-long-bay.md` | 1894 | 63 | 139 | 10 | 5 | ✓ |
| 26 | `_reworked/vi/hanoi.md` | 2215 | 53 | 146 | 10 | 5 | ✓ |
| 27 | `_reworked/vi/ho-chi-minh-city.md` | 2006 | 65 | 145 | 9 | 5 | ✓ |
| 28 | `_reworked/vi/hoi-an.md` | 1999 | 64 | 136 | 9 | 5 | ✓ |
| 29 | `_reworked/vi/hue.md` | 1815 | 49 | 138 | 10 | 6 | ✓ |
| 30 | `_reworked/vi/mai-chau.md` | 1701 | 52 | 159 | 9 | 5 | ✓ |
| 31 | `_reworked/vi/mekong-phuquoc.md` | 1962 | 63 | 160 | 11 | 6 | ✓ |
| 32 | `_reworked/vi/mui-ne.md` | 2021 | 65 | 157 | 10 | 5 | ✓ |
| 33 | `_reworked/vi/nha-trang.md` | 2013 | 63 | 137 | 11 | 5 | ✓ |
| 34 | `_reworked/vi/ninh-binh.md` | 1872 | 63 | 151 | 11 | 5 | ✓ |
| 35 | `_reworked/vi/phong-nha.md` | 1820 | 63 | 138 | 10 | 5 | ✓ |
| 36 | `_reworked/vi/pu-luong.md` | 1682 | 52 | 152 | 9 | 5 | ✓ |
| 37 | `_reworked/vi/quy-nhon.md` | 1683 | 61 | 145 | 9 | 5 | ✓ |
| 38 | `_reworked/vi/sapa.md` | 2436 | 66 | 147 | 12 | 7 | ✓ |

**Tổng:** 68.683 từ · trung bình 1.807 · ngắn nhất 1.492 (`en/pu-luong.md`) · dài nhất 2.436 (`vi/sapa.md`) · 381 H2 · 202 câu hỏi FAQ · 38/38 có CTA ở cuối bài.

---

## 4. Các kiểm tra đã chạy

| Kiểm tra | Ngưỡng | Kết quả |
|---|---|---|
| Front matter đủ 7 trường | 7/7 | 38/38 đạt |
| `slug` khớp `/{lang}/{tên-file}` | khớp tuyệt đối | 38/38 đạt |
| `language` khớp thư mục | khớp tuyệt đối | 38/38 đạt |
| Số H1 | đúng 1 | 38/38 = 1 |
| Số H2 | ≥ 6 | min 9, max 12 |
| Câu hỏi FAQ | ≥ 3 | min 5, max 7 |
| CTA ở cuối bài | có | 38/38 |
| Độ dài `title` | ≤ 66 ký tự | max 66 |
| Độ dài `description` | 120–165 ký tự | 136–164 |
| Độ dài bài | ≥ 1.200 từ | min 1.492 |
| Trùng lặp đoạn văn giữa các bài | 0 | **0** (đã loại trừ dòng ghi chú giá dùng chung) |
| Thẻ HTML sót (`<div>`, `<span>`…) | 0 | 0 |
| Placeholder (`TODO`, `TBD`, `lorem`, `[insert`) | 0 | 0 |
| Hai dấu cách liên tiếp | 0 | 0 |
| Khoảng trắng cuối dòng | 0 | 0 |
| Ký tự tab | 0 | 0 |
| Bảng markdown lệch số cột | 0 | 0 |

Bảng markdown dùng đúng cú pháp `| … |`, không có dòng tiêu đề thiếu dấu phân cách.

---

## 5. Từ khóa chính — vị trí và mật độ

**Vị trí xuất hiện nguyên cụm** (tính bằng số từ từ đầu thân bài):

| Nhóm | Số file |
|---|---|
| Ngay trong H1 (vị trí 1–2) | 8 |
| Từ thứ 3 đến 100 | 20 |
| Từ 101 đến 120 | 9 |
| Trên 120 từ | 1 (`vi/ha-long-bay.md`, 143) |

Trung vị 86 từ; xa nhất 143 từ.

**7 "cảnh báo" của script — đã xác minh là dương tính giả.** Script chỉ quét đoạn 2–5 của bài để tìm cụm từ khóa; 7 file sau có cụm từ khóa **nằm ngay trong dòng H1** nên bị bỏ qua khỏi cửa sổ quét: `en/hoi-an.md`, `vi/cat-ba.md`, `vi/da-lat.md`, `vi/hoi-an.md`, `vi/nha-trang.md`, `vi/ninh-binh.md`, `vi/phong-nha.md`. Đọc trực tiếp cả 7 file xác nhận cụm từ khóa có mặt ở vị trí từ thứ 1. Không cần sửa nội dung.

**Mật độ tên điểm đến** (gộp mọi cách viết hợp lệ, ví dụ `Hanoi`/`Hà Nội`, `TP.HCM`/`Sài Gòn`):

| Chỉ số | Giá trị |
|---|---|
| Thấp nhất | 9 lần (`en/da-nang.md`, `en/pu-luong.md`, `vi/ha-long-bay.md`) |
| Trung vị | 15 lần |
| Cao nhất | 26 lần (`en/hue.md`, `vi/hue.md`) |

**Hạn chế cần biết:** cụm từ khóa chính **nguyên văn** thường chỉ xuất hiện **1 lần** trong thân bài (37/38 file; riêng `en/ha-giang-loop.md` 3 lần vì "Ha Giang Loop" là tên riêng của cung đường). Đây là chủ ý — các cụm như "Ninh Binh travel guide" lặp lại sẽ đọc rất máy móc; thay vào đó tên điểm đến được nhắc 9–26 lần và các biến thể dài nằm trong H2/FAQ. Nếu Bố muốn tối ưu theo hướng lặp cụm chính xác nhiều lần, cần chỉ định rõ vì nó đánh đổi độ tự nhiên.

---

## 6. Ghi chú giá và thông tin dao động

- **24/38 file** có nêu giá cụ thể (VND hoặc USD).
- **24/24 file đó** đều có câu ghi chú cuối bài về việc giá đã kiểm tra tháng 10/2026 và có thể thay đổi.
- **37/38 file** có câu ghi chú (13 file có ghi chú dù không nêu giá — dạng "giờ mở cửa/giờ tàu").
- **1 file không có**: `en/ha-giang-nature.md` — bài thuần văn hóa/chợ/homestay, không nêu con số giá nào.

Câu ghi chú **không dùng chung một câu lặp lại**: có 16 biến thể khác nhau, điều chỉnh theo loại bài (vé tham quan, giá tour hang động, giá phà, giá cabin du thuyền, giá món ăn). Việc này tránh cảm giác nội dung hàng loạt.

**4 file được bổ sung ghi chú trong vòng QA này:** `en/ha-long-bay.md`, `vi/ha-long-bay.md`, `en/ho-chi-minh-city.md`, `vi/ho-chi-minh-city.md` — trước đó có nêu giá nhưng thiếu câu ghi chú.

---

## 7. Slug và chuyển hướng

Slug mới đều dạng sạch, không đuôi `.html`. 9 cặp file HTML đang chạy có tên khác slug, cần 301 redirect khi chuyển lên site (bảng đầy đủ ở `SEO_CONTENT_INVENTORY.md` mục 4). Ba trường hợp đáng chú ý:

| HTML hiện tại | Slug mới |
|---|---|
| `/en/hoi-an-food-culture.html`, `/vi/hoi-an-food-culture.html` | `/en/hoi-an`, `/vi/hoi-an` |
| `/en/mekong-phuquoc-water.html`, `/vi/mekong-phuquoc-water.html` | `/en/mekong-phuquoc`, `/vi/mekong-phuquoc` |
| `/en/ha-giang-loop-adventure.html`, `/en/ha-giang-nature-culture.html` | `/en/ha-giang-loop`, `/en/ha-giang-nature` |

**Hai trang VI của Hà Giang** (`/vi/ha-giang-loop-adventure.html`, `/vi/ha-giang-nature-culture.html`) hiện **chưa có bản markdown thay thế** vì lần này chỉ yêu cầu bản EN. Nếu chuyển toàn site sang nội dung mới, hai trang này sẽ mất nội dung — cần quyết định: viết bổ sung bản VI, hoặc giữ nguyên HTML cũ.

---

## 8. Những gì báo cáo này KHÔNG kiểm

Nói rõ để không hiểu nhầm là "đã sạch tuyệt đối":

1. **Độ chính xác số liệu** — tách riêng ở `FACT_CHECK_REPORT.md`, và ở đó cũng có mục "thông tin cần xác nhận trước khi publish".
2. **Đạo văn so với bài nguồn** — chưa chạy công cụ so khớp văn bản. Việc viết lại là thủ công, nhưng không có bằng chứng định lượng về tỉ lệ trùng câu.
3. **Search volume và độ cạnh tranh của từ khóa** — không có quyền truy cập công cụ keyword. `primary_keyword` được chọn theo logic tìm kiếm phổ biến, chưa đối chiếu dữ liệu thật.
4. **Hiển thị thực tế** — Google cắt title/description theo pixel, không theo ký tự. Giới hạn 66/165 là ước lệ an toàn, chưa kiểm bằng SERP thật.
5. **`canonical`, `hreflang`, Open Graph, JSON-LD** — nội dung markdown không chứa các thẻ này; phải bổ sung ở tầng template/render. Cặp EN–VI là điều kiện cần để đặt `hreflang` đúng.
6. **Ảnh và alt text** — bài mới không kèm ảnh; cần bổ sung khi lên site.
7. **Liên kết nội bộ** — bài chưa gắn link chéo đến các bài khác trong cụm 20 điểm đến; nên bổ sung ở bước dựng site.

---

## 9. Kết luận

Về mặt **cấu trúc và kỹ thuật SEO**, 38/38 bài đạt: front matter đồng nhất, một H1, 9–12 H2 có thứ tự, 5–7 câu FAQ, CTA rõ ở cuối, title/description trong giới hạn, không trùng lặp, không lỗi định dạng.

Về mặt **nội dung**, các lỗi hệ thống về địa giới hành chính 2025–2026 đã được sửa (chi tiết ở `FACT_CHECK_REPORT.md`), thông tin không kiểm chứng được đã loại bỏ, và mọi con số giá đều kèm ghi chú thời điểm.

**Trước khi publish cần Bố quyết:**
1. Giá tour thực tế và chính sách hoa hồng — bài đang dùng giá thị trường tham khảo.
2. Chính sách miễn thị thực Phú Quốc — cần xác nhận lại với nguồn chính thức.
3. Có viết bản VI cho hai bài Hà Giang hay giữ HTML cũ.
4. Tên phường/xã mới cho các địa chỉ lưu trú cụ thể trong bài.

---

## 10. File liên quan

| File | Nội dung |
|---|---|
| `_reworked/SEO_CONTENT_INVENTORY.md` | Kiểm kê 38 file, ánh xạ nguồn → đầu ra, slug ↔ HTML cũ, phần chưa xử lý |
| `_reworked/FACT_CHECK_REPORT.md` | Những gì đã kiểm chứng, sửa, loại bỏ; nguồn tham chiếu |
| `_reworked/en/`, `_reworked/vi/` | 38 bài viết hoàn chỉnh |
