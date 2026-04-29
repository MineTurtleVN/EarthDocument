# 📁 Config Index

Plugin chính: các config đã kiểm tra

📁 Config: /plugins/

| Config path | Dùng trong docs |
|---|---|
| `/plugins/Multiverse-Core/worlds.yml` | Worlds, README |
| `/plugins/TurtleDungeon/config.yml` | PvE, PvP regions, dungeon settings |
| `/plugins/TurtleDungeon/bossbar.yml` | PvE bossbar/stage states |
| `/plugins/TurtleDungeon/messages.yml` | Dungeon messages, failure/reward/capture text |
| `/plugins/TurtleDungeon/Dungeons/dungeon1.yml` ... `dungeon10.yml` | Dungeon details |
| `/plugins/TurtleLevel/gui.yml` | Level GUI |
| `/plugins/MMOItems/item/` | Item category files |
| `/plugins/MMOItems/item/material.yml` | Dungeon materials, upgrade materials |
| `/plugins/MMOItems/drops.yml` | Vanilla mob MMOItems drops |
| `/plugins/ExcellentCrates/config.yml` | Crate behavior/rarity |
| `/plugins/ExcellentCrates/crates/` | Crate rewards |
| `/plugins/ExcellentCrates/crates/dungeons.yml` | Dungeon crate |
| `/plugins/ExcellentCrates/crates/koth.yml` | KOTH crate preview |
| `/plugins/ExcellentCrates/keys/` | Crate keys |
| `/plugins/ExcellentCrates/keys/dungeon.yml` | Dungeon key |
| `/plugins/ExcellentShop/config.yml` | Shop modules/clicks |
| `/plugins/ExcellentShop/virtual_shop/` | Shop GUI/settings |
| `/plugins/ExcellentShop/virtual_shop/shops/` | Shop categories |
| `/plugins/zMenu/inventories/` | Player-facing menus |
| `/plugins/zMenu/inventories/DONATE/` | Donate, mốc nạp, chuỗi nạp |
| `/plugins/AxKoth/config.yml` | KOTH global settings |
| `/plugins/AxKoth/schedulers.yml` | KOTH schedule |
| `/plugins/AxKoth/koths/Hero.yml` | KOTH Địa Bàn arena/reward |
| `/plugins/TurtleTop/points.yml` | Top point keys, reset settings |
| `/plugins/TurtleTop/gui/diaban.yml` | Top Địa Bàn GUI |
| `/plugins/zMenu/inventories/DUATOP.yml` | Top menu placeholders/rewards |

Sensitive values found in database sections were intentionally excluded from player documentation.

## ⚠️ Config Không Dùng Làm Nguồn Chính

| Path | Lý do |
|---|---|
| `/plugins/TurtleDungeon/config.yml` database section | Có credential, không copy vào docs |
| `/plugins/MythicMobs/skills/Dungeon.yml` | Pterodactyl trả HTTP 504 khi đọc |
| `/plugins/zMenu/inventories/SHOP.yml` | Optional read bị HTTP 504 trong pass non-PvE |

Xem thêm: [plugin-mapping.md](plugin-mapping.md), [commands-permissions.md](commands-permissions.md)
