# 📍 Vị Trí Và Cách Vào Shop

Plugin chính: `ExcellentShop`, `zMenu`, `AxPlayerWarps`, `zAuctionHouseV3`, `Citizens`

📁 Config: /plugins/ExcellentShop/config.yml  
📁 Config: /plugins/ExcellentShop/virtual_shop/settings.yml  
📁 Config: /plugins/zMenu/inventories/CSHOP.yml  
📁 Config: /plugins/zMenu/inventories/MENU.yml  
📁 Config: /plugins/zMenu/inventories/WARPS.yml  
📁 Config: /plugins/zMenu/inventories/AFK.yml  
📁 Config: /plugins/AxPlayerWarps/config.yml  
📁 Config: /plugins/zAuctionHouseV3/config.yml

Earth có nhiều kiểu shop khác nhau. Không phải shop nào cũng là NPC đứng ở một chỗ; nhiều shop mở bằng lệnh/menu.

## 🛒 Shop Hệ Thống Chính

📁 Config: /plugins/ExcellentShop/virtual_shop/settings.yml

| Shop | Cách vào | Tiền tệ | Công dụng |
|---|---|---|---|
| VirtualShop main | `/shop` hoặc `/vshop` | Vault money | Mua/bán vật phẩm cơ bản theo danh mục |
| Sell GUI | `/sellgui`, `/sellmenu`, `/sellg` | Nhận Vault money | Bỏ đồ vào GUI để bán khi đóng/mua bán nhanh |
| Sell all | `/sellall` | Nhận Vault money | Bán nhanh item bán được trong túi |
| Sell hand | `/sellhand` | Nhận Vault money | Bán item đang cầm |
| Sell hand all | `/sellhandall` | Nhận Vault money | Bán toàn bộ loại item đang cầm |

`Default_Currency: vault`, `Main_Menu.Enabled: true`, `Shop_Shortcut.Commands: shop`, `Sell_Menu.Enabled: true`, `Sell_Menu.Simplified: true`.

## 🧭 Danh Mục VirtualShop

📁 Config: /plugins/ExcellentShop/virtual_shop/main.menu.yml  
📁 Config: /plugins/ExcellentShop/virtual_shop/shops/

| Category | Mục đích |
|---|---|
| `building_blocks` | Block xây dựng |
| `colored_blocks` | Block màu/trang trí |
| `decoration` | Trang trí |
| `farming` | Nông nghiệp/farm |
| `food` | Đồ ăn |
| `minerals` | Khoáng sản |
| `miscellaneous` | Vật phẩm linh tinh |
| `mob_drops` | Drop từ mob |

## 💠 Xu Shop Và Shop Menu zMenu

📁 Config: /plugins/zMenu/inventories/CSHOP.yml  
📁 Config: /plugins/zMenu/inventories/MENU.yml

`CSHOP.yml` là shop dùng Xu/PlayerPoints cho vật phẩm premium hoặc tiện ích như key, booster, gem chest, sell wand, đục ngọc. Người chơi thường vào từ menu chính hoặc lệnh/menu được cấu hình bởi zMenu.

| Shop zMenu | Vai trò | Xem thêm |
|---|---|---|
| `CSHOP.yml` | Xu Shop, vật phẩm premium/tiện ích | [shop-prices.md](shop-prices.md) |
| `CLAIM.yml` | Mua claim block bằng tiền | [shop-prices.md](shop-prices.md) |
| `AFK.yml` | Đổi điểm AFK lấy EXP/key/rank tạm/vật phẩm | [../Gameplay/levels-ranks-rebirth.md](../Gameplay/levels-ranks-rebirth.md) |
| `TANGCUONG.yml` | Mua booster bằng tiền hoặc Xu | [../Donate/boosters-keys.md](../Donate/boosters-keys.md) |
| `DONATE/DONATE.yml` | Hướng dẫn nạp và dùng Xu | [../Donate/README.md](../Donate/README.md) |

## 🏪 Player Warp Shop `/pwarp`

📁 Config: /plugins/AxPlayerWarps/config.yml

Player warp là cách người chơi tự tạo điểm dịch chuyển, thường dùng để mở shop, farm public, máy farm hoặc khu giao dịch.

| Thiết lập | Giá trị |
|---|---|
| Lệnh chính | `/pwarp`, `/pwarps`, `/pw`, `/playerwarp`, `/playerwarps`, `/axpw` |
| Tạo warp có phí | `enabled: true` |
| Giá tạo warp | `10,000` Vault money |
| Cần xác nhận khi tạo | `confirm: true` |
| Delay teleport | `3` giây, di chuyển sẽ hủy |
| Kiểm tra warp nguy hiểm | `check-unsafe-warps: true` |
| Thời gian xác nhận | `10,000ms` |
| Độ dài tên warp | `1-16` ký tự |
| Cho phép dấu cách | `false` |
| Mô tả | Tối đa `3` dòng, mặc định `Không có mô tả` |

Category player warp:

| Category | Tên hiển thị | Gợi ý dùng |
|---|---|---|
| `building` | `CÔNG TRÌNH` | Nhà đẹp, build tham quan |
| `shop` | `CỬA HÀNG` | Shop người chơi |
| `farm` | `MÁY FARM` | Farm public/auto farm |
| `pvp` | `ĐÁNH NHAU` | Khu PvP tự phát |
| `event` | `SỰ KIỆN` | Warp sự kiện |
| `fun` | `GIẢI TRÍ` | Minigame/khu vui chơi |
| `special` | `ĐẶC BIỆT` | Khu đặc biệt |
| `other` | `KHU KHÁC` | Khác |

## 🧺 Auction House `/ah`

📁 Config: /plugins/zAuctionHouseV3/config.yml

Auction House là chợ đấu giá/người chơi rao bán item.

| Mục | Giá trị |
|---|---|
| Lệnh chính | `/zauctionhouse` |
| Alias | `/ah`, `/choden`, `/hdv`, `/zauction`, `/zah`, `/zhdv` |
| Lệnh bán | `/ah sell <price> [amount]`, alias `sell`, `vendre`, `s` |
| Kinh tế mặc định | `VAULT` |
| Giá tối thiểu | `10` |
| Giá tối đa | `999999999999999999` |
| Thuế | Bật `globalTax: true`, loại `SELL`, `2.0%` |
| Cooldown bán | `10` giây |
| Hết hạn tin bán | `172800s` = 2 ngày |
| Xóa item mua/hết hạn | `604800s` = 7 ngày |
| Giới hạn item bán theo quyền | `2`, `3`, `4`, `5`, `7`, `10` item |
| Tắt ở world | `world_the_end` |

## 🧭 Nên Đi Shop Nào?

| Nhu cầu | Đi đâu |
|---|---|
| Bán nhanh đồ farm được | `/sellgui`, `/sellall`, `/sellhand` |
| Mua block/farm/mob drop cơ bản | `/shop` hoặc `/vshop` |
| Mua vật phẩm bằng Xu | Xu Shop từ menu/zMenu |
| Mua bán với người chơi | `/ah`, `/pwarp` category `CỬA HÀNG` |
| Tạo shop riêng | Tạo `/pwarp` với category `shop`, giá tạo `10,000` |
| Kiếm deal hiếm | Kiểm tra `/ah` và shop player trước khi mua bằng Xu |

Xem thêm: [shop-prices.md](shop-prices.md), [player-shops.md](player-shops.md), [../Gui/shop-guis.md](../Gui/shop-guis.md)
