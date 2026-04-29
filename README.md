# 🌍 EarthDocument - Hướng Dẫn A-Z

Plugin chính: `Multiverse-Core`, `TurtleDungeon`, `TurtleLevel`, `MMOItems`, `ExcellentShop`, `ExcellentCrates`, `zMenu`, `PvPManager`

📁 Config: /plugins/Multiverse-Core/worlds.yml
📁 Config: /plugins/TurtleDungeon/config.yml
📁 Config: /plugins/TurtleLevel/config.yml
📁 Config: /plugins/MMOItems/item-types.yml

## Server này chơi như thế nào?

Earth là server sinh tồn/RPG xoay quanh vòng lặp: vào `Lobby`, di chuyển sang thế giới `earth` hoặc `world`, farm tài nguyên, nâng cấp level, kiếm MMOItems, đi dungeon, mở crate, mua bán bằng shop, rồi cạnh tranh PvP/KOTH/event khi đã đủ trang bị.

## Người mới vào làm gì trước?

| Bước | Việc cần làm | Nơi đọc thêm |
|---|---|---|
| 1 | Mở menu chính, xem hướng dẫn và warp | [GUI](Gui/README.md) |
| 2 | Vào `earth` hoặc `world` để bắt đầu farm | [Worlds](Worlds/world-list.md) |
| 3 | Kiếm tiền/tài nguyên đầu tiên, dùng `/vshop` khi cần mua bán | [Shops](Shops/player-shops.md) |
| 4 | Theo dõi level và mốc nâng cấp nhân vật | [Gameplay](Gameplay/levels-ranks-rebirth.md) |
| 5 | Giữ key/crate, MMOItems và nguyên liệu nâng cấp | [Items](Items/README.md) |

## Early-game làm gì?

Tập trung vào sinh tồn ở `earth`, kiếm tiền qua tài nguyên cơ bản, mở các GUI hướng dẫn như `HUONGDAN.yml`, `MENU.yml`, `WARPS.yml`, rồi mua vật phẩm cần thiết ở shop ảo `/vshop`. Nếu nhận key AFK, dungeon hoặc nguyên liệu, xem trước phần thưởng trước khi mở crate.

## Mid-game làm gì?

Khi đã có bộ đồ MMOItems cơ bản, bắt đầu đi dungeon thấp (`dungeon1` đến `dungeon3`), nâng tier trang bị, gom nguyên liệu từ crate `nguyenlieu`, `dungeons`, và kiểm tra các GUI dungeon trong zMenu (`DUNGEONS.yml`, `DUNGEON_D1.yml`...).

## Late-game/end-game làm gì?

Mục tiêu cuối là clear dungeon cao (`dungeon8` đến `dungeon10`), săn item 5 sao từ MMOItems/ExcellentCrates, tham gia PvP/KOTH/event, tối ưu bộ trang bị theo loại vũ khí và giáp, rồi cạnh tranh top server.

## Nạp thẻ mua gì?

Ưu tiên mua thứ tăng tốc tiến trình lâu dài: key crate giá trị, booster, bundle nguyên liệu, hoặc rank/VIP nếu GUI donate đang mở bán. Không nên dồn tiền vào vật phẩm dùng một lần quá sớm nếu chưa có nền trang bị ổn định.

| Giai đoạn | Nên mua | Tránh mua quá sớm |
|---|---|---|
| Newbie | Key nguyên liệu, booster farm, gói khởi đầu | Item PvP đắt tiền |
| Mid-game | Key dungeon, vật liệu nâng cấp, VIP tiện ích | Skin/trang trí nếu thiếu đồ farm |
| End-game | Key trang bị, booster, bundle sự kiện | Gói thấp không còn tác dụng |

## Farm ở đâu?

| Mục tiêu | Nơi farm | Ghi chú |
|---|---|---|
| Tài nguyên cơ bản | `earth`, `world` | Thế giới sinh tồn chính |
| Dungeon loot | `Dungeon1` đến `Dungeon10` | Có bản PvP theo region dungeon PvP |
| Crate/key | ExcellentCrates | Key AFK, dungeon, nguyên liệu, spawner |
| Shop tiền | `/vshop` | ExcellentShop VirtualShop |

## Mua đồ ở đâu?

| Hệ thống | Cách vào | Tài liệu |
|---|---|---|
| Shop ảo | `/vshop` | [Shops/player-shops.md](Shops/player-shops.md) |
| Menu chính | zMenu `MENU.yml` | [Gui/system-guis.md](Gui/system-guis.md) |
| Donate | zMenu `DONATE/`, `EVENT_MOCNAP.yml` | [Donate](Donate/README.md) |
| Crate | ExcellentCrates hologram/block | [Items/rewards-crates.md](Items/rewards-crates.md) |

## Mục lục chi tiết

| Folder | Nội dung |
|---|---|
| [Gameplay](Gameplay/README.md) | Vòng lặp chơi, level, tiền tệ, nâng cấp |
| [PvE](PvE/README.md) | Dungeon, boss, mob, phần thưởng PvE |
| [PvP](PvP/README.md) | Combat tag, PvP, KOTH/event |
| [Worlds](Worlds/README.md) | Danh sách world, warp, region |
| [Shops](Shops/README.md) | Shop, giá, mua bán |
| [Donate](Donate/README.md) | Rank, bundle, booster, key nạp |
| [Gui](Gui/README.md) | zMenu và các GUI quan trọng |
| [Items](Items/README.md) | MMOItems, crate rewards, vật liệu |
| [Plugins](Plugins/README.md) | Mapping plugin, config, lệnh/quyền |
