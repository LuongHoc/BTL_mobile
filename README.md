# Họ và tên: Lương Văn Học - MSSV: K225480106025
# Lớp: K58KTP
# MÔN HỌC: PHÁT TRIỂN ỨNG DỤNG TRÊN THIẾT BỊ DI ĐỘNG - TEE0419

BÀI TẬP LỚN:
1. Viết phần mềm trên công cụ Mit App inventor
   (tập trung vào quy trình tạo ra phần mềm)
   app có 3 screen:
   + about về bản thân+nút gọi sang 2 screen còn lại
   + giải 1 bài toán đơn giản
   + sử dụng webview: hiển thị 1 trang web có sẵn, hỗ trợ giao diện điện thoại
   mô tả: thanh công cụ có gì? kéo thả + thay đổi thuộc tính: làm ntn, để làm gì?
          block: mô tả bản chất việc kéo thả block ntn?
                 ưu điểm gì so với viết code? nhược điểm?
                 copy paste block ? (backpack)

BÀI LÀM


## 1. Bài toán cần giải quyết

Ứng dụng hỗ trợ sinh viên tính tổng chi phí thuê phòng trọ trong một tháng và xác định số tiền mỗi người cần đóng.

## 2. Tạo dự án

Truy cập MIT App Inventor, đăng nhập và chọn: ```New project```

Đặt tên dự án: ```TinhTienPhongTro```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/999b79da-cb2b-40ed-9af5-111316fd8d9f" />

Sau khi tạo dự án, bạn sẽ thấy hai khu vực chính:

- Designer:	Kéo thả và thiết kế giao diện
- Blocks:	Ghép các khối lệnh để xử lý sự kiện và dữ liệu

## 3. Tạo đủ 3 Screen

Giữ nguyên màn hình mặc định:
```
Screen1
```
Bấm: Add Screen...

Tạo thêm:
```
ScreenTinhTienTro
ScreenWeb
```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/3a4880a4-9095-43d8-a041-95a9e2fb150b" />


## 4. Làm Screen1: Giới thiệu bản thân

Chọn Screen1, sau đó kéo các thành phần từ Palette vào Viewer.

### 4.1. Thiết kế giao diện

| STT | Thành phần | Tên thành phần | Chức năng |
|---:|---|---|---|
| 1 | VerticalArrangement | `arrMain` | Chứa và sắp xếp các thành phần theo chiều dọc |
| 2 | Label | `lblTieuDe` | Hiển thị tên ứng dụng |
| 3 | Label | `lblMoTa` | Mô tả ngắn chức năng của ứng dụng |
| 4 | Label | `lblKhoangTrong1` | Tạo khoảng cách giữa các khu vực |
| 5 | Label | `lblKhoangTrong2` | Tạo khoảng cách giữa các khu vực |
| 6 | Label | `lblHoTen` | Hiển thị họ và tên sinh viên |
| 7 | Label | `lblMaSV` | Hiển thị mã sinh viên |
| 8 | Label | `lblLop` | Hiển thị lớp |
| 9 | Button | `btnTinhTienTro` | Mở màn hình tính tiền phòng trọ |
| 10 | Button | `btnMoWeb` | Mở màn hình hiển thị trang web |

#### Cấu hình Screen1

| Thuộc tính | Giá trị |
|---|---|
| `Title` | `Giới thiệu` |
| `AlignHorizontal` | `Center` |
| `AlignVertical` | `Top` |
| `Scrollable` | Bật |
| `Sizing` | `Responsive` |

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/908be2e3-f57d-4b63-a8d7-dc335882e3ac" />

#### Cấu hình arrMain

| Thuộc tính | Giá trị |
|---|---|
| `Width` | `Fill parent` |
| `Height` | `Automatic` |
| `AlignHorizontal` | `Center` |
| `AlignVertical` | `Top` |

### 4.2. Tạo Block chuyển Screen

Chuyển sang tab: ```Blocks```

B1: Kéo Block sự kiện của nút tính tiền

Ở cột bên trái, chọn:
```
btnTinhTienTro
```

Chọn Block  ở trên cùng:

```
when btnTinhTienTro.Click
do
```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/f180b710-d508-431c-a28d-883dae24df7c" />

