# 👹 MythicMobs Và Mob Dungeon

Plugin chính: `MythicMobs`, `TurtleDungeon`

📁 Config: /plugins/MythicMobs/mobs/Dungeon/Dungeon1.yml
📁 Config: /plugins/MythicMobs/mobs/Dungeon/Dungeon2.yml
📁 Config: /plugins/MythicMobs/mobs/Dungeon/Dungeon3.yml
📁 Config: /plugins/MythicMobs/mobs/Dungeon/Dungeon4.yml
📁 Config: /plugins/MythicMobs/mobs/Dungeon/Dungeon5.yml
📁 Config: /plugins/TurtleDungeon/config.yml → `mob-display-names`
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon1.yml → dungeon10.yml

`TurtleDungeon` dùng MythicMobs để spawn quái và boss trong 5 dungeon theme. Mỗi theme có quái thường, quái tinh anh và 2 boss. Bản thường và PvP của cùng một theme dùng chung bộ mob, nhưng bản PvP có `max-mobs` cao hơn và phần thưởng tốt hơn.

## 🧩 Cách Mob Được Tính Trong Dungeon

| Cơ chế | Config | Ý nghĩa |
|---|---|---|
| Quái thường | `normal-mobs:` trong từng dungeon | Spawn chính để làm mục tiêu `KILL_MOBS` |
| Quái tinh anh | `elite-mobs:` trong từng dungeon | Mob nguy hiểm hơn, thường có debuff/knockback/tank |
| Boss | `bosses:` trong từng dungeon | Dùng cho stage `KILL_BOSS`, bossbar máu riêng |
| Kill tổng | `20 * players * stage` | Giết đủ điểm quái để qua stage |
| Kill theo loại | `10 * players * stage` | Giết đúng loại mob được yêu cầu |
| Scale theo người | `scale-per-player: 1.2` | Đi đông thì mục tiêu/sức ép tăng |

## 🪨 D1 - Ngôi Đền Của Đá

| Loại | Tên hiển thị | MythicMob ID | Vai trò/đặc điểm |
|---|---|---|---|
| Thường | Hồn Đá Vất Vưởng | `Dungeon1-HonDaVatVuong` | Quái mở đầu, dạng hồn/đá, áp lực nhẹ |
| Thường | Vệ Binh Hóa Thạch | `Dungeon1-VeBinhHoaThach` | Vệ binh tank hơn, dùng để học cách kite/dồn damage |
| Thường | Tàn Tích Của Đất | `Dungeon1-TanTichCuaDat` | Quái nền của D1, xuất hiện trong mục tiêu kill |
| Thường | Xác Sống Trầm Mặc | `Dungeon1-XacSongTramMac` | Zombie chậm nhưng bám sát |
| Tinh anh | Đội Trưởng U Linh | `Dungeon1-DoiTruongULinh` | Elite đầu tiên, nguy hiểm hơn mob thường |
| Tinh anh | Oán Linh Tế Đàn | `Dungeon1-OanLinhTeDan` | Gây áp lực bằng hiệu ứng bất lợi |
| Tinh anh | Bụi Gai Oán Hận | `Dungeon1-BuiGaiOanHan` | Có xu hướng khống chế/đẩy lùi |
| Tinh anh | Kẻ Gác Cổng Trầm Mặc | `Dungeon1-KeGacCongTramMac` | Mob giữ cổng, tank/áp sát |
| Boss | Hồn Rực Cháy | `Dungeon1-HonRucChay` | Blaze boss, lửa/AoE |
| Boss | Thần Oán Hận | `Dungeon1-ThanOanHan` | Warden boss, darkness/sonic, chống projectile |

## 🔥 D2 - Bản Di Chúc Của Đất Và Lửa

| Loại | Tên hiển thị | MythicMob ID | Vai trò/đặc điểm |
|---|---|---|---|
| Thường | Khối Nham Thạch | `Dungeon2-KhoiNhamThach` | Mob đất/lửa nền, cứng hơn D1 |
| Thường | Tinh Linh Khói | `Dungeon2-TinhLinhKhoi` | Gây khó chịu bằng di chuyển/hiệu ứng khói |
| Thường | Nấm Lửa Nguyên Tố | `Dungeon2-NamLuaNguyenTo` | Áp lực lửa/poison nhẹ |
| Thường | Tàn Lửa Vô Danh | `Dungeon2-TanLuaVoDanh` | Mob lửa dùng trong stage kill |
| Tinh anh | Hỏa Thần Tội Nhân | `Dungeon2-HoaThanToiNhan` | Elite lửa, damage cao hơn |
| Tinh anh | Hộ Pháp Dung Nham | `Dungeon2-HoPhapDungNham` | Tank/giữ khu vực dung nham |
| Tinh anh | Kẻ Hành Hương Rực Lửa | `Dungeon2-KeHanhHuongRucLua` | Áp lực cận chiến và lửa |
| Tinh anh | Sứ Giả Lòng Đất | `Dungeon2-SuGiaLongDat` | Elite đất, chống chịu tốt |
| Boss | Ấn Cháy Bỏng | `Dungeon2-AnChayBong` | Wither Skeleton, miễn fire/lava |
| Boss | Giao Hưởng Của Đất Và Lửa | `Dungeon2-GiaoHuongDatLua` | Iron Golem, tank, giảm sát thương projectile |

## ☠️ D3 - Tế Đàn Rừng Sương Độc

