# Website Vietnam Charming — Content Repository

## Cấu trúc thư mục

```
Website_vietnamcharming/
├── content/
│   ├── en/
│   │   ├── destinations/     # 20 bài EN destination-level (đã xong)
│   │   └── attractions/      # attraction-level EN (đang viết)
│   └── vi/
│       ├── destinations/     # 18 bài VI destination-level (đã xong)
│       └── attractions/      # attraction-level VI (đang viết)
├── data/
│   └── master_plan.json      # Kế hoạch tổng 262 bài
├── FACT_CHECK_REPORT.md
├── SEO_CONTENT_INVENTORY.md
├── SEO_QA_REPORT.md
└── README.md
```

## Trạng thái

| Loại | EN done | VI done | Còn lại |
|------|---------|---------|---------|
| Destination | 20 | 18 | 2 VI |
| Attraction | 0 | 0 | 122 EN + 120 VI |
| **Tổng** | **20** | **18** | **224** |

## Quy ước đặt tên

- **Destination**: `{slug}.md` (ví dụ: `hanoi.md`, `phong-nha.md`)
- **Attraction**: `{destination}-{attraction}.md` (ví dụ: `hanoi-old-quarter.md`, `phong-nha-son-doong.md`)

## Format bài viết

Xem `SEO_QA_REPORT.md` mục 2 — YAML front matter 7 trường + 4 trường attraction:
`location`, `coordinates`, `opening_hours`, `ticket_price`

## Cách viết bài mới

1. Đọc `data/master_plan.json` → lấy slug attraction `status: pending`
2. Viết theo format chuẩn (xem mẫu trong `content/en/destinations/`)
3. Cập nhật `status` trong `master_plan.json` → `done`
4. Commit & push
