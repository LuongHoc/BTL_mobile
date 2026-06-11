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

Tính chỉ số BMI

## 2. Tạo dự án

Truy cập MIT App Inventor, đăng nhập và chọn: ```New project```

Đặt tên dự án: ```BMI_Calculator```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/86272e42-9fdb-452b-aac7-87e0bd48e4b6" />

Sau khi tạo dự án, bạn sẽ thấy hai khu vực chính:

- Designer:	Kéo thả và thiết kế giao diện
- Blocks:	Ghép các khối lệnh để xử lý sự kiện và dữ liệu

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/8519bad8-532d-4b84-ad4f-516965022c42" />

## 2. Làm Screen1: Màn hình giới thiệu

Screen1 là màn hình xuất hiện khi mở ứng dụng. Màn hình này giới thiệu sinh viên thực hiện và có hai nút chuyển sang hai Screen còn lại.

### 2.1. Thiết kế giao diện

Trong giao diện Designer, bấm chọn Screen1, sau đó chỉnh các thuộc tính:

- Title:	Ứng dụng tính chỉ số BMI
- AlignHorizontal:	Center
- AlignVertical:	Center
- Scrollable:	Chọn

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/c2386779-aa77-45a2-af15-595267df9b8c" />

Mở nhóm: Palette → Layout

Kéo một thành phần:
```
VerticalArrangement
```
vào màn hình.

Đổi tên: VerticalArrangement1 → VA_Main

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/58619c8f-371a-47f4-affe-2709828d8822" />

Chỉnh thuộc tính:

- Width:	Fill parent
- Height:	Automatic
- AlignHorizontal:	Center

Tiếp theo, mở:

Palette → User Interface

Kéo các thành phần vào trong VA_Main theo đúng thứ tự:

| Thành phần | Đổi tên | Nội dung hoặc thiết lập |
|------------|----------|-------------------------|
| Label | lblTieuDe | ỨNG DỤNG TÍNH CHỈ SỐ BMI |
| Label | lblMoTa | Ứng dụng hỗ trợ tính BMI dựa trên cân nặng và chiều cao. |
| Label | lblSinhVien | Họ tên, mã sinh viên và lớp của bạn |
| Button | btnTinhBMI | TÍNH CHỈ SỐ BMI |
| Button | btnWebView | XEM THÔNG TIN THAM KHẢO |

Định dạng thêm:

| Thành phần | Thuộc tính nên chỉnh |
|------------|----------------------|
| lblTieuDe | FontBold = true, FontSize = 22, TextAlignment = Center |
| lblMoTa | FontSize = 16, Width = Fill parent, TextAlignment = Center |
| lblSinhVien | FontSize = 15, Width = Fill parent, TextAlignment = Center |
| Hai nút | Width = 250 pixels, FontBold = true |

Sau khi hoàn thành:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9ab5918e-eb4d-4225-b0f9-e8a7c7209850" />

### 2.2. Tạo thêm hai Screen

Trên thanh công cụ, chọn:
```
Add Screen...
```
Tạo lần lượt:
```
ScreenTinhBMI
ScreenWebView
```
<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/471def01-db35-4304-95d4-548e78e0b5e4" />

### 2.3. Tạo Blocks chuyển màn hình

Chuyển từ tab:

Designer → Blocks
Nút mở màn hình tính BMI

Trong danh sách Blocks bên trái, chọn:
```
btnTinhBMI
```
Kéo Block:
```
when btnTinhBMI.Click
do
```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/3f944940-8d6d-4cb6-9bfe-a99f7e56c379" />


Mở nhóm:

Control

Kéo Block:
```
open another screen screenName
```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/a1cce6bf-370c-465f-90fc-6c496a2f7c47" />

Mở nhóm:

Text

Kéo Block chuỗi văn bản ```""```, gắn vào screenName và nhập:

ScreenTinhBMI

Kết quả:
<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/41a0edd3-81ea-460a-952d-1e2443d8217d" />

Nút mở màn hình WebView

Làm tương tự với btnWebView:

```
when btnWebView.Click
    open another screen screenName "ScreenWebView"
```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b87f0e66-6ba4-4c41-b08e-e5e578e336a4" />

## 3. Làm ScreenTinhBMI: Màn hình tính BMI

Chuyển sang:

ScreenTinhBMI
### 3.1. Thiết kế giao diện

