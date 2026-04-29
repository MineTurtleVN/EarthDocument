# 👑 Rank Và VIP

Plugin chính: `zMenu`, `LuckPerms`, `PlayerPoints`, `Vault`

📁 Config: /plugins/zMenu/inventories/RANK.yml
📁 Config: /plugins/zMenu/inventories/REPAIR.yml
📁 Config: /plugins/zMenu/inventories/DONATE/

Rank trong `/rank` được mua theo chuỗi nâng cấp: mỗi rank yêu cầu rank trước đó (`rank`) và cấp rank mới (`rank-buy`). Giá dùng Xu (`coin`). Quyền thực tế do LuckPerms xử lý, còn menu zMenu ghi quyền lợi, quà và lệnh thưởng.

## 📈 Bảng Rank Đã Đọc

| Rank | Yêu cầu | Giá Xu | Claim bonus | Homes | `/pv` | AFK | Quà bạc | Booster nổi bật |
|---|---|---:|---:|---:|---:|---|---:|---|
| `bee` | `default` | `19` | `500` | `5` | `1` | `1h` | `5,000` | Sinh Tồn `x1.05` |
| `frog` | `bee` | `39` | `800` | `6` | gồm rank trước | `1.5h` | `10,000` | Shop sell `x1.05` |
| `rabbit` | `frog` | `69` | `1,200` | `7` | `2` | `2h` | `20,000` | Sinh Tồn/Shop `x1.1` |
| `fox` | `rabbit` | `99` | `1,800` | `8` | `3` | `2.5h` | `30,000` | Mythic EXP `x1.1` |
| `wolf` | `fox` | `199` | `2,500` | `9` | `4` | `3h` | `40,000` | Mobcoins `x1.15` |
| `boar` | `wolf` | `299` | `4,000` | `8` | `5` | `4h` | `50,000` | Soul `x1.15` |
| `panda` | `boar` | `499` | `6,000` | `12` | `6` | `5h` | `80,000` | Bộ chỉ số hiện có `x1.2` |
| `tiger` | `panda` | `799` | `8,000` | `14` | `8` | `6h` | `100,000` | Turtle Skill `x1.25` |
| `slime` | `tiger` | `1,299` | `10,000` | `16` | `10` | `7h` | `120,000` | Toàn bộ chỉ số `x1.3` |
| `spider` | `slime` | `1,899` | `12,000` | `18` | `12` | `8h` | `150,000` | Toàn bộ chỉ số `x1.4` |
| `blaze` | `spider` | `2,799` | `15,000` | `20` | `14` | `9h` | `200,000` | Toàn bộ chỉ số `x1.5` |
| `enderman` | `blaze` | `3,999` | `20,000` | `25` | `16` | `10h` | `250,000` | Toàn bộ chỉ số `x1.6` |
| `wither` | `enderman` | `5,999` | `30,000` | `30` | `18` | `11h` | `300,000` | Toàn bộ chỉ số `x1.75` |
| `warden` | `wither` | `8,999` | `50,000` | `35` | `21` | `12h` | `400,000` | Toàn bộ chỉ số `x1.85` |
| `turtlegod` | `warden` | `12,999` | `80,000` | `40` | `25` | `14h` | `600,000` | Toàn bộ `x2.0` |

## 🧰 Quyền Lệnh Nổi Bật Theo Rank

| Rank mở được | Lệnh/quyền lợi menu ghi |
|---|---|
| `bee` | `/suicide` |
| `frog` | `/hat`, `/suicide` |
| `rabbit` | `/workbench`, `/fix hand` |
| `fox` | `/sell hand`, thêm player warp |
| `wolf` | `/anvil` |
| `boar` | `/ec`, nhiều player warp |
| `panda` | `/msgtoggle` |
| `tiger` | `/rtoggle`, `/back`, `/ec` |
| `slime` | `/tptoggle`, `/condense`, `/rtoggle` |
| `spider` | `/sellall`, `/top`, `/feed`, `/tptoggle`, `/suicide` |
| `blaze` | `/chatcolor`, `/heal` |
| `enderman` | `/fix all`, `/nick`, `/realname` |
| `wither` | `/fly`, `/tpa` no cooldown |
| `warden` | `/nick` màu, `/invsee`, nametag đẹp |
| `turtlegod` | `/fly`, `/nick` full color, `/invsee`, `/fix all`, `/condense`, nametag RGB, bỏ chờ lệnh |

## 🔧 Repair Liên Quan Rank

📁 Config: /plugins/zMenu/inventories/REPAIR.yml

| Tính năng | Điều kiện thường | Điều kiện rank/quyền |
|---|---|---|
| Sửa 1 item | Trả `50$`, chạy `repair` | Có `essentials.repair`, menu ghi Rank `Rabbit`, dùng miễn phí |
| Sửa tất cả | Trả `1,000$`, chạy `repair all` | Có `essentials.repair.all`, menu ghi Rank `Ender`, dùng miễn phí |

## 💡 Nên Mua Rank Nào?

| Mục tiêu | Rank đáng chú ý | Lý do |
|---|---|---|
| Newbie muốn tiện ích rẻ | `bee`/`frog` | Claim, home, `/pv`, AFK, booster nhẹ |
| Người farm nhiều | `fox` đến `wolf` | `/sell hand`, sell booster, Mythic/Mobcoins bonus |
| Người cần repair tiện | `rabbit` và `enderman` | `/fix hand`, sau đó `/fix all` |
| Builder/base lớn | `panda` trở lên | Nhiều claim, homes, `/pv` |
| End-game tối ưu toàn bộ | `wither` đến `turtlegod` | `/fly`, toàn bộ booster cao, nhiều tiện ích |

Xem thêm: [README.md](README.md), [spending-guide.md](spending-guide.md), [../Shops/shop-prices.md](../Shops/shop-prices.md)
