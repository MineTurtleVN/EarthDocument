# 🛒 Shops Tổng Quan

Plugin chính: `ExcellentShop`, `zMenu`, `PlayerPoints`

📁 Config: /plugins/ExcellentShop/config.yml
📁 Config: /plugins/ExcellentShop/virtual_shop/settings.yml
📁 Config: /plugins/ExcellentShop/virtual_shop/main.menu.yml
📁 Config: /plugins/ExcellentShop/virtual_shop/shops/
📁 Config: /plugins/zMenu/inventories/CSHOP.yml
📁 Config: /plugins/zMenu/inventories/CLAIM.yml
📁 Config: /plugins/zMenu/inventories/RANK.yml

Shop của Earth chia thành 2 nhóm tiền tệ lớn: shop thường dùng Vault money qua `ExcellentShop`, và shop đặc biệt dùng Xu qua zMenu/PlayerPoints. Người mới nên dùng `/shop` để mua/bán vật phẩm cơ bản, dùng `/sellgui` hoặc `/sellall` để xả đồ farm, còn Xu nên giữ cho rank, vật phẩm tiện ích hoặc mốc quan trọng.

## 🧭 Lệnh Shop Chính

| Lệnh | Plugin | Chức năng | Ghi chú config |
|---|---|---|---|
| `/shop` | ExcellentShop | Mở main VirtualShop | `Shop_Shortcut.Commands: shop` |
| `/vshop` | ExcellentShop | Alias module VirtualShop | `Command_Aliases: vshop` |
| `/sellgui`, `/sellmenu`, `/sellg` | ExcellentShop | Mở GUI kéo thả đồ để bán | `Sell_Menu.Enabled: true`, `Simplified: true` |
| `/sellall` | ExcellentShop | Bán toàn bộ item hợp lệ trong túi | `Sell_All.Enabeled: true` |
| `/sellhand` | ExcellentShop | Bán item đang cầm | `Sell_Hand.Enabled: true` |
| `/sellhandall` | ExcellentShop | Bán toàn bộ stack/item cùng loại đang cầm | `Sell_Hand_All.Enabled: true` |
| `/rank` | zMenu | Mua rank bằng Xu | `RANK.yml` |
| `/claimshop` | zMenu | Mua block claim bằng tiền | `CLAIM.yml` |

## 🧱 Danh Mục VirtualShop

📁 Config: /plugins/ExcellentShop/virtual_shop/shops/

| Danh mục | Ý nghĩa người chơi | Ghi chú |
|---|---|---|
| `building_blocks` | Khối xây dựng cơ bản | Dùng cho nhà/base |
| `colored_blocks` | Khối màu/trang trí màu | Dùng cho decor |
| `decoration` | Vật phẩm trang trí | Dùng cho build chi tiết |
| `farming` | Cây trồng/nguyên liệu farm | Dùng cho farm tiền/nguyên liệu |
| `food` | Đồ ăn | Dùng khi mới chơi hoặc đi dungeon |
| `minerals` | Khoáng sản | Liên quan nâng cấp/craft |
| `miscellaneous` | Vật phẩm linh tinh | Kiểm tra giá trước khi mua số lượng lớn |
| `mob_drops` | Drop từ mob | Có thể dùng craft, trade hoặc bán |

## 💰 Cơ Chế Giá Và Bán

| Cơ chế | Giá trị config | Người chơi cần biết |
|---|---|---|
| Tiền mặc định | `Default_Currency: vault` | `/shop` dùng tiền server, không phải Xu |
| Click trái | `LEFT: BUY_SELECTION` | Mở chọn số lượng mua |
| Click phải | `RIGHT: SELL_SELECTION` | Mở chọn số lượng bán |
| Shift trái | `SHIFT_LEFT: BUY_SINGLE` | Mua nhanh 1 lần |
| Shift phải | `SHIFT_RIGHT: SELL_SINGLE` | Bán nhanh 1 lần |
| Đổi tay phụ | `SWAP_OFFHAND: SELL_ALL` | Bán tất cả item hợp lệ |
| Túi đầy | `Buy_With_Full_Inventory: false` | Không mua được khi inventory đầy |
| Đóng GUI sau giao dịch | `Close_GUI_After_Trade: false` | Mua/bán xong menu vẫn mở |
| Log giao dịch | `Transaction_Logs.Output.File: true` | Giao dịch được ghi file, không spam console |

## 🛍️ Xu Shop Và Claim Shop

| Shop | Tiền tệ | Ví dụ config đã đọc | Khuyến nghị |
|---|---|---|---|
| Xu Shop | Xu `%playerpoints_points%` | `GEM_REMOVER` giá `14 Xu`, chạy `mi give CONSUMABLE GEM_REMOVER` | Chỉ mua khi cần đục/ngọc/nâng cấp thật sự |
| Claim Shop | Vault money | `Claim I`: `20K` mua `10` claim; `Claim II`: `50K` mua `30` claim | Mua sớm nếu xây base lớn ở world sinh tồn |
| Rank Shop | Xu | Rank `bee` giá `19 Xu` | Ưu tiên nếu muốn thêm homes, claim, sell item, `/pv`, AFK |

## 📚 Tài Liệu Chi Tiết

| File | Nội dung |
|---|---|
| [shop-locations.md](shop-locations.md) | Cách vào từng shop/menu |
| [player-shops.md](player-shops.md) | Player warp/shop người chơi và cách dùng an toàn |
| [shop-prices.md](shop-prices.md) | Giá, tiền tệ, click mua/bán, danh mục shop |

Xem thêm: [../Donate/spending-guide.md](../Donate/spending-guide.md), [../Gui/shop-guis.md](../Gui/shop-guis.md), [../Gameplay/economy-currencies.md](../Gameplay/economy-currencies.md)