B2: Kéo Block mở Screen khác

Chọn: ```Control```

Tìm Block:

```
open another screen screenName
```
<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/22532ed0-1d78-414d-8424-f00b1a5f6728" />

Giữ chuột kéo Block này vào bên trong vùng ```do``` của: ```when btnTinhTienTro.Click```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/ae8629f1-d7f8-4b09-b7e9-81bebce6a344" />

B3: Nhập tên Screen cần mở

Ở danh sách bên trái, chọn:

```
Text
```
Kéo Block chuỗi văn bản rỗng có dạng:

""
<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/979c4102-e0c9-4ddc-b43f-33da1987c967" />

Gắn vào vị trí trống bên phải của:
```
open another screen screenName
```
Bấm vào phần văn bản bên trong Block và nhập:
```
ScreenTinhTienTro
```
Kết quả hoàn chỉnh:

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/547bfa00-8577-44da-9e34-b6d562a101ee" />

B4: Làm tương tự cho nút mở website

Ở cột bên trái, chọn:
```
btnMoWeb
```
Kéo Block:
```
when btnMoWeb.Click
do
```
sang vùng làm việc.

Sau đó kéo từ nhóm Control:
```
open another screen screenName
```
Tiếp tục kéo Block chữ từ nhóm Text và nhập:
```
ScreenWeb
```
Kết quả:

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/b7dee591-490d-4620-a1b2-e01b8352e4ea" />

## 5. Làm ScreenTinhTienTro: Tính và chia tiền phòng trọ

### 5.1. Thiết kế giao diện

Tạo một Screen mới và đặt tên:

```text
ScreenTinhTienTro
```

Trong phần `Properties` của Screen, cấu hình:

```text
Title: Tính tiền phòng trọ
Scrollable: true
```

Kéo một `VerticalArrangement` vào Viewer để chứa và sắp xếp các thành phần theo chiều dọc.

| STT | Thành phần          | Tên thành phần     | Chức năng                                      |
| --: | ------------------- | ------------------ | ---------------------------------------------- |
|   1 | VerticalArrangement | `arrTinhTien`      | Chứa và sắp xếp các thành phần theo chiều dọc  |
|   2 | Label               | `lblTieuDe`        | Hiển thị tiêu đề `TÍNH VÀ CHIA TIỀN PHÒNG TRỌ` |
|   3 | TextBox             | `txtTienPhong`     | Nhập tiền thuê phòng                           |
|   4 | TextBox             | `txtDienCu`        | Nhập chỉ số điện cũ                            |
|   5 | TextBox             | `txtDienMoi`       | Nhập chỉ số điện mới                           |
|   6 | TextBox             | `txtGiaDien`       | Nhập giá điện trên mỗi kWh                     |
|   7 | TextBox             | `txtNuocCu`        | Nhập chỉ số nước cũ                            |
|   8 | TextBox             | `txtNuocMoi`       | Nhập chỉ số nước mới                           |
|   9 | TextBox             | `txtGiaNuoc`       | Nhập giá nước trên mỗi m³                      |
|  10 | TextBox             | `txtTienMang`      | Nhập tiền mạng                                 |
|  11 | TextBox             | `txtDichVu`        | Nhập tiền dịch vụ                              |
|  12 | TextBox             | `txtSoNguoi`       | Nhập số người ở                                |
|  13 | Button              | `btnTinhTien`      | Thực hiện tính tiền phòng trọ                  |
|  14 | Label               | `lblKetQua`        | Hiển thị kết quả sau khi tính                  |
|  15 | Button              | `btnNhapLai`       | Xóa dữ liệu đã nhập                            |
|  16 | Button              | `btnQuayLai`       | Quay lại màn hình trước                        |
|  17 | Notifier            | `notifierThongBao` | Hiển thị cảnh báo khi dữ liệu không hợp lệ     |

Cấu hình cho `arrTinhTien`:

| Thuộc tính        | Giá trị       |
| ----------------- | ------------- |
| `Width`           | `Fill parent` |
| `Height`          | `Automatic`   |
| `AlignHorizontal` | `Center`      |
| `AlignVertical`   | `Top`         |

Đối với tất cả các `TextBox`, cấu hình:

