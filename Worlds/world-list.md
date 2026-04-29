# 🧭 Danh Sách World

Plugin chính: `Multiverse-Core`, `TurtleDungeon`

📁 Config: /plugins/Multiverse-Core/worlds.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/

| World | Generator | PvP | Spawn/tọa độ | Mục đích |
|---|---|---|---|---|
| `Lobby` | VoidGen | `true` | `0,168,0` | Hub chính, crate, KOTH, menu, NPC/khu dịch vụ |
| `earth` | VoidGen | `true` | `13824,75,-7680` | World Earth/sinh tồn chính, đích `/rtp` |
| `world` | vanilla | `true` | `16,64,-48` | World sinh tồn mặc định/legacy |
| `KhuNuoiRua` | VoidGen | `true` | `0.807,201,-0.127` | Khu nuôi rùa/farm đặc thù |
| `Dungeon1` | VoidGen | `true` | spawn `0,65,0`; center `0,33,79` | D1 Ngôi Đền Của Đá, bản PvP center `500,33,580` |
| `Dungeon2` | VoidGen | `true` | spawn `0,65,0`; center `500,59,443` | D2 Bản Di Chúc Đất & Lửa, bản PvP center `734,59,450` |
| `Dungeon3` | VoidGen | `true` | spawn `0,65,0`; center `0,65,-1` | D3 Tế Đàn Rừng Sương Độc, bản PvP center `499,68,621` |
| `Dungeon4` | chưa thấy trong `worlds.yml` | chưa xác nhận | center `102,77,116`; PvP `535,19,499` | D4 từ TurtleDungeon config |
| `Dungeon5` | chưa thấy trong `worlds.yml` | chưa xác nhận | center `-13,51,-313`; PvP `488,51,193` | D5 từ TurtleDungeon config |

## ⚙️ Thuộc Tính Chung Từ Multiverse

| Thuộc tính | Giá trị thường gặp | Ý nghĩa |
|---|---|---|
| `gamemode` | `survival` | Người chơi vào world ở chế độ sinh tồn |
| `allow-flight` | `false` | Bay phụ thuộc permission/plugin rank, không phải world mặc định |
| `entry-fee.enabled` | `false` | Không thu phí vào world ở Multiverse |
| `player-limit` | `-1` | Không giới hạn người chơi theo world trong config này |
| `portal-form` | `all` | Cho phép dạng portal theo Multiverse |
| `spawning.*.spawn` | `true` | Nhóm mob/animal mặc định bật, trừ khi plugin khác chặn |

Lưu ý: `pvp: true` ở Multiverse chỉ là cấu hình world cấp cao. An toàn thực tế còn phụ thuộc WorldGuard, PvPManager, region dungeon và plugin riêng. Không nên suy luận rằng mọi vị trí trong `Lobby` đều đánh được chỉ từ dòng này.

Xem thêm: [warps-portals.md](warps-portals.md), [regions.md](regions.md), [../PvE/dungeons.md](../PvE/dungeons.md)
