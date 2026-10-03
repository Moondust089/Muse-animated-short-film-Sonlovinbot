# 🎬 Muse Animated Short Film

**Tác giả:** Đặng Hữu Sơn ([sonlovinbot](https://github.com/sonlovinbot))

Skill dựng phim hoạt hình ngắn **từ đầu đến cuối trên Muse AI** — từ một ý tưởng thô thành file MP4 hoàn chỉnh: nhân vật, kịch bản, hình ảnh, video, thuyết minh và dựng phim.

*An end-to-end skill for producing animated short films on Muse AI — from a raw idea to a finished MP4.*

## Skill này làm gì?

Pipeline 7 giai đoạn đã kiểm chứng qua dự án thật "The Last Lantern" (8 cảnh, 2D Disney/Pixar):

| # | Giai đoạn | Kết quả |
|---|-----------|---------|
| 0 | Thu thập đầu vào | Thời lượng → số cảnh, ngôn ngữ, tỷ lệ 16:9/9:16 |
| 1 | Character sheets | Khóa nhân vật (nhiều góc + biểu cảm) |
| 2 | Story bible | Chốt kịch bản: logline, character lock, từng cảnh |
| 3 | Keyframes | K1..K(N+1), luật match-cut |
| 4 | Mega prompt | 1 prompt copy-paste cho mỗi cảnh |
| 5 | Generate video | Từng clip first-frame → last-frame |
| 6 | Làm VO | Kịch bản thuyết minh kiểu kể chuyện |
| 7 | Dựng phim | ffmpeg: normalize, nối, mix VO |

Kèm theo: **luật realism** (hành động vật lý phải đúng thực tế), **STRICT ASPECT RATIO LOCK** (ref đầu vào phải cùng tỷ lệ với output), và **10+ bài học xương máu**.

## Cách dùng (cho người mới)

1. **Cài skill:** copy cả folder này vào thư mục skills của Muse AI, VD: `~/workspace/skills/animated-short-film/`
   - Hoặc: dán link repo này vào chat Muse, Muse sẽ tự cài.
2. **Mở chat và nói:** "Tôi muốn làm phim hoạt hình ngắn."
3. **Trả lời 3 câu hỏi đầu tiên:** phim dài bao lâu? ngôn ngữ nào? tỷ lệ 16:9 hay 9:16?
4. **Duyệt ở các điểm chốt:** mô tả nhân vật → story bible → keyframes → từng video → VO → phim cuối. Bạn chỉ việc xem và nói "ok" hoặc "sửa chỗ này".

Bạn không cần đọc các file reference — Muse tự đọc khi cần. Mọi prompt kỹ thuật, câu lệnh generate và dựng phim đã nằm trong skill.

## Cấu trúc

```
├── SKILL.md                  # Quy trình + luật vận hành (Muse đọc)
├── README.md                 # File này (người đọc)
└── references/
    ├── 01-character-sheets.md
    ├── 02-story-and-script.md
    ├── 03-keyframes.md
    ├── 04-mega-prompts.md
    ├── 05-video-generation.md
    ├── 06-vo-production.md
    ├── 07-assembly.md
    └── 08-lessons.md
```

## Giấy phép

MIT — dùng tự do, ghi credit tác giả khi chia sẻ lại.
