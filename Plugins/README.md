# 🔌 Plugins Tổng Quan

Plugin chính: toàn bộ thư mục `/plugins/`

📁 Config: /plugins/

Trang này là inventory nhanh cho các plugin đã được tài liệu tham chiếu. Mục tiêu không phải liệt kê từng file JAR, mà nối plugin với hệ thống người chơi thật sự thấy: dungeon, world, shop, donate, GUI, item, PvP/event và placeholder.

## 🧭 Plugin Theo Hệ Thống

| Plugin | Hệ thống | Người chơi thấy gì | Config chính |
|---|---|---|---|
| `zMenu` | GUI điều hướng | `/menu`, `/warps`, `/rtp`, `/rank`, `/donate`, Xu Shop, dungeon menu | `/plugins/zMenu/inventories/` |
| `ExcellentShop` | Shop thường | `/shop`, `/vshop`, `/sellgui`, `/sellall`, `/sellhand` | `/plugins/ExcellentShop/config.yml`, `/virtual_shop/` |
| `TurtleDungeon` | Dungeon D1-D5 | Stage, boss, capture heart, reward, PvP variants | `/plugins/TurtleDungeon/` |
| `MythicMobs` | Mob/boss PvE | Quái dungeon, boss, kỹ năng, drop skill | `/plugins/MythicMobs/` |
| `MMOItems` | Item tùy chỉnh | Trang bị, nguyên liệu, consumable, đá nâng cấp | `/plugins/MMOItems/item/` |
| `ExcellentCrates` | Crate/key | Dungeon crate, KOTH crate preview, key | `/plugins/ExcellentCrates/` |
| `Multiverse-Core` | Worlds | `Lobby`, `earth`, `Dungeon1-3`, `KhuNuoiRua` | `/plugins/Multiverse-Core/worlds.yml` |
| `WorldGuard` | Region | Safe zone, dungeon region, PvP/non-PvP vùng | `/plugins/WorldGuard/` |
| `TurtleLevel` | Cấp Độ Rùa | GUI level, reward thường/Premium, stats | `/plugins/TurtleLevel/gui.yml` |
| `AxKoth` | KOTH Địa Bàn | Event `12:00` và `20:00`, capture 60s, reward | `/plugins/AxKoth/` |
| `TurtleTop` | Bảng top | Top Địa Bàn, placeholder top player/point | `/plugins/TurtleTop/` |
| `PlayerPoints` | Xu | Xu trong menu, rank shop, Xu Shop | placeholder `%playerpoints_points%` |
| `Vault`/economy | Tiền thường | Balance, shop thường, repair, claim shop | dùng bởi ExcellentShop/zMenu |

## 📁 Config Đã Đọc Nhiều Nhất

| Nhóm | Config |
|---|---|
| GUI | `MENU.yml`, `WARPS.yml`, `RTP.yml`, `HUONGDAN.yml`, `RANK.yml`, `CSHOP.yml`, `CLAIM.yml`, `REPAIR.yml`, `CHATCOLOR.yml`, `KIT.yml` |
| Donate | `DONATE/DONATE.yml`, `DONATE/MOCNAP.yml`, `DONATE/MOCNAP2.yml`, `DONATE/CHUOINAP.yml` |
| Shop | `ExcellentShop/config.yml`, `virtual_shop/settings.yml`, `virtual_shop/main.menu.yml`, `virtual_shop/shops/` |
| Worlds | `Multiverse-Core/worlds.yml`, `TurtleDungeon/Dungeons/*.yml` |
| PvE | `TurtleDungeon/config.yml`, `bossbar.yml`, `messages.yml`, `Dungeons/dungeon1-10.yml`, `MythicMobs/mobs/Dungeon/Dungeon1-5.yml` |
| PvP | `AxKoth/config.yml`, `schedulers.yml`, `koths/Hero.yml`, `TurtleTop/points.yml`, `TurtleTop/gui/diaban.yml` |

## ⚠️ Admin Notes

| Lưu ý | Chi tiết |
|---|---|
| Không copy secrets | `/plugins/TurtleDungeon/config.yml` có thông tin database, tài liệu chỉ dùng gameplay setting |
| Server offline khi audit | Một số live value như top hiện tại không xác minh được |
| Một file MythicMobs skill bị 504 | `/plugins/MythicMobs/skills/Dungeon.yml` không dùng làm nguồn chính vì panel trả HTTP 504 |
| zMenu không phải DeluxeMenus | Folder docs vẫn có `deluxemenus.md` từ cấu trúc cũ, nhưng config thực tế là zMenu |

## 📚 Tài Liệu Chi Tiết

| File | Nội dung |
|---|---|
| [plugin-mapping.md](plugin-mapping.md) | Plugin -> hệ thống |
| [commands-permissions.md](commands-permissions.md) | Lệnh/quyền quan trọng |
| [placeholders.md](placeholders.md) | PlaceholderAPI và placeholder |
| [config-index.md](config-index.md) | Index config đã đọc/tham chiếu |

Xem thêm: [../Gui/README.md](../Gui/README.md), [../Gameplay/README.md](../Gameplay/README.md), [../PvE/README.md](../PvE/README.md)
