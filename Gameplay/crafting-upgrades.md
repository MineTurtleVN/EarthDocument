# 🛠️ Crafting, Phân Rã Và Cường Hóa

Plugin chính: `MMOItems`, `MMOUpgrade`, `zMenu`, `GemFusion`, `ExcellentCrates`

📁 Config: /plugins/zMenu/inventories/CUONGHOA.yml  
📁 Config: /plugins/MMOUpgrade/config.yml  
📁 Config: /plugins/MMOItems/item-tiers.yml  
📁 Config: /plugins/MMOItems/item/material.yml  
📁 Config: /plugins/MMOItems/item/gem_stone.yml  
📁 Config: /plugins/MMOItems/item/consumable.yml

Earth dùng vòng nâng cấp khá rõ: kiếm trang bị, phân rã đồ thừa, lấy nguyên liệu cường hóa, nạp EXP cho đồ chính, rồi vượt mốc tiến hóa ở các cấp lớn.

## 🔥 Lò Rèn `/loren`

📁 Config: /plugins/zMenu/inventories/CUONGHOA.yml

Menu `LÒ RÈN TRANG BỊ [/loren]` có 2 hành động chính:

| Nút | Lệnh | Mục đích |
|---|---|---|
| `⚡ CƯỜNG HÓA TRANG BỊ` | `/upgrade` | Mở giao diện cường hóa để nâng trang bị chính lên `+1`, `+2`, `+3`... |
| `♻ PHÂN RÃ VẬT PHẨM` | `/phanra` | Nghiền trang bị thừa thành nguyên liệu cường hóa |

Lore trong menu mô tả đúng quy trình:

1. Thu thập vũ khí/trang bị thừa từ `/warp trade`, quay rương hoặc hoạt động khác.
2. Dùng máy `Phân Rã` để đổi đồ thừa thành nguyên liệu.
3. Đưa trang bị chính vào `Cường Hóa` để tăng chỉ số.

## ⚡ Nguyên Liệu Nạp EXP Cường Hóa

📁 Config: /plugins/MMOUpgrade/config.yml → `experience-materials`

| ID MMOItems | EXP cường hóa | Tiền mỗi lần nạp | Ghi chú |
|---|---:|---:|---|
| `DACUONGHOASOCAP` | `20` | `50` | Đá sơ cấp, dùng sớm |
| `DACUONGHOATRUNGCAP` | `100` | `200` | Đá trung cấp |
| `DACUONGHOACAOCAP` | `500` | `1,000` | Đá cao cấp |
| `DACUONGHOATOITHUONG` | `10,000` | `20,000` | Đá tối thượng |
| `DACUOCTINHCHE` | `1` | `5` | Khoáng tinh chế thấp |
| `THANTINHCHE` | `2` | `8` | Khoáng tinh chế |
| `DONGTINHCHE` | `4` | `12` | Khoáng tinh chế |
| `SATTINHCHE` | `6` | `20` | Khoáng tinh chế |
| `VANGTINHCHE` | `10` | `30` | Khoáng tinh chế |
| `KCTINHCHE` | `15` | `45` | Khoáng tinh chế |
| `LBTINHCHE` | `25` | `65` | Khoáng tinh chế |
| `NETHERITETINHCHE` | `40` | `100` | Khoáng tinh chế cao |

Tinh hoa dungeon cũng nạp trực tiếp được, và config ghi chú đây là cách `+50%` so với đổi đá.

| Tinh hoa | EXP | Tiền mỗi lần nạp | Nguồn chính |
|---|---:|---:|---|
| `TINHHOATHACH` | `3` | `10` | Dungeon 1 |
| `TINHHOADIEM` | `15` | `50` | Dungeon 2 |
| `TINHHOASUONGDOC` | `75` | `250` | Dungeon 3 |
| `TINHHOAVUCTHAM` | `1,500` | `5,000` | Dungeon 4 |
| `TINHHOADIADANG` | `4,500` | `15,000` | Dungeon 5 |

## 📈 Mốc EXP Và Tiến Hóa Trang Bị

📁 Config: /plugins/MMOUpgrade/config.yml → `levels`

Các mốc `10`, `20`, `30`... có `chance` và yêu cầu nguyên liệu `evolution`. Đây là các mốc cần chuẩn bị trước, vì thất bại hoặc thiếu nguyên liệu sẽ làm kẹt tiến độ nâng đồ.

| Mốc | EXP yêu cầu tại mốc | Tỉ lệ | Nguyên liệu tiến hóa nổi bật |
|---|---:|---:|---|
| `10` | `300` | `50%` | `10 DACUONGHOACAOCAP`, `1 DACUONGHOATOITHUONG`, `128 TINHHOATHACH` |
| `20` | `1,000` | `45%` | `3 DACUONGHOATOITHUONG`, `192 TINHHOATHACH`, `128 TINHHOADIEM` |
| `30` | `6,000` | `40%` | Thêm `128 TINHHOASUONGDOC` |
| `40` | `40,000` | `35%` | Thêm nhiều tinh hoa D1-D3 |
| `50` | `250,000` | `30%` | `PHOIRENVUKHI`, `PHOIRENGIAP`, bắt đầu cần `TINHHOAVUCTHAM` |
| `60` | `1,560,000` | `25%` | `2` phôi mỗi loại, nhiều tinh hoa D4 |
| `70` | `9,680,000` | `20%` | Bắt đầu cần `TINHHOADIADANG` |
| `80` | `59,800,000` | `15%` | `5` phôi mỗi loại, tinh hoa D5 nhiều hơn |
| `90` | `370,600,000` | `10%` | `8` phôi mỗi loại, lượng tinh hoa rất lớn |

