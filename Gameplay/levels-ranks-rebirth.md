# 🧬 Level, Rank Và Mốc Sức Mạnh

Plugin chính: `TurtleLevel`, `zMenu`, `LuckPerms`, `TurtleAFKZone`

📁 Config: /plugins/TurtleLevel/gui.yml  
📁 Config: /plugins/zMenu/inventories/RANK.yml  
📁 Config: /plugins/zMenu/inventories/AFK.yml  
📁 Config: /plugins/zMenu/inventories/DUNGEONS.yml

Trang này gom các mốc sức mạnh mà người chơi thực sự gặp khi chơi: `Cấp Độ Rùa`, rank mua bằng Xu, rank tạm mua bằng điểm AFK, và điều kiện mở dungeon.

## 🐢 Cấp Độ Rùa

`TurtleLevel` không cộng toàn bộ skill rồi chia đều. GUI giải thích rõ: mỗi nhánh kỹ năng được tính riêng, cứ mỗi `5` level trong một kỹ năng sẽ cộng `+1 Cấp Độ Rùa`.

| Ví dụ | Cách tính | Cấp Độ Rùa nhận được |
|---|---:|---:|
| Đào khoáng cấp `7` | `floor(7 / 5)` | `+1` |
| Câu cá cấp `13` | `floor(13 / 5)` | `+2` |
| Tổng hai nhánh trên | `1 + 2` | `3` |

Ý nghĩa thực tế: muốn mở dungeon nhanh thì không nên chỉ cày một nhánh quá lệch. Cày nhiều nhánh lên các mốc `5`, `10`, `15`, `20` thường tăng `Cấp Độ Rùa` hiệu quả hơn.

## 🏰 Mốc Dungeon Theo Cấp Độ Sinh Tồn

📁 Config: /plugins/zMenu/inventories/DUNGEONS.yml  
📁 Config: /plugins/zMenu/inventories/DUNGEON_D1.yml đến `/plugins/zMenu/inventories/DUNGEON_D5.yml`

| Dungeon | Yêu cầu hiển thị trong GUI | Gợi ý giai đoạn |
|---|---|---|
| Ngôi Đền Của Đá | `Cấp 1+`, `★☆☆☆☆` | Vào sớm để học vòng stage |
| Bản Di Chúc Đất && Lửa | `Cấp 15+`, `★★☆☆☆` | Khi đã có đồ cơ bản và nguyên liệu D1 |
| Tế Đàn Rừng Sương Độc | `Cấp 30+`, `★★★☆☆` | Cần bắt đầu nâng trang bị đều hơn |
| Vực Thẳm Rực Cháy | `Cấp 50+`, `★★★★☆`, gear `T4+` | Mid/late-game, ưu tiên đồ đã cường hóa |
| Vườn Địa Đàng | `Cấp 70+`, `★★★★★`, gear `T4-T5` | End-game PvE |

Mỗi dungeon có bản thường và bản PvP. Bản PvP nguy hiểm hơn nhưng GUI dungeon mô tả phần thưởng cao hơn `x2,5`.

## 👑 Rank Xu Vĩnh Viễn/Tiến Trình Chính

📁 Config: /plugins/zMenu/inventories/RANK.yml

Rank trong `/rank` đi theo chuỗi nối tiếp. Muốn mua rank sau cần đang có rank trước đó.

| Rank | Giá Xu | Cần có trước | Vai trò |
|---|---:|---|---|
| `bee` | `19` | `default` | Mở đầu tuyến rank |
| `frog` | `39` | `bee` | Tăng tiện ích cơ bản |
| `rabbit` | `69` | `frog` | Bắt đầu có nhiều quyền sinh tồn hơn |
| `fox` | `99` | `rabbit` | Early-game ổn định |
| `wolf` | `199` | `fox` | Mid-game đầu |
| `boar` | `299` | `wolf` | Thêm quyền tiện ích |
| `panda` | `499` | `boar` | Mid-game tốt |
| `tiger` | `799` | `panda` | Chuẩn bị late-game |
| `slime` | `1,299` | `tiger` | Late-game |
| `spider` | `1,899` | `slime` | Late-game cao |
| `blaze` | `2,799` | `spider` | End-game đầu |
| `enderman` | `3,999` | `blaze` | End-game |
| `wither` | `5,999` | `enderman` | End-game cao |
| `warden` | `8,999` | `wither` | Gần tối đa |
| `turtlegod` | `12,999` | `warden` | Rank cao nhất trong menu |

Gợi ý: nếu chỉ nạp ít, đừng dồn hết Xu vào rank cao ngay. Rank thấp mở tiện ích, nhưng tiến độ PvE vẫn phụ thuộc vào đồ, dungeon, cường hóa và kinh tế.

## 💤 Rank Tạm Từ Điểm AFK

📁 Config: /plugins/zMenu/inventories/AFK.yml

Menu AFK cho phép đổi điểm AFK lấy EXP, key, vật phẩm và rank tạm `14 ngày`. Đây là tuyến miễn phí/treo máy để thử quyền rank trước khi mua bằng Xu.

| Mục | Giá điểm AFK | Lệnh/phần thưởng cấu hình |
|---|---:|---|
| `1,000 Kinh nghiệm` | `250` | `exp give %player% 1000` |
| `5,000 Kinh nghiệm` | `1,000` | `exp give %player% 5000` |
| Rank `bee` 14 ngày | `500` | `lp user %player% parent addtemp bee 14d`, `eco give 5000`, `+500 claim blocks` |
| Rank `frog` 14 ngày | `1,200` | `lp user %player% parent addtemp frog 14d`, `eco give 10000`, `+800 claim blocks` |
| Rank `rabbit` 14 ngày | `2,500` | `lp user %player% parent addtemp rabbit 14d`, `eco give 20000`, `+1200 claim blocks` |
| Chìa khóa AFK | `35` | `crates key give %player% afk 1` |
| Thùng Quặng Lv.1 | `80` | `av give %player% ThungQuang-Lv1 1` |
| Thùng Quặng Lv.2 | `200` | `av give %player% ThungQuang-Lv2 1` |
| Gậy Bán Đồ Cấp I | `50` | `tools give %player% sell_wand1` |
| Gậy Ghép Đồ | `80` | `tools give %player% crafting_wand` |

## 📌 Lộ Trình Gợi Ý

| Giai đoạn | Nên tập trung |
|---|---|
| 0-1 giờ đầu | Cày nhiều nhánh skill lên mốc `5`, vào D1, dùng `/menu`, `/warps`, `/shop` |
| Early-game | Lấy `Cấp Độ Rùa` để mở D2, gom vật liệu cường hóa, bán đồ bằng `/sellgui` |
| Mid-game | Mốc D3-D4, bắt đầu phân rã đồ thừa, nâng đồ chính qua `/loren` và `/upgrade` |
| Late-game | D4-D5, đồ T4/T5, ngọc khảm, booster, kinh tế đấu giá/player warp |
| End-game | Tối ưu gear, farm dungeon PvP, đua top, săn vật phẩm hiếm |

Xem thêm: [progression.md](progression.md), [crafting-upgrades.md](crafting-upgrades.md), [../PvE/dungeons.md](../PvE/dungeons.md), [../Donate/ranks-vip.md](../Donate/ranks-vip.md)
