# 🧩 GUI Tổng Quan

Plugin chính: `zMenu`, `ExcellentShop`, `ExcellentCrates`, `TurtleLevel`

📁 Config: /plugins/zMenu/inventories/
📁 Config: /plugins/zMenu/inventories/MENU.yml
📁 Config: /plugins/zMenu/inventories/WARPS.yml
📁 Config: /plugins/zMenu/inventories/RTP.yml
📁 Config: /plugins/zMenu/inventories/RANK.yml
📁 Config: /plugins/zMenu/inventories/CSHOP.yml
📁 Config: /plugins/zMenu/inventories/DONATE/DONATE.yml
📁 Config: /plugins/ExcellentShop/virtual_shop/main.menu.yml
📁 Config: /plugins/ExcellentShop/virtual_shop/settings.yml
📁 Config: /plugins/TurtleLevel/gui.yml

GUI của Earth không chỉ là menu trang trí. Đây là lớp điều hướng chính nối người chơi tới world, dungeon, donate, rank, shop, repair, màu chat, kit, hướng dẫn và các hệ thống phần thưởng. Người mới nên nhớ 4 lệnh trước: `/menu`, `/warps`, `/rtp`, `/shop`.

## 🧭 Menu Quan Trọng

| GUI | Lệnh/cách mở | Mục đích | Config |
|---|---|---|---|
| Menu chính | `/menu` | Hồ sơ người chơi, tiền, Xu, máu, kill/death, link tới hệ thống khác | `MENU.yml` |
| Khu vực | `/warps` | Chọn khu vực, player warp, các điểm đến lớn | `WARPS.yml` |
| Random teleport | `/rtp` | Bay ngẫu nhiên tới `trái đất`; menu ghi thời gian `2 phút` | `RTP.yml` |
| Hướng dẫn | từ menu | Danh sách lệnh cơ bản cho người mới | `HUONGDAN.yml` |
| Cửa hàng cấp bậc | `/rank` | Mua rank bằng Xu, xem quyền lợi | `RANK.yml` |
| Xu Shop | từ menu/shop | Mua vật phẩm đặc biệt bằng `%playerpoints_points%` | `CSHOP.yml` |
| Donate | `/donate` | Bảng nạp, mốc nạp, chuỗi nạp | `DONATE/DONATE.yml` |
| Virtual Shop | `/shop` hoặc `/vshop` | Mua/bán vật phẩm bằng Vault money | `ExcellentShop/virtual_shop/*.yml` |
| Level Rùa | menu TurtleLevel | Xem cấp Rùa, claim reward, Premium reward | `TurtleLevel/gui.yml` |

## 🧑‍💻 Placeholder Người Chơi Thấy

| Placeholder | Hiển thị trong GUI | Ý nghĩa |
|---|---|---|
| `%player_name%` | Menu chính | Tên người chơi |
| `%player_first_played_formatted%` | Menu chính | Ngày vào server lần đầu |
| `%vault_eco_balance_formatted%` | Menu chính | Tiền Vault |
| `%playerpoints_points%` | Menu chính, Xu Shop | Xu donate/PlayerPoints |
| `%statistic_player_kills%` | Menu chính | Số kill vanilla/statistic |
| `%statistic_deaths%` | Menu chính | Số lần chết |
| `%turtlelevel_level%` | TurtleLevel GUI | Cấp Độ Rùa hiện tại |
| `%turtlelevel_is_premium%` | TurtleLevel GUI | Trạng thái Premium reward |
| `%turtlelevel_stats%` | TurtleLevel GUI | Chỉ số cộng thêm từ cấp Rùa |

## 📚 Tài Liệu Chi Tiết

| File | Nội dung |
|---|---|
| [deluxemenus.md](deluxemenus.md) | Bản đồ zMenu: menu nào mở menu nào, slot/chức năng chính |
| [shop-guis.md](shop-guis.md) | GUI shop: `/shop`, `/sellgui`, Xu Shop, claim shop, rank shop |
| [system-guis.md](system-guis.md) | GUI hệ thống: `/menu`, `/warps`, `/rtp`, `/donate`, `/kit`, `/suachua`, chat color |

Xem thêm: [../Shops/README.md](../Shops/README.md), [../Donate/README.md](../Donate/README.md), [../Gameplay/getting-started.md](../Gameplay/getting-started.md)
