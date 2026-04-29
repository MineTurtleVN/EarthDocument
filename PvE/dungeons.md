# 🏛️ Dungeon / Hầm Ngục

Plugin chính: `TurtleDungeon`, `zMenu`, `MythicMobs`, `MMOItems`, `ExcellentCrates`

📁 Config: /plugins/TurtleDungeon/config.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon1.yml → dungeon thường D1
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon2.yml → dungeon PvP D1
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon3.yml → dungeon thường D2
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon4.yml → dungeon PvP D2
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon5.yml → dungeon thường D3
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon6.yml → dungeon PvP D3
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon7.yml → dungeon thường D4
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon8.yml → dungeon PvP D4
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon9.yml → dungeon thường D5
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon10.yml → dungeon PvP D5
📁 Config: /plugins/zMenu/inventories/DUNGEONS.yml
📁 Config: /plugins/zMenu/inventories/DUNGEON_D1.yml đến DUNGEON_D5.yml

Dungeon của Earth là hệ thống `chinh phạt hầm ngục` theo stage. Người chơi vào map dungeon, tiêu diệt quái để thức tỉnh hầm ngục, vượt các mục tiêu theo stage, đánh boss định kỳ và nhận thưởng tại khu `Tim Hầm Ngục`. Có 5 chủ đề dungeon chính, mỗi chủ đề có bản thường an toàn và bản PvP nguy hiểm hơn nhưng thưởng/EXP cao hơn.

## 🧭 Cách Vào Dungeon

| Cách vào | Nguồn config | Ghi chú |
|---|---|---|
| Menu dungeon | `/plugins/zMenu/inventories/DUNGEONS.yml` | Menu tên `⚔ Chinh Phục Hầm Ngục`, size `54` |
| Nút chi tiết | `DUNGEON_D1.yml` đến `DUNGEON_D5.yml` | Xem boss, drop, kỹ năng, nút vào thường/PvP |
| Warp thường | `runasop %player_name% warp dungeon1..dungeon5` | Chế độ an toàn, farm bình thường |
| Warp PvP | `runasop %player_name% warp dungeon1pvp..dungeon5pvp` | Player khác có thể đánh bạn, loot và EXP x2.5 theo GUI |

## ⚙️ Luật Chung Của TurtleDungeon

| Cơ chế | Giá trị | Ý nghĩa cho người chơi |
|---|---:|---|
| Kill chuẩn bị theo người | `20` | Server dùng làm chuẩn số kill khi chuẩn bị/chinh phạt; từng dungeon có thêm công thức riêng |
| Chờ vào lại sau khi chết | `60 giây` | Chết trong dungeon phải đợi trước khi quay lại |
| Không hoạt động bị xử lý | `300 giây` | Không đóng góp/hành động 5 phút sẽ bị đưa về spawn |
| Cooldown sau khi bị kick AFK | `300 giây` | Bị kick vì không hoạt động sẽ phải chờ 5 phút |
| Giới hạn rời vùng | `100 block` | Nếu rời quá xa dungeon có thể fail vì `fail-on-leave: true` |
| Boss đi quá xa | `30 block` | Boss bị kéo về điểm chuẩn nếu bị kéo khỏi khu đánh |
| Kiểm tra boss mất | `5 giây` | Boss mất/despawn sẽ được kiểm tra và gọi lại |
| Đồng bộ mob còn sống | `5 giây` | Server reconcile số mob còn trong dungeon |
| Bán kính xử lý mob | `200 block` | Dùng để đếm/dọn mob quanh tâm dungeon |
| Thời gian nhận thưởng | `30 giây` | Sau stage/reward phase, người chơi có 30 giây nhận thưởng |

## 🌀 Vòng Lặp Một Lượt Dungeon