| Thuộc tính    | Giá trị                          |
| ------------- | -------------------------------- |
| `Width`       | `Fill parent`                    |
| `NumbersOnly` | `true`                           |
| `Text`        | Để trống                         |
| `Hint`        | Nhập nội dung phù hợp với từng ô |

Kết quả giao diện:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1cbf4539-af24-4490-a675-278e08088651" />


### 5.2. Công thức tính tiền phòng trọ

Ứng dụng tính chi phí theo các công thức:

```text
Số điện tiêu thụ = Chỉ số điện mới - Chỉ số điện cũ

Tiền điện = Số điện tiêu thụ × Giá điện

Số nước tiêu thụ = Chỉ số nước mới - Chỉ số nước cũ

Tiền nước = Số nước tiêu thụ × Giá nước

Tổng tiền = Tiền phòng + Tiền điện + Tiền nước + Tiền mạng + Tiền dịch vụ

Tiền mỗi người = Tổng tiền / Số người ở
```

---

### 5.3. Tạo các biến trong Blocks

#### 5.3.1. Tạo biến soDien

Giữ chuột vào Block:
```
initialize global name to
```
kéo sang vùng trắng bên phải.

Sau đó bấm trực tiếp vào chữ:
```
name
```
và đổi thành:
```
soDien
```
<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/fbe25252-3d45-403d-bb7a-9738a578111c" />

Bên phải Block vẫn còn một ô trống.

#### 5.3.2. Gắn giá trị ban đầu bằng 0

Ở danh sách bên trái, chọn:
```
Math
```
Kéo Block số:
```
0
```
gắn vào ô trống bên phải.

Kết quả:

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/e0001e2e-edab-4657-b268-eab34f07b7d0" />

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/b6e24ded-5f63-4042-8704-d833b0b9e9dc" />

tạo các biến còn lại như vậy:

| STT | Tên biến       | Chức năng                      |
| --: | -------------- | ------------------------------ |
|   1 | `soDien`       | Lưu số điện đã sử dụng         |
|   2 | `tienDien`     | Lưu tiền điện                  |
|   3 | `soNuoc`       | Lưu số nước đã sử dụng         |
|   4 | `tienNuoc`     | Lưu tiền nước                  |
|   5 | `tongTien`     | Lưu tổng chi phí               |
|   6 | `tienMoiNguoi` | Lưu số tiền mỗi người cần đóng |

Khởi tạo ban đầu:

