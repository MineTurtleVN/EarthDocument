# 🎁 Rewards Và Crates

Plugin chính: `ExcellentCrates`

📁 Config: /plugins/ExcellentCrates/config.yml
📁 Config: /plugins/ExcellentCrates/crates/
📁 Config: /plugins/ExcellentCrates/keys/

Crate đang có:

| Crate | Config | Gợi ý dùng |
|---|---|---|
| AFK | `crates/afk.yml` | Thưởng thụ động |
| Dungeons | `crates/dungeons.yml` | Farm PvE/dungeon |
| KOTH `Địa Bàn` | `crates/koth.yml` | Preview phần thưởng KOTH/PvP; thưởng thật khi thắng lấy từ `AxKoth/koths/Hero.yml` |

## 👑 Crate Preview KOTH `Địa Bàn`

Plugin chính: `ExcellentCrates`, `AxKoth`

📁 Config: /plugins/ExcellentCrates/crates/koth.yml
📁 Config: /plugins/AxKoth/koths/Hero.yml → `reward-commands`

Crate `Địa Bàn` dùng để người chơi xem phần thưởng KOTH. Block preview đặt tại `Lobby, -56, 46, -9`. Phần thưởng thực tế khi chiếm KOTH thành công được chạy bởi AxKoth, gồm `50,000` tiền, `20` Xu, `3` Hòm Ngọc Bậc II, `3` Sách Phù Phép Ngẫu Nhiên và `+1` điểm top Địa Bàn.

| Reward preview | Tên hiển thị | Rarity | Ghi chú |
|---|---|---|---|
| `tien_50k` | `+50,000⛀ Tiền` | `common` | Khớp thưởng thật `eco give %player% 50000` |
| `xu_20` | `+20⛃ Xu` | `common` | Khớp thưởng thật `points give %player% 20` |
| `key_trangbi` | `Chìa Khóa Thiên Mệnh x1` | `rare` | Hiện trong preview, nhưng lệnh key trong AxKoth đang bị comment |
| `gemchest_2` | `Hòm Ngọc Bậc II x3` | `epic` | Khớp thưởng thật `av give %player% GemChest-2 3` |
| `enchant_random` | `Sách Phù Phép Ngẫu Nhiên x3` | `epic` | Khớp thưởng thật `av give %player% EnchantmentRandom-3 3` |
| La Chong | `crates/lachong.yml` | Nội dung sự kiện/vật phẩm đặc biệt |
| Nguyen Lieu | `crates/nguyenlieu.yml` | Nâng cấp/crafting |
| Spawner | `crates/spawner.yml` | Farm mob/spawner |
| Trang bi ngau nhien | `crates/trangbingaunhien.yml` | Roll trang bị |

Rarity trong ExcellentCrates: common, rare, epic, legendary, mythic với weight giảm dần.
