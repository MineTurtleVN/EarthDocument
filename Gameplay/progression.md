# 📈 Lộ Trình Tiến Trình

Plugin chính: `TurtleLevel`, `TurtleDungeon`, `MMOItems`, `ExcellentCrates`

📁 Config: /plugins/TurtleLevel/gui.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon1.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon3.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon5.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon7.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon9.yml
📁 Config: /plugins/ExcellentCrates/crates/dungeons.yml

| Giai đoạn | Mục tiêu | Nên làm | Mốc config |
|---|---|---|
| Newbie | Sống sót, biết menu/warp/shop | Farm `earth`, mở hướng dẫn, bán đồ qua `/shop` | `/rtp`, `/shop`, `/skill` |
| Early-game | Có set đồ cơ bản, bắt đầu Cấp Rùa | Cày từng nhánh skill tới mốc 5, mua claim/rank rẻ | TurtleLevel: mỗi 5 cấp kỹ năng = +1 cấp Rùa |
| PvE đầu | Vào dungeon thấp | D1 `Ngôi Đền Của Đá`, farm vật liệu đầu | Level menu D1: `1+` |
| Mid-game | Mở dungeon D2-D3, nâng gear | D2 yêu cầu `15+`, D3 yêu cầu `30+` | zMenu `DUNGEON_D2/D3.yml` |
| Late-game | Farm dungeon cao | D4 yêu cầu `50+`, D5 yêu cầu `70+` | Cần gear T4-T5 theo menu |
| Risk/reward | Chuyển sang bản PvP dungeon | Đi bản PvP nếu chấp nhận bị đánh | Menu tổng ghi PvP reward/EXP `x2.5` |
| End-game | Cạnh tranh top/PvP | KOTH Địa Bàn, dungeon PvP, crate/key hiếm | KOTH `12:00`, `20:00` |

## 🐢 Cấp Độ Rùa Trong Lộ Trình

TurtleLevel GUI nói rõ mỗi nhánh kỹ năng tính riêng. Vì vậy cách lên cấp hiệu quả là đưa nhiều kỹ năng qua các mốc 5/10/15 thay vì chỉ cày một kỹ năng quá cao rồi mong tổng level cộng dồn.

| Cách cày | Kết quả |
|---|---|
| Đào khoáng 7 | Tính 1 mốc 5, dư 2 |
| Câu cá 13 | Tính 2 mốc 5, dư 3 |
| Tổng cấp Rùa | `1 + 2 = 3` |

## 🏛️ Dungeon Unlock Tóm Tắt

| Dungeon | Level menu | Vai trò |
|---|---:|---|
| D1 Ngôi Đền Của Đá | `1+` | Làm quen stage/boss/capture |
| D2 Bản Di Chúc Đất & Lửa | `15+` | Bắt đầu mob/boss mạnh hơn |
| D3 Tế Đàn Rừng Sương Độc | `30+` | Cần né hiệu ứng/khống chế tốt hơn |
| D4 Vực Thẳm Rực Cháy | `50+` | Menu khuyên gear `T4+` |
| D5 Vườn Địa Đàng | `70+` | Menu khuyên gear `T4-T5` |

## 💰 Kinh Tế Đi Kèm Tiến Trình

| Giai đoạn | Tiền nên ưu tiên | Chi tiêu nên ưu tiên |
|---|---|---|
| Newbie | Vault money | Claim, repair, đồ ăn, vật phẩm farm |
| Early-game | Vault money + key nguyên liệu | Claim IV nếu cần base rộng, nguyên liệu nâng cấp |
| Mid-game | Dungeon materials + Xu nếu có | Key Dungeon, booster XP/Turtle Skill |
| Late-game | Key hiếm, gem, tinh hoa | Gear/gem/cường hóa thay vì mua trang trí |
| End-game | Rank cao, crate hiếm | `/fly`, `/fix all`, booster toàn bộ, Key Thiên Mệnh |

Xem thêm: [dungeons.md](../PvE/dungeons.md), [mmoitems.md](../Items/mmoitems.md)
