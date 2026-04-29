# ⚙️ GUI Hệ Thống

Plugin chính: `zMenu`, `TurtleLevel`, `TurtleDungeon`, `ExcellentShop`

📁 Config: /plugins/zMenu/inventories/MENU.yml
📁 Config: /plugins/zMenu/inventories/WARPS.yml
📁 Config: /plugins/zMenu/inventories/RTP.yml
📁 Config: /plugins/zMenu/inventories/HUONGDAN.yml
📁 Config: /plugins/zMenu/inventories/REPAIR.yml
📁 Config: /plugins/zMenu/inventories/CLAIM.yml
📁 Config: /plugins/zMenu/inventories/DONATE/DONATE.yml
📁 Config: /plugins/TurtleLevel/gui.yml

Trang này gom các GUI không thuần shop nhưng người chơi dùng mỗi ngày.

## 🧭 Menu Điều Hướng

| GUI | Lệnh/cách mở | Slot/nút đáng chú ý | Hành động |
|---|---|---|---|
| `MENU.yml` | `/menu` | Player info | Hiển thị tên, ngày vào server, tiền, Xu, máu, kill/death |
| `WARPS.yml` | `/warps` | `Player Warp` slot `28` | Chạy `/pwarp` |
| `WARPS.yml` | `/warps` | `Warp Trade` slot `11` | Chạy `/warp trade` |
| `WARPS.yml` | `/warps` | `Warp Crate` slot `13` | Chạy `/warp crates` |
| `WARPS.yml` | `/warps` | `Warp Afk` slot `14` | Chạy `/warp afk` |
| `WARPS.yml` | `/warps` | `Warp Top` slot `15` | Chạy `/warp top` |
| `WARPS.yml` | `/warps` | `Warp PvP` slot `16` | Chạy `/warp pvp` |
| `RTP.yml` | `/rtp` | Trái đất | Dịch chuyển ngẫu nhiên, menu ghi `2 phút` |

## 📖 Hướng Dẫn Trong Game

📁 Config: /plugins/zMenu/inventories/HUONGDAN.yml

| Nhóm | Lệnh trong menu | Công dụng |
|---|---|---|
| Di chuyển | `/spawn`, `/rtp`, `/tpa`, `/tpaccept`, `/tpadeny`, `/ewarp` | Về hub, random teleport, teleport người chơi/cứ điểm |
| Điều hướng | `/menu`, `/shop`, `/warp trade`, `/map` | Mở menu, shop, khu trade, bản đồ Earth |
| Chat/giao dịch | `/trade`, `/msg`, `/r`, `/pay`, `/money` | Giao dịch, chat riêng, chuyển tiền, xem ví |
| Bang hội | `/banghoi create`, `/banghoi invite`, `/banghoi accept` | Tạo/mời/tham gia bang hội |
| Tiện ích | `/suachua`, `/rank`, `/kit`, `/skill`, `/claimblock`, `/quest`, `/tags` | Repair, rank, kit, skill, claim, nhiệm vụ, biệt danh |
| PvP/cứ điểm | `/thanhchien cudiem` | Xem danh sách cứ điểm |
| Enchant | `/ce` | Mua sách XP/enchant theo menu |

## 🔧 Repair GUI

📁 Config: /plugins/zMenu/inventories/REPAIR.yml

| Nút | Giá/điều kiện | Lệnh chạy | Ghi chú |
|---|---|---|---|
| Sửa 1 vật phẩm | `50$` | `runasop %player% repair` | Sửa item đang cầm |
| Sửa tất cả | `1,000$` | `runasop %player% repair all` | Sửa item trong túi |
| Sửa 1 miễn phí | permission `essentials.repair`, menu ghi Rank `Rabbit` | `/repair hand` | Không trừ tiền |
| Sửa tất cả miễn phí | permission `essentials.repair.all`, menu ghi Rank `Ender` | `/repair all` | Không trừ tiền |

## 🐢 TurtleLevel GUI

📁 Config: /plugins/TurtleLevel/gui.yml

| Nút | Chức năng |
|---|---|
| Player info slot `4` | Xem cấp hiện tại, Premium status, stats cộng thêm |
| Claim all | Nhận toàn bộ reward cấp đã đạt |
| Guide item | Giải thích cách tính Cấp Độ Rùa theo từng nhánh kỹ năng, mỗi 5 cấp kỹ năng = +1 cấp Rùa |
| Confirm Premium | Xác nhận mua gói Premium bằng Xu, hiển thị `%cost% Xu` |

## 🎨 Trang Trí Và Màu Viền

Nhiều GUI dùng placeholder `%ledatapi_color_material%`, `%ledatapi_color_skull%`, `%ledatapi_color_name%` và nút `changecolor nextcolor`. Đây là nút đổi màu viền GUI, không phải nâng cấp sức mạnh.

Xem thêm: [README.md](README.md), [shop-guis.md](shop-guis.md), [../Gameplay/getting-started.md](../Gameplay/getting-started.md)
