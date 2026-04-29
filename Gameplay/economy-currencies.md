# 💰 Tiền Tệ Và Kinh Tế

Plugin chính: `ExcellentShop`, `PlayerPoints`, `Vault`, `zMenu`, `MobsCoin`

📁 Config: /plugins/ExcellentShop/config.yml
📁 Config: /plugins/ExcellentShop/virtual_shop/settings.yml
📁 Config: /plugins/zMenu/inventories/HUONGDAN.yml
📁 Config: /plugins/zMenu/inventories/CSHOP.yml
📁 Config: /plugins/zMenu/inventories/DONATE/DONATE.yml

Earth có nhiều loại tiền/tài nguyên. Quan trọng nhất là đừng nhầm `Vault money` với `Xu`: `/shop`, `/repair`, `/claimshop` dùng tiền thường; `/rank`, Xu Shop và donate dùng Xu/PlayerPoints.

## 🪙 Bảng Tiền Tệ

| Tiền/tài nguyên | Cách kiếm đã được menu ghi | Dùng cho |
|---|---|---|
| Bạc/Vault money | Bán đồ ở `/shop`; menu hướng dẫn cũng nhắc `/ah` | Shop thường, repair, claim shop, giao dịch `/pay` |
| Xu/PlayerPoints | `/donate`, chuyển Xu về cụm Turtle Earth | `/rank`, Xu Shop, key, booster, gem chest |
| MobsCoin | Giết mob hiền hoặc ác ngoài tự nhiên | Tiền quái/hệ thống đổi thưởng nếu menu/plugin liên quan bật |
| XP | Giết mob hiền hoặc ác ngoài tự nhiên | Mua sách ở `/ce` theo hướng dẫn GUI |
| Công huân | Chiếm cứ điểm ngoài tự nhiên | Cứ điểm/Thánh Chiến, xem `/thanhchien cudiem` |
| Key | AFK, mốc nạp, dungeon, KOTH, Xu Shop | Mở crate ở `/warp crates` |
| Nguyên liệu đặc biệt | Mob tự nhiên tỉ lệ thấp, trade từ vanilla item, dungeon | Craft, nâng cấp, trade NPC |

## 🏪 ExcellentShop Trạng Thái

| Module | Trạng thái | Lệnh |
|---|---|---|
| VirtualShop | Bật | `/vshop`, `/shop` |
| ChestShop | Tắt | `chestshop`, `cs` không phải shop chính |
| Auction | Tắt trong ExcellentShop | `auction`, `auc`, `ah` module ExcellentShop tắt; nếu `/ah` hoạt động thì do plugin khác |
| Sell GUI | Bật | `/sellgui`, `/sellmenu`, `/sellg` |
| Sell All | Bật | `/sellall` |
| Sell Hand | Bật | `/sellhand`, `/sellhandall` |

## 💱 Luồng Kiếm Tiền Cơ Bản

| Giai đoạn | Làm gì | Vì sao |
|---|---|---|
| Newbie | `/rtp` tới `earth`, farm khoáng/nông sản/mob drop | Có item để bán/trade |
| Có inventory đầy | Mở `/shop` hoặc `/sellgui` | Bán item hợp lệ lấy bạc |
| Có base | Mua claim ở `/claimshop` | Bảo vệ khu xây dựng |
| Có gear | Đi dungeon D1-D3 | Lấy nguyên liệu MMOItems, key, reward scaling |
| Có Xu | Mua rank/booster/key theo nhu cầu | Tăng tiện ích và tốc độ farm |

## ⚠️ Lưu Ý Kinh Tế

| Lưu ý | Chi tiết |
|---|---|
| Túi đầy không mua được | `Buy_With_Full_Inventory: false` trong ExcellentShop |
| Giá có thể biến động | Lore product có placeholder biến động giá `%product_price_avg_diff_buy%` và `%product_price_avg_diff_sell%` |
| Giao dịch shop có log | `Transaction_Logs.Output.File: true` |
| Xu Shop trừ Xu bằng command | Ví dụ `points take %player% 14` trước khi cấp item |

Xem thêm: [shop-prices.md](../Shops/shop-prices.md), [spending-guide.md](../Donate/spending-guide.md)
