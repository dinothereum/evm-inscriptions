## ⚠️⚠️⚠️ Disclaimer ⚠️⚠️⚠️

Tất cả các thao tác đều thực hiện và chạy dưới local, chú ý quản lý private key wallet.

## 1. Yêu cầu cần có

### Cài đặt NodeJS

Vui lòng truy cập [https://nodejs.org/en/download](https://nodejs.org/en/download) và làm theo hướng dẫn cài đặt.

download bản cho windown về cài đặt như phầm mềm bình thường

### Cài đặt git bash

Do windown ko hỗ chợ chạy file `.sh` nên cần cài thêm https://gitforwindows.org/

download bản cho windown về cài đặt như phầm mềm bình thường

## 2. Download code về (join Discord tạo ticket để nhận code: https://discord.gg/z4rXJdcstq)

## 3. Cấu hình môi trường

Tạo file `.env` với key như file `.env.example` như sau:

```
PROVIDER_URL= <đăng ký account và lấy endpoitn trên https://app.infura.io/dashboard>

PRIVATE_KEY= <địa chỉ ví thực hiện ký giao dịch>

RECIEPT_ADDRESS= <địa chỉ nhận inscription, có thể giống địa chỉ ký giao dịch>

RANGE_INDEX= <danh sách ID muốn mint, phân tách nhau bởi dấu phẩy>

DATA= <là format json của token muốn mint, chú ý id thay bằng "xxxxxx">
ví dụ: data:,{"p":"erc-20","op":"mint","tick":"gwei","id":"xxxxxx","amt":"1000"}
```

### 4. Run

```
node index.js
```
### 5. Note

Script này chạy được cho tất cả các network EVM khác nhau như ERC20, BEP20, Polygon, Celo ...
