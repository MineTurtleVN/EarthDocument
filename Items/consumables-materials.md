# 🧪 Consumables, Vật Liệu Và Gem

Plugin chính: `MMOItems`, `MMOUpgrade`, `GemFusion`, `zMenu`, `ExcellentCrates`

📁 Config: /plugins/MMOItems/item/consumable.yml  
📁 Config: /plugins/MMOItems/item/material.yml  
📁 Config: /plugins/MMOItems/item/gem_stone.yml  
📁 Config: /plugins/MMOItems/item/miscellaneous.yml  
📁 Config: /plugins/MMOUpgrade/config.yml  
📁 Config: /plugins/zMenu/inventories/CSHOP.yml  
📁 Config: /plugins/zMenu/inventories/AFK.yml

Trang này tập trung vào item không phải trang bị chính: đá cường hóa, tinh hoa, gem, đục ngọc, huy hiệu, vật phẩm AFK/shop và công cụ tiện ích.

## ⚡ Đá Cường Hóa Và EXP Nâng Đồ

📁 Config: /plugins/MMOUpgrade/config.yml → `experience-materials`

| ID | EXP | Chi phí nạp | Khi nào dùng |
|---|---:|---:|---|
| `DACUONGHOASOCAP` | `20` | `50` | Đồ thấp, mốc đầu |
| `DACUONGHOATRUNGCAP` | `100` | `200` | Đồ 3 sao/mid sớm |
| `DACUONGHOACAOCAP` | `500` | `1,000` | Đồ 4 sao trở lên |
| `DACUONGHOATOITHUONG` | `10,000` | `20,000` | Mốc lớn/đồ cuối game |

## 🏰 Tinh Hoa Dungeon

📁 Config: /plugins/MMOUpgrade/config.yml  
📁 Config: /plugins/MMOItems/item/material.yml

| ID | EXP khi nạp trực tiếp | Chi phí nạp | Gắn với dungeon |
|---|---:|---:|---|
| `TINHHOATHACH` | `3` | `10` | Ngôi Đền Của Đá |
| `TINHHOADIEM` | `15` | `50` | Bản Di Chúc Đất && Lửa |
| `TINHHOASUONGDOC` | `75` | `250` | Tế Đàn Rừng Sương Độc |
| `TINHHOAVUCTHAM` | `1,500` | `5,000` | Vực Thẳm Rực Cháy |
| `TINHHOADIADANG` | `4,500` | `15,000` | Vườn Địa Đàng |

Tinh hoa không chỉ để đổi/craft; config `MMOUpgrade` cho phép dùng trực tiếp làm EXP cường hóa. Với đồ cao, giữ tinh hoa D4-D5 quan trọng hơn bán lẻ.

## 💎 Dòng Gem Chính

📁 Config: /plugins/MMOItems/item/gem_stone.yml

| Dòng | ID pattern | Slot | Chỉ số | Cấp I | Cấp XV |
|---|---|---|---|---:|---:|
| Tỉ lệ chí mạng | `NGOCTILECHIMANG1-15` | `ᴠũ ᴋʜí` | `critical-strike-chance` | `1.0` | `12.0` |
| ST chí mạng | `NGOCSTCHIMANG1-15` | `ᴠũ ᴋʜí` | `critical-strike-power` | `5` | `80` |
| Hút máu | `NGOCHUTMAU1-15` | `ᴠũ ᴋʜí` | `lifesteal` | `0.5` | `6.0` |
| Săn Bắt | `NGOCSANBAT1-15` | `ᴠũ ᴋʜí` | `pve-damage` | `5` | `85` |
| Né đòn | `NGOCNE1-15` | `ɢɪáᴘ` | `dodge-rating` | `0.2` | `5.0` |
| Sinh Mệnh | `NGOCMAU1-15` | `ɢɪáᴘ` | `max-health` | `1` | `50` |

Tỉ lệ thành công giảm theo cấp: cấp I-III thường `100%`, cấp IV khoảng `95%`, rồi giảm dần đến cấp XV chỉ còn `15%`.

## 🔧 Đục Ngọc Và Gỡ Gem