Chọn ScreenTinhBMI, chỉnh:

| Thuộc tính | Giá trị |
|------------|----------|
| Title | Tính chỉ số BMI |
| AlignHorizontal | Center |
| Scrollable | Chọn |

Kéo một VerticalArrangement vào màn hình và đổi tên:

VerticalArrangement1 → VA_Main

Chỉnh:

Width = Fill parent
AlignHorizontal = Center

Kéo các thành phần sau vào trong VA_Main:

| Thành phần | Đổi tên         | Nội dung hoặc thiết lập               |
| ---------- | --------------- | ------------------------------------- |
| Label      | lblTieuDe       | TÍNH CHỈ SỐ BMI                       |
| Label      | lblNhapCanNang  | Nhập cân nặng (kg):                   |
| TextBox    | txtCanNang      | Hint = Ví dụ: 60, NumbersOnly = true  |
| Label      | lblNhapChieuCao | Nhập chiều cao (m):                   |
| TextBox    | txtChieuCao     | Hint = Ví dụ: 1.7, NumbersOnly = true |
| Button     | btnTinh         | TÍNH BMI                              |
| Button     | btnLamMoi       | LÀM MỚI                               |
| Label      | lblKetQua       | Để trống                              |
| Label      | lblDanhGia      | Để trống                              |
| Button     | btnQuayLai      | QUAY LẠI                              |
| Notifier   | Notifier1       | Thành phần ẩn dùng để hiện thông báo  |


Cây thành phần:

ScreenTinhBMI
└── VA_Main
    ├── lblTieuDe
    ├── lblNhapCanNang
    ├── txtCanNang
    ├── lblNhapChieuCao
    ├── txtChieuCao
    ├── btnTinh
    ├── btnLamMoi
    ├── lblKetQua
    ├── lblDanhGia
    └── btnQuayLai

Non-visible components
└── Notifier1

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c8c7013c-4cbe-4f96-a22c-bf34f2457c83" />

### 3.2. Tạo biến lưu BMI

Chuyển sang tab:

Blocks

Mở nhóm:
```
Variables
```
Kéo Block:
```
initialize global name to
```
Đổi tên biến thành:
```
bmi
```
<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/9817c5f8-96d5-405d-ae98-3a7ff66d615a" />

Mở nhóm:

Math

Gắn giá trị:

0

Kết quả:

initialize global bmi to 0

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/5238b65c-d4d6-4d3d-b557-d7c22d820c94" />

### 3.3. Tạo Block cho nút TÍNH BMI

Chọn:
```
btnTinh
```
Kéo:
```
when btnTinh.Click
do
```
Cần xử lý theo ba bước:

- Bước 1: Kiểm tra người dùng đã nhập đủ dữ liệu chưa
- Bước 2: Kiểm tra giá trị có lớn hơn 0 không
- Bước 3: Tính BMI và đưa ra kết luận

**Điều kiện 1: Không được để trống**

Tạo điều kiện:

txtCanNang.Text = ""
or
txtChieuCao.Text = ""

Nếu đúng, gọi:

```
call Notifier1.ShowAlert
    notice "Vui lòng nhập đầy đủ cân nặng và chiều cao"
```
**Điều kiện 2: Giá trị phải lớn hơn 0**

Tạo điều kiện:
```
txtCanNang.Text <= 0
or
txtChieuCao.Text <= 0
```
Nếu đúng, gọi:
```
call Notifier1.ShowAlert
    notice "Cân nặng và chiều cao phải lớn hơn 0"
```
**Tính BMI**

Nếu dữ liệu hợp lệ:
```
set global bmi to
    txtCanNang.Text /
    (txtChieuCao.Text × txtChieuCao.Text)
```
Hiển thị kết quả:
```
set lblKetQua.Text to
    join "Chỉ số BMI của bạn: " global bmi
```
**Đánh giá kết quả**

