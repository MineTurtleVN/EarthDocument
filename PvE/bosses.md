# 🐲 Boss Và Cơ Chế Dungeon

Plugin chính: `TurtleDungeon`

📁 Config: /plugins/TurtleDungeon/config.yml
📁 Config: /plugins/TurtleDungeon/bossbar.yml

Boss trong dungeon có cơ chế giữ vùng và tự kiểm tra trạng thái.

| Cơ chế | Config | Ý nghĩa |
|---|---|---|
| Kéo boss về | `boss-teleport-radius: 30` | Boss đi quá 30 block khỏi điểm chuẩn sẽ bị đưa về |
| Kiểm tra boss mất | `boss-check-interval: 5` | Mỗi 5 giây kiểm tra boss bị despawn/unload |
| Reconcile mob | `mob-reconcile-interval: 5` | Đồng bộ số mob còn sống |
| Dọn/đếm mob | `mob-kill-radius: 200` | Bán kính xử lý mob quanh dungeon |

Gợi ý: đừng kéo boss ra khỏi khu vực đánh, vì cơ chế radius có thể làm mất nhịp combat hoặc reset vị trí.
