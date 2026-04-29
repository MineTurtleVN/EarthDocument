# 🗺️ PvP Maps Và Event

Plugin chính: `AxKoth`, `TurtleTop`, `ExcellentCrates`, `zMenu`, `TurtleDungeon`, `ThanhChien`

📁 Config: /plugins/AxKoth/config.yml
📁 Config: /plugins/AxKoth/schedulers.yml
📁 Config: /plugins/AxKoth/koths/Hero.yml
📁 Config: /plugins/TurtleTop/config.yml → `CustomPoints`, placeholder leaderboard
📁 Config: /plugins/TurtleTop/points.yml → `diaban`
📁 Config: /plugins/TurtleTop/gui/diaban.yml
📁 Config: /plugins/ExcellentCrates/crates/koth.yml
📁 Config: /plugins/zMenu/inventories/DUATOP.yml
📁 Config: /plugins/zMenu/inventories/EVENT.yml
📁 Config: /plugins/zMenu/inventories/HELP_THANHCHIEN.yml
📁 Config: /plugins/TurtleDungeon/config.yml → `bossbar-regions`

Trang này ghi chi tiết các khu PvP/event đang có trong config, đặc biệt là KOTH `Địa Bàn`. Những thông tin như giờ, tọa độ, điều kiện thắng, thưởng và top được lấy trực tiếp từ config server.

## ⚔️ Tổng Quan Nhanh

| Nội dung | Plugin | Người chơi làm gì? | Thưởng chính |
|---|---|---|---|
| KOTH `Địa Bàn` | `AxKoth` + `TurtleTop` | Vào vùng chiếm điểm ở Lobby, giữ vùng đủ thời gian để thắng | Tiền, Xu, Hòm Ngọc, sách phù phép, điểm top Địa Bàn |
| Top Địa Bàn | `TurtleTop` + `zMenu` | Tích điểm bằng mỗi lần chiếm KOTH thành công | Xu + danh hiệu `[ʙá ᴄʜủ]` theo hạng top |
| Dungeon PvP | `TurtleDungeon` | Đi các bản dungeon PvP để tranh farm/tài nguyên | Phụ thuộc dungeon và rơi đồ PvE |
| Thánh Chiến | `ThanhChien` + `zMenu` | Nội dung chiến đấu theo menu hướng dẫn | Điểm top Thánh Chiến, thưởng top tháng nếu bật trao thưởng |

## 👑 KOTH Là Gì?

KOTH là viết tắt của `King of the Hill`: một khu vực tranh chấp nơi người chơi phải đứng trong vùng chiếm để trở thành người kiểm soát. Trên server này KOTH được đặt tên hiển thị là `Địa Bàn`.

Khi KOTH mở, người chơi chạy vào vùng `Địa Bàn`. Nếu một người giữ vùng đủ `60 giây` mà không bị mất quyền chiếm, người đó thắng. Nếu không ai chiếm xong trước khi hết thời gian tối đa, KOTH kết thúc không có người thắng.

## 🏰 KOTH `Địa Bàn` / `Hero`

| Thuộc tính | Giá trị |
|---|---|
| ID config | `Hero` |
| Tên hiển thị | `Địa Bàn` |
| Chế độ | `CAPTURE` |
| Team mode | `false` - tính theo người chơi, không theo bang/team |
| Cần giữ vùng | `60 giây` |
| Thời gian tối đa mỗi trận | `930 giây` = `15 phút 30 giây` |
| Số người online tối thiểu để dùng starter | `2` |
| Bossbar | Bật, hiện trong bán kính `64 block` |
| Scoreboard | Bật, hiện toàn server khi liên quan KOTH |
| Glow người đang chiếm | Bật trong `/plugins/AxKoth/config.yml` |
| Cập nhật leaderboard AxKoth | Mỗi `180 giây` |
| Cập nhật bossbar/scoreboard | Mỗi `10 tick` = `0.5 giây` |

### 📍 KOTH Đặt Ở Đâu?

📁 Config: /plugins/AxKoth/koths/Hero.yml → `zone`

KOTH `Địa Bàn` nằm trong world `Lobby`, gần khu crate/event.

| Góc vùng | World | X | Y | Z |
|---|---:|---:|---:|---:|
| `location1` | `Lobby` | `-46` | `45` | `-13` |
| `location2` | `Lobby` | `-38` | `49` | `-5` |