Ghép thêm một Block if then else if:
```
if global bmi < 18.5
    set lblDanhGia.Text to "Kết luận: Thiếu cân"

else if global bmi < 25
    set lblDanhGia.Text to "Kết luận: Cân nặng hợp lý"

else if global bmi < 30
    set lblDanhGia.Text to "Kết luận: Thừa cân"

else
    set lblDanhGia.Text to "Kết luận: Béo phì"
```
Sơ đồ logic hoàn chỉnh:
```
when btnTinh.Click
    if txtCanNang.Text = "" or txtChieuCao.Text = ""
        thông báo "Vui lòng nhập đầy đủ cân nặng và chiều cao"

    else if txtCanNang.Text <= 0 or txtChieuCao.Text <= 0
        thông báo "Cân nặng và chiều cao phải lớn hơn 0"

    else
        set global bmi to
            txtCanNang.Text /
            (txtChieuCao.Text × txtChieuCao.Text)

        set lblKetQua.Text to
            join "Chỉ số BMI của bạn: " global bmi

        if global bmi < 18.5
            set lblDanhGia.Text to "Kết luận: Thiếu cân"
        else if global bmi < 25
            set lblDanhGia.Text to "Kết luận: Cân nặng hợp lý"
        else if global bmi < 30
            set lblDanhGia.Text to "Kết luận: Thừa cân"
        else
            set lblDanhGia.Text to "Kết luận: Béo phì"
```
<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/7f398cd5-2771-426b-9376-e366072c64d9" />

Các nhóm Blocks cần sử dụng

| Nhóm        | Block cần lấy                             |
| ----------- | ----------------------------------------- |
| Control     | if then else, close screen                |
| Logic       | or, =                                     |
| Math        | 0, /, ×, <, <=                            |
| Text        | Chuỗi văn bản "", join                    |
| Variables   | initialize global, set global, get global |
| txtCanNang  | txtCanNang.Text                           |
| txtChieuCao | txtChieuCao.Text                          |
| lblKetQua   | set lblKetQua.Text to                     |
| lblDanhGia  | set lblDanhGia.Text to                    |
| Notifier1   | call Notifier1.ShowAlert                  |


### 3.4. Tạo Block cho nút LÀM MỚI

Chọn:
```
btnLamMoi
```
Tạo:
```
when btnLamMoi.Click
    set txtCanNang.Text to ""
    set txtChieuCao.Text to ""
    set lblKetQua.Text to ""
    set lblDanhGia.Text to ""
    set global bmi to 0
```

### 3.5. Tạo Block cho nút QUAY LẠI

Chọn:
```
btnQuayLai
```
Tạo:
```
when btnQuayLai.Click
    close screen
```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/9eb5c370-7f04-45e1-abea-2edce2a4d8ec" />


## 4. Làm ScreenWebView: Hiển thị trang web
Chuyển sang: ```ScreenWebView```

### 5.1. Thiết kế giao diện

Chọn ScreenWebView, chỉnh:

| Thuộc tính | Giá trị |
|------------|----------|
| Title | Thông tin tham khảo |
| AlignHorizontal | Center |


Kéo các thành phần:

| Thành phần | Đổi tên | Nội dung hoặc thiết lập |
|------------|----------|-------------------------|
| Label | lblTieuDe | THÔNG TIN THAM KHẢO VỀ BMI |
| Button | btnQuayLai | QUAY LẠI |
| WebViewer | WebViewer1 | Width = Fill parent, Height = Fill parent |

Trong thuộc tính HomeUrl

nhập:

```
https://www.cdc.gov/bmi/adult-calculator/index.html
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/890459bb-fe8c-4a7a-bf20-8e7b5a991025" />

WebViewer là thành phần dùng để hiển thị trang web trong ứng dụng. Thuộc tính HomeUrl xác định trang được mở ban đầu. Tuy nhiên, WebViewer không phải một trình duyệt đầy đủ như Chrome. 

### 4.2. Tạo Block quay lại

Chuyển sang tab Blocks và tạo:

```
when btnQuayLai.Click
    close screen
```
Với yêu cầu cơ bản,không cần tạo Block cho WebViewer1, vì trang web sẽ tự mở theo giá trị HomeUrl.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7d40dd2c-d71e-4c85-a61b-e69b1e8d3dba" />

## 5. Kiểm tra ứng dụng

Chạy thử bằng MIT AI2 Companion.

### 5.1. Cài ứng dụng trên điện thoại

Trên điện thoại Android, mở CH Play và tìm: ```MIT AI2 Companion```

Sau đó cài đặt ứng dụng.

### 5.2. Kết nối điện thoại và máy tính cùng mạng Wi-Fi

- Điện thoại và máy tính đang mở MIT App Inventor phải dùng cùng một mạng Wi-Fi.

- Vì hai thiết bị khác mạng có thể không kết nối được.

### 5.3. Mở mã QR trên máy tính

Trong trang MIT App Inventor của bạn, trên thanh công cụ phía trên.

Bấm: ```Connect```

Sau đó chọn: ```AI Companion```

Một cửa sổ sẽ xuất hiện, trong đó có:

- Mã QR
- Mã gồm 6 ký tự

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d2a9c7bc-c06a-4067-b78a-d975876b8a0a" />

### 5.4. Quét mã QR bằng điện thoại

Mở ứng dụng: ```MIT AI2 Companion``