| Pha | Bossbar/Title | Việc cần làm |
|---|---|---|
| `Thức Tỉnh` | `Tiêu diệt {max} quái vật để khởi động hầm ngục` | Mỗi người cần giết đủ quái để được tính tham gia chinh phạt |
| `Chinh Phạt` | `Stage {stage}` + mục tiêu | Làm mục tiêu stage: giết tổng quái, giết loại quái, đánh boss hoặc bảo vệ tim |
| `Boss` | Bossbar máu boss | Tập trung damage boss, tránh kéo boss ra khỏi vùng |
| `Capture Heart` | `Bảo vệ trái tim của hầm ngục` | Ở trong khu tim đủ thời gian `5 * stage` giây |
| `Rewarding` | `Nhận thưởng tại Trái Tim Hầm Ngục` | Nhặt/nhận thưởng trong `30 giây` |
| `Cooldown/Idle` | Hồi phục/chờ người chơi | Dungeon chờ lượt tiếp theo |

Mỗi stage dùng các công thức chính:

| Mục tiêu | Công thức |
|---|---|
| `KILL_MOBS` | `20 * {number_of_player} * {stage}` điểm/quái |
| `KILL_TYPE` | `10 * {number_of_player} * {stage}` con đúng loại |
| `KILL_BOSS` | `1` boss |
| `CAPTURE_HEART` | `5 * {stage}` giây |

## 📍 Bảng Dungeon Tổng Hợp

| Chủ đề | Bản | File | Region | Warp | Level menu | Max mobs | Tâm dungeon | Ghi chú |
|---|---|---|---|---|---:|---:|---|---|
| Ngôi Đền Của Đá | Thường | `dungeon1.yml` | `dungeon1` | `dungeon1` | `1+` | `40` | `Dungeon1, 0,33,79` | Dễ nhất, mở hành trình dungeon |
| Ngôi Đền Của Đá | PvP | `dungeon2.yml` | `dungeon1pvp` | `dungeon1pvp` | `10+` trong menu tổng, chi tiết D1 ghi `1+` | `56` | `Dungeon1, 500,33,580` | Thưởng PvP x2.5, rủi ro bị đánh |
| Bản Di Chúc Của Đất Và Lửa | Thường | `dungeon3.yml` | `dungeon2` | `dungeon2` | `15+` | `48` | `Dungeon2, 500,59,443` | Bắt đầu có SoulCoins và key nguyên liệu |
| Bản Di Chúc Của Đất Và Lửa | PvP | `dungeon4.yml` | `dungeon2pvp` | `dungeon2pvp` | `25+` trong menu tổng, chi tiết D2 ghi `15+` | `64` | `Dungeon2, 734,59,450` | MobCoins/SoulCoins tăng mạnh |
| Tế Đàn Rừng Sương Độc | Thường | `dungeon5.yml` | `dungeon3` | `dungeon3` | `30+` | `56` | `Dungeon3, 0,65,-1` | Bắt đầu rơi phôi, ấn ký, GemChest II |
| Tế Đàn Rừng Sương Độc | PvP | `dungeon6.yml` | `dungeon3pvp` | `dungeon3pvp` | `40+` trong menu tổng, chi tiết D3 ghi `30+` | `74` | `Dungeon3, 499,68,621` | Bản PvP có nguyên liệu 5-10 và reward cao hơn |
| Tế Đàn Vực Thẳm Rực Cháy | Thường | `dungeon7.yml` | `dungeon4` | `dungeon4` | `50+` | `66` | `Dungeon4, 102,77,116` | Cần trang bị T4+, có đá tiến hóa I |
| Tế Đàn Vực Thẳm Rực Cháy | PvP | `dungeon8.yml` | `dungeon4pvp` | `dungeon4pvp` | `60+` trong menu tổng, chi tiết D4 ghi `50+` | `86` | `Dungeon4, 535,19,499` | PvP endgame trung-cao, key dungeon/nguyên liệu tốt |
| Vườn Địa Đàng | Thường | `dungeon9.yml` | `dungeon5` | `dungeon5` | `70+` | `78` | `Dungeon5, -13,51,-313` | Endgame PvE, GemChest IV-V, Enchant V-VI |
| Vườn Địa Đàng | PvP | `dungeon10.yml` | `dungeon5pvp` | `dungeon5pvp` | `80+` trong menu tổng, chi tiết D5 ghi `70+` | `86` | `Dungeon5, 488,51,193` | Rủi ro cao nhất, thưởng PvP x2.5, có key Thiên Mệnh |

