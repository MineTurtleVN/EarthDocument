# 🛍️ Shop Người Chơi, Player Warp Và Đấu Giá

Plugin chính: `AxPlayerWarps`, `zAuctionHouseV3`, `ExcellentShop`, `AxTrade`

📁 Config: /plugins/AxPlayerWarps/config.yml  
📁 Config: /plugins/zAuctionHouseV3/config.yml  
📁 Config: /plugins/ExcellentShop/config.yml  
📁 Config: /plugins/ExcellentShop/virtual_shop/settings.yml

Shop người chơi trên Earth có 3 lớp: player warp để dẫn khách đến khu bán hàng, Auction House để rao bán item trực tiếp, và trade trực tiếp nếu hai người đã thỏa thuận.

## 🏪 Player Warp Là Gì?

📁 Config: /plugins/AxPlayerWarps/config.yml

Player warp là điểm dịch chuyển do người chơi tạo. Vì config có category `shop`, đây là kênh phù hợp để mở cửa hàng, khu bán đồ, máy farm public hoặc khu trưng bày.

| Thiết lập | Giá trị |
|---|---|
| Lệnh mở | `/pwarp`, `/pwarps`, `/pw`, `/playerwarp`, `/playerwarps` |
| GUI mặc định | `categories` |
| Category shop | `shop` → `CỬA HÀNG` |
| Phí tạo warp | `10,000` Vault money |
| Cần xác nhận phí | Có, `confirm: true` |
| Delay teleport | `3` giây |
| Di chuyển khi chờ teleport | Hủy dịch chuyển |
| Check vị trí không an toàn | Bật |
| Tên warp | `1-16` ký tự, không có dấu cách |
| Ký tự được phép | Chữ, số và `!@#$%^&*()_-` |
| Mô tả | Tối đa `3` dòng |

## 📂 Category Player Warp

| Category | Tên hiển thị | Người bán nên dùng khi |
|---|---|---|
| `shop` | `CỬA HÀNG` | Bán item, mở shop chest/NPC/khu trade |
| `farm` | `MÁY FARM` | Cho người khác dùng farm hoặc xem máy farm |
| `building` | `CÔNG TRÌNH` | Khoe build, có thể dẫn vào shop trang trí |
| `event` | `SỰ KIỆN` | Khu event do người chơi tổ chức |
| `special` | `ĐẶC BIỆT` | Khu hiếm, dịch vụ đặc biệt |
| `other` | `KHU KHÁC` | Không khớp category nào |

Sorting trong GUI hỗ trợ `A > Z`, `Z > A`, nhiều/ít lượt thăm, đánh giá cao/thấp, nhiều/ít đánh giá, nhiều/ít lượt thích, gần/xa nhất, mới/cũ nhất.

## 🧺 Auction House `/ah`

📁 Config: /plugins/zAuctionHouseV3/config.yml

Auction House dùng `VAULT` làm kinh tế mặc định và phù hợp để bán item lẻ mà không cần dựng shop.

| Lệnh | Công dụng | Permission ghi trong config |
|---|---|---|
| `/ah` | Mở chợ | `zauctionhouse.use` |
| `/ah sell <price> [amount]` | Bán item đang cầm | `zauctionhouse.sell` |
| `/ah sellinventory <price>` | Bán inventory | `zauctionhouse.sell.inventory` |
| `/ah history [page] [type]` | Xem lịch sử mua/bán | `zauctionhouse.history` |
| `/ah transaction <player>` | Xem giao dịch người chơi | `zauctionhouse.transaction` |
| `/ah search <string>` | Tìm item | `zauctionhouse.search` |

## 💸 Luật Giá Và Thuế AH

| Mục | Giá trị |
|---|---|
| Kinh tế | `VAULT` |
| Giá tối thiểu | `10` |
| Giá tối đa | `999999999999999999` |
| Hiển thị giá đẹp | Bật `betterPrice: true`, dùng khoảng trắng |
| Rút gọn `500k` khi bán | Tắt `enableNumberFormatSell: false` |
| Thuế toàn cục | Bật |
| Thuế áp dụng khi | `SELL` |
| Phần trăm thuế | `2.0%` |
| Quyền bypass thuế | `zauctionhouse.bypass.tax` |
| Cooldown bán | `10` giây |
| Cooldown lệnh | `5` giây |
| Cooldown giao dịch | `30` giây |

## ⏳ Thời Gian Và Giới Hạn AH

| Mục | Giá trị |
|---|---:|
| Tin bán hết hạn | `172800s` = 2 ngày |
| Item mua/hết hạn bị xóa | `604800s` = 7 ngày |
| Transaction bị xóa | `604800s` = 7 ngày |
| Auto save | `6000s` |
| TPS thấp chặn dùng AH | Dưới `16` TPS |
| Ping cao chặn dùng AH | Trên `600ms` |

Giới hạn số item bán theo permission:

| Permission | Limit |
|---|---:|
| `zauctionhouse.max.2` | `2` |
| `zauctionhouse.max.3` | `3` |
| `zauctionhouse.max.4` | `4` |
| `zauctionhouse.max.5` | `5` |
| `zauctionhouse.max.7` | `7` |
| `zauctionhouse.max.10` | `10` |

## 🧾 Khi Nào Dùng `/ah`, Khi Nào Dùng `/pwarp`?

| Tình huống | Nên dùng |
|---|---|
| Bán 1 món hiếm, muốn người khác tìm thấy ngay | `/ah sell <price>` |
| Bán nhiều loại hàng lâu dài | `/pwarp` category `shop` |
| Muốn xây thương hiệu shop riêng | `/pwarp`, đặt mô tả rõ ràng |
| Muốn bán nhanh vật phẩm vanilla/farm | `/sellgui`, `/sellall` từ ExcellentShop |
| Muốn trao đổi trực tiếp với người quen | Trade trực tiếp hoặc hẹn tại warp |

## ✅ Mẹo Cho Người Mua

| Mẹo | Lý do |
|---|---|
| So giá `/ah` trước khi mua Xu Shop | Có thể người chơi bán rẻ hơn |
| Kiểm tra tier và type trước khi mua gear | Sao cao không luôn đúng build |
| Cẩn thận item gần hết hạn trong AH | Item hết hạn sẽ rời khỏi danh sách bán |
| Ưu tiên shop có nhiều lượt thăm/đánh giá | AxPlayerWarps có sorting theo visits/rating |
| Khi teleport player warp, đừng di chuyển 3 giây | Di chuyển sẽ hủy teleport |

## ✅ Mẹo Cho Người Bán

| Mẹo | Lý do |
|---|---|
| Đặt tên warp ngắn, dễ nhớ, không dấu cách | Config không cho dấu cách và giới hạn 16 ký tự |
| Dùng category `CỬA HÀNG` | Người mua lọc shop dễ hơn |
| Ghi mô tả tối đa 3 dòng rõ mặt hàng | Config hỗ trợ `max-lines: 3` |
| Tính thêm thuế AH `2%` khi định giá | Thuế áp dụng lúc bán |
| Không spam lệnh bán | Có cooldown bán/lệnh |

Xem thêm: [shop-locations.md](shop-locations.md), [shop-prices.md](shop-prices.md), [../Items/mmoitems.md](../Items/mmoitems.md)