trên điện thoại.

Chọn: ```Scan QR code```

Sau đó đưa camera điện thoại quét mã QR đang hiển thị trên máy tính.

<img width="1253" height="2529" alt="image" src="https://github.com/user-attachments/assets/941b37cb-ba07-41a0-9f52-d90b54fe7a2b" />

### 5.5. Kiểm tra

#### 5.5.1. Kiểm tra màn hình chính

Khi app mở, xuất hiện:

- Tiêu đề ứng dụng
- Thông tin sinh viên
- Nút TÍNH CHỈ SỐ BMI
- Nút XEM THÔNG TIN THAM KHẢO

<img width="1220" height="2712" alt="image" src="https://github.com/user-attachments/assets/a22405e8-9907-4abc-a9ef-fdb111bb0711" />

Bấm:
```
TÍNH CHỈ SỐ BMI
```
<img width="1220" height="2712" alt="image" src="https://github.com/user-attachments/assets/3698af98-751e-42fc-80fa-4bd76a35fb9c" />

#### 5.5.2. Kiểm tra trường hợp để trống

Không nhập gì, bấm:
```
TÍNH BMI
```
Kết quả:

Vui lòng nhập đầy đủ cân nặng và chiều cao

<img width="1220" height="2712" alt="image" src="https://github.com/user-attachments/assets/2576c07e-9cba-476f-9eb9-a6f19dd8c9c3" />

### 5.5.3. Kiểm tra dữ liệu bằng 0

Nhập:

Cân nặng: 0
Chiều cao: 1.7

Bấm:
```
TÍNH BMI
```
Kết quả:

Cân nặng và chiều cao phải lớn hơn 0

<img width="1220" height="2712" alt="image" src="https://github.com/user-attachments/assets/3b3a51f9-deb5-4565-9d4f-71217bf17a55" />

#### 5.5.4. Kiểm tra tính BMI bình thường

Nhập:
```
Cân nặng: 60
Chiều cao: 1.7
```
Bấm:
```
TÍNH BMI
```
Kết quả:

- Chỉ số BMI của bạn: khoảng 20.76
- Kết luận: Cân nặng hợp lý

<img width="1220" height="2712" alt="image" src="https://github.com/user-attachments/assets/f2c58230-a4b7-4a64-b07b-b8f8cd3553d7" />

#### 5.5.5. Kiểm tra nút LÀM MỚI

Sau khi có kết quả, bấm:
```
LÀM MỚI
```
Kết quả:

- Hai ô nhập bị xóa
- Kết quả BMI bị xóa
- Kết luận bị xóa

<img width="1220" height="2712" alt="image" src="https://github.com/user-attachments/assets/65b5d105-4d34-44c0-b99c-11f41f44917c" />

#### 5.5.6. Kiểm tra nút QUAY LẠI

Bấm:
```
QUAY LẠI
```
Ứng dụng phải quay về Screen1.

<img width="1220" height="2712" alt="image" src="https://github.com/user-attachments/assets/88bee774-1f1e-418c-bed0-2332475c8adc" />


#### 5.5.7. Kiểm tra WebView

Từ Screen1, bấm:
```
XEM THÔNG TIN THAM KHẢO
```
Ứng dụng phải chuyển sang ScreenWebView và hiển thị trang web bạn đã nhập trong HomeUrl.

<img width="1220" height="2712" alt="image" src="https://github.com/user-attachments/assets/9c048408-2f9b-4023-9d56-86a4f429873d" />

Sau đó bấm:
```
QUAY LẠI
```
Ứng dụng phải trở về Screen1.

<img width="1220" height="2712" alt="image" src="https://github.com/user-attachments/assets/08b2ba6b-663f-41e5-89b6-f5d551c7fbd8" />





















     