```text
initialize global soDien to 0
initialize global tienDien to 0
initialize global soNuoc to 0
initialize global tienNuoc to 0
initialize global tongTien to 0
initialize global tienMoiNguoi to 0
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/27c19773-68f9-44a4-83f5-ff86f6e9b4df" />

### 5.4. Tạo Block cho nút TÍNH TIỀN

Chọn thành phần:

```text
btnTinhTien
```

Kéo Block:

```text
when btnTinhTien.Click
do
```
<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/c1b0fae3-71ab-44ec-8ce8-1728065f9be9" />

Bước 1: Thêm khối điều kiện

Ở cột bên trái, chọn:

Built-in → Control

Kéo Block:

if then

vào bên trong:

when btnTinhTien.Click
do

Bấm biểu tượng bánh răng màu xanh trên Block if, sau đó kéo thêm:
```
else if
else if
else if
else
```
<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/0cbb1829-e5fb-4473-b2cc-1b7d79cdc103" />


Bước 2: Kiểm tra các ô nhập bị bỏ trống
2.1. Lấy Block so sánh

Chọn:

Built-in → Logic

Kéo Block:

=


2.2. Lấy nội dung của TextBox

Ở danh sách thành phần bên trái, bấm:

txtTienPhong

Kéo Block:

txtTienPhong.Text

gắn vào bên trái Block =.

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/75e4ac8b-cc17-45f9-abf9-be998aeee8df" />

Chọn:

Built-in → Text

Kéo Block văn bản rỗng:

""

gắn vào bên phải.

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/ad5b3871-828c-4bbf-a2fc-9cbd04591e83" />

2.3. Ghép nhiều điều kiện bằng or

Trong:

Built-in → Logic

kéo Block:

or

Bạn cần kiểm tra lần lượt 10 ô:

txtTienPhong.Text = ""
txtDienCu.Text = ""
txtDienMoi.Text = ""
txtGiaDien.Text = ""
txtNuocCu.Text = ""
txtNuocMoi.Text = ""
txtGiaNuoc.Text = ""
txtTienMang.Text = ""
txtDichVu.Text = ""
txtSoNguoi.Text = ""

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5dec968d-bdba-4504-a46c-60a02c6e9353" />

Ghép các Block or lồng vào nhau:

or
├── txtTienPhong.Text = ""
└── or
    ├── txtDienCu.Text = ""
    └── or
        ├── txtDienMoi.Text = ""
        └── ...

Sau đó gắn toàn bộ cụm này vào điều kiện if đầu tiên.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/eb89220b-74dc-40d0-90f4-2bd4ab1a6f93" />

Bước 3: Hiển thị thông báo khi thiếu dữ liệu

Ở danh sách thành phần bên trái, chọn:

notifierThongBao

Kéo Block:

call notifierThongBao.ShowAlert
    notice

gắn vào phần then của điều kiện đầu tiên.
<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/ebc3ec19-62ec-449c-8088-b3b1292f17b5" />

Từ nhóm Text, kéo Block văn bản và nhập:

Vui lòng nhập đầy đủ thông tin

Kết quả:

if có ô nhập bị bỏ trống
then
    call notifierThongBao.ShowAlert
        notice "Vui lòng nhập đầy đủ thông tin"
Bước 4: Kiểm tra chỉ số điện

Tại else if thứ nhất, dùng Block < trong nhóm:

Built-in → Math

Ghép:

txtDienMoi.Text < txtDienCu.Text

Trong phần then, thêm thông báo:

call notifierThongBao.ShowAlert
    notice "Chỉ số điện mới phải lớn hơn hoặc bằng chỉ số điện cũ"

Kết quả:

else if txtDienMoi.Text < txtDienCu.Text
then
    thông báo lỗi chỉ số điện
Bước 5: Kiểm tra chỉ số nước

Tại else if thứ hai, ghép:

txtNuocMoi.Text < txtNuocCu.Text

Trong phần then, thêm:

call notifierThongBao.ShowAlert
    notice "Chỉ số nước mới phải lớn hơn hoặc bằng chỉ số nước cũ"
Bước 6: Kiểm tra số người ở

Tại else if thứ ba, dùng Block:

≤

trong nhóm Math.

Ghép:

txtSoNguoi.Text ≤ 0

Số 0 lấy từ:

Built-in → Math

Trong phần then, thêm:

call notifierThongBao.ShowAlert
    notice "Số người ở phải lớn hơn 0"
Bước 7: Tính số điện tiêu thụ

Trong nhánh else cuối cùng, chọn:

Built-in → Variables

Kéo Block:

set global soDien to

Từ nhóm Math, kéo Block phép trừ:

-

Ghép:

set global soDien to
    txtDienMoi.Text - txtDienCu.Text
Bước 8: Tính tiền điện

Kéo:

set global tienDien to

Dùng Block phép nhân:

×

Ghép:

set global tienDien to
    get global soDien × txtGiaDien.Text

Block:

get global soDien

lấy từ:

Built-in → Variables

Sau khi kéo Block get, bấm mũi tên để chọn tên biến soDien.

Bước 9: Tính số nước tiêu thụ

Ghép:

set global soNuoc to
    txtNuocMoi.Text - txtNuocCu.Text
Bước 10: Tính tiền nước

Ghép:

set global tienNuoc to
    get global soNuoc × txtGiaNuoc.Text
Bước 11: Tính tổng tiền

Kéo:

set global tongTien to

Trong nhóm Math, kéo Block cộng. Bấm biểu tượng bánh răng màu xanh để thêm đủ 5 vị trí.

Ghép:

set global tongTien to
    txtTienPhong.Text
    + get global tienDien
    + get global tienNuoc
    + txtTienMang.Text
    + txtDichVu.Text
Bước 12: Tính số tiền mỗi người

Ghép:

set global tienMoiNguoi to
    get global tongTien / txtSoNguoi.Text
Bước 13: Hiển thị kết quả

Ở danh sách thành phần bên trái, chọn:

lblKetQua

Kéo:

set lblKetQua.Text to

Trong:

Built-in → Text

kéo Block:

join

Bấm bánh răng màu xanh của Block join để thêm nhiều vị trí.

Ghép nội dung:

set lblKetQua.Text to join
    "Số điện tiêu thụ: "
    get global soDien
    " kWh
Tiền điện: "
    get global tienDien
    " đồng
Số nước tiêu thụ: "
    get global soNuoc
    " m³
Tiền nước: "
    get global tienNuoc
    " đồng
Tổng tiền: "
    get global tongTien
    " đồng
Mỗi người cần đóng: "
    get global tienMoiNguoi
    " đồng"

Trong các Block văn bản, bạn có thể nhấn Enter để xuống dòng.













Trước khi tính, kiểm tra dữ liệu nhập:

| STT | Điều kiện kiểm tra                     | Thông báo                        |
| --: | -------------------------------------- | -------------------------------- |
|   1 | Có ô nhập bị bỏ trống                  | `Vui lòng nhập đầy đủ thông tin` |
|   2 | Chỉ số điện mới nhỏ hơn chỉ số điện cũ | `Chỉ số điện không hợp lệ`       |
|   3 | Chỉ số nước mới nhỏ hơn chỉ số nước cũ | `Chỉ số nước không hợp lệ`       |
|   4 | Số người ở nhỏ hơn hoặc bằng `0`       | `Số người ở phải lớn hơn 0`      |

Sơ đồ xử lý:

```text
when btnTinhTien.Click
do
    nếu có ô nhập bị bỏ trống
        hiển thị cảnh báo

    nếu chỉ số điện mới < chỉ số điện cũ
        hiển thị cảnh báo

    nếu chỉ số nước mới < chỉ số nước cũ
        hiển thị cảnh báo

    nếu số người ở <= 0
        hiển thị cảnh báo

    ngược lại
        tính số điện
        tính tiền điện
        tính số nước
        tính tiền nước
        tính tổng tiền
        tính tiền mỗi người
        hiển thị kết quả