Ghi chú admin: menu tổng `DUNGEONS.yml` và menu chi tiết `DUNGEON_D*.yml` không hoàn toàn đồng nhất về level yêu cầu PvP ở một số dungeon. Khi cần xác định điều kiện click thực tế, ưu tiên menu người chơi đang mở và requirement nằm trong chính item click.

## 🪨 D1 - Ngôi Đền Của Đá

📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon1.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon2.yml
📁 Config: /plugins/zMenu/inventories/DUNGEON_D1.yml

| Nội dung | Thường | PvP |
|---|---|---|
| Warp | `dungeon1` | `dungeon1pvp` |
| Level menu | `1+` | `10+` ở menu tổng, `1+` trong chi tiết D1 |
| Max mobs | `40` | `56` |
| Spawn cooldown | `3 giây` | `10 giây` |
| Awakening kills | `10-10` | `10-10` |
| Chủ đề | Đá cổ đại, quái sơ cấp | Bản nguy hiểm hơn, loot/EXP x2.5 |

| Nhóm | Mob/Boss | Vai trò |
|---|---|---|
| Quái thường | `Hồn Đá Vất Vưởng`, `Vệ Binh Hóa Thạch`, `Tàn Tích Của Đất`, `Xác Sống Trầm Mặc` | Quái mở đầu, làm quen với lao đến, chậm, độc/lửa nhẹ |
| Tinh anh | `Đội Trưởng U Linh`, `Oán Linh Tế Đàn`, `Bụi Gai Oán Hận`, `Kẻ Gác Cổng Trầm Mặc` | Có blind/poison/knockback, rơi vật liệu nâng cấp tỉ lệ thấp |
| Boss | `Hồn Rực Cháy` | Blaze boss, chống lửa/lava, AoE lửa, hồi máu boss |
| Boss | `Thần Oán Hận` | Warden boss, projectile nhận 50%, darkness, sonic/knockback |

| Reward thường | Giá trị/tỉ lệ config |
|---|---|
| `HUYETDICH`, `MANHHONLACLOI`, `TINHTHELUUHUYNH`, `NANHVUOTTAMDOC` | `1-2`, chance `20 + players*3` |
| `DACUOCTINHCHE` | `1` đến `3 + stage`, chance `40 + players*5` |
| `DACUONGHOASOCAP` | `1`, chance `5 + stage*2` |
| `MANHTHOSAN` | `1`, chance `5 + players` |
| MobCoins | `mc give 10`, chance `20 + players*2` |
| `GemChest-1`, `EnchantmentRandom-1`, `RandomMoney1`, `ThungQuang-Lv1` | Rơi theo chance tăng dần theo stage |
| `TINHHOATHACH` | `1-4`, chance `45 + players*5` |

## 🔥 D2 - Bản Di Chúc Của Đất Và Lửa

📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon3.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon4.yml
📁 Config: /plugins/zMenu/inventories/DUNGEON_D2.yml

| Nội dung | Thường | PvP |
|---|---|---|
| Warp | `dungeon2` | `dungeon2pvp` |
| Level menu | `15+` | `25+` ở menu tổng, `15+` trong chi tiết D2 |
| Max mobs | `48` | `64` |
| Tâm dungeon | `Dungeon2, 500,59,443` | `Dungeon2, 734,59,450` |
| Chủ đề | Nham thạch, đất và lửa | Bản PvP với nguyên liệu/MobCoins/SoulCoins cao hơn |