📁 Config: /plugins/MMOItems/item/consumable.yml

| ID | Tên | Cấp gem hỗ trợ | Cách dùng |
|---|---|---|---|
| `DUCNGOC1` | Đục Ngọc thô sơ | `I-VI` | Dùng `/ducngoc` |
| `DUCNGOC2` | Đục Ngọc cao cấp | `VII-XII` | Dùng `/ducngoc` |
| `GEM_REMOVER` | Đục Ngọc ngẫu nhiên | Gỡ `1` ngọc ngẫu nhiên | Kéo và thả vào trang bị, `random-unsocket: 1.0`, tỉ lệ `100%` |

`GEM_REMOVER` có bán trong Xu Shop theo tài liệu shop trước đó, nhưng vì chỉ gỡ ngẫu nhiên 1 viên nên không nên dùng trên món có nhiều gem quý nếu bạn muốn chọn đúng viên.

## 🏅 Huy Hiệu Sự Kiện 30/4

📁 Config: /plugins/MMOItems/item/miscellaneous.yml

| ID | Sao/tier | Hiệu ứng khi dùng | Cooldown |
|---|---|---|---:|
| `HUYHIEUTANBINH` | `⭐`, tier `1` | Hồi `15%` máu tối đa và nửa thanh đói | `60s` |
| `HUYHIEUCAMTU` | `⭐⭐`, tier `3` | Hồi `20%` máu tối đa và đầy đói | `55s` |
| `HUYHIEUVEQUOC` | `⭐⭐⭐`, tier `5` | Hồi `25%` máu tối đa, đầy đói, xóa hiệu ứng bất lợi | `50s` |
| `HUYHIEUGIAIPHONG` | `⭐⭐⭐⭐`, tier `7` | Hồi `30%`, xóa hiệu ứng bất lợi, nhận buff bùng nổ 3 giây | `45s` |
| `HUANCHUONGDOCLAP` | `⭐⭐⭐⭐⭐`, tier `9` | Hồi `40%`, đầy no, xóa hiệu ứng bất lợi, buff mạnh 3 giây | `40s` |

Các item này dùng ability riêng ở `mode: RIGHT_CLICK`, phù hợp làm vật phẩm hồi phục/thoát nguy trong PvE hoặc PvP nếu server cho phép dùng.

## 💤 Vật Phẩm AFK Shop

📁 Config: /plugins/zMenu/inventories/AFK.yml

| Vật phẩm | Giá điểm AFK | Lệnh nhận |
|---|---:|---|
| Chìa khóa AFK | `35` | `crates key give %player% afk 1` |
| Thùng Quặng Lv.1 | `80` | `av give %player% ThungQuang-Lv1 1` |
| Thùng Quặng Lv.2 | `200` | `av give %player% ThungQuang-Lv2 1` |
| Gậy Bán Đồ Cấp I | `50` | `tools give %player% sell_wand1` |
| Gậy Ghép Đồ | `80` | `tools give %player% crafting_wand` |

## 🧭 Ưu Tiên Sử Dụng

| Item | Nên dùng khi | Lưu ý |
|---|---|---|
| Đá sơ/trung cấp | Đồ thấp, nâng nhanh để farm | Không cần tiếc quá nhiều |
| Đá cao/tối thượng | Đồ 4-5 sao, mốc tiến hóa | Giữ cho trang bị chính |
| Tinh hoa D4-D5 | Mốc 50+ hoặc đồ late-game | Không tiêu bừa vào đồ thay sớm |
| Gem cấp cao | Đồ dùng lâu dài | Kiểm tra slot `ᴠũ ᴋʜí`/`ɢɪáᴘ` |
| Đục ngọc | Khi thay build hoặc nâng cấp đồ | Chọn đúng loại để tránh phí |
| Huy hiệu | Tình huống nguy hiểm/boss/PvP | Kiểm tra cooldown trước khi lao vào đánh |

Xem thêm: [mmoitems.md](mmoitems.md), [dungeon-items.md](dungeon-items.md), [../Gameplay/crafting-upgrades.md](../Gameplay/crafting-upgrades.md)
