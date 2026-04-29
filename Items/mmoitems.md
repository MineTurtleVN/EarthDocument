# ⚔️ MMOItems: Type, Tier Và Trang Bị

Plugin chính: `MMOItems`

📁 Config: /plugins/MMOItems/item-types.yml  
📁 Config: /plugins/MMOItems/item-tiers.yml  
📁 Config: /plugins/MMOItems/item/sword.yml  
📁 Config: /plugins/MMOItems/item/swordnew.yml  
📁 Config: /plugins/MMOItems/item/bow.yml  
📁 Config: /plugins/MMOItems/item/mu.yml  
📁 Config: /plugins/MMOItems/item/ao.yml  
📁 Config: /plugins/MMOItems/item/quan.yml  
📁 Config: /plugins/MMOItems/item/giay.yml  
📁 Config: /plugins/MMOItems/item/tool.yml

`MMOItems` là nền tảng của trang bị custom. Mỗi item có `type`, `tier`, chỉ số, cờ khóa thao tác vanilla, và có thể có khả năng đặc biệt.

## 🧩 Type ID Quan Trọng

📁 Config: /plugins/MMOItems/item-types.yml

| Type ID | Tên hiển thị | Parent | Vai trò |
|---|---|---|---|
| `MU` | Mũ | `ARMOR` | Giáp đầu |
| `AO` | Áo | `ARMOR` | Giáp ngực |
| `QUAN` | Quần | `ARMOR` | Giáp chân |
| `GIAY` | Giày | `ARMOR` | Giày |
| `SWORDNEW` | Kiem | `SWORD` | Kiếm mới, vũ khí chính |
| `BOW_NEW` | Bow New | `BOW` | Cung mới |
| `RIU` | Rìu | `AXE` | Vũ khí rìu, có `slashing_attack_effect` |
| `CUP` | Cúp | `TOOL` | Công cụ đào |
| `CUOCSANHO` | Cuốc San Hô | `TOOL` | Công cụ đặc thù |
| `MATERIAL` | Material | `MISCELLANEOUS` | Vật liệu nâng cấp/crafting |
| `NGOCTHIENSU` | Ngọc Thiên Sứ | `CONSUMABLE` | Consumable đặc biệt |
| `GEM_STONE` | Gem Stone | Không parent custom | Ngọc khảm |
| `TALISMAN` | Talisman | `CATALYST` | Phụ kiện/chất xúc tác |
| `SHIELD` | Shield | `CATALYST` | Phụ kiện/đỡ đòn |

Các type chưa giám định dùng lore `Phẩm chất: #prefix##tier#`, nên khi thấy item chưa giám định, thông tin quan trọng nhất là type và tier dự kiến.

## ⭐ Tier Chính `1-11`

📁 Config: /plugins/MMOItems/item-tiers.yml

| Tier | Hiển thị | Màu/prefix | Giai đoạn |
|---|---|---|---|
| `1` | `★★☆☆☆` | `<#AAAAAA>` | Đồ 2 sao base |
| `2` | `★★☆☆☆` | `<#CCCCCC>` | Đồ 2 sao base tốt hơn |
| `3` | `★★★☆☆` | `<#80FF60>` | 3 sao R1 |
| `4` | `★★★☆☆` | `<#40E020>` | 3 sao R2 |
| `5` | `★★★☆☆` | `<#00C000>` | 3 sao R3 |
| `6` | `★★★★☆` | `<#60D0FF>` | 4 sao R1 |
| `7` | `★★★★☆` | `<#2090FF>` | 4 sao R2 |
| `8` | `★★★★☆` | `<#0050DD>` | 4 sao R3 |
| `9` | `★★★★★` | `<#FF80FF>` | 5 sao R1 |
| `10` | `★★★★★` | `<#CC40FF>` | 5 sao R2 |
| `11` | `★★★★★` | `<#9900FF>` | 5 sao R3 |

Ngoài tier gear chính còn có tier item phụ `i1-i6`, dùng cho vật phẩm như đục ngọc, gem hoặc item tiện ích.

## 🎣 Công Cụ Và Cần Câu Đặc Biệt

📁 Config: /plugins/MMOItems/item/tool.yml

