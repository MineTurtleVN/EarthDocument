# 🐲 Boss Và Cơ Chế Dungeon

Plugin chính: `TurtleDungeon`, `MythicMobs`, `zMenu`

📁 Config: /plugins/TurtleDungeon/config.yml
📁 Config: /plugins/TurtleDungeon/bossbar.yml
📁 Config: /plugins/TurtleDungeon/messages.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon1.yml → dungeon10.yml
📁 Config: /plugins/MythicMobs/mobs/Dungeon/Dungeon1.yml → Dungeon5.yml
📁 Config: /plugins/zMenu/inventories/DUNGEON_D1.yml → DUNGEON_D5.yml

Boss dungeon không chỉ là mob mạnh. Boss là một pha riêng trong vòng lặp stage của `TurtleDungeon`, có bossbar máu, kiểm tra vị trí, kiểm tra despawn, thưởng boss và có thể làm cả nhóm mất nhịp nếu kéo boss ra khỏi vùng đánh.

## 🌀 Boss Xuất Hiện Khi Nào?

| Nguồn | Cơ chế |
|---|---|
| Menu dungeon | GUI ghi `Mỗi 5 stage sẽ xuất hiện BOSS mạnh` |
| TurtleDungeon messages | Có thông báo thưởng boss tại stage `5/10/15/20` |
| Dungeon config | Stage objective có loại `KILL_BOSS`, mỗi lần cần giết `1` boss |
| Boss list | Mỗi dungeon theme có 2 boss trong `bosses:` |

Luồng thường gặp: người chơi thức tỉnh dungeon bằng cách giết quái, làm mục tiêu stage, sau đó tới stage boss thì server chọn boss trong danh sách của dungeon đó. Khi boss chết, người chơi nhận thưởng theo cấu hình dungeon và chuyển tiếp sang stage/reward tiếp theo.

## 📊 Cơ Chế Kỹ Thuật Quan Trọng

| Cơ chế | Config | Ý nghĩa cho người chơi |
|---|---:|---|
| Boss bị kéo quá xa | `boss-teleport-radius: 30` | Đừng kéo boss quá xa khu đánh, boss có thể bị kéo về điểm chuẩn |
| Kiểm tra boss mất | `boss-check-interval: 5` giây | Nếu boss despawn/mất entity, plugin kiểm tra định kỳ để xử lý |
| Đồng bộ mob còn sống | `mob-reconcile-interval: 5` giây | Tránh lệch số mob còn sống trong stage |
| Dọn/đếm mob quanh dungeon | `mob-kill-radius: 200` block | Chỉ mob trong vùng xử lý mới được tính/dọn đúng |
| Rời quá xa vùng dungeon | `proximity-check.radius: 100` block | Rời xa có thể làm fail vì `fail-on-leave: true` |
| Chờ quay lại sau khi chết | `death-seconds: 60` | Chết trong dungeon phải chờ 60 giây trước khi vào lại |

## 📋 Danh Sách Boss Theo Dungeon

| Dungeon | Boss | MythicMob ID | Loại mob | Vai trò |
|---|---|---|---|---|
| D1 Ngôi Đền Của Đá | Hồn Rực Cháy | `Dungeon1-HonRucChay` | Blaze | Boss lửa mở đầu, gây áp lực bằng fire/AoE |
| D1 Ngôi Đền Của Đá | Thần Oán Hận | `Dungeon1-ThanOanHan` | Warden | Boss trâu hơn, darkness/sonic, giảm sát thương projectile |
| D2 Đất Và Lửa | Ấn Cháy Bỏng | `Dungeon2-AnChayBong` | Wither Skeleton | Boss melee/lửa, miễn fire/lava |
| D2 Đất Và Lửa | Giao Hưởng Của Đất Và Lửa | `Dungeon2-GiaoHuongDatLua` | Iron Golem | Boss tank, projectile nhận giảm, sát thương cao |
| D3 Rừng Sương Độc | Tư Tế Huyết Lễ | `Dungeon3-TuTeHuyetLe` | Witch | Boss độc, hồi máu, gây blind/poison |
| D3 Rừng Sương Độc | Linh Rừng Thiêng | `Dungeon3-LinhRungThieng` | Warden | Boss tank, darkness, damage cao |
| D4 Vực Thẳm Rực Cháy | Vua Không Ngai | `Dungeon4-VuaKhongNgai` | Wither Skeleton | Boss vực sâu, fire/lava immune, áp lực cận chiến |
| D4 Vực Thẳm Rực Cháy | Tế Ma Vương | `Dungeon4-TeMaVuong` | Warden | Boss late-game, darkness/wither/heal/counter |
| D5 Vườn Địa Đàng | Giao Hưởng Của Lá Và Gió | `Dungeon5-GiaoHuongLaGio` | Iron Golem | Boss AoE vật lý, knockback/áp lực khu vực |
| D5 Vườn Địa Đàng | Linh Vườn Địa Đàng | `Dungeon5-LinhVuonDiaDang` | Warden | Boss endgame mạnh nhất, HP/damage/armor cao |

## 🧱 Bossbar Và Trạng Thái Người Chơi Thấy

| Bossbar | Khi nào thấy | Ý nghĩa |
|---|---|---|
| `bossbar-awakening` | Trước khi dungeon bắt đầu | Giết đủ quái để khởi động hầm ngục |
| `bossbar-conquest` | Đang làm stage | Theo dõi mục tiêu stage hiện tại |
| `bossbar-boss` | Boss đang sống | Theo dõi máu boss |
| `bossbar-capture` | Stage giữ tim | Bảo vệ/capture Tim Hầm Ngục |
| `bossbar-rewarding` | Sau khi clear | Nhận thưởng tại Tim Hầm Ngục |
| `bossbar-cooldown` | Dungeon hồi phục | Chờ lượt sau |
| `bossbar-idle` | Chưa có người chơi | Dungeon đang chờ người tham gia |

## 🫀 Capture Heart Sau Boss/Stage

| Cấu hình | Giá trị |
|---|---:|
| Mục tiêu | `CAPTURE_HEART` |
| Thời gian giữ | `5 * {stage}` giây |
| Thời gian nhận thưởng | `30` giây |
| Nơi nhận | `Tim Hầm Ngục` theo message TurtleDungeon |

Người chơi cần đứng trong khu tim và sống sót đủ thời gian. Nếu cả nhóm rời vùng hoặc không còn người hợp lệ, dungeon có thể fail/reset stage.

## ⚠️ Mẹo Đánh Boss

| Tình huống | Cách xử lý |
|---|---|
| Boss Warden/Darkness | Giữ đội hình gần nhau, tránh kéo quá xa tâm dungeon |
| Boss có projectile reduction | Đừng chỉ đứng bắn cung; cần người tank/melee gây sát thương ổn định |
| Boss poison/blind | Chuẩn bị hồi máu, giữ khoảng cách và dọn quái phụ nếu có |
| Boss PvP dungeon | Cử người canh player khác, đừng dồn toàn bộ người vào boss nếu khu đang tranh chấp |
| Sau khi boss chết | Di chuyển ngay về Tim Hầm Ngục để không bỏ lỡ reward phase |

Xem thêm: [dungeons.md](dungeons.md), [mythicmobs.md](mythicmobs.md), [drops-rewards.md](drops-rewards.md)
