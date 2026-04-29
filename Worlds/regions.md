# 🧱 Regions Và Khu Vực

Plugin chính: `WorldGuard`, `TurtleDungeon`, `PvPManager`

📁 Config: /plugins/WorldGuard/
📁 Config: /plugins/TurtleDungeon/Dungeons/
📁 Config: /plugins/TurtleDungeon/config.yml
📁 Config: /plugins/AxKoth/koths/Hero.yml

Region quan trọng nhất đã xác nhận đến từ TurtleDungeon và AxKoth. WorldGuard có thể quyết định cờ PvP/build/use thực tế, nhưng tài liệu này chỉ ghi các region/path đã đọc được từ config gameplay.

## 🏛️ Region Dungeon

| Region | Tên hiển thị | World | Tâm khu | Loại |
|---|---|---|---|---|
| `dungeon1` | Ngôi Đền Của Đá | `Dungeon1` | `0,33,79` | Thường |
| `dungeon1pvp` | Ngôi Đền Của Đá (PvP) | `Dungeon1` | `500,33,580` | PvP |
| `dungeon2` | Bản Di Chúc Của Đất Và Lửa | `Dungeon2` | `500,59,443` | Thường |
| `dungeon2pvp` | Bản Di Chúc Của Đất Và Lửa (PvP) | `Dungeon2` | `734,59,450` | PvP |
| `dungeon3` | Tế Đàn Rừng Sương Độc | `Dungeon3` | `0,65,-1` | Thường |
| `dungeon3pvp` | Tế Đàn Rừng Sương Độc (PvP) | `Dungeon3` | `499,68,621` | PvP |
| `dungeon4` | Tế Đàn Vực Thẳm Rực Cháy | `Dungeon4` | `102,77,116` | Thường |
| `dungeon4pvp` | Tế Đàn Vực Thẳm Rực Cháy (PvP) | `Dungeon4` | `535,19,499` | PvP |
| `dungeon5` | Vườn Địa Đàng | `Dungeon5` | `-13,51,-313` | Thường |
| `dungeon5pvp` | Vườn Địa Đàng (PvP) | `Dungeon5` | `488,51,193` | PvP |

## 🏳️ KOTH Địa Bàn

📁 Config: /plugins/AxKoth/koths/Hero.yml

| Khu | World | Góc 1 | Góc 2 | Mục đích |
|---|---|---|---|---|
| `Hero` / `Địa Bàn` | `Lobby` | `-46,45,-13` | `-38,49,-5` | Đứng chiếm trong `60` giây để thắng KOTH |

## ⚠️ Lưu Ý Region

| Lưu ý | Chi tiết |
|---|---|
| Dungeon PvP tách region riêng | Tên có hậu tố `pvp`, reward/EXP menu ghi cao hơn bản thường |
| Dungeon có kiểm tra rời vùng | TurtleDungeon có proximity check radius `100`, fail-on-leave `true` |
| Boss bị kiểm tra vị trí | Boss teleport/check radius trong config tránh kéo boss ra ngoài khu |
| KOTH nằm ở Lobby | Dù Lobby là hub, vùng KOTH là vùng cạnh tranh theo lịch |

Xem thêm: [world-list.md](world-list.md), [../PvE/dungeons.md](../PvE/dungeons.md), [../PvP/maps-events.md](../PvP/maps-events.md)