| ID | Tên/nhóm | Chỉ số đáng chú ý |
|---|---|---|
| `CANCAURUA1` | Cần câu Rùa I | `LINH_KHI +10%`, `FISHING_LUCK +2%`, Lure 3, Luck 2 |
| `CANCAURUA2` | Cần câu Rùa II | `LINH_KHI +35%`, `FISHING_LUCK +8%` |
| `CANCAURUA3` | Cần câu Rùa III | `LINH_KHI +42%`, `FISHING_LUCK +10%` |
| `CANCAURUA4` | Cần câu Rùa IV | `LINH_KHI +50%`, `FISHING_LUCK +12%` |
| `CANCAURUA5` | Cần câu Rùa V | `LINH_KHI +70%`, `FISHING_LUCK +16%` |
| `CANCAUHOANGKIM` | Cần câu Hoàng Kim VI | `LINH_KHI +100%`, `FISHING_LUCK +22%`, premium |
| `CANCAULONGVUONG` | Cần câu Long Vương VII | `LINH_KHI +150%`, `FISHING_LUCK +30%`, premium |
| `CANCAOTHANNGU` | Cần câu Thần Ngư VIII | `LINH_KHI +200%`, `FISHING_LUCK +40%`, legendary |
| `CUPRUA` | Cúp Rùa Thần | `farming-speed-fortune 10`, `efficiency 10`, `lucky 5`, Fortune 10 |

## 🧱 Bộ Nông Nô Và Công Cụ Đầu Game

📁 Config: /plugins/MMOItems/item/tool.yml

| ID | Loại | Chỉ số cơ bản |
|---|---|---|
| `KIEMNONGNO` | Kiếm sắt | Attack damage `6.0`, attack speed `1.6`, Unbreaking 3 |
| `CUPNONGNO` | Cúp sắt | Efficiency 3, Unbreaking 2 |
| `RIUNONGNO` | Rìu sắt | Attack damage `9.0`, Efficiency 3, Unbreaking 2 |
| `XENGNONGNO` | Xẻng sắt | Efficiency 3, Unbreaking 2 |
| `CUOCNONGNO` | Cuốc sắt | Efficiency 3, Unbreaking 2 |
| `CUPMEMMAI` | Cúp Silk Touch I | Diamond Pickaxe, Efficiency 4, Silk Touch 1, Unbreaking 6 |
| `CUPMEMMAI2` | Cúp Silk Touch II | Netherite Pickaxe, Efficiency 6, Silk Touch 2, Unbreaking 8 |

## 🧠 Cách Đọc Một Item MMOItems

| Key thường gặp | Ý nghĩa cho người chơi |
|---|---|
| `material` | Vật phẩm nền hiển thị trong Minecraft |
| `custom-model-data` | Model/texture custom nếu resource pack hỗ trợ |
| `tier` | Phẩm chất, liên quan phân rã và sức mạnh |
| `enchants` | Enchant vanilla có sẵn |
| `attack-damage`, `attack-speed` | Chỉ số đánh cận chiến |
| `max-health`, `defense`, `dodge-rating` | Chỉ số sinh tồn/giáp |
| `pve-damage`, `critical-strike-*`, `lifesteal` | Chỉ số đánh quái/boss/PvP |
| `gem-color` | Loại slot ngọc có thể khảm |
| `disable-crafting/enchanting/repairing` | Không dùng được hệ vanilla tương ứng |

## ✅ Quy Tắc Chọn Đồ

| Nếu bạn đang ở | Ưu tiên |
|---|---|
| Newbie | Đồ type đúng vai trò, tier `1-3`, dễ thay |
| Early-game | Đồ `★★★`, chỉ số chính rõ ràng, đủ farm D2-D3 |
| Mid-game | Đồ `★★★★`, bắt đầu giữ món có slot ngọc tốt |
| Late-game | Đồ `★★★★★`, cường hóa và khảm gem theo build |
| End-game | So sánh từng chỉ số, không chỉ nhìn sao |

Xem thêm: [consumables-materials.md](consumables-materials.md), [dungeon-items.md](dungeon-items.md), [../Gameplay/crafting-upgrades.md](../Gameplay/crafting-upgrades.md)
