# viettien117.github.io

Trang web của bộ công cụ chấm bài trắc nghiệm **RuBi**.

| Đường dẫn | Nội dung |
|---|---|
| `index.html` | Trang chủ — giới thiệu 4 app và nút tải. **Đây là trang Play Console và App Store trỏ tới**, nên không được để trống. |
| `examscan/index.html` | Trang tải chi tiết, có mã QR cho từng nền tảng. |
| `app-ads.txt` | Khai báo người bán quảng cáo được uỷ quyền (ironSource / Unity LevelPlay). |

## Hai chỗ phải sửa cùng nhau

Mô tả từng app (`mixer_body`, `insight_body`, `sheet_body`, các khoá `*_sub`
và nhãn nút) có mặt ở **cả `index.html` lẫn `examscan/index.html`**, nguyên văn
giống nhau, đủ 5 ngôn ngữ `vi / en / pt / es / id`. Sửa một bên mà quên bên kia
thì hai trang sẽ nói khác nhau về cùng một app.

Hai trang dùng chung khoá `localStorage` tên `examscan-lang`, nên người dùng
chọn ngôn ngữ ở trang chủ thì sang trang tải vẫn giữ nguyên.

## app-ads.txt

Danh sách reseller **thỉnh thoảng được Unity cập nhật**. Mỗi lần Unity gửi mail
nhắc thì lấy lại bản mới tại
<https://docs.unity.com/en-us/grow/programmatic/ironsource-exchange/app-ads-txt>.

Ô "Trang web" trên Play Console (và Marketing URL trên App Store) quyết định file
này có được đọc hay không: trình thu thập lấy phần tên miền rồi tìm
`<tên miền>/app-ads.txt`. Hiện là `https://viettien117.github.io` — đúng.
