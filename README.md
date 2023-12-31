## ⚠️⚠️⚠️ Disclaimer ⚠️⚠️⚠️

Tất cả các thao tác đều thực hiện và chạy dưới local, chú ý quản lý private key wallet.

## 1. Yêu cầu cần có

### Cài đặt NodeJS

Vui lòng truy cập [https://nodejs.org/en/download](https://nodejs.org/en/download) và làm theo hướng dẫn cài đặt.

download bản cho windown về cài đặt như phầm mềm bình thường

## 2. Download code về

Join Discord tạo ticket để nhận source code từ admin: https://discord.gg/z4rXJdcstq

## 3. Cấu hình môi trường

Tạo file `.env` với key như file `.env.example` như sau:

```
PROVIDER_URL= <đăng ký account và lấy endpoint trên https://app.infura.io/dashboard>

PRIVATE_KEY= <địa chỉ private_key của ví thực hiện ký giao dịch>

RECIEPT_ADDRESS= <địa chỉ public address của ví nhận inscription, có thể giống địa chỉ public của ví ký giao dịch>

RANGE_INDEX= <danh sách ID muốn mint, phân tách nhau bởi dấu phẩy>

DATA= <là format json của token muốn mint, chú ý id thay bằng "xxxxxx">
```

Ví dụ:

```
PROVIDER_URL=https://bsc-dataseed.binance.org
PRIVATE_KEY=xxxyyyzzz
RECIEPT_ADDRESS=0x123456
RANGE_INDEX=1011,1234,5678
DATA=data:,{"p":"erc-20","op":"mint","tick":"gwei","id":"xxxxxx","amt":"1000"}
```

## 4. Run

Run command

```
node index.js
```

### Ubuntu & MacOS
Mở cửa sổ Terminal và `cd` đến đường dẫn thư mục và run command trên

### Window
Mở Window PowerShell và `cd` đến đường dẫn thư mục và run command trên.
Nếu bị lỗi k fix được thì cài đặt WSL2 (giả lập môi trường Ubuntu trên Window) để chạy code.

## 5. Note

Script này chạy được cho tất cả các network EVM khác nhau như ERC20, BEP20, Polygon, Celo ... chỉ cần thay đổi `PROVIDER_URL` tương ứng với network là oke.