| Nhóm | Mob/Boss | Vai trò |
|---|---|---|
| Quái thường | `Khối Nham Thạch`, `Tinh Linh Khói`, `Nấm Lửa Nguyên Tố`, `Tàn Lửa Vô Danh` | Lửa, bắn xa, lao đến, poison nhẹ |
| Tinh anh | `Hỏa Thần Tội Nhân`, `Hộ Pháp Dung Nham`, `Kẻ Hành Hương Rực Lửa`, `Sứ Giả Lòng Đất` | Damage/armor tăng rõ, blind/lava/fire pressure |
| Boss | `Ấn Cháy Bỏng` | Wither Skeleton, HP `5000`, damage `38`, armor `15`, miễn fire/lava |
| Boss | `Giao Hưởng Của Đất Và Lửa` | Iron Golem, HP `7000`, damage `48`, armor `35`, projectile nhận 50% |

| Reward chính | Thường | PvP |
|---|---|---|
| Nguyên liệu quái 4 loại | `1-3`, chance `25 + players*3` | `3-8`, chance `55 + players*5` |
| `DONGTINHCHE` | `2` đến `3 + stage` | `5` đến `8 + stage*2` |
| `DACUONGHOATRUNGCAP` | `1`, chance `5 + stage*2` | `1-2`, chance `12 + stage*5` |
| MobCoins | `20` | `50` |
| SoulCoins | `5` | `12` |
| Crate/key | `GemChest-1`, `Enchant II`, `RandomMoney2`, `ThungQuang-Lv1`, key `nguyenlieu` | Cùng nhóm nhưng tỉ lệ cao hơn |
| Exclusive | `TINHHOADIEM` `2-4` | `TINHHOADIEM` `3-5` |

## ☠️ D3 - Tế Đàn Rừng Sương Độc

📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon5.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon6.yml
📁 Config: /plugins/zMenu/inventories/DUNGEON_D3.yml

| Nội dung | Thường | PvP |
|---|---|---|
| Warp | `dungeon3` | `dungeon3pvp` |
| Level menu | `30+` | `40+` ở menu tổng, `30+` trong chi tiết D3 |
| Max mobs | `56` | `74` |
| Tâm dungeon | `Dungeon3, 0,65,-1` | `Dungeon3, 499,68,621` |
| Chủ đề | Độc, rễ cây, rừng sương | PvP có lượng nguyên liệu và currency cao hơn |

| Nhóm | Mob/Boss | Vai trò |
|---|---|---|
| Quái thường | `Thợ Săn Huyết Tộc`, `Tuần Tra Viên Rừng Độc`, `Tàn Tích Hiến Tế`, `Kẻ Gác Đêm Mê Muội` | Nhanh, poison, ranged, tank |
| Tinh anh | `Đại Tư Tế Sương Mù`, `Sứ Giả Đầm Lầy`, `Pháp Sư Mặt Nạ`, `Thủ Lĩnh Thợ Săn` | Blind/poison, tank, knockback, shield |
| Boss | `Tư Tế Huyết Lễ` | Witch, HP `6000`, damage `60`, poison AoE, darkness, heal |
| Boss | `Linh Rừng Thiêng` | Warden, HP `8000`, damage `75`, armor `35`, projectile nhận 50% |

| Reward chính | Thường | PvP |
|---|---|---|
| Nguyên liệu quái 4 loại | `2-4`, chance `30 + players*3` | `5-10`, chance `60 + players*5` |
| `SATTINHCHE` | `2` đến `4 + stage` | `5` đến `10 + stage*2` |
| `DACUONGHOACAOCAP` | `1`, chance `3 + stage*2` | `1-2`, chance `8 + stage*5` |
| `ANKYTHOSAN` | `1`, chance `1.5 + stage*0.2` | `1`, chance `1.5 + stage*0.3` |
| `PHOIRENVUKHI`, `PHOIRENGIAP` | `1`, chance `4 + stage*0.5` | `1`, chance `6 + stage*0.8` |
| MobCoins/SoulCoins | `35` / `10` | `85` / `25` |
| Crate/key | `GemChest-2`, `Enchant III`, `RandomMoney3`, `ThungQuang-Lv2`, key `dungeon` | Cùng nhóm nhưng tỉ lệ cao hơn |
| Exclusive | `TINHHOASUONGDOC` `1-3` | `TINHHOASUONGDOC` `2-6` |

