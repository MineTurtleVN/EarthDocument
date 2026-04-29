# 📋 zMenu Inventories

Plugin chính: `zMenu`

📁 Config: /plugins/zMenu/inventories/

Tên file này giữ lại vì cấu trúc docs ban đầu gọi là `deluxemenus.md`, nhưng plugin menu thực tế đang dùng là `zMenu`. Các inventory quan trọng đã đọc hoặc tham chiếu:

| File/folder | Mục đích | Trạng thái audit |
|---|---|
| `MENU.yml` | Menu chính `/menu`, hồ sơ người chơi, tiền/Xu, điều hướng | Đã đọc |
| `HUONGDAN.yml` | Hướng dẫn lệnh, farm, tài nguyên, mạng xã hội | Đã đọc |
| `WARPS.yml` | Menu `/warps`, player warp, trade, crates, afk, top, pvp | Đã đọc |
| `RTP.yml` | Random teleport tới trái đất | Đã đọc |
| `DUNGEONS.yml` | Menu dungeon tổng, stage vô hạn, boss mỗi 5 stage, PvP x2.5 | Đã đọc |
| `DUNGEON_D1.yml` đến `DUNGEON_D5.yml` | Menu từng dungeon, yêu cầu cấp, boss, độ khó | Đã đọc |
| `KIT.yml` | Kit rank | Đã đọc một phần, nhiều mục comment |
| `RANK.yml` | Cửa hàng rank bằng Xu | Đã đọc |
| `CSHOP.yml` | Xu Shop: key, booster, gem, consumable | Đã đọc |
| `CLAIM.yml` | Claim shop bằng Vault money | Đã đọc |
| `REPAIR.yml` | Sửa đồ bằng tiền hoặc quyền rank | Đã đọc |
| `CHATCOLOR.yml` | Màu chat | Đã đọc metadata/màu |
| `EVENT.yml` | Event hub, KOTH/Top liên quan | Đã đọc trong pass PvP |
| `DUATOP.yml` | Top Địa Bàn/Thánh Chiến placeholder | Đã đọc trong pass PvP |
| `DONATE/DONATE.yml` | Donate menu, bảng nạp, hướng dẫn nạp | Đã đọc |
| `DONATE/MOCNAP.yml` | Mốc nạp trang 1 | Đã đọc |
| `DONATE/MOCNAP2.yml` | Mốc nạp trang 2 | Đã đọc |
| `DONATE/CHUOINAP.yml` | Chuỗi nạp | Đã đọc |

## 🔗 Luồng Menu Chính

| Người chơi muốn | Menu/lệnh nên dùng | Đi tiếp tới |
|---|---|---|
| Không biết làm gì | `/menu` | `HUONGDAN.yml`, `WARPS.yml`, shop, donate |
| Đi farm | `/rtp` hoặc `/warps` | `earth`, `/warp trade`, `/warp afk` |
| Mua/bán | `/shop`, Xu Shop | ExcellentShop, `CSHOP.yml` |
| Nâng rank | `/rank` | `RANK.yml` |
| Nạp và nhận mốc | `/donate`, `/mocnap` | `DONATE/` |
| Đi dungeon | Menu dungeon | `DUNGEONS.yml`, `DUNGEON_D*.yml` |
| Xem top/event | `/warp top`, event menu | `DUATOP.yml`, `EVENT.yml` |

Xem thêm: [system-guis.md](system-guis.md), [shop-guis.md](shop-guis.md), [../Plugins/placeholders.md](../Plugins/placeholders.md)