| Loại | Tên hiển thị | MythicMob ID | Vai trò/đặc điểm |
|---|---|---|---|
| Thường | Thợ Săn Huyết Tộc | `Dungeon3-ThoSanHuyetToc` | Mob nhanh, bắt đầu gây áp lực mid-game |
| Thường | Tuần Tra Viên Rừng Độc | `Dungeon3-TuanTraVienRungDoc` | Poison/kiểm soát khu vực |
| Thường | Tàn Tích Hiến Tế | `Dungeon3-TanTichHienTe` | Quái tế đàn, dùng trong mục tiêu kill |
| Thường | Kẻ Gác Đêm Mê Muội | `Dungeon3-KeGacDemMeMuoi` | Gây khó chịu bằng blind/darkness-like pressure |
| Tinh anh | Đại Tư Tế Sương Mù | `Dungeon3-DaiTuTeSuongMu` | Elite phép, debuff mạnh |
| Tinh anh | Sứ Giả Đầm Lầy | `Dungeon3-SuGiaDamLay` | Poison/tank |
| Tinh anh | Pháp Sư Mặt Nạ | `Dungeon3-PhapSuMatNa` | Ranged/caster |
| Tinh anh | Thủ Lĩnh Thợ Săn | `Dungeon3-ThuLinhThoSan` | Elite melee mạnh |
| Boss | Tư Tế Huyết Lễ | `Dungeon3-TuTeHuyetLe` | Witch boss, poison/heal/blind |
| Boss | Linh Rừng Thiêng | `Dungeon3-LinhRungThieng` | Warden boss, tank/darkness |

## 🌋 D4 - Tế Đàn Vực Thẳm Rực Cháy

| Loại | Tên hiển thị | MythicMob ID | Vai trò/đặc điểm |
|---|---|---|---|
| Thường | Đá Vụn Đỏ Thẫm | `Dungeon4-DaVunDoTham` | Mob nền late-game, cứng và đau hơn |
| Thường | Hỏa Hồn Lang Thang | `Dungeon4-HoaHonLangThang` | Lửa linh hồn, áp lực liên tục |
| Thường | Kẻ Canh Giữ Tro Tàn | `Dungeon4-KeCanhGiuTroTan` | Guard/tank cận chiến |
| Thường | Linh Kiện Cổ Đại | `Dungeon4-LinhKienCoDai` | Mob cổ đại, stage kill |
| Tinh anh | Sứ Giả Vực Sâu | `Dungeon4-SuGiaVucSau` | Elite nguy hiểm, damage cao |
| Tinh anh | Thẩm Phán Tro Tàn | `Dungeon4-ThamPhanTroTan` | Debuff/áp lực vùng |
| Tinh anh | Thiết Giáp Tế Đàn | `Dungeon4-ThietGiapTeDan` | Tank/armor cao |
| Tinh anh | Sứ Giả Lòng Đất Sâu | `Dungeon4-SuGiaLongDatSau` | Wither/đất sâu, khó chịu khi đông |
| Boss | Vua Không Ngai | `Dungeon4-VuaKhongNgai` | Wither Skeleton boss, miễn fire/lava |
| Boss | Tế Ma Vương | `Dungeon4-TeMaVuong` | Warden boss late-game, darkness/wither/heal/counter |

## 🌳 D5 - Vườn Địa Đàng

| Loại | Tên hiển thị | MythicMob ID | Vai trò/đặc điểm |
|---|---|---|---|
| Thường | Linh Hồn Của Gió | `Dungeon5-LinhHonCuaGio` | Phantom/di chuyển khó chịu |
| Thường | Vệ Binh Hoàng Hôn | `Dungeon5-VeBinhHoangHon` | Guard endgame |
| Thường | Kẻ Canh Giữ Vô Danh | `Dungeon5-KeCanhGiuVoDanh` | Mob tank, pressure cận chiến |
| Thường | Kẻ Hành Hương Cuối Cùng | `Dungeon5-KeHanhHuongCuoiCung` | Mob cuối tuyến, sát thương cao |
| Tinh anh | Kẻ Thi Hành Lời Thề | `Dungeon5-KeThiHanhLoiThe` | Elite damage cao |
| Tinh anh | Chấp Pháp Viên Phế Tích | `Dungeon5-ChapPhapVienPheTich` | Tank/knockback |
| Tinh anh | Tu Sĩ Mùa Thu | `Dungeon5-TuSiMuaThu` | Caster/debuff |
| Tinh anh | Hộ Pháp Bàn Thạch | `Dungeon5-HoPhapBanThach` | Tank rất cứng |
| Boss | Giao Hưởng Của Lá Và Gió | `Dungeon5-GiaoHuongLaGio` | Iron Golem boss, AoE/knockback |
| Boss | Linh Vườn Địa Đàng | `Dungeon5-LinhVuonDiaDang` | Warden boss endgame, mạnh nhất trong nhóm dungeon |

## 🧠 Ghi Chú Cho Người Chơi

| Vấn đề | Gợi ý |
|---|---|
| Stage yêu cầu kill type | Nhìn tên mob trên bossbar/title, tập trung đúng loại thay vì giết lan man |
| Mob tinh anh quá đông | Lùi về đội hình, dọn elite trước rồi mới đánh boss |
| Projectile bị giảm | Một số boss giảm sát thương từ projectile, nên cần sát thương cận chiến hoặc skill khác |
| PvP dungeon | Quái không phải nguy hiểm duy nhất; cần canh người chơi khác |

Xem thêm: [dungeons.md](dungeons.md), [bosses.md](bosses.md), [drops-rewards.md](drops-rewards.md)
