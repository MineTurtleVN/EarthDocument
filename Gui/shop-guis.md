# 🛒 GUI Shop Và Crate

Plugin chính: `ExcellentShop`, `ExcellentCrates`, `zMenu`

📁 Config: /plugins/ExcellentShop/virtual_shop/main.menu.yml
📁 Config: /plugins/ExcellentShop/virtual_shop/sell.menu.yml
📁 Config: /plugins/ExcellentShop/virtual_shop/settings.yml
📁 Config: /plugins/zMenu/inventories/CSHOP.yml
📁 Config: /plugins/zMenu/inventories/CLAIM.yml
📁 Config: /plugins/zMenu/inventories/RANK.yml
📁 Config: /plugins/ExcellentCrates/crates/dungeons.yml

## 🏪 ExcellentShop Main Menu

| Thành phần | Slot | Chức năng |
|---|---:|---|
| Thông tin tiền | `37` | Hiển thị `%balance%` |
| Sell GUI | `43` | Click chạy `player: sellgui` |
| Danh mục shop | Theo VirtualShop | Các thư mục `building_blocks`, `farming`, `minerals`, `mob_drops`, ... |

## 🖱️ Click Shop

| Click | Hành động |
|---|---|
| Chuột trái | Mua/chọn mua |
| Chuột phải | Bán/chọn bán |
| Shift | Mua/bán nhanh |
| Swap offhand | Bán tất cả |

## 🛍️ zMenu Shop GUIs

| GUI | Lệnh/cách mở | Tiền tệ | Mục đích |
|---|---|---|---|
| `CSHOP.yml` | Xu Shop | Xu `%playerpoints_points%` | Key, booster, gem chest, consumable, gậy bán đồ |
| `CLAIM.yml` | `/claimshop` | Vault money | Mua block claim |
| `RANK.yml` | `/rank` | Xu | Mua rank theo chuỗi nâng cấp |
| `DONATE/DONATE.yml` | `/donate` | VNĐ -> Xu | Hướng dẫn nạp, mốc nạp, chuỗi nạp |

## 🎁 Crate Liên Quan Shop

| Crate/key | Nguồn | Ghi chú |
|---|---|---|
| `dungeon` | Xu Shop, mốc nạp, dungeon rewards | Mở crate Phó Bản |
| `spawner` | Xu Shop, mốc nạp | Roll spawner/farm |
| `trangbingaunhien` | Xu Shop, mốc nạp | Key Thiên Mệnh, có bảo hiểm theo lore Xu Shop |
| `nguyenlieu` | Xu Shop, mốc nạp | Nguyên liệu nâng cấp |

Xem thêm: [../Shops/shop-prices.md](../Shops/shop-prices.md), [../Donate/boosters-keys.md](../Donate/boosters-keys.md), [../Items/rewards-crates.md](../Items/rewards-crates.md)