```

Các phép tính trong Block:

```text
set global soDien to
    txtDienMoi.Text - txtDienCu.Text

set global tienDien to
    global soDien × txtGiaDien.Text

set global soNuoc to
    txtNuocMoi.Text - txtNuocCu.Text

set global tienNuoc to
    global soNuoc × txtGiaNuoc.Text

set global tongTien to
    txtTienPhong.Text
    + global tienDien
    + global tienNuoc
    + txtTienMang.Text
    + txtDichVu.Text

set global tienMoiNguoi to
    global tongTien / txtSoNguoi.Text
```

Hiển thị kết quả tại `lblKetQua`:

```text
Số điện tiêu thụ
Tiền điện
Số nước tiêu thụ
Tiền nước
Tổng tiền
Tiền mỗi người cần đóng
```

---

### 5.5. Tạo Block cho nút NHẬP LẠI

Chọn:

```text
btnNhapLai
```

Kéo Block:

```text
when btnNhapLai.Click
do
```

Xóa nội dung các TextBox và đặt lại nội dung kết quả:

```text
set txtTienPhong.Text to ""
set txtDienCu.Text to ""
set txtDienMoi.Text to ""
set txtGiaDien.Text to ""
set txtNuocCu.Text to ""
set txtNuocMoi.Text to ""
set txtGiaNuoc.Text to ""
set txtTienMang.Text to ""
set txtDichVu.Text to ""
set txtSoNguoi.Text to ""

set lblKetQua.Text to "Kết quả sẽ hiển thị tại đây"
```

---

### 5.6. Tạo Block cho nút QUAY LẠI

Chọn:

```text
btnQuayLai
```

Kéo Block:

```text
when btnQuayLai.Click
do
    close screen
```

Block `close screen` giúp đóng `ScreenTinhTienTro` và quay lại `Screen1`.

---

### 5.7. Hình ảnh Blocks

Sau khi hoàn thành, chụp ảnh các Blocks và chèn vào README:

```md
![Blocks xử lý ScreenTinhTienTro](images/screen-tinh-tien-tro-blocks.png)
```




















     
