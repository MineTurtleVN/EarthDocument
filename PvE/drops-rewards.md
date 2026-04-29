# 🎁 Drop Và Phần Thưởng PvE

Plugin chính: `TurtleDungeon`, `MMOItems`, `ExcellentCrates`, `MobsCoin`, `PlayerPoints`

📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon1.yml → dungeon10.yml
📁 Config: /plugins/MMOItems/drops.yml
📁 Config: /plugins/MMOItems/item/material.yml
📁 Config: /plugins/ExcellentCrates/crates/dungeons.yml
📁 Config: /plugins/ExcellentCrates/keys/dungeon.yml

Nguồn thưởng PvE quan trọng nhất là dungeon stage reward, boss reward, MMOItems material, key/crate và currency. Phần lớn reward trong TurtleDungeon dùng công thức có `{stage}` và `{players}`, nên stage cao và nhóm đủ người thường đem lại nhiều vật phẩm hơn.

## 🧭 Nguồn Thưởng Chính

| Nguồn | Plugin/config | Người chơi nhận gì |
|---|---|---|
| Quái thường ngoài dungeon | `/plugins/MMOItems/drops.yml` | Nguyên liệu quái cơ bản từ vanilla mob |
| Stage dungeon | `/plugins/TurtleDungeon/Dungeons/*.yml` | Vật liệu tinh chế, đá cường hóa, MobCoins, SoulCoins, crate/voucher |
| Boss dungeon | `/plugins/TurtleDungeon/Dungeons/*.yml` | Ấn ký, tinh hoa dungeon, vật phẩm hiếm, reward stage cao |
| Crate Phó Bản | `/plugins/ExcellentCrates/crates/dungeons.yml` | Key, vật liệu, đá cường hóa, voucher, item nâng cấp |
| Key Dungeon | `/plugins/ExcellentCrates/keys/dungeon.yml` | Key ảo `dungeon` dùng mở crate `Phó Bản` |

## 🧟 Drop MMOItems Từ Vanilla Mob

| Mob vanilla | MMOItems group | Item | Số lượng |
|---|---|---|---:|
| `ZOMBIE` | `NGUYENLIEUQUAI1` | `MATERIAL:HUYETDICH` | `1-2` |
| `SKELETON` | `NGUYENLIEUQUAI2` | `MATERIAL:MANHHONLACLOI` | `1-2` |
| `SPIDER` | `NGUYENLIEUQUAI3` | `MATERIAL:NANHVUOTTAMDOC` | `1-2` |
| `CREEPER` | `NGUYENLIEUQUAI4` | `MATERIAL:TINHTHELUUHUYNH` | `1-2` |

Những item này cũng xuất hiện trong reward dungeon/crate và dùng cho trao đổi tại `/warp trade` hoặc `/warp tradedungeon` theo lore MMOItems.

## 🗝️ Crate Phó Bản

| Thuộc tính | Giá trị |
|---|---|
| Tên crate | `&cPhó Bản` |
| Key required | `true` |
| Key ID | `dungeon` |
| Vị trí crate | `Lobby, X -40, Y 168, Z 16` |
| Preview | `Enabled: true` |
| Animation | `csgo` |
| Cooldown mở | `0` |
| Hologram | Bật |

### Reward Đáng Chú Ý Trong Crate Phó Bản

| Reward ID | Loại | Weight | Rarity | Lệnh thưởng |
|---|---|---:|---|---|
| `keynguyenlieu` | Key | `5.0` | `rare` | `ecrates key give %player% nguyenlieu 1` |
| `keyspawner` | Key | `1.0` | `legendary` | `ecrates key give %player% spawner 1` |
| `materialhuyetdich` | MMOItems | `7.0` | `common` | `mi give MATERIAL HUYETDICH %player% 10` |
| `materialmanhhonlacloi` | MMOItems | `7.0` | `common` | `mi give MATERIAL MANHHONLACLOI %player% 10` |
| `materialtinhtheluuhuynh` | MMOItems | `7.0` | `common` | `mi give MATERIAL TINHTHELUUHUYNH %player% 10` |
| `materialnanhvuottamdoc` | MMOItems | `7.0` | `common` | `mi give MATERIAL NANHVUOTTAMDOC %player% 10` |
| `materialmanhthosan` | MMOItems | `5.0` | `rare` | `mi give MATERIAL MANHTHOSAN %player% 3` |
| `materialankythosan` | MMOItems | `3.0` | `epic` | `mi give MATERIAL ANKYTHOSAN %player% 1` |
| `materialdatienhoa_1` | MMOItems | `4.0` | `rare` | `mi give MATERIAL DATIENHOA_1 %player% 1` |
| `materialdatienhoa_2` | MMOItems | `3.0` | `epic` | `mi give MATERIAL DATIENHOA_2 %player% 1` |
| `materialdacuonghoasocap` | MMOItems | `6.0` | `common` | `mi give MATERIAL DACUONGHOASOCAP %player% 3` |
| `materialdacuonghoatrungcap` | MMOItems | `4.5` | `rare` | `mi give MATERIAL DACUONGHOATRUNGCAP %player% 2` |
| `materialdacuonghoacaocap` | MMOItems | `3.0` | `epic` | `mi give MATERIAL DACUONGHOACAOCAP %player% 1` |
| `materialdacuonghoatoithuong` | MMOItems | `1.5` | `legendary` | `mi give MATERIAL DACUONGHOATOITHUONG %player% 1` |
| `materialtinhhoathach` | MMOItems | `4.0` | `rare` | `mi give MATERIAL TINHHOATHACH %player% 2` |
| `materialtinhhoadiem` | MMOItems | `3.5` | `rare` | `mi give MATERIAL TINHHOADIEM %player% 2` |
| `materialtinhhoasuongdoc` | MMOItems | `3.0` | `epic` | `mi give MATERIAL TINHHOASUONGDOC %player% 1` |
| `materialtinhhoavuctham` | MMOItems | `2.0` | `legendary` | `mi give MATERIAL TINHHOAVUCTHAM %player% 1` |
| `materialtinhhoadiadang` | MMOItems | `1.5` | `legendary` | `mi give MATERIAL TINHHOADIADANG %player% 1` |
| `materialphoirenvukhi` | MMOItems | `3.5` | `epic` | `mi give MATERIAL PHOIRENVUKHI %player% 1` |
| `materialphoirengiap` | MMOItems | `3.5` | `epic` | `mi give MATERIAL PHOIRENGIAP %player% 1` |
| `vouchergemchest2` | Voucher | `5.0` | `rare` | `av give %player% GemChest-2 1` |
| `vouchergemchest3` | Voucher | `2.5` | `epic` | `av give %player% GemChest-3 1` |
| `voucherenchant3` | Voucher | `4.0` | `rare` | `av give %player% EnchantmentRandom-3 1` |
| `voucherenchant4` | Voucher | `1.5` | `legendary` | `av give %player% EnchantmentRandom-4 1` |
| `voucherthungquang2` | Voucher | `4.0` | `rare` | `av give %player% ThungQuang-Lv2 1` |

