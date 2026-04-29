# 🏛️ Dungeon Items

Plugin chính: `TurtleDungeon`, `MMOItems`, `ExcellentCrates`

📁 Config: /plugins/TurtleDungeon/Dungeons/dungeon1.yml → dungeon10.yml
📁 Config: /plugins/MMOItems/item/material.yml
📁 Config: /plugins/MMOItems/drops.yml
📁 Config: /plugins/ExcellentCrates/crates/dungeons.yml
📁 Config: /plugins/ExcellentCrates/keys/dungeon.yml

Dungeon items là nhóm vật phẩm dùng để nâng cấp trang bị, trao đổi, mở crate và tiến hóa hệ thống phụ như Rùa Thần. Có 4 nhóm lớn: nguyên liệu quái, nguyên liệu tinh chế, đá cường hóa/tinh hoa dungeon, và key/voucher.

## 🧱 Nhóm Vật Phẩm Chính

| Nhóm | Item ID | Nguồn | Công dụng |
|---|---|---|---|
| Nguyên liệu quái | `HUYETDICH`, `MANHHONLACLOI`, `TINHTHELUUHUYNH`, `NANHVUOTTAMDOC` | Mob/quái dungeon/crate | Đổi vật phẩm tại `/warp trade` hoặc `/warp tradedungeon` |
| Mảnh/Ấn thợ săn | `MANHTHOSAN`, `ANKYTHOSAN` | Công phá dungeon/boss dungeon/crate | Đổi vật phẩm giá trị, liên quan boss dungeon |
| Tinh chế khoáng | `DACUOCTINHCHE`, `DONGTINHCHE`, `SATTINHCHE`, `KCTINHCHE`, `NETHERITETINHCHE` | Dungeon theo tier | Nguyên liệu nâng cấp/trao đổi |
| Đá cường hóa | `DACUONGHOASOCAP`, `DACUONGHOATRUNGCAP`, `DACUONGHOACAOCAP`, `DACUONGHOATOITHUONG` | Dungeon/crate | Tăng EXP cường hóa trang bị tại `/cuonghoa` |
| Tinh hoa dungeon | `TINHHOATHACH`, `TINHHOADIEM`, `TINHHOASUONGDOC`, `TINHHOAVUCTHAM`, `TINHHOADIADANG` | Dungeon 1-5 | Đột phá trang bị, chế tạo đá cường hóa |
| Phôi rèn | `PHOIRENVUKHI`, `PHOIRENGIAP` | D3+, crate | Rèn vũ khí/giáp bậc cao |
| Tiến hóa | `DATIENHOA_1`, `DATIENHOA_2`, `DATIENHOA_3` | D4/D5, crate | Tiến hóa Rùa Thần theo level yêu cầu |
| Key/voucher | `dungeon`, `GemChest-*`, `EnchantmentRandom-*`, `ThungQuang-*` | Reward/crate | Mở crate hoặc nhận vật phẩm phụ trợ |

## 🩸 Nguyên Liệu Quái Cơ Bản

| Item ID | Tên hiển thị | Material | Nguồn config | Ghi chú |
|---|---|---|---|---|
| `HUYETDICH` | Huyết Dịch Ô Uế | `FERMENTED_SPIDER_EYE` | `MMOItems/drops.yml` từ `ZOMBIE`; crate Phó Bản | Dùng `/warp trade` |
| `MANHHONLACLOI` | Mảnh Hồn Lạc Lối | `LIGHT_GRAY_DYE` | Từ `SKELETON`; crate Phó Bản | Dùng `/warp trade` |
| `TINHTHELUUHUYNH` | Tinh Thể Lưu Huỳnh | `IRON_INGOT` | Từ `CREEPER`; crate Phó Bản | Lore ghi `/warp tradedungeon` |
| `NANHVUOTTAMDOC` | Nanh Vuốt Tẩm Độc | `BONE` | Từ `SPIDER`; crate Phó Bản | Dùng `/warp trade` |
| `MANHTHOSAN` | Mảnh Thợ Săn | `NETHERITE_SCRAP` | Công phá dungeon; crate Phó Bản | Tier `i3` |
| `ANKYTHOSAN` | Ấn Ký Thợ Săn | `BOOK` | Boss dungeon; crate Phó Bản | Tier `i5`, rơi từ boss dungeon |

## ⛏️ Nguyên Liệu Tinh Chế Theo Tier

| Item ID | Tên | Dungeon liên quan | Vai trò |
|---|---|---|---|
| `DACUOCTINHCHE` | Đá Cuội Tinh Chế | D1 | Nguyên liệu đầu game, dùng trade |
| `DONGTINHCHE` | Đồng Tinh Chế | D2 | Nguyên liệu early/mid |
| `SATTINHCHE` | Sắt Tinh Chế | D3 | Nguyên liệu mid-game |
| `KCTINHCHE` | Kim Cương Tinh Chế | D4 | Nguyên liệu late-game |
| `NETHERITETINHCHE` | Netherite Tinh Chế | D5 | Nguyên liệu endgame |

