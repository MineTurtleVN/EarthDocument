# 🎮 Gameplay Tổng Quan

Plugin chính: `TurtleLevel`, `TurtleDungeon`, `MMOItems`, `ExcellentShop`, `zMenu`, `PlayerPoints`

📁 Config: /plugins/TurtleLevel/gui.yml
📁 Config: /plugins/TurtleDungeon/config.yml
📁 Config: /plugins/TurtleDungeon/Dungeons/
📁 Config: /plugins/ExcellentShop/config.yml
📁 Config: /plugins/ExcellentShop/virtual_shop/settings.yml
📁 Config: /plugins/zMenu/inventories/HUONGDAN.yml
📁 Config: /plugins/zMenu/inventories/RANK.yml

Gameplay của Earth đi theo vòng: vào `Lobby`, dùng `/menu` để định hướng, `/rtp` tới `earth` để farm/build, bán đồ qua `/shop` hoặc `/sellgui`, tăng Cấp Độ Rùa qua kỹ năng, build trang bị MMOItems, đi dungeon D1-D5, rồi tham gia KOTH/PvP hoặc tối ưu donate/rank nếu muốn tăng tốc.

## 🧭 Vòng Lặp Chơi Chính

| Giai đoạn | Việc làm | Lệnh/menu | Lý do |
|---|---|---|---|
| 0-10 phút | Mở hướng dẫn, xem tiền/Xu, chọn nơi farm | `/menu`, `/warps`, `/rtp` | Biết server có gì và tránh lạc |
| 10-30 phút | Farm `earth`, bán đồ cơ bản | `/rtp`, `/shop`, `/sellgui` | Lấy tiền đầu tiên |
| Early-game | Mua claim/homes/rank rẻ, chuẩn bị đồ ăn/vật phẩm | `/claimshop`, `/rank`, `/shop` | Xây base và giảm thời gian di chuyển |
| Mid-game | Đi D1-D3, farm nguyên liệu dungeon, nâng gear | menu dungeon, PvE docs | Mở khóa nguyên liệu nâng cấp thật sự |
| Late-game | D4-D5, bản PvP dungeon, KOTH `Địa Bàn` | dungeon PvP, event `12:00/20:00` | Loot cao, cạnh tranh top |
| End-game | Tối ưu MMOItems, gem, key hiếm, top sự kiện | `/rank`, `/donate`, crate, KOTH | Hoàn thiện build và mục tiêu cạnh tranh |

## 🐢 Cấp Độ Rùa

📁 Config: /plugins/TurtleLevel/gui.yml

TurtleLevel GUI ghi rõ cách tính: hệ thống không cộng tổng level của mọi nghề rồi chia 5. Mỗi nhánh kỹ năng được tính độc lập, cứ đạt `5 cấp` của một kỹ năng riêng biệt thì tăng `+1 Cấp Độ Rùa`. Ví dụ Đào khoáng cấp `7` được `+1`, Câu cá cấp `13` được `+2`, tổng là Cấp Rùa `3`; phần dư được giữ lại cho mốc sau.

| Thành phần | Ý nghĩa |
|---|---|
| `/skill` | Lệnh được GUI hướng dẫn để cày kỹ năng như đào khoáng, chặt cây, phiêu lưu |
| `%turtlelevel_level%` | Cấp Độ Rùa hiện tại |
| `%turtlelevel_stats%` | Chỉ số cộng thêm từ cấp |
| Claim all | Nút nhận tất cả phần thưởng cấp đã đạt |
| Premium reward | Phần thưởng thêm nếu mua gói Premium trong GUI |

## 💰 Tiền Tệ Người Chơi Gặp Sớm

| Tiền tệ | Nguồn chính | Dùng cho |
|---|---|---|
| Vault money | Bán đồ qua `/shop`, farm, reward | Mua shop thường, sửa đồ, claim shop |
| Xu/PlayerPoints | Donate, reward đặc biệt | `/rank`, Xu Shop, vật phẩm đặc biệt |
| Bạc `⛀` | Mốc nạp | Quà mốc/đặc biệt theo donate docs |
| Key | Crate, mốc nạp, dungeon/KOTH | Mở crate như Dungeon, Spawner, Thiên Mệnh, AFK |
| Nguyên liệu MMOItems | Dungeon, mob drops, crate | Cường hóa, rèn, tiến hóa, craft |

## 📚 Tài Liệu Chi Tiết

| File | Nội dung |
|---|---|
| [getting-started.md](getting-started.md) | Việc cần làm trong 10-30 phút đầu |
| [progression.md](progression.md) | Lộ trình newbie đến end-game |
| [levels-ranks-rebirth.md](levels-ranks-rebirth.md) | TurtleLevel, rank, Premium reward |
| [economy-currencies.md](economy-currencies.md) | Tiền tệ, shop, bán đồ, Xu |
| [crafting-upgrades.md](crafting-upgrades.md) | Nâng cấp trang bị, MMOItems, crate nguyên liệu |

Xem thêm: [../PvE/README.md](../PvE/README.md), [../Shops/README.md](../Shops/README.md), [../Donate/README.md](../Donate/README.md), [../Worlds/README.md](../Worlds/README.md)
