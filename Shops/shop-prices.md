# 💵 Giá Và Cách Giao Dịch

Plugin chính: `ExcellentShop`, `zMenu`, `PlayerPoints`

📁 Config: /plugins/ExcellentShop/config.yml → GUI.Click_Types
📁 Config: /plugins/ExcellentShop/virtual_shop/settings.yml
📁 Config: /plugins/ExcellentShop/virtual_shop/shops/
📁 Config: /plugins/zMenu/inventories/CSHOP.yml
📁 Config: /plugins/zMenu/inventories/CLAIM.yml

Shop thường của Earth dùng `Vault` money, còn Xu Shop dùng `%playerpoints_points%`. Trước khi mua số lượng lớn, hãy phân biệt rõ tiền đang dùng vì `/shop` và Xu Shop là hai hệ kinh tế khác nhau.

## 🖱️ Click Trong ExcellentShop

| Click | Hành động config | Người chơi nên dùng khi nào |
|---|---|---|
| Left | `BUY_SELECTION` | Mua có chọn số lượng |
| Right | `SELL_SELECTION` | Bán có chọn số lượng |
| Shift Left | `BUY_SINGLE` | Mua nhanh 1 lần |
| Shift Right | `SELL_SINGLE` | Bán nhanh 1 lần |
| Swap Offhand | `SELL_ALL` | Xả toàn bộ item hợp lệ |

## 🧺 Danh Mục `/shop`

| Danh mục | Tập trung vào | Gợi ý |
|---|---|---|
| `building_blocks` | Khối xây nhà | Mua khi xây base, không nên mua sớm quá nhiều |
| `colored_blocks` | Khối màu | Chủ yếu trang trí |
| `decoration` | Decor | Dành cho builder |
| `farming` | Cây trồng/nông sản | Nên kiểm tra giá bán nếu farm tiền |
| `food` | Đồ ăn | Hữu ích cho newbie/dungeon |
| `minerals` | Khoáng sản | Dùng craft/nâng cấp, giá có thể biến động |
| `miscellaneous` | Vật phẩm linh tinh | Kiểm tra mục đích trước khi mua |
| `mob_drops` | Drop mob | Có thể dùng trade/craft/bán |

## 🛒 Giá Xu Shop Đã Xác Nhận

| Vật phẩm | Giá | Lệnh thưởng | Nên mua khi nào |
|---|---:|---|---|
| Đục Ngọc ngẫu nhiên `GEM_REMOVER` | `14 Xu` | `mi give CONSUMABLE GEM_REMOVER` | Khi cần gỡ 1 ngọc ngẫu nhiên khỏi gear |
| Chìa Spawner | `14 Xu` | `crates key give spawner 1` | Khi cần thử vận may spawner |
| Chìa Dungeon | `19 Xu` | `crates key give dungeon 1` | Tốt cho người đang farm PvE/dungeon |
| Chìa Thiên Mệnh | `29 Xu` | `crates key give trangbingaunhien 1` | Mở gear/random hiếm, có bảo hiểm 80 lượt |
| Chìa Thiên Mệnh x10 | `261 Xu` | `crates key give trangbingaunhien 10` | Combo giảm 10% so với mua lẻ |
| Chìa Nguyên Liệu | `5 Xu` | `crates key give nguyenlieu 1` | Rẻ, phù hợp cần nguyên liệu |
| Lửa Thanh Tẩy | `20 Xu` | `ae giveitem blackscroll 1 100` | Gỡ enchant ngẫu nhiên, tỉ lệ 100% |
| Gậy Thần Tài | `299 Xu` | `tools give sellwandvip` | End-game/farm chest, +100% khi bán bằng gậy theo lore |
| Hòm Ngọc Bậc II | `24 Xu` | `boxreward give gemchest-2 1` | Gem level 4-6 |
| Hòm Ngọc Bậc III | `89 Xu` | `boxreward give gemchest-3 1` | Gem level 7-9 |
| Hòm Ngọc Bậc IV | `179 Xu` | `boxreward give gemchest-4 1` | Gem level 10-12 |
| Mảnh Vỡ Chiêm Tinh | `9 Xu` | `ae giveitem magic 1` | Tăng tỉ lệ thành công sách ma thuật `+1 -> +10%` |
| Hòm Cường Hóa VII | `12 Xu` | `av give EnchantmentRandom-7 1` | Tỉ lệ thành công `95-100%`, rủi ro `0-2%` |

## 🧱 Claim Shop

| Gói | Giá | Claim nhận | Giá trung bình |
|---|---:|---:|---:|
| Claim I | `20K` | `10` | `2,000`/claim |
| Claim II | `50K` | `30` | `1,667`/claim |
| Claim III | `100K` | `50` | `2,000`/claim |
| Claim IV | `100K` | `100` | `1,000`/claim |
| Claim V | `400K` | `150` | `2,667`/claim |
| Claim VI | `550K` | `210` | `2,619`/claim |
| Claim VII | `750K` | `260` | `2,885`/claim |

Gợi ý: nếu chỉ nhìn giá/claim, `Claim IV` là mốc hiệu quả nhất trong config đã đọc. Tuy nhiên người chơi nên mua theo nhu cầu base, không cần gom claim nếu chưa xây lớn.

Xem thêm: [README.md](README.md), [../Donate/spending-guide.md](../Donate/spending-guide.md), [../Items/rewards-crates.md](../Items/rewards-crates.md)
