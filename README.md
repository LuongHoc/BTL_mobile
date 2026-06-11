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

4. Làm ScreenTinhBMI: Màn hình tính BMI

Chuyển sang:

ScreenTinhBMI
4.1. Thiết kế giao diện

Chọn ScreenTinhBMI, chỉnh:

Thuộc tính	Giá trị
Title	Tính chỉ số BMI
AlignHorizontal	Center
Scrollable	Chọn

Kéo một VerticalArrangement vào màn hình và đổi tên:

VerticalArrangement1 → VA_Main

Chỉnh:

Width = Fill parent
AlignHorizontal = Center

Kéo các thành phần sau vào trong VA_Main:

Thành phần	Đổi tên	Nội dung hoặc thiết lập
Label	lblTieuDe	TÍNH CHỈ SỐ BMI
Label	lblNhapCanNang	Nhập cân nặng (kg):
TextBox	txtCanNang	Hint = Ví dụ: 60, NumbersOnly = true
Label	lblNhapChieuCao	Nhập chiều cao (m):
TextBox	txtChieuCao	Hint = Ví dụ: 1.7, NumbersOnly = true
Button	btnTinh	TÍNH BMI
Button	btnLamMoi	LÀM MỚI
Label	lblKetQua	Để trống
Label	lblDanhGia	Để trống
Button	btnQuayLai	QUAY LẠI
Notifier	Notifier1	Thành phần ẩn dùng để hiện thông báo

TextBox có thuộc tính Hint để hướng dẫn cách nhập và NumbersOnly để giới hạn bàn phím nhập dữ liệu dạng số.

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
4.2. Tạo biến lưu BMI

Chuyển sang tab:

Blocks

Mở nhóm:

Variables

Kéo Block:

initialize global name to

Đổi tên biến thành:

bmi

Mở nhóm:

Math

Gắn giá trị:

0

Kết quả:

initialize global bmi to 0
4.3. Tạo Block cho nút TÍNH BMI

Chọn:

btnTinh

Kéo:

when btnTinh.Click
do

Bạn cần xử lý theo ba bước:

Bước 1: Kiểm tra người dùng đã nhập đủ dữ liệu chưa
Bước 2: Kiểm tra giá trị có lớn hơn 0 không
Bước 3: Tính BMI và đưa ra kết luận
Điều kiện 1: Không được để trống

Tạo điều kiện:

txtCanNang.Text = ""
or
txtChieuCao.Text = ""

Nếu đúng, gọi:

call Notifier1.ShowAlert
    notice "Vui lòng nhập đầy đủ cân nặng và chiều cao"
Điều kiện 2: Giá trị phải lớn hơn 0

Tạo điều kiện:

txtCanNang.Text <= 0
or
txtChieuCao.Text <= 0

Nếu đúng, gọi:

call Notifier1.ShowAlert
    notice "Cân nặng và chiều cao phải lớn hơn 0"
Tính BMI

Nếu dữ liệu hợp lệ:

set global bmi to
    txtCanNang.Text /
    (txtChieuCao.Text × txtChieuCao.Text)

Hiển thị kết quả:

set lblKetQua.Text to
    join "Chỉ số BMI của bạn: " global bmi
Đánh giá kết quả

Ghép thêm một Block if then else if:

if global bmi < 18.5
    set lblDanhGia.Text to "Kết luận: Thiếu cân"

else if global bmi < 25
    set lblDanhGia.Text to "Kết luận: Cân nặng hợp lý"

else if global bmi < 30
    set lblDanhGia.Text to "Kết luận: Thừa cân"

else
    set lblDanhGia.Text to "Kết luận: Béo phì"

Sơ đồ logic hoàn chỉnh:

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
Các nhóm Blocks cần sử dụng
Nhóm	Block cần lấy
Control	if then else, close screen
Logic	or, =
Math	0, /, ×, <, <=
Text	Chuỗi văn bản "", join
Variables	initialize global, set global, get global
txtCanNang	txtCanNang.Text
txtChieuCao	txtChieuCao.Text
lblKetQua	set lblKetQua.Text to
lblDanhGia	set lblDanhGia.Text to
Notifier1	call Notifier1.ShowAlert
4.4. Tạo Block cho nút LÀM MỚI

Chọn:

btnLamMoi

Tạo:

when btnLamMoi.Click
    set txtCanNang.Text to ""
    set txtChieuCao.Text to ""
    set lblKetQua.Text to ""
    set lblDanhGia.Text to ""
    set global bmi to 0
4.5. Tạo Block cho nút QUAY LẠI

Chọn:

btnQuayLai

Tạo:

when btnQuayLai.Click
    close screen





























     
