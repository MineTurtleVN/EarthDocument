# ⌨️ Commands Và Permissions

Plugin chính: `ExcellentShop`, `zMenu`, `LuckPerms`, `TurtleDungeon`, `AxKoth`

📁 Config: /plugins/ExcellentShop/config.yml
📁 Config: /plugins/ExcellentShop/virtual_shop/settings.yml
📁 Config: /plugins/zMenu/inventories/
📁 Config: /plugins/zMenu/inventories/HUONGDAN.yml
📁 Config: /plugins/zMenu/inventories/RANK.yml
📁 Config: /plugins/zMenu/inventories/REPAIR.yml

## 🧭 Lệnh Người Chơi Cơ Bản

| Lệnh/Menu | Nguồn | Ghi chú |
|---|---|---|
| `/spawn` | `HUONGDAN.yml` | Về đại sảnh |
| `/menu` | `MENU.yml`, `HUONGDAN.yml` | Mở tiện ích chính |
| `/rtp` | `RTP.yml`, `HUONGDAN.yml` | Random teleport tới khu farm |
| `/warps` | `WARPS.yml` | Mở khu vực/warp |
| `/pwarp` | `WARPS.yml` | Xem khu người chơi tự tạo |
| `/shop`, `/vshop` | ExcellentShop | Mở shop ảo |
| `/sellgui`, `/sellmenu`, `/sellg` | ExcellentShop | GUI bán đồ kéo thả |
| `/sellall` | ExcellentShop | Bán tất cả item hợp lệ |
| `/sellhand`, `/sellhandall` | ExcellentShop | Bán item đang cầm/cùng loại |
| `/trade` | `HUONGDAN.yml` | Giao dịch với người chơi gần |
| `/msg`, `/r` | `HUONGDAN.yml` | Chat riêng/trả lời |
| `/pay`, `/money` | `HUONGDAN.yml` | Chuyển tiền/xem tiền |
| `/skill` | `HUONGDAN.yml`, `TurtleLevel/gui.yml` | Mở kỹ năng, dùng để tăng Cấp Độ Rùa |
| `/rank` | `RANK.yml` | Mở cửa hàng cấp bậc |
| `/kit` | `KIT.yml` | Mở kit rank |
| `/suachua` | `REPAIR.yml` | Sửa đồ bằng tiền/quyền rank |
| `/claimblock`, `/claimshop` | `HUONGDAN.yml`, `CLAIM.yml` | Mua block claim |
| `/donate`, `/napthe` | `DONATE/DONATE.yml` | Donate/nạp thẻ |
| `/quest` | `HUONGDAN.yml` | Mở nhiệm vụ |
| `/tags` | `HUONGDAN.yml` | Mở biệt danh |
| `/ce` | `HUONGDAN.yml` | Mua sách XP/enchant |
| `/map` | `HUONGDAN.yml` | Lấy link bản đồ Trái Đất |

## 🏰 Bang Hội Và Cứ Điểm

| Lệnh | Nguồn | Ghi chú |
|---|---|---|
| `/banghoi create` | `HUONGDAN.yml` | Tạo bang hội |
| `/banghoi invite` | `HUONGDAN.yml` | Mời người chơi vào bang |
| `/banghoi accept` | `HUONGDAN.yml` | Đồng ý lời mời |
| `/ewarp` | `HUONGDAN.yml` | Dịch chuyển tới cứ điểm |
| `/thanhchien cudiem` | `HUONGDAN.yml` | Xem danh sách cứ điểm |

## 👑 Lệnh Theo Rank

| Rank | Lệnh/quyền lợi được menu ghi |
|---|---|
| `bee` | `/suicide` |
| `frog` | `/hat`, `/suicide` |
| `rabbit` | `/workbench`, `/fix hand`, repair miễn phí nếu có `essentials.repair` |
| `fox` | `/sell hand` |
| `wolf` | `/anvil` |
| `boar` | `/ec` |
| `panda` | `/msgtoggle` |
| `tiger` | `/rtoggle`, `/back`, `/ec` |
| `slime` | `/tptoggle`, `/condense`, `/rtoggle` |
| `spider` | `/sellall`, `/top`, `/feed`, `/tptoggle`, `/suicide` |
| `blaze` | `/chatcolor`, `/heal` |
| `enderman` | `/fix all`, `/nick`, `/realname`, repair all miễn phí nếu có `essentials.repair.all` |
| `wither` | `/fly`, `/tpa` no cooldown |
| `warden` | `/nick` màu, `/invsee` |
| `turtlegod` | `/fly`, `/nick` full color, `/invsee`, `/fix all`, `/condense`, bỏ chờ lệnh |

## 🔐 Permission Đã Thấy Trực Tiếp

| Permission placeholder | Nguồn | Ý nghĩa |
|---|---|---|
| `%luckperms_has_permission_essentials.repair%` | `REPAIR.yml` | Cho phép sửa item đang cầm miễn phí |
| `%luckperms_has_permission_essentials.repair.all%` | `REPAIR.yml` | Cho phép sửa tất cả miễn phí |
| `excellentshop.virtual.sellmultiplier.[name]` | `ExcellentShop/virtual_shop/settings.yml` | Pattern permission nếu Sell_Multipliers dùng permission mode; hiện config đang `Mode: RANK` |

Ghi chú: tài liệu này không liệt kê permission node cụ thể nếu chưa đọc storage LuckPerms để tránh đoán sai.

Xem thêm: [placeholders.md](placeholders.md), [plugin-mapping.md](plugin-mapping.md), [../Donate/ranks-vip.md](../Donate/ranks-vip.md)
