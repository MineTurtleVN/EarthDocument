# 🛡️ PvP Tổng Quan

Plugin chính: `PvPManager`, `AxKoth`, `TurtleTop`, `zMenu`, `TurtleDungeon`, `ThanhChien`

📁 Config: /plugins/PvPManager/config.yml
📁 Config: /plugins/AxKoth/
📁 Config: /plugins/TurtleTop/points.yml
📁 Config: /plugins/zMenu/inventories/EVENT.yml
📁 Config: /plugins/zMenu/inventories/DUATOP.yml

PvP đang bật mặc định. Dungeon có vùng PvP riêng, server có KOTH/event và combat-tag để chống thoát giao tranh.

Điểm quan trọng nhất hiện tại là KOTH `Địa Bàn`: mở hằng ngày lúc `12:00` và `20:00` theo giờ Việt Nam, đặt tại world `Lobby` quanh tọa độ `X -42, Y 47, Z -9`, yêu cầu giữ vùng `60 giây`, thời lượng tối đa `15 phút 30 giây`, thưởng trực tiếp `50,000` tiền, `20` Xu, `3` Hòm Ngọc Bậc II, `3` sách phù phép và `+1` điểm top Địa Bàn.

Top Địa Bàn có tracking bằng TurtleTop qua lệnh `tt add %player% diaban 1`. Người chơi xem top bằng `/duatop` hoặc menu top Địa Bàn. Cấu hình reset/trao thưởng tự động trong `points.yml` đang để `Reset.Enable: false`, nên top vẫn hiển thị/cộng điểm nhưng auto tổng kết cần admin xác nhận hoặc bật lại.

| File | Nội dung |
|---|---|
| [maps-events.md](maps-events.md) | Map/event/KOTH/PvP dungeon, lịch, tọa độ, top và thưởng chi tiết |
| [pvp-settings.md](pvp-settings.md) | Combat tag và hạn chế khi giao tranh |
| [kits-rewards.md](kits-rewards.md) | Kit, thưởng KOTH, top Địa Bàn, top Thánh Chiến |
