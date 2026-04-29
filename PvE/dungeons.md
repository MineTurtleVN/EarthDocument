# 🏛️ Dungeon

Plugin chính: `TurtleDungeon`, `zMenu`, `Multiverse-Core`

📁 Config: /plugins/TurtleDungeon/config.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon1.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon10.yml
📁 Config: /plugins/zMenu/inventories/DUNGEONS.yml

Server có 10 file dungeon chính từ `dungeon1.yml` đến `dungeon10.yml`, cộng GUI dungeon trong zMenu.

| Dungeon/Region | Tên hiển thị | Ghi chú |
|---|---|---|
| dungeon1 | Ngôi Đền Của Đá | Có biến thể PvP `dungeon1pvp` |
| dungeon2 | Bản Di Chúc Của Đất Và Lửa | Có biến thể PvP |
| dungeon3 | Tế Đàn Rừng Sương Độc | Có biến thể PvP |
| dungeon4 | Tế Đàn Vực Thẳm Rực Cháy | Có biến thể PvP |
| dungeon5 | Vườn Địa Đàng | Có biến thể PvP |
| dungeon6-10 | Dungeon cấp cao | Có file riêng trong `Dungeons/` |

Thiết lập quan trọng:

| Key | Giá trị | Ý nghĩa |
|---|---:|---|
| `settings.preparing-kills-per-player` | 20 | Số kill chuẩn bị theo mỗi người chơi |
| `settings.reentry-cooldown.death-seconds` | 60 | Chết trong dungeon phải chờ 60 giây để vào lại |
| `settings.inactivity.kick-after-seconds` | 300 | Không hoạt động 5 phút sẽ bị xử lý |
| `settings.proximity-check.radius` | 100 | Rời quá xa vùng dungeon có thể fail |
| `settings.boss-teleport-radius` | 30 | Boss đi quá xa sẽ bị kéo về |

Xem thêm: [bosses.md](bosses.md), [dungeon-items.md](../Items/dungeon-items.md)
