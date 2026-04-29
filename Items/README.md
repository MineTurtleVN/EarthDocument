# 🎒 Items Tổng Quan

Plugin chính: `MMOItems`, `MMOUpgrade`, `ExcellentCrates`, `ArcaneVouchers`, `GemFusion`, `WildTools`

📁 Config: /plugins/MMOItems/item-types.yml  
📁 Config: /plugins/MMOItems/item-tiers.yml  
📁 Config: /plugins/MMOItems/item/  
📁 Config: /plugins/MMOUpgrade/config.yml  
📁 Config: /plugins/ExcellentCrates/crates/  
📁 Config: /plugins/zMenu/inventories/CSHOP.yml  
📁 Config: /plugins/zMenu/inventories/AFK.yml

Items của Earth chia thành 5 nhóm lớn: trang bị MMOItems, vật liệu nâng cấp, ngọc khảm, item crate/voucher, và công cụ tiện ích. Người chơi nên đọc theo tuyến: hiểu tier → kiếm đồ → phân rã/nâng cấp → khảm ngọc → tối ưu bằng crate/shop/donate.

## 🧭 Đọc Nhanh Theo Nhu Cầu

| Bạn muốn biết | Đọc file | Nội dung chính |
|---|---|---|
| Trang bị, loại item, tier sao | [mmoitems.md](mmoitems.md) | Type ID, tier `1-11`, đồ chưa giám định |
| Vật liệu nâng cấp, ngọc, consumable | [consumables-materials.md](consumables-materials.md) | Đá cường hóa, tinh hoa, gem, đục ngọc, huy hiệu |
| Dungeon drop và vật phẩm phó bản | [dungeon-items.md](dungeon-items.md) | Tinh hoa dungeon, phôi rèn, key/crate dungeon |
| Crate, key, voucher, reward item | [rewards-crates.md](rewards-crates.md) | Key KOTH/dungeon/event, crate preview |

## ⚔️ Trang Bị Chính

📁 Config: /plugins/MMOItems/item-types.yml  
📁 Config: /plugins/MMOItems/item/sword.yml  
📁 Config: /plugins/MMOItems/item/swordnew.yml  
📁 Config: /plugins/MMOItems/item/mu.yml  
📁 Config: /plugins/MMOItems/item/ao.yml  
📁 Config: /plugins/MMOItems/item/quan.yml  
📁 Config: /plugins/MMOItems/item/giay.yml

| Nhóm | Type ID quan trọng | Vai trò |
|---|---|---|
| Vũ khí cận chiến | `SWORDNEW`, `RIU`, `AXE`, `DAGGER`, `SPEAR`, `HAMMER`, `GAUNTLET` | Đánh quái, PvP, boss |
| Vũ khí tầm xa | `BOW`, `BOW_NEW`, `CROSSBOW`, `MUSKET`, `STAFF` | Giữ khoảng cách, PvE đặc thù |
| Giáp | `MU`, `AO`, `QUAN`, `GIAY`, `ARMOR` | Máu, thủ, né, sống sót |
| Công cụ | `CUP`, `CUOCSANHO`, `TOOL` | Đào/farm/resource |
| Phụ kiện/chất xúc tác | `TALISMAN`, `CATALYST`, `OFF_CATALYST`, `ORNAMENT`, `SHIELD` | Tăng chỉ số bổ trợ |

## ⭐ Tier Và Giai Đoạn Sử Dụng

📁 Config: /plugins/MMOItems/item-tiers.yml

| Tier | Hiển thị | Giai đoạn | Cách xử lý khi thừa |
|---|---|---|---|
| `1-2` | `★★` | Newbie/early | Phân rã lấy `DACUONGHOASOCAP` |
| `3-5` | `★★★` | Early/mid | Giữ món chỉ số tốt, còn lại phân rã |
| `6-8` | `★★★★` | Mid/late | So sánh kỹ trước khi phân rã |
| `9-11` | `★★★★★` | End-game | Ưu tiên giữ, kiểm tra chỉ số/ngọc trước |

## 🔁 Vòng Đời Một Món Đồ

1. Kiếm đồ từ dungeon, crate, shop, trade hoặc hoạt động sự kiện.
2. Kiểm tra type, tier, chỉ số chính và slot ngọc.
3. Đồ không dùng thì đưa vào `/phanra` để lấy đá cường hóa.
4. Đồ chính đưa vào `/upgrade` để nạp EXP cường hóa.
5. Qua mốc lớn cần tinh hoa/phôi/đá theo `/plugins/MMOUpgrade/config.yml`.
6. Khi đồ đủ lâu dài, bắt đầu khảm gem và dùng đục ngọc nếu cần thay ngọc.

## 🛒 Nguồn Kiếm Item

| Nguồn | Cấu hình | Nên kiếm gì |
|---|---|---|
| Dungeon | `/plugins/TurtleDungeon/Dungeons/*.yml`, `/plugins/MMOItems/item/material.yml` | Tinh hoa, phôi, đá, key dungeon |
| Crate | `/plugins/ExcellentCrates/crates/` | Key, voucher, đồ hiếm, reward item |
| Xu Shop | `/plugins/zMenu/inventories/CSHOP.yml` | Đục ngọc, key, booster, gem chest, sell wand |
| AFK shop | `/plugins/zMenu/inventories/AFK.yml` | Key AFK, thùng quặng, sell wand, crafting wand |
| Player market | `/plugins/AxPlayerWarps/config.yml`, `/plugins/zAuctionHouseV3/config.yml` | Đồ người chơi bán, trade, warp shop |

## ✅ Lời Khuyên Giữ/Phân Rã

| Trường hợp | Nên làm |
|---|---|
| Đồ `★★` hoặc `★★★` không còn dùng | Phân rã lấy đá sơ/trung cấp |
| Đồ `★★★★` có chỉ số hợp build | Giữ lại để so với đồ đang mặc |
| Đồ `★★★★★` | Không phân rã vội; kiểm tra type, chỉ số, slot ngọc, nhu cầu PvE/PvP |
| Gem cấp cao | Chỉ khảm vào đồ dự định dùng lâu dài |
| Đục ngọc | Dùng đúng cấp gem; `GEM_REMOVER` chỉ gỡ ngẫu nhiên 1 viên |

Xem thêm: [../Gameplay/crafting-upgrades.md](../Gameplay/crafting-upgrades.md), [../PvE/drops-rewards.md](../PvE/drops-rewards.md), [../Shops/shop-prices.md](../Shops/shop-prices.md)
