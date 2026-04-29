# 🎖️ Kit Và Phần Thưởng PvP

Plugin chính: `zMenu`, `ExcellentCrates`, `AxKoth`, `TurtleTop`, `PvPManager`

📁 Config: /plugins/zMenu/inventories/KIT.yml
📁 Config: /plugins/AxKoth/koths/Hero.yml → `reward-commands`
📁 Config: /plugins/ExcellentCrates/crates/koth.yml
📁 Config: /plugins/TurtleTop/points.yml → `diaban`, `thanhchien`
📁 Config: /plugins/zMenu/inventories/DUATOP.yml
📁 Config: /plugins/PvPManager/config.yml → `Player Kills`

PvPManager không thưởng tiền trực tiếp khi kill (`Money Reward: 0.0`). Phần thưởng PvP chính của server đến từ KOTH `Địa Bàn`, top Địa Bàn, top Thánh Chiến, kit trong menu và loot rơi khi giao tranh.

## 🎁 Nguồn Thưởng PvP

| Nguồn | Plugin | Cách nhận | Thưởng/ý nghĩa |
|---|---|---|---|
| Kit | `zMenu` | Mở menu kit | Nhận trang bị/hỗ trợ theo cấu hình `KIT.yml` |
| KOTH `Địa Bàn` | `AxKoth` | Chiếm vùng đủ `60 giây` | `50,000` tiền, `20` Xu, `3` Hòm Ngọc Bậc II, `3` sách phù phép, `+1` điểm top Địa Bàn |
| Top Địa Bàn | `TurtleTop` | Tích điểm từ mỗi lần thắng KOTH | Top 1-5 nhận Xu và danh hiệu `[ʙá ᴄʜủ]` theo menu |
| Top Thánh Chiến | `TurtleTop`/`ThanhChien` | Tích điểm Thánh Chiến | Xu, key, đá cường hóa, hòm ngọc, sách cường hóa, danh hiệu `[ᴄʜɪếɴ ᴛʜầɴ]` |
| Loot PvP | `PvPManager` | Hạ người chơi trong vùng PvP | Loot được bảo vệ theo `PvPManager` trong thời gian ngắn |

## 👑 Thưởng KOTH `Địa Bàn`

📁 Config: /plugins/AxKoth/koths/Hero.yml → `reward-commands`

KOTH là nguồn thưởng PvP trực tiếp rõ nhất. Khi người chơi chiếm thành công:

| Thưởng | Số lượng | Ghi chú |
|---|---:|---|
| Tiền | `50,000` | Lệnh `eco give %player% 50000` |
| Xu | `20` | Lệnh `points give %player% 20` |
| Hòm Ngọc Bậc II | `3` | Lệnh `av give %player% GemChest-2 3` |
| Sách Phù Phép Ngẫu Nhiên | `3` | Lệnh `av give %player% EnchantmentRandom-3 3` |
| Điểm top Địa Bàn | `1` | Lệnh `tt add %player% diaban 1` |

ExcellentCrates có preview `Địa Bàn` tại `/plugins/ExcellentCrates/crates/koth.yml`, nhưng phần thưởng thực tế lấy từ AxKoth. Nếu preview có item khác với `reward-commands`, ưu tiên `reward-commands` để xác định quà thật.

## 🏆 Thưởng Top Địa Bàn

📁 Config: /plugins/zMenu/inventories/DUATOP.yml → `DB R1` đến `DB R5`

| Hạng | Xu | Danh hiệu menu hiển thị | Thời hạn |
|---:|---:|---|---|
| Top 1 | `50` | `[ʙá ᴄʜủ]` | `7 ngày` |
| Top 2 | `40` | `[ʙá ᴄʜủ]` | `5 ngày` |
| Top 3 | `30` | `[ʙá ᴄʜủ]` | `4 ngày` |
| Top 4 | `20` | `[ʙá ᴄʜủ]` | `3 ngày` |
| Top 5 | `10` | `[ʙá ᴄʜủ]` | `3 ngày` |

`/plugins/TurtleTop/points.yml` hiện có cấu hình reset/trao thưởng `diaban`, nhưng `Reset.Enable: false`, nên top vẫn được tracking nhưng auto reset/auto trao thưởng không chắc chắn chạy nếu admin chưa bật hoặc không có hệ thống ngoài xử lý.

## ⚔️ Thưởng Top Thánh Chiến

📁 Config: /plugins/zMenu/inventories/DUATOP.yml → `TC R1` đến `TC R5`

| Hạng | Thưởng chính |
|---:|---|
| Top 1 | `50 Xu`, `2 Chìa Khóa Thiên Mệnh`, đá cường hóa tối thượng, Hòm Ngọc Bậc IV, sách cường hóa VI, tag `[ᴄʜɪếɴ ᴛʜầɴ]` 7 ngày |
| Top 2 | `40 Xu`, `1 Chìa Khóa Thiên Mệnh`, đá cường hóa cao cấp, Hòm Ngọc Bậc III, sách cường hóa V, tag 5 ngày |
| Top 3 | `30 Xu`, `3 Chìa Khóa Phó Bản`, đá cường hóa trung cấp, Hòm Ngọc Bậc II, sách cường hóa V, tag 4 ngày |
| Top 4 | `20 Xu`, `3 Chìa Khóa Phó Bản`, Hòm Ngọc Bậc I, sách cường hóa III, tag 3 ngày |
| Top 5 | `10 Xu`, `2 Chìa Khóa Phó Bản`, Hòm Ngọc Bậc I, sách cường hóa III, tag 3 ngày |

## 🧰 Kit PvP

📁 Config: /plugins/zMenu/inventories/KIT.yml

Kit được mở qua GUI `KIT.yml`. File này là nguồn chính để biết slot kit, điều kiện, quyền, cooldown và item phát ra. Khi dùng kit cho PvP, nên kiểm tra:

| Cần kiểm tra | Vì sao quan trọng |
|---|---|
| Cooldown kit | Tránh vào KOTH mà kit chưa hồi |
| Permission/rank | Một số kit có thể gắn với rank/donate |
| Giáp/vũ khí | Quyết định khả năng trụ trong vùng KOTH |
| Hồi máu/buff | Quan trọng khi cần giữ vùng `60 giây` |

Xem thêm: [maps-events.md](maps-events.md), [pvp-settings.md](pvp-settings.md), [../Items/rewards-crates.md](../Items/rewards-crates.md)