## 🌋 D4 - Tế Đàn Vực Thẳm Rực Cháy

📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon7.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon8.yml
📁 Config: /plugins/zMenu/inventories/DUNGEON_D4.yml

| Nội dung | Thường | PvP |
|---|---|---|
| Warp | `dungeon4` | `dungeon4pvp` |
| Level menu | `50+` | `60+` ở menu tổng, `50+` trong chi tiết D4 |
| Max mobs | `66` | `86` |
| Tâm dungeon | `Dungeon4, 102,77,116` | `Dungeon4, 535,19,499` |
| Khuyến nghị menu | Cần trang bị `T4+` | Cần T4+ và chấp nhận rủi ro PvP |

| Nhóm | Mob/Boss | Vai trò |
|---|---|---|
| Quái thường | `Đá Vụn Đỏ Thẫm`, `Hỏa Hồn Lang Thang`, `Kẻ Canh Giữ Tro Tàn`, `Linh Kiện Cổ Đại` | Lửa linh hồn, tank, brute melee |
| Tinh anh | `Sứ Giả Vực Sâu`, `Thẩm Phán Tro Tàn`, `Thiết Giáp Tế Đàn`, `Sứ Giả Lòng Đất Sâu` | Damage cao, blind, golem tank, wither pressure |
| Boss | `Vua Không Ngai` | Wither Skeleton, HP `9500`, damage `78`, armor `28`, fire/lava immune |
| Boss | `Tế Ma Vương` | Warden, HP `14000`, damage `100`, armor `45`, darkness/wither/heal/counter |

| Reward chính | Thường | PvP |
|---|---|---|
| `KCTINHCHE` | `2` đến `3 + stage` | `5` đến `8 + stage*2` |
| `DACUONGHOATOITHUONG` | `1`, chance `2 + stage` | `1-2`, chance `5 + stage*3` |
| `ANKYTHOSAN` | `1`, chance `1 + stage*0.2` | `1`, chance `2.5 + stage*0.5` |
| Phôi rèn | `5 + stage*0.6` | `8 + stage*1.0` |
| MobCoins/SoulCoins | `50` / `20` | `120` / `50` |
| Crate/key | `GemChest-3`, `Enchant IV`, `RandomMoney4`, `ThungQuang-Lv2`, key `dungeon`, key `nguyenlieu` | Tỉ lệ cao hơn trong PvP |
| Exclusive | `DATIENHOA_1`, `TINHHOAVUCTHAM` | Cùng loại, PvP tăng số lượng/tỉ lệ |

## 🌳 D5 - Vườn Địa Đàng

📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon9.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon10.yml
📁 Config: /plugins/zMenu/inventories/DUNGEON_D5.yml

| Nội dung | Thường | PvP |
|---|---|---|
| Warp | `dungeon5` | `dungeon5pvp` |
| Level menu | `70+` | `80+` ở menu tổng, `70+` trong chi tiết D5 |
| Max mobs | `78` | `86` |
| Tâm dungeon | `Dungeon5, -13,51,-313` | `Dungeon5, 488,51,193` |
| Khuyến nghị menu | `T4-T5` | T5/team mạnh, rủi ro PvP cao nhất |

