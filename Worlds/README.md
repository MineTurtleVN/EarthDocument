# 🌎 Worlds Tổng Quan

Plugin chính: `Multiverse-Core`, `zMenu`, `WorldGuard`, `TurtleDungeon`

📁 Config: /plugins/Multiverse-Core/worlds.yml
📁 Config: /plugins/zMenu/inventories/WARPS.yml
📁 Config: /plugins/zMenu/inventories/RTP.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/

Earth hiện có các world Multiverse đã đọc được: `Lobby`, `earth`, `world`, `KhuNuoiRua`, `Dungeon1`, `Dungeon2`, `Dungeon3`. Các dungeon D4/D5 dùng trong TurtleDungeon config có world `Dungeon4` và `Dungeon5`, nhưng chúng không xuất hiện trong phần `worlds.yml` đã đọc ở thời điểm audit này, nên tài liệu đánh dấu là nguồn từ TurtleDungeon thay vì Multiverse.

## 📍 Bảng World Chính

| World | Spawn/Tâm đã đọc | Mục đích | PvP Multiverse | Nguồn |
|---|---|---|---|---|
| `Lobby` | `0,168,0` | Hub, crate, donate, KOTH `Địa Bàn`, menu điều hướng | `true` | `worlds.yml`, AxKoth |
| `earth` | `13824,75,-7680` | World sinh tồn/trái đất, đích `/rtp` | `true` | `worlds.yml`, `RTP.yml` |
| `world` | `16,64,-48` | World vanilla/sinh tồn phụ hoặc legacy | `true` | `worlds.yml` |
| `KhuNuoiRua` | `0.807,201,-0.127` | Khu nuôi/rùa, liên quan hệ thống Turtle | `true` | `worlds.yml` |
| `Dungeon1` | spawn `0,65,0`; dungeon center `0,33,79` và PvP `500,33,580` | D1 Ngôi Đền Của Đá | `true` | `worlds.yml`, TurtleDungeon |
| `Dungeon2` | spawn `0,65,0`; dungeon center `500,59,443` và PvP `734,59,450` | D2 Bản Di Chúc Đất & Lửa | `true` | `worlds.yml`, TurtleDungeon |
| `Dungeon3` | spawn `0,65,0`; dungeon center `0,65,-1` và PvP `499,68,621` | D3 Tế Đàn Rừng Sương Độc | `true` | `worlds.yml`, TurtleDungeon |
| `Dungeon4` | center `102,77,116` và PvP `535,19,499` | D4 Vực Thẳm Rực Cháy | chưa xác nhận từ Multiverse | TurtleDungeon |
| `Dungeon5` | center `-13,51,-313` và PvP `488,51,193` | D5 Vườn Địa Đàng | chưa xác nhận từ Multiverse | TurtleDungeon |

## 🧭 Đi Đâu Làm Gì?

| Nhu cầu | Đi tới | Cách vào |
|---|---|---|
| Về hub, mở crate, xem sự kiện | `Lobby` | `/spawn`, `/hub`, hoặc menu server |
| Farm/build/sinh tồn | `earth` | `/rtp` trong GUI `VIETJET` hoặc menu `/warps` |
| Đi dungeon D1-D5 | `Dungeon1` đến `Dungeon5` | Menu dungeon hoặc warp dungeon trong GUI |
| KOTH Địa Bàn | `Lobby`, vùng `X -46..-38`, `Y 45..49`, `Z -13..-5` | Event lúc `12:00` và `20:00` |
| Mua/bán và dịch vụ | Thường ở `Lobby` hoặc GUI | `/shop`, `/rank`, `/donate`, `/claimshop` |

## ⚠️ Ghi Chú Về PvP

Multiverse đang ghi `pvp: true` cho các world đã đọc. Điều này không có nghĩa mọi khu đều cho đánh tự do, vì WorldGuard, region dungeon, PvPManager hoặc plugin riêng có thể chặn theo vùng. Riêng dungeon PvP đã được TurtleDungeon tách bằng region `dungeon1pvp` đến `dungeon5pvp`; người chơi nên xem kỹ tên bản trước khi vào.

## 📚 Tài Liệu Chi Tiết

| File | Nội dung |
|---|---|
| [world-list.md](world-list.md) | Bảng world, spawn, mục đích, trạng thái PvP |
| [warps-portals.md](warps-portals.md) | `/warps`, `/rtp`, player warp, đường vào khu vực |
| [regions.md](regions.md) | Region dungeon, PvP variants, lưu ý WorldGuard |

Xem thêm: [../PvE/dungeons.md](../PvE/dungeons.md), [../PvP/maps-events.md](../PvP/maps-events.md), [../Gui/system-guis.md](../Gui/system-guis.md)