Vùng chiếm là khối hộp giữa hai tọa độ trên. Tâm vùng xấp xỉ `Lobby, X -42, Y 47, Z -9`. ExcellentCrates cũng đặt crate preview KOTH tại `Lobby, -56, 46, -9`, tức là khu xem thưởng nằm gần khu KOTH.

### 🕛 KOTH Mở Lúc Nào?

📁 Config: /plugins/AxKoth/schedulers.yml → `Daily-1`

Timezone của lịch là `Asia/Ho_Chi_Minh`.

| Lịch | Giờ Việt Nam | Ngày | KOTH |
|---|---|---|---|
| `0 12 * * *` | `12:00` | Hằng ngày | `Hero` / `Địa Bàn` |
| `0 20 * * *` | `20:00` | Hằng ngày | `Hero` / `Địa Bàn` |

`random: false`, nghĩa là lịch này luôn mở đúng KOTH `Hero`, không random sang arena khác.

### 🧭 Khi KOTH Đang Chạy Người Chơi Thấy Gì?

📁 Config: /plugins/AxKoth/koths/Hero.yml → `bossbar`, `scoreboard`, `messages.yml`

| Thành phần | Nội dung |
|---|---|
| Bossbar | Hiện `Địa Bàn`, người đang chiếm và thời gian còn lại để chiếm |
| Scoreboard | Hiện thời gian kết thúc, tọa độ KOTH, người đang chiếm, thời gian còn lại |
| Broadcast bắt đầu | Thông báo KOTH đã bắt đầu và thời gian còn lại |
| Broadcast đang chiếm | Thông báo ai đang chiếm, lặp theo `capture-broadcast-every-seconds: 5` |
| Broadcast mất chiếm | Thông báo người chơi đã mất quyền kiểm soát |
| Broadcast thắng | Thông báo người chơi đã chiếm thành công |

Scoreboard có dòng tọa độ dạng `X%x%; Y%y%; Z%z%`, nên trong lúc event chạy người chơi có thể nhìn ngay vị trí KOTH trên sidebar.

## 🎁 Thưởng Khi Chiếm Thành Công

📁 Config: /plugins/AxKoth/koths/Hero.yml → `reward-commands`

Khi chiếm `Địa Bàn` thành công, server chạy các lệnh thưởng sau cho người thắng:

| Thưởng | Lệnh config | Ý nghĩa |
|---|---|---|
| `50,000` tiền | `eco give %player% 50000` | Cộng tiền Vault/Essentials cho người thắng |
| `20` Xu | `points give %player% 20` | Cộng PlayerPoints/Xu |
| `3` Hòm Ngọc Bậc II | `av give %player% GemChest-2 3` | Voucher/hòm ngọc bậc II |
| `3` Sách Phù Phép Ngẫu Nhiên | `av give %player% EnchantmentRandom-3 3` | Voucher sách phù phép ngẫu nhiên bậc tương ứng |
| `+1` điểm top Địa Bàn | `tt add %player% diaban 1` | Cộng vào TurtleTop loại `diaban` |

Config có một dòng thưởng key bị comment:

```yaml
# - crates key give %player% trangbingaunhien 1
```

Vì đang có dấu `#`, key `trangbingaunhien` không được phát trực tiếp bởi KOTH ở thời điểm đọc config.

## 🎲 Preview Thưởng KOTH Ở Crate

📁 Config: /plugins/ExcellentCrates/crates/koth.yml

ExcellentCrates có crate tên `Địa Bàn` dùng để xem preview phần thưởng KOTH. Crate này đặt block tại `Lobby, -56, 46, -9` và yêu cầu key `koth_preview_dummy` để mở theo cấu hình crate, nhưng phần `Preview.Enabled: true` cho phép dùng như giao diện xem quà.

| Reward ID | Tên hiển thị trong preview | Rarity | Mô tả |
|---|---|---|---|
| `tien_50k` | `+50,000⛀ Tiền` | `common` | Nhận `50,000` tiền mặt |
| `xu_20` | `+20⛃ Xu` | `common` | Nhận `20` Xu |
| `key_trangbi` | `Chìa Khóa Thiên Mệnh x1` | `rare` | Preview hiển thị chìa khóa trang bị, nhưng lệnh thưởng key đang bị comment trong AxKoth |
| `gemchest_2` | `Hòm Ngọc Bậc II x3` | `epic` | Ngọc ngẫu nhiên Lv `4-6` |
| `enchant_random` | `Sách Phù Phép Ngẫu Nhiên x3` | `epic` | Sách phù phép ngẫu nhiên |