## 💎 Đá Cường Hóa

| Item ID | Tên | EXP cường hóa | Chi phí lore | Nguồn tốt nhất |
|---|---|---:|---:|---|
| `DACUONGHOASOCAP` | Đá Cường Hóa Sơ Cấp | `+20 EXP` | `$50` | D1, crate Phó Bản |
| `DACUONGHOATRUNGCAP` | Đá Cường Hóa Trung Cấp | `+100 EXP` | `$200` | D2, crate Phó Bản |
| `DACUONGHOACAOCAP` | Đá Cường Hóa Cao Cấp | `+500 EXP` | `$1,000` | D3, crate Phó Bản |
| `DACUONGHOATOITHUONG` | Đá Cường Hóa Tối Thượng | `+10,000 EXP` | `$20,000` | D4/D5, crate Phó Bản |

## ✨ Tinh Hoa Dungeon

| Item ID | Tên | Nơi rơi | Công dụng trong lore |
|---|---|---|---|
| `TINHHOATHACH` | Tinh Hoa Cổ Thạch | Dungeon 1 - Ngôi Đền Của Đá | Đột phá trang bị; chế tạo Đá Cường Hóa Sơ Cấp `10:1` |
| `TINHHOADIEM` | Tinh Hoa Hỏa Diệm | Dungeon 2 - Đất/Lửa | Đột phá trang bị; chế tạo Đá Cường Hóa Trung Cấp `10:1` |
| `TINHHOASUONGDOC` | Tinh Hoa Sương Độc | Dungeon 3 - Rừng Sương Độc | Đột phá trang bị; chế tạo Đá Cường Hóa Cao Cấp `10:1` |
| `TINHHOAVUCTHAM` | Tinh Hoa Vực Thẳm | Dungeon 4 - Vực Thẳm | Đột phá trang bị; chế tạo Đá Cường Hóa Tối Thượng `10:1` |
| `TINHHOADIADANG` | Tinh Hoa Địa Đàng | Dungeon 5 - Địa Đàng | Đột phá trang bị; chế tạo Đá Cường Hóa Tối Thượng x3 `10:3` |

## 🛠️ Rèn Và Tiến Hóa

| Item ID | Tên | Công dụng |
|---|---|---|
| `PHOIRENVUKHI` | Phôi Rèn Vũ Khí | Phôi thép huyền bí dùng để rèn vũ khí bậc cao |
| `PHOIRENGIAP` | Phôi Rèn Giáp Trụ | Phôi thép huyền bí dùng để rèn giáp trụ bậc cao |
| `DATIENHOA_1` | Mảnh Vỡ Thủy Triều | Tiến hóa Rùa Thần level `10` và `20` |
| `DATIENHOA_2` | Tinh Thể Biển Sâu | Tiến hóa Rùa Thần level `30` và `50` |
| `DATIENHOA_3` | Long Quy Chi Ấn | Tiến hóa Rùa Thần level `70`, `90` và `100` |

## 🗝️ Key Dungeon Và Crate

| Item | Config | Ghi chú |
|---|---|---|
| Key ID `dungeon` | `/plugins/ExcellentCrates/keys/dungeon.yml` | Virtual key, dùng mở crate `Phó Bản` |
| Crate `Phó Bản` | `/plugins/ExcellentCrates/crates/dungeons.yml` | Vị trí `Lobby -40 168 16`, preview bật, animation `csgo` |
| Key `nguyenlieu` | Reward trong crate Phó Bản | Có thể nhận từ crate dungeon, rarity `rare` |
| Key `spawner` | Reward trong crate Phó Bản | Rarity `legendary`, có broadcast |

## 🧭 Lộ Trình Farm Item

| Giai đoạn | Farm gì | Lý do |
|---|---|---|
| D1 | `DACUOCTINHCHE`, `DACUONGHOASOCAP`, `TINHHOATHACH` | Mở nền cường hóa và trade đầu game |
| D2 | `DONGTINHCHE`, `DACUONGHOATRUNGCAP`, `TINHHOADIEM` | Chuyển sang nâng cấp trung cấp |
| D3 | `SATTINHCHE`, `PHOIRENVUKHI`, `PHOIRENGIAP`, `TINHHOASUONGDOC` | Bắt đầu rèn gear và farm item mid-game |
| D4 | `KCTINHCHE`, `DACUONGHOATOITHUONG`, `DATIENHOA_1`, `TINHHOAVUCTHAM` | Chuẩn bị gear late-game/Rùa Thần |
| D5 | `NETHERITETINHCHE`, `DATIENHOA_2`, `DATIENHOA_3`, `TINHHOADIADANG` | Endgame, vật phẩm hiếm nhất |

Xem thêm: [../PvE/dungeons.md](../PvE/dungeons.md), [../PvE/drops-rewards.md](../PvE/drops-rewards.md), [mmoitems.md](mmoitems.md), [rewards-crates.md](rewards-crates.md)
