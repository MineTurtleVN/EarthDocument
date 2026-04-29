# 🚪 Warp Và Portal

Plugin chính: `zMenu`, `BetterRTP`, `Multiverse-Core`

📁 Config: /plugins/zMenu/inventories/WARPS.yml
📁 Config: /plugins/zMenu/inventories/RTP.yml
📁 Config: /plugins/zMenu/inventories/HUONGDAN.yml

Người chơi nên dùng menu `/warps` và `/rtp` thay vì đoán tên world trực tiếp. `WARPS.yml` là menu khu vực chính, còn `RTP.yml` là menu random teleport tới `trái đất`.

## 🧭 Warp Trong `/warps`

| Nút | Slot | Lệnh chạy | Dùng để làm gì |
|---|---:|---|---|
| Khu Người Chơi | `28` | `/pwarp` | Xem player warp, ghé khu người chơi tự tạo |
| Khu Thế Giới | `34` | `/pwarp` | Menu ghi khu định nghĩa ở các thành phố lớn trên thế giới |
| Khu Trao Đổi | `11` | `/warp trade` | Đổi vật phẩm, nguyên liệu, định hướng cày cuốc |
| Khu Gacha | `13` | `/warp crates` | Mở crate/key |
| Khu AFK | `14` | `/warp afk` | AFK nhận điểm online/key theo hướng dẫn |
| Bảng Xếp Hạng | `15` | `/warp top` | Xem top server |
| Đánh Nhau | `16` | `/warp pvp` | Khu PvP |

## ✈️ Random Teleport

📁 Config: /plugins/zMenu/inventories/RTP.yml

| Nút | Mô tả |
|---|---|
| Trái đất | Random teleport miễn phí tới world sinh tồn chính |
| Thời gian hiển thị | `2 phút` |
| Command | `rtp` |

Menu `RTP.yml` có các lựa chọn Nether/End-like được comment trong bản đã đọc, nên tài liệu chỉ coi `trái đất` là lựa chọn đã xác nhận.

## 📖 Lệnh Liên Quan Trong Hướng Dẫn

| Lệnh | Ý nghĩa |
|---|---|
| `/spawn` | Về đại sảnh |
| `/rtp` | Random teleport |
| `/tpa`, `/tpaccept`, `/tpadeny` | Teleport giữa người chơi |
| `/ewarp` | Dịch chuyển tới cứ điểm |
| `/thanhchien cudiem` | Xem danh sách cứ điểm |
| `/map` | Lấy link xem bản đồ Trái Đất |

Xem thêm: [system-guis.md](../Gui/system-guis.md)