| Nhóm | Mob/Boss | Vai trò |
|---|---|---|
| Quái thường | `Linh Hồn Của Gió`, `Vệ Binh Hoàng Hôn`, `Kẻ Canh Giữ Vô Danh`, `Kẻ Hành Hương Cuối Cùng` | Phantom/ranged/golem/wither skeleton, damage cao |
| Tinh anh | `Kẻ Thi Hành Lời Thề`, `Chấp Pháp Viên Phế Tích`, `Tu Sĩ Mùa Thu`, `Hộ Pháp Bàn Thạch` | Tinh anh endgame, blind, poison, shield, knockback |
| Boss | `Giao Hưởng Của Lá Và Gió` | Iron Golem, HP `15000`, damage `100`, armor `35`, AoE mạnh |
| Boss | `Linh Vườn Địa Đàng` | Warden, HP `22000`, damage `130`, armor `55`, projectile nhận 50%, darkness/heal/counter |

| Reward chính | Thường | PvP |
|---|---|---|
| `NETHERITETINHCHE` | `2` đến `3 + stage` | `5` đến `8 + stage*2` |
| `DACUONGHOATOITHUONG` | `1`, chance `2 + stage` | `1-2`, chance `5 + stage*3` |
| `ANKYTHOSAN` | `1`, chance `2 + stage*0.3` | `1-2`, chance `5 + stage*0.8` |
| Phôi rèn | `6 + stage*0.7` | `10 + stage*1.2` |
| MobCoins/SoulCoins | `75` / `30` | `180` / `75` |
| Crate/key | `GemChest-4`, `Enchant V`, `RandomMoney5`, `ThungQuang-Lv3`, key `dungeon`, key `trangbingaunhien` | PvP thêm tỉ lệ cao và key có thể rơi `1-2` dungeon key |
| Hiếm/cực hiếm | `GemChest-5`, `Enchant VI`, `DATIENHOA_2`, `DATIENHOA_3`, `TINHHOADIADANG` | Cùng nhóm, PvP tăng chance/số lượng |

## ⚔️ Nên Đi Dungeon Nào?

| Giai đoạn | Nên đi | Lý do |
|---|---|---|
| Mới bắt đầu | D1 thường | Dễ, có đá cuội tinh chế, đá cường hóa sơ cấp, GemChest I |
| Cấp 15-30 | D2 thường | Mở Đồng Tinh Chế, SoulCoins, Enchant II, key nguyên liệu |
| Cấp 30-50 | D3 thường | Bắt đầu farm phôi rèn, ấn ký, Sắt Tinh Chế, GemChest II |
| Cấp 50-70 | D4 thường | Farm Kim Cương Tinh Chế, Đá Cường Hóa Tối Thượng, Đá Tiến Hóa I |
| Cấp 70+ | D5 thường | Farm Netherite Tinh Chế, GemChest IV/V, Enchant V/VI, Đá Tiến Hóa II/III |
| Có team/đồ mạnh | Bản PvP cùng tier | Loot/EXP x2.5 theo menu, nhưng có nguy cơ bị player khác hạ |

## ⚠️ Lưu Ý Khi Đi Dungeon

| Tình huống | Lời khuyên |
|---|---|
| Boss bị kéo khỏi khu đánh | Đừng kéo quá `30 block`, boss có thể bị kéo về làm mất nhịp combat |
| Bị debuff độc/blind/darkness | D3 trở lên nên chuẩn bị đồ hồi phục/giải hiệu ứng nếu server cho phép |
| Đi PvP | Chỉ đi khi chấp nhận mất lợi thế vì player khác có thể tấn công |
| Đứng ngoài vùng quá xa | Có thể làm fail stage do proximity check `100 block` |
| Sau khi clear stage | Về khu Tim Hầm Ngục để nhận thưởng trong `30 giây` |
| Không đóng góp | Sau `300 giây` không hoạt động có thể bị đưa về spawn |

Xem thêm: [bosses.md](bosses.md), [mythicmobs.md](mythicmobs.md), [drops-rewards.md](drops-rewards.md), [../Items/dungeon-items.md](../Items/dungeon-items.md), [../PvP/maps-events.md](../PvP/maps-events.md)
