# ⚔️ PvE Tổng Quan

Plugin chính: `TurtleDungeon`, `MythicMobs`, `MMOItems`, `ExcellentCrates`, `zMenu`

📁 Config: /plugins/TurtleDungeon/config.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/
📁 Config: /plugins/MythicMobs/mobs/Dungeon/
📁 Config: /plugins/MMOItems/item/
📁 Config: /plugins/zMenu/inventories/DUNGEONS.yml

PvE của Earth tập trung vào dungeon nhiều stage, mob/boss MythicMobs, nguyên liệu nâng cấp MMOItems, crate/key và các vật phẩm tiến hóa. Người chơi farm từ D1 đến D5 theo cấp độ, sau đó chọn bản PvP nếu muốn đổi rủi ro lấy loot/EXP x2.5.

## 🧭 Lộ Trình PvE Nhanh

| Giai đoạn | Mục tiêu | Nơi farm chính | Thứ nên ưu tiên |
|---|---|---|---|
| Newbie | Làm quen dungeon, lấy vật liệu đầu | D1 Ngôi Đền Của Đá | Đá Cuội Tinh Chế, Đá Cường Hóa Sơ Cấp, GemChest I |
| Early | Mở thêm currency và nâng cấp | D2 Đất Và Lửa | Đồng Tinh Chế, SoulCoins, Enchant II, key nguyên liệu |
| Mid | Bắt đầu build gear nghiêm túc | D3 Rừng Sương Độc | Sắt Tinh Chế, phôi rèn, ấn ký, GemChest II |
| Late | Chuẩn bị gear T4+ | D4 Vực Thẳm Rực Cháy | Kim Cương Tinh Chế, Đá Cường Hóa Tối Thượng, Đá Tiến Hóa I |
| Endgame | Farm đồ hiếm nhất | D5 Vườn Địa Đàng | Netherite Tinh Chế, GemChest IV-V, Enchant V-VI, Đá Tiến Hóa II-III |
| Competitive | Farm nhanh nhưng nguy hiểm | Dungeon PvP | Loot/EXP x2.5, chấp nhận bị người chơi khác tấn công |

## 📚 Tài Liệu PvE

| File | Nội dung |
|---|---|
| [dungeons.md](dungeons.md) | Dungeon thường/PvP, level yêu cầu, stage, tọa độ, mob, boss, reward chi tiết |
| [mythicmobs.md](mythicmobs.md) | Mob/boss MythicMobs theo từng dungeon, HP/damage/skill chính |
| [bosses.md](bosses.md) | Boss, cơ chế stage, bossbar, capture heart, fail/reset |
| [drops-rewards.md](drops-rewards.md) | Drop, reward, key, crate, currency, vật phẩm nâng cấp |

## 🔑 Điều Cần Nhớ

| Chủ đề | Tóm tắt |
|---|---|
| Dungeon không phải map tĩnh | Là chuỗi stage có mục tiêu thay đổi: giết quái, giết loại quái, đánh boss, giữ tim |
| Boss xuất hiện định kỳ | Menu nói mỗi `5 stage` có boss; config boss list dùng cho `KILL_BOSS` stage |
| Reward tăng theo stage/người chơi | Nhiều chance dùng `{stage}` và `{players}` nên party/stage cao có lợi hơn |
| PvP dungeon nguy hiểm | Có thể bị player khác đánh, nhưng GUI ghi loot và EXP x2.5 |
| Không AFK trong dungeon | Không hoạt động 5 phút sẽ bị xử lý và có cooldown vào lại |

Xem thêm: [../Gameplay/progression.md](../Gameplay/progression.md), [../Items/dungeon-items.md](../Items/dungeon-items.md), [../PvP/pvp-settings.md](../PvP/pvp-settings.md)