## ♻️ Phân Rã Theo Tier

📁 Config: /plugins/MMOUpgrade/config.yml → `decompose.tiers`  
📁 Config: /plugins/MMOItems/item-tiers.yml

`decompose.allowed-tiers` cho phép phân rã tier `1` đến `11`.

| Tier | Sao/tier item | Kết quả phân rã |
|---|---|---|
| `1` | `★★` base | `2-4 DACUONGHOASOCAP` |
| `2` | `★★` base | `6-10 DACUONGHOASOCAP` |
| `3` | `★★★ R1` | `1-2 DACUONGHOATRUNGCAP`, `3-5 DACUONGHOASOCAP` |
| `4` | `★★★ R2` | `3-5 DACUONGHOATRUNGCAP`, `5-8 DACUONGHOASOCAP` |
| `5` | `★★★ R3` | `6-8 DACUONGHOATRUNGCAP`, `1 DACUONGHOACAOCAP` |
| `6` | `★★★★ R1` | `1-2 DACUONGHOACAOCAP`, `3-5 DACUONGHOATRUNGCAP` |
| `7` | `★★★★ R2` | `3-4 DACUONGHOACAOCAP`, `5-8 DACUONGHOATRUNGCAP` |
| `8` | `★★★★ R3` | `5-6 DACUONGHOACAOCAP`, `1 DACUONGHOATOITHUONG` |
| `9` | `★★★★★ R1` | `1 DACUONGHOATOITHUONG`, `2-4 DACUONGHOACAOCAP` |
| `10` | `★★★★★ R2` | `1-2 DACUONGHOATOITHUONG`, `3-5 DACUONGHOACAOCAP` |
| `11` | `★★★★★ R3` | `2-3 DACUONGHOATOITHUONG`, `5-8 DACUONGHOACAOCAP` |

## 💎 Ngọc Khảm Và Gỡ Ngọc

📁 Config: /plugins/MMOItems/item/gem_stone.yml  
📁 Config: /plugins/MMOItems/item/consumable.yml

Gem có `15` cấp độ, nhiều dòng chia theo vị trí khảm:

| Dòng ngọc | Vị trí `gem-color` | Chỉ số chính | Cấp thấp → cấp cao |
|---|---|---|---|
| `NGOCTILECHIMANG1-15` | `ᴠũ ᴋʜí` | Tỉ lệ chí mạng | `1.0` → `12.0` |
| `NGOCSTCHIMANG1-15` | `ᴠũ ᴋʜí` | Sát thương chí mạng | `5` → `80` |
| `NGOCHUTMAU1-15` | `ᴠũ ᴋʜí` | Hút máu | `0.5` → `6.0` |
| `NGOCSANBAT1-15` | `ᴠũ ᴋʜí` | Sát thương PvE | `5` → `85` |
| `NGOCNE1-15` | `ɢɪáᴘ` | Né đòn | `0.2` → `5.0` |
| `NGOCMAU1-15` | `ɢɪáᴘ` | Máu tối đa | `1` → `50` |

Tỉ lệ khảm giảm dần theo cấp: các cấp đầu thường `100%`, lên cấp cao giảm dần xuống `15%` ở cấp XV.

| Dụng cụ | ID | Công dụng |
|---|---|---|
| Đục Ngọc thô sơ | `DUCNGOC1` | Gỡ ngọc cấp `I-VI`, dùng `/ducngoc` |
| Đục Ngọc cao cấp | `DUCNGOC2` | Gỡ ngọc cấp `VII-XII`, dùng `/ducngoc` |
| Đục Ngọc ngẫu nhiên | `GEM_REMOVER` | Gỡ `1` ngọc ngẫu nhiên, tỉ lệ `100%`, kéo thả vào trang bị |

## ✅ Ưu Tiên Nâng Cấp

| Giai đoạn | Nên làm | Tránh |
|---|---|---|
| Early-game | Phân rã đồ tier thấp, nâng đồ đang dùng vừa đủ farm D1-D2 | Đốt đá cao cấp vào đồ sắp thay |
| Mid-game | Giữ đồ `★★★★`, gom tinh hoa D3-D4, bắt đầu dùng ngọc đúng vị trí | Khảm ngọc cao vào đồ chưa ổn định |
| Late-game | Chuẩn bị phôi, tinh hoa D5, đá tối thượng cho mốc 70+ | Nâng nhiều món cùng lúc làm thiếu nguyên liệu mốc tiến hóa |
| End-game | Tập trung một bộ chính, tối ưu ngọc vũ khí/giáp theo mục tiêu PvE/PvP | Phân rã nhầm đồ tier cao chưa so sánh chỉ số |

Xem thêm: [../Items/mmoitems.md](../Items/mmoitems.md), [../Items/consumables-materials.md](../Items/consumables-materials.md), [../PvE/drops-rewards.md](../PvE/drops-rewards.md)