Lưu ý: `koth.yml` trong ExcellentCrates chủ yếu là preview/hiển thị phần thưởng. Thưởng thực tế khi thắng lấy từ `reward-commands` của `/plugins/AxKoth/koths/Hero.yml`.

## 🏆 KOTH Có Tracking Top Không?

Có. Mỗi lần người chơi chiếm `Địa Bàn` thành công, AxKoth chạy:

```yaml
- tt add %player% diaban 1
```

Điều này cộng `1` điểm vào TurtleTop loại `diaban`. Menu `/duatop` hiển thị mục `TOP Địa Bàn (Tuần)` bằng placeholder:

```text
%turtletop_top_name_1_diaban%
%turtletop_top_point_1_diaban%
...
%turtletop_top_name_5_diaban%
%turtletop_top_point_5_diaban%
```

TurtleTop GUI riêng `diaban.yml` cũng ghi rõ: hiện top `10` người chiếm đất nhiều nhất, mỗi điểm là số lần chiếm thành công.

### ⚠️ Trạng Thái Reset/Trao Thưởng Top Hiện Tại

📁 Config: /plugins/TurtleTop/points.yml → `diaban.Reset`

| Key | Giá trị config | Ý nghĩa thực tế |
|---|---|---|
| `DisplayName` | `TOP Địa Bàn` | Tên loại top |
| `Reset.Enable` | `false` | Tự động reset top đang tắt |
| `Reset.EnableReport` | `false` | Tự động báo cáo/tổng kết đang tắt |
| `Reset.Time.Type` | `weekly` | Có cấu hình lịch tuần nhưng không hoạt động khi `Enable: false` |
| `Reset.Time.Value` | `1` | Thứ Hai nếu bật reset tuần |
| `Reset.Time.Time` | `12:00:00` | 12:00 trưa nếu bật reset |

Menu `/duatop` ghi thể lệ là tổng kết `12:00 Trưa Thứ Hai hàng tuần`, nhưng file `points.yml` hiện đang để `Reset.Enable: false`. Vì vậy tài liệu phải hiểu là: top vẫn được cộng và hiển thị, nhưng auto reset/auto trao thưởng chỉ chắc chắn chạy nếu admin bật lại `Reset.Enable` hoặc có hệ thống ngoài xử lý.

## 🥇 Thưởng Top Địa Bàn

📁 Config: /plugins/zMenu/inventories/DUATOP.yml → `DB R1` đến `DB R5`
📁 Config: /plugins/TurtleTop/points.yml → `diaban.Reset.Rewards`

Menu `/duatop` hiển thị phần thưởng top Địa Bàn như sau:

| Hạng | Xu | Danh hiệu | Thời hạn danh hiệu |
|---:|---:|---|---|
| Top 1 | `50 Xu` | `[ʙá ᴄʜủ]` | `7 ngày` |
| Top 2 | `40 Xu` | `[ʙá ᴄʜủ]` | `5 ngày` |
| Top 3 | `30 Xu` | `[ʙá ᴄʜủ]` | `4 ngày` |
| Top 4 | `20 Xu` | `[ʙá ᴄʜủ]` | `3 ngày` |
| Top 5 | `10 Xu` | `[ʙá ᴄʜủ]` | `3 ngày` |

Trong `points.yml`, lệnh thưởng tự động hiện chỉ có `points give <player> ...` và `src msg ...`. Phần cấp tag/danh hiệu không thấy lệnh cấp tag trong `diaban.Reset.Rewards`, nên danh hiệu có thể được xử lý bởi hệ thống khác, trao thủ công, hoặc menu đang mô tả phần thưởng dự kiến.

## 📊 Top Địa Bàn Hiện Tại

📁 Config/Data: /plugins/TurtleTop/data/players/

Top hiện tại được tính từ điểm `diaban` trong TurtleTop. Cách xem trong game:

| Cách xem | Lệnh/Giao diện |
|---|---|
| Mở menu đua top tổng | `/duatop` |
| Mở top Địa Bàn trực tiếp từ menu | Click `TOP Địa Bàn` trong `/duatop` |
| Lệnh nội bộ từ menu | `tt open %player% diaban` |
| Placeholder top 1 | `%turtletop_top_name_1_diaban%` + `%turtletop_top_point_1_diaban%` |

Khi tài liệu này được cập nhật, server đang `offline` sau một chu kỳ shutdown/restart, nên không thể xác nhận live placeholder bằng console ở thời điểm đó. Config xác nhận chắc chắn rằng top `diaban` đang được cộng qua KOTH; giá trị top live nên được refresh bằng `/duatop` khi server online.

## 🧠 Chiến Thuật Đi KOTH

| Giai đoạn | Nên làm |
|---|---|
| Trước giờ mở | Chuẩn bị giáp, hồi máu, đồ chạy, kiểm tra ping và inventory trống đủ để nhận voucher |
| Khi KOTH bắt đầu | Đến vùng `Lobby -42 47 -9`, quan sát bossbar/scoreboard |
| Khi có người đang chiếm | Đẩy người đó ra khỏi vùng hoặc hạ gục trước khi họ đủ `60 giây` |
| Khi mình đang chiếm | Không rời vùng, giữ máu, tránh bị knockback ra ngoài khối chiếm |
| Sau khi thắng | Kiểm tra tiền, Xu, voucher `GemChest-2`, `EnchantmentRandom-3`, và điểm top trong `/duatop` |

## 🧩 Dungeon PvP

📁 Config: /plugins/TurtleDungeon/config.yml → `bossbar-regions`

Các region dungeon có bản PvP riêng: `dungeon1pvp`, `dungeon2pvp`, `dungeon3pvp`, `dungeon4pvp`, `dungeon5pvp`.

| Khu | Mục đích | Ghi chú |
|---|---|---|
| `dungeon1pvp` | Farm rủi ro cao ở dungeon 1 | Có thể bị tranh tài nguyên |
| `dungeon2pvp` | Farm rủi ro cao ở dungeon 2 | Cần gear tốt hơn dungeon thường |
| `dungeon3pvp` | Farm rủi ro cao ở dungeon 3 | Nên đi theo nhóm |
| `dungeon4pvp` | Farm rủi ro cao ở dungeon 4 | Chuẩn bị hồi máu/buff |
| `dungeon5pvp` | Farm rủi ro cao ở dungeon 5 | Dành cho người đã có build ổn |

## 🛡️ Thánh Chiến

📁 Config: /plugins/zMenu/inventories/HELP_THANHCHIEN.yml
📁 Config: /plugins/zMenu/inventories/DUATOP.yml → `TOP Thánh Chiến`

`Thánh Chiến` là hệ PvP/event riêng được hướng dẫn bằng menu `HELP_THANHCHIEN.yml` và có top trong `/duatop`. Menu đua top ghi `TOP Thánh Chiến (Tháng)` xếp hạng theo điểm thánh chiến, dùng placeholder `thanhchien`.

| Hạng Top Thánh Chiến | Thưởng menu hiển thị |
|---:|---|
| Top 1 | `50 Xu`, `2 Chìa Khóa Thiên Mệnh`, đá cường hóa tối thượng, Hòm Ngọc Bậc IV, sách cường hóa VI, tag `[ᴄʜɪếɴ ᴛʜầɴ]` 7 ngày |
| Top 2 | `40 Xu`, `1 Chìa Khóa Thiên Mệnh`, đá cường hóa cao cấp, Hòm Ngọc Bậc III, sách cường hóa V, tag 5 ngày |
| Top 3 | `30 Xu`, `3 Chìa Khóa Phó Bản`, đá cường hóa trung cấp, Hòm Ngọc Bậc II, sách cường hóa V, tag 4 ngày |
| Top 4 | `20 Xu`, `3 Chìa Khóa Phó Bản`, Hòm Ngọc Bậc I, sách cường hóa III, tag 3 ngày |
| Top 5 | `10 Xu`, `2 Chìa Khóa Phó Bản`, Hòm Ngọc Bậc I, sách cường hóa III, tag 3 ngày |

Xem thêm: [kits-rewards.md](kits-rewards.md), [pvp-settings.md](pvp-settings.md), [../Gui/system-guis.md](../Gui/system-guis.md), [../Items/rewards-crates.md](../Items/rewards-crates.md)