## 🏛️ Reward Theo Dungeon

| Dungeon | Tài nguyên chính | Đá cường hóa | Tinh hoa riêng | Voucher/key nổi bật |
|---|---|---|---|---|
| D1 Ngôi Đền Của Đá | `DACUOCTINHCHE`, nguyên liệu quái cơ bản | `DACUONGHOASOCAP` | `TINHHOATHACH` | `GemChest-1`, `EnchantmentRandom-1`, `RandomMoney1`, `ThungQuang-Lv1` |
| D2 Đất Và Lửa | `DONGTINHCHE` | `DACUONGHOATRUNGCAP` | `TINHHOADIEM` | `GemChest-1`, `Enchant II`, key `nguyenlieu` |
| D3 Rừng Sương Độc | `SATTINHCHE`, `PHOIRENVUKHI`, `PHOIRENGIAP` | `DACUONGHOACAOCAP` | `TINHHOASUONGDOC` | `GemChest-2`, `Enchant III`, key `dungeon` |
| D4 Vực Thẳm | `KCTINHCHE`, phôi rèn | `DACUONGHOATOITHUONG` | `TINHHOAVUCTHAM` | `GemChest-3`, `Enchant IV`, `DATIENHOA_1`, key `dungeon` |
| D5 Địa Đàng | `NETHERITETINHCHE`, phôi rèn | `DACUONGHOATOITHUONG` | `TINHHOADIADANG` | `GemChest-4/5`, `Enchant V/VI`, `DATIENHOA_2/3`, key trang bị |

## 💰 Currency Trong Dungeon

| Dungeon | Thường | PvP |
|---|---|---|
| D1 | MobCoins `10` theo reward config | Cao hơn theo bản PvP |
| D2 | MobCoins `20`, SoulCoins `5` | MobCoins `50`, SoulCoins `12` |
| D3 | MobCoins `35`, SoulCoins `10` | MobCoins `85`, SoulCoins `25` |
| D4 | MobCoins `50`, SoulCoins `20` | MobCoins `120`, SoulCoins `50` |
| D5 | MobCoins `75`, SoulCoins `30` | MobCoins `180`, SoulCoins `75` |

## 📈 Reward Scaling

| Biến | Xuất hiện trong config | Ý nghĩa |
|---|---|---|
| `{stage}` | Chance/số lượng reward | Stage càng cao càng tăng tỉ lệ hoặc số lượng |
| `{players}` | Chance reward | Nhiều người tham gia có thể tăng tỉ lệ rơi |
| `1-2`, `5-10` | Amount range | Số lượng vật phẩm ngẫu nhiên trong khoảng |
| `chance` | Tỉ lệ nhận | Không phải reward nào cũng chắc chắn rơi |
| `commands` | Lệnh thưởng | Một số reward là lệnh `mi give`, `av give`, `mc give`, `points give` |

## 🎯 Nên Farm Gì Trước?

| Mục tiêu | Nơi farm |
|---|---|
| Vật liệu quái cơ bản | D1 hoặc vanilla mob theo `MMOItems/drops.yml` |
| Đá cường hóa sơ/trung/cao | D1 → D2 → D3 |
| Đá cường hóa tối thượng | D4/D5, crate Phó Bản |
| Phôi rèn | D3 trở lên, crate Phó Bản |
| Đá tiến hóa Rùa | D4/D5 hoặc crate Phó Bản |
| Key/crate dungeon | D3 trở lên hoặc reward dungeon PvP |

Xem thêm: [dungeons.md](dungeons.md), [bosses.md](bosses.md), [../Items/dungeon-items.md](../Items/dungeon-items.md), [../Items/rewards-crates.md](../Items/rewards-crates.md)
