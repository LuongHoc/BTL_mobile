# Họ và tên: Lương Văn Học - MSSV: K225480106025
# Lớp: K58KTP
# MÔN HỌC: PHÁT TRIỂN ỨNG DỤNG TRÊN THIẾT BỊ DI ĐỘNG - TEE0419

# BÀI TẬP LỚN:

# Phần 1. Viết phần mềm trên công cụ Mit App inventor

   (tập trung vào quy trình tạo ra phần mềm)
   
   app có 3 screen:
   
   + about về bản thân+nút gọi sang 2 screen còn lại
   + giải 1 bài toán đơn giản
   + sử dụng webview: hiển thị 1 trang web có sẵn, hỗ trợ giao diện điện thoại

   mô tả: thanh công cụ có gì? kéo thả + thay đổi thuộc tính: làm ntn, để làm gì?
   
   block: mô tả bản chất việc kéo thả block ntn?
                 ưu điểm gì so với viết code? nhược điểm?
                 copy paste block ? (backpack)
     
# BÀI LÀM

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

### 4.1. Thiết kế giao diện

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

#### 5.5.3. Kiểm tra dữ liệu bằng 0

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

## 6. Giải thích thanh công cụ trong MIT App Inventor

MIT App Inventor có hai khu vực làm việc chính:

- Designer
- Blocks
### 6.1. Designer

Designer được dùng để tạo giao diện ứng dụng. Kéo các thành phần từ Palette sang Viewer, sau đó thay đổi cấu hình trong bảng Properties. Cấu trúc ứng dụng được thể hiện dưới dạng cây trong khu vực Components. 

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/13e23405-5b01-4bee-8caa-b238e7e6e58d" />

| Khu vực | Chức năng |
|----------|-----------|
| Palette | Chứa các thành phần có thể kéo thả như Label, Button, TextBox, WebViewer |
| Viewer | Mô phỏng giao diện điện thoại để sắp xếp thành phần |
| Components | Hiển thị danh sách các thành phần đã thêm vào Screen |
| Properties | Thay đổi thuộc tính của thành phần đang chọn |
| Media | Tải lên và quản lý hình ảnh, âm thanh hoặc tệp cần dùng |

Ví dụ:
Kéo Button từ Palette sang Viewer

→ Chọn Button trong Components

→ Đổi Text trong Properties thành "TÍNH BMI"

→ Đổi tên Button thành btnTinh

#### 6.2. Tại sao cần đổi tên thành phần?

Tên mặc định như:

- Button1
- Label3
- TextBox2

Sẽ khó hiểu khi tạo Blocks.

Nên đổi thành:

- btnTinh
- lblKetQua
- txtCanNang

Nhờ đó, khi đọc Blocks, sẽ biết ngay thành phần có chức năng gì.

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/190ad2dd-f581-48bc-8568-f3077129c0bc" />

### 6.3. Vai trò của Properties

Properties dùng để thay đổi giao diện và hành vi ban đầu của một thành phần.

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/36aa0a36-102a-4c05-9df8-fe2c0664bdbd" />

Ví dụ:

| Thuộc tính | Ý nghĩa |
|------------|----------|
| Text | Nội dung hiển thị |
| FontSize | Kích thước chữ |
| Width | Chiều rộng |
| Height | Chiều cao |
| Hint | Văn bản hướng dẫn trong ô nhập |
| NumbersOnly | Hạn chế bàn phím nhập dữ liệu số |
| HomeUrl | Trang web được mở ban đầu trong WebViewer |


## 7. Bản chất của việc kéo thả Blocks

Trong MIT App Inventor, Blocks đóng vai trò giống như các câu lệnh trong lập trình truyền thống. Thay vì tự gõ code, người lập trình kéo các khối lệnh và ghép chúng lại theo logic mong muốn. MIT App Inventor mô tả quá trình này là sử dụng Blocks Editor để xác định hành vi của các thành phần. 

## 8. Ưu điểm và nhược điểm của Blocks

### 8.1. Ưu điểm

| Ưu điểm | Giải thích |
|----------|-----------|
| Dễ tiếp cận | Không cần nhớ nhiều cú pháp |
| Hạn chế lỗi cú pháp | Chỉ những Blocks phù hợp mới ghép được với nhau |
| Dễ theo dõi logic | Có thể quan sát trực tiếp luồng xử lý |
| Phù hợp với người mới học | Tập trung vào cách giải quyết bài toán |
| Tạo ứng dụng nhanh | Thao tác kéo thả giúp rút ngắn thời gian xây dựng ứng dụng đơn giản |

### 8.2. Nhược điểm

| Nhược điểm | Giải thích |
|------------|-----------|
| Khó quản lý khi ứng dụng lớn | Khi có nhiều Blocks, màn hình làm việc trở nên rối |
| Khả năng tùy chỉnh có giới hạn | Một số chức năng phức tạp khó triển khai hơn so với viết code |
| Khó tái sử dụng ở dự án lớn | Việc tổ chức mã nguồn không linh hoạt như Java hoặc Kotlin |
| Không phù hợp với ứng dụng chuyên nghiệp quá phức tạp | Các dự án lớn thường cần công cụ lập trình đầy đủ hơn |

## 9. Sao chép Blocks bằng Backpack

Backpack là công cụ dùng để lưu tạm và sao chép Blocks giữa các Screen hoặc giữa các Project. Tài liệu chính thức mô tả Backpack là chức năng copy và paste Blocks sang Screen hoặc Project khác. 
Cách sử dụng:

- Bước 1: Chuyển sang tab Blocks
- Bước 2: Kéo nhóm Blocks cần sao chép vào biểu tượng Backpack

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/69004313-1db6-4e6d-a577-af272688f751" />

- Bước 3: Mở Screen hoặc Project đích
- Bước 4: Mở Backpack
- Bước 5: Kéo Blocks từ Backpack ra vùng làm việc

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/a1b635c7-13ab-4461-b421-481e6ba21df1" />








# Phần 2. Viết app sử dụng Android Studio

1. Tạo Project Android Studio

Bước 1.1. Mở Android Studio

Mở Android Studio.

Nếu đang ở màn hình chào mừng, bấm:

New Project

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/d17d7e37-739c-4123-b5a3-4eea11bc05d8" />


Bước 1.2. Chọn mẫu Project

Trong danh sách mẫu, chọn:

Phone and Tablet → Empty Views Activity

Sau đó bấm: Next

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/469019db-344c-42c0-b834-184770de8e23" />

Empty Views Activity:	Dùng Java và file giao diện XML

Bước 1.3. Điền thông tin Project

Điền các giá trị sau:

| Mục | Giá trị |
|------|----------|
| Name | BMI Calculator |
| Package name | com.example.bmicalculator |
| Save location | Chọn thư mục bạn dễ tìm, ví dụ D:\AndroidProjects\BMICalculator |
| Language | Java |
| Minimum SDK | API 24: Android 7.0 |

Sau đó bấm: Finish

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4624d80f-56af-40e1-a74b-2535aaba2350" />

Chờ Android Studio tải và đồng bộ Project.

Bước 1.4. Kiểm tra Project đã tạo thành công

Ở cột bên trái, chọn chế độ hiển thị:

Android

Sau đó mở cây thư mục:
```
app
├── manifests
│   └── AndroidManifest.xml
├── java
│   └── com.example.bmicalculator
│       └── MainActivity.java
└── res
    ├── layout
    │   └── activity_main.xml
    └── values
        ├── colors.xml
        ├── strings.xml
        └── themes.xml
```
Thấy MainActivity.java và activity_main.xml, đã tạo Project đúng.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0483f7ee-4ccb-4b5f-91af-08c29b8ab7e3" />

## 2. Tạo BmiActivity

### 2.1. Mở thư mục chứa code Java

Ở cột bên trái, mở:
```
app
└── java
    └── com.example.bmicalculator
```
Nhấp chuột phải vào:

com.example.bmicalculator

Chọn:

New → Activity → Empty Views Activity

Android Studio có thể tự tạo Activity, file layout XML và cập nhật Manifest khi bạn sử dụng thao tác này.

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/6093016f-db78-487b-88cb-c3034bf0e84e" />


### 3.2. Điền thông tin

Trong cửa sổ hiện ra, nhập:

| Mục | Giá trị |
|------|----------|
| Activity Name | BmiActivity |
| Layout Name | activity_bmi |
| Source Language | Java |
| Launcher Activity | Không chọn |

Bấm: Finish

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f8099754-3f67-4288-914b-d4dd6faf067a" />

## 4. Tạo WebViewActivity

Làm tương tự:

Nhấp chuột phải vào:

com.example.bmicalculator

Chọn:

New → Activity → Empty Views Activity

Nhập:

| Mục | Giá trị |
|------|----------|
| Activity Name | WebViewActivity |
| Layout Name | activity_web_view |
| Source Language | Java |
| Launcher Activity | Không chọn |

Bấm:

Finish

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8233818b-9973-4764-905a-5ca73f2780b6" />

## 5. Kiểm tra cấu trúc sau khi tạo 3 Activity

Cấu trúc Project cần có dạng:

```
app
├── manifests
│   └── AndroidManifest.xml
├── java
│   └── com.example.bmicalculator
│       ├── MainActivity.java
│       ├── BmiActivity.java
│       └── WebViewActivity.java
└── res
    └── layout
        ├── activity_main.xml
        ├── activity_bmi.xml
        └── activity_web_view.xml
```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/f602c5ae-28f9-403e-9477-fc529604ff39" />

Mở:

app → manifests → AndroidManifest.xml

Sẽ thấy 3 Activity đã được khai báo gần giống:

```
<application
    ... >

    <activity
        android:name=".WebViewActivity"
        android:exported="false" />

    <activity
        android:name=".BmiActivity"
        android:exported="false" />

    <activity
        android:name=".MainActivity"
        android:exported="true">

        <intent-filter>
            <action android:name="android.intent.action.MAIN" />
            <category android:name="android.intent.category.LAUNCHER" />
        </intent-filter>

    </activity>

</application>
```
<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/28f80d75-fdb2-44dd-aed8-8cd2e0be5898" />

MainActivity là màn hình khởi động nên có intent-filter chứa MAIN và LAUNCHER. Hai Activity còn lại được mở từ bên trong ứng dụng nên chưa cần intent-filter. Activity không khai báo intent-filter chỉ có thể được khởi chạy bằng Intent tường minh.


### 6. thiết kế giao diện MainActivity

Màn hình này tương đương với Screen1 trong MIT App Inventor. Nó cần có:

Tiêu đề ứng dụng
Mô tả ngắn
Thông tin sinh viên
Nút TÍNH CHỈ SỐ BMI
Nút XEM THÔNG TIN THAM KHẢO
Bước 1. Mở file giao diện

Ở cây thư mục bên trái, mở:

app
→ res
→ layout
→ activity_main.xml
Bước 2. Chuyển sang chế độ viết XML

Ở góc trên bên phải của vùng chỉnh sửa giao diện, chọn:

Code

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/591c469a-ee5a-4122-b9e3-b69bb5efbc97" />

Bước 3. Xóa code cũ và dán giao diện mới

Xóa toàn bộ nội dung trong activity_main.xml, sau đó dán đoạn này:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="24dp">

    <TextView
        android:id="@+id/tvTitle"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="ỨNG DỤNG TÍNH CHỈ SỐ BMI"
        android:textSize="22sp"
        android:textStyle="bold"
        android:gravity="center"
        android:layout_marginBottom="16dp" />

    <TextView
        android:id="@+id/tvDescription"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Ứng dụng hỗ trợ tính BMI dựa trên cân nặng và chiều cao."
        android:textSize="16sp"
        android:gravity="center"
        android:layout_marginBottom="16dp" />

    <TextView
        android:id="@+id/tvStudent"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Sinh viên: Lương Văn Học\nMSSV: K225480106025"
        android:textSize="15sp"
        android:gravity="center"
        android:layout_marginBottom="24dp" />

    <Button
        android:id="@+id/btnOpenBmi"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="TÍNH CHỈ SỐ BMI"
        android:layout_marginBottom="12dp" />

    <Button
        android:id="@+id/btnOpenWebView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="XEM THÔNG TIN THAM KHẢO" />

</LinearLayout>
```
Bước 4. Kiểm tra giao diện

Sau khi dán xong, chọn:

Design

hoặc:

Split

để xem trước giao diện.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/03b5eb34-f888-41c9-bb2b-8313f04ff72a" />


## 7. Đưa nội dung vào strings.xml

Bước 1. Mở file strings.xml

Ở cây thư mục bên trái, bấm:

app
→ res
→ values
→ strings.xml
Bước 2. Chuyển sang chế độ Code

Nếu Android Studio mở giao diện khác, bấm biểu tượng ba dòng ngang ở góc trên bên phải để chuyển sang chế độ viết code.

Bạn sẽ thấy nội dung gần giống:
```
<resources>
    <string name="app_name">BMI Calculator</string>

    <string name="main_title">ỨNG DỤNG TÍNH CHỈ SỐ BMI</string>
    <string name="main_description">Ứng dụng hỗ trợ tính BMI dựa trên cân nặng và chiều cao.</string>
    <string name="student_info">Sinh viên: Lương Văn Học\nMã sinh viên: K225480106025</string>

    <string name="btn_open_bmi">TÍNH CHỈ SỐ BMI</string>
    <string name="btn_open_web_view">XEM THÔNG TIN THAM KHẢO</string>
</resources>
```
Nhấn:

Ctrl + S

để lưu.

Sửa lại activity_main.xml
Bước 4. Mở lại file giao diện

Bấm:

app
→ res
→ layout
→ activity_main.xml

Chuyển sang chế độ Code.

Bước 5. Thay các nội dung hardcode

Nội dung đầy đủ của activity_main.xml nên có dạng:

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="24dp">

    <TextView
        android:id="@+id/tvTitle"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/main_title"
        android:textSize="22sp"
        android:textStyle="bold"
        android:gravity="center"
        android:layout_marginBottom="16dp" />

    <TextView
        android:id="@+id/tvDescription"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/main_description"
        android:textSize="16sp"
        android:gravity="center"
        android:layout_marginBottom="16dp" />

    <TextView
        android:id="@+id/tvStudent"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/student_info"
        android:textSize="15sp"
        android:gravity="center"
        android:layout_marginBottom="24dp" />

    <Button
        android:id="@+id/btnOpenBmi"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/btn_open_bmi"
        android:layout_marginBottom="12dp" />

    <Button
        android:id="@+id/btnOpenWebView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/btn_open_web_view" />

</LinearLayout>
```
Nhấn:

Ctrl + S

## 8. Viết code chuyển màn hình trong MainActivity
### Bước 8.1. Mở file Java

Ở cây thư mục bên trái, bấm:

app
→ kotlin+java
→ com.example.bmicalculator
→ MainActivity

Tệp được mở là:

MainActivity.java


Bước 8.3. Dán code mới

Dán toàn bộ đoạn sau vào MainActivity.java:
```
package com.example.bmicalculator;

import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    private Button btnOpenBmi;
    private Button btnOpenWebView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Liên kết các Button trong file XML với code Java
        btnOpenBmi = findViewById(R.id.btnOpenBmi);
        btnOpenWebView = findViewById(R.id.btnOpenWebView);

        // Mở màn hình tính BMI khi người dùng bấm nút
        btnOpenBmi.setOnClickListener(v -> {
            Intent intent = new Intent(MainActivity.this, BmiActivity.class);
            startActivity(intent);
        });

        // Mở màn hình WebView khi người dùng bấm nút
        btnOpenWebView.setOnClickListener(v -> {
            Intent intent = new Intent(MainActivity.this, WebViewActivity.class);
            startActivity(intent);
        });
    }
}
```
Nhấn:

Ctrl + S

để lưu file.


## 10. Kiểm tra lỗi sau khi dán code

Sau khi lưu, quan sát file MainActivity.java.

Nếu không có chữ màu đỏ hoặc gạch chân đỏ thì code đã hợp lệ.

Bạn cũng có thể chọn:

Build


hoặc dùng phím tắt:

Ctrl + F9

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/97c89a7b-e141-4429-8300-ef2debba12d6" />

Hiện ```Build MOBILE: finished```

Điều đó nghĩa là Project hiện tại không có lỗi làm hỏng quá trình build.


## 10. Thiết kế giao diện activity_bmi.xml

Giao diện gồm:

Tiêu đề
Ô nhập cân nặng
Ô nhập chiều cao
Nút TÍNH BMI
Nút LÀM MỚI
Vùng hiển thị kết quả
Vùng hiển thị đánh giá
Nút QUAY LẠI

Ta sử dụng LinearLayout với orientation="vertical" để sắp xếp các thành phần theo chiều dọc. EditText được khai báo inputType="numberDecimal" để phù hợp với dữ liệu số có phần thập phân như chiều cao 1.7.

Bước 10.1. Bổ sung nội dung vào strings.xml

Mở:

app
→ res
→ values
→ strings.xml

Giữ lại các dòng đã có và thêm nội dung mới vào bên trong cặp thẻ:

<resources>
...
</resources>

Bạn có thể thay toàn bộ file bằng đoạn hoàn chỉnh sau:
```
<resources>
    <string name="app_name">BMI Calculator</string>

    <!-- Nội dung màn hình chính -->
    <string name="main_title">ỨNG DỤNG TÍNH CHỈ SỐ BMI</string>
    <string name="main_description">Ứng dụng hỗ trợ tính BMI dựa trên cân nặng và chiều cao.</string>
    <string name="student_info">Sinh viên: Lương Văn Học\nMã sinh viên: K225480106025</string>
    <string name="btn_open_bmi">TÍNH CHỈ SỐ BMI</string>
    <string name="btn_open_web_view">XEM THÔNG TIN THAM KHẢO</string>

    <!-- Nội dung màn hình tính BMI -->
    <string name="bmi_title">TÍNH CHỈ SỐ BMI</string>
    <string name="weight_label">Nhập cân nặng (kg):</string>
    <string name="weight_hint">Ví dụ: 60</string>
    <string name="height_label">Nhập chiều cao (m):</string>
    <string name="height_hint">Ví dụ: 1.7</string>
    <string name="btn_calculate">TÍNH BMI</string>
    <string name="btn_reset">LÀM MỚI</string>
    <string name="btn_back">QUAY LẠI</string>
    <string name="empty"></string>
</resources>
```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/82542fcf-b172-4c85-8e9c-abc97d0731f3" />

Nhấn:

Ctrl + S
Bước 10.2. Mở file activity_bmi.xml

Ở cây thư mục bên trái, mở:

app
→ res
→ layout
→ activity_bmi.xml

Chuyển sang chế độ viết XML bằng biểu tượng ba dòng ngang ở góc trên bên phải vùng chỉnh sửa.

Bước 10.3. Xóa code cũ và dán giao diện mới

Nhấn:

Ctrl + A

sau đó dán toàn bộ đoạn sau:
```
<?xml version="1.0" encoding="utf-8"?>
<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <LinearLayout
        android:id="@+id/main"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:gravity="center_horizontal"
        android:padding="24dp">

        <TextView
            android:id="@+id/tvBmiTitle"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="@string/bmi_title"
            android:textSize="22sp"
            android:textStyle="bold"
            android:gravity="center"
            android:layout_marginBottom="24dp" />

        <TextView
            android:id="@+id/tvWeightLabel"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="@string/weight_label"
            android:textSize="16sp"
            android:layout_marginBottom="4dp" />

        <EditText
            android:id="@+id/edtWeight"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:hint="@string/weight_hint"
            android:inputType="numberDecimal"
            android:layout_marginBottom="16dp" />

        <TextView
            android:id="@+id/tvHeightLabel"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="@string/height_label"
            android:textSize="16sp"
            android:layout_marginBottom="4dp" />

        <EditText
            android:id="@+id/edtHeight"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:hint="@string/height_hint"
            android:inputType="numberDecimal"
            android:layout_marginBottom="20dp" />

        <Button
            android:id="@+id/btnCalculate"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="@string/btn_calculate"
            android:layout_marginBottom="10dp" />

        <Button
            android:id="@+id/btnReset"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="@string/btn_reset"
            android:layout_marginBottom="20dp" />

        <TextView
            android:id="@+id/tvResult"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="@string/empty"
            android:textSize="17sp"
            android:textStyle="bold"
            android:gravity="center"
            android:layout_marginBottom="10dp" />

        <TextView
            android:id="@+id/tvEvaluation"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="@string/empty"
            android:textSize="17sp"
            android:gravity="center"
            android:layout_marginBottom="24dp" />

        <Button
            android:id="@+id/btnBack"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="@string/btn_back" />

    </LinearLayout>

</ScrollView>
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a153c52f-5265-4890-aa19-8ad923f99727" />

Nhấn:

Ctrl + S
11. Xem trước giao diện

Bấm biểu tượng Design hoặc Split ở góc trên bên phải.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3580990a-ad24-431a-b31d-273a51d6e040" />


Hai vùng:

tvResult
tvEvaluation

ban đầu để trống nên bạn chưa nhìn thấy chữ. Sau này code Java sẽ đưa kết quả vào hai vị trí này.

12. Ý nghĩa các thành phần quan trọng
Thành phần	ID	Mục đích
EditText	edtWeight	Nhập cân nặng
EditText	edtHeight	Nhập chiều cao
Button	btnCalculate	Tính BMI
Button	btnReset	Xóa dữ liệu cũ
TextView	tvResult	Hiển thị chỉ số BMI
TextView	tvEvaluation	Hiển thị kết luận
Button	btnBack	Quay về màn hình trước

TextView dùng để hiển thị văn bản, còn EditText dùng để nhận nội dung người dùng nhập vào.

13. Kiểm tra Build

Sau khi dán XML, nhấn:

Ctrl + F9

Nếu xuất hiện:

Build MOBILE: finished

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/fe35dd67-53c7-4159-bb92-c770ca1d83ae" />

## 14. Viết code xử lý trong BmiActivity.java

Code sẽ thực hiện:

Nhấn TÍNH BMI
→ kiểm tra dữ liệu
→ tính BMI
→ làm tròn kết quả đến 2 chữ số thập phân
→ hiển thị đánh giá

Nhấn LÀM MỚI
→ xóa dữ liệu cũ

Nhấn QUAY LẠI
→ trở về MainActivity
Bước 14.1. Thêm nội dung vào strings.xml

Mở:

app
→ res
→ values
→ strings.xml

Thêm các dòng sau trước thẻ đóng:

</resources>

Nội dung cần thêm:
```
    <!-- Nội dung thông báo và kết quả BMI -->
    <string name="error_empty">Vui lòng nhập đầy đủ cân nặng và chiều cao</string>
    <string name="error_positive">Cân nặng và chiều cao phải lớn hơn 0</string>
    <string name="error_invalid_number">Dữ liệu nhập không hợp lệ</string>

    <string name="bmi_result_format">Chỉ số BMI của bạn: %.2f</string>
    <string name="evaluation_underweight">Kết luận: Thiếu cân</string>
    <string name="evaluation_normal">Kết luận: Cân nặng hợp lý</string>
    <string name="evaluation_overweight">Kết luận: Thừa cân</string>
    <string name="evaluation_obese">Kết luận: Béo phì</string>
```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f5d1d364-85eb-47f9-b54b-92252e65efe8" />

Sau đó nhấn:

Ctrl + S

Việc đặt nội dung hiển thị trong strings.xml thay vì viết trực tiếp trong code giúp dễ quản lý và hỗ trợ nhiều ngôn ngữ hơn.

Bước 14.2. Mở BmiActivity.java

Ở cây thư mục bên trái, chọn:

app
→ kotlin+java
→ com.example.bmicalculator
→ BmiActivity

Nhấn:

Ctrl + A

để chọn toàn bộ code cũ, sau đó xóa đi.

Bước 14.3. Dán code xử lý BMI

Dán toàn bộ đoạn code sau:
```
package com.example.bmicalculator;

import android.os.Bundle;
import android.text.TextUtils;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class BmiActivity extends AppCompatActivity {

    private EditText edtWeight;
    private EditText edtHeight;
    private TextView tvResult;
    private TextView tvEvaluation;
    private Button btnCalculate;
    private Button btnReset;
    private Button btnBack;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_bmi);

        // Liên kết các thành phần trong XML với code Java
        edtWeight = findViewById(R.id.edtWeight);
        edtHeight = findViewById(R.id.edtHeight);
        tvResult = findViewById(R.id.tvResult);
        tvEvaluation = findViewById(R.id.tvEvaluation);
        btnCalculate = findViewById(R.id.btnCalculate);
        btnReset = findViewById(R.id.btnReset);
        btnBack = findViewById(R.id.btnBack);

        // Xử lý khi người dùng bấm nút TÍNH BMI
        btnCalculate.setOnClickListener(v -> calculateBmi());

        // Xử lý khi người dùng bấm nút LÀM MỚI
        btnReset.setOnClickListener(v -> resetForm());

        // Đóng Activity hiện tại để quay về màn hình trước
        btnBack.setOnClickListener(v -> finish());
    }

    private void calculateBmi() {
        String weightText = edtWeight.getText().toString().trim();
        String heightText = edtHeight.getText().toString().trim();

        // Kiểm tra người dùng đã nhập đủ dữ liệu chưa
        if (TextUtils.isEmpty(weightText) || TextUtils.isEmpty(heightText)) {
            Toast.makeText(this, R.string.error_empty, Toast.LENGTH_SHORT).show();
            return;
        }

        try {
            // Cho phép nhập 1.7 hoặc 1,7
            double weight = Double.parseDouble(weightText.replace(',', '.'));
            double height = Double.parseDouble(heightText.replace(',', '.'));

            // Kiểm tra giá trị hợp lệ
            if (weight <= 0 || height <= 0) {
                Toast.makeText(this, R.string.error_positive, Toast.LENGTH_SHORT).show();
                return;
            }

            // Công thức: BMI = cân nặng / chiều cao bình phương
            double bmi = weight / (height * height);

            // Hiển thị BMI với 2 chữ số sau dấu phẩy
            tvResult.setText(getString(R.string.bmi_result_format, bmi));

            // Phân loại kết quả
            if (bmi < 18.5) {
                tvEvaluation.setText(R.string.evaluation_underweight);
            } else if (bmi < 25) {
                tvEvaluation.setText(R.string.evaluation_normal);
            } else if (bmi < 30) {
                tvEvaluation.setText(R.string.evaluation_overweight);
            } else {
                tvEvaluation.setText(R.string.evaluation_obese);
            }

        } catch (NumberFormatException e) {
            Toast.makeText(this, R.string.error_invalid_number, Toast.LENGTH_SHORT).show();
        }
    }

    private void resetForm() {
        edtWeight.setText("");
        edtHeight.setText("");
        tvResult.setText("");
        tvEvaluation.setText("");
        edtWeight.requestFocus();
    }
}
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e210b188-fdcd-464f-8ba7-5e962ec92853" />

Nhấn:

Ctrl + S
15. Ý nghĩa các phần quan trọng
15.1. Lấy dữ liệu từ hai ô nhập
String weightText = edtWeight.getText().toString().trim();
String heightText = edtHeight.getText().toString().trim();

Hai dòng này lấy nội dung người dùng đã nhập trong EditText.

15.2. Kiểm tra ô trống
if (TextUtils.isEmpty(weightText) || TextUtils.isEmpty(heightText))

Ký hiệu:

||

có nghĩa là hoặc. Chỉ cần một ô bị bỏ trống, ứng dụng sẽ hiển thị thông báo.

15.3. Công thức tính BMI
double bmi = weight / (height * height);

Dòng này tương đương với Blocks bạn đã ghép trong MIT App Inventor:

BMI = cân nặng / (chiều cao × chiều cao)
15.4. Làm tròn kết quả
tvResult.setText(getString(R.string.bmi_result_format, bmi));

Trong strings.xml, cú pháp:

<string name="bmi_result_format">Chỉ số BMI của bạn: %.2f</string>

giúp hiển thị 2 chữ số sau dấu phẩy.

Ví dụ:

Chỉ số BMI của bạn: 20.76
15.5. Quay lại màn hình trước
btnBack.setOnClickListener(v -> finish());

finish() đóng BmiActivity, vì vậy ứng dụng quay về MainActivity.

16. Build lại Project

Nhấn:

Ctrl + F9

Kết quả mong đợi:

BUILD SUCCESSFUL

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d657dab2-4500-48b4-bdbb-2adeb0a26bd0" />




## 17. Khai báo quyền Internet

Ứng dụng cần Internet để:

Gửi kết quả BMI lên API
Hiển thị trang web trong WebViewActivity

Android yêu cầu khai báo quyền mạng trong AndroidManifest.xml. Tài liệu Android khuyến nghị khai báo INTERNET và ACCESS_NETWORK_STATE cho thao tác mạng; đây là các quyền thông thường, được cấp khi cài app và không cần hiện hộp thoại xin quyền khi chạy.

Bước 17.1. Mở Manifest

Ở cây thư mục bên trái, mở:

app
→ manifests
→ AndroidManifest.xml
Bước 17.2. Thêm hai dòng quyền

Tìm phần đầu file:

<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">

Ngay bên dưới thẻ mở <manifest> và phía trên <application>, thêm:

    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

File sẽ gần giống:

<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">

    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

    <application
        android:allowBackup="true"
        ...

Lưu ý: không đặt hai dòng quyền vào bên trong <application>.

Nhấn:

Ctrl + S
18. Gửi kết quả BMI lên API

API phải được gọi ở luồng nền thay vì luồng giao diện chính. Android cảnh báo rằng thao tác mạng trên luồng chính có thể làm ứng dụng bị treo hoặc phát sinh NetworkOnMainThreadException.

Để đơn giản, bạn thay toàn bộ code của BmiActivity.java bằng một phiên bản đã tích hợp sẵn phần gửi API.

Bước 18.1. Mở file Java

Mở:

app
→ kotlin+java
→ com.example.bmicalculator
→ BmiActivity

Bấm:

Ctrl + A

sau đó dán toàn bộ code dưới đây.
```
package com.example.bmicalculator;

import android.os.Bundle;
import android.text.TextUtils;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

import org.json.JSONObject;

import java.io.BufferedReader;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.io.OutputStream;
import java.net.HttpURLConnection;
import java.net.URL;
import java.nio.charset.StandardCharsets;
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

public class BmiActivity extends AppCompatActivity {

    private static final String API_URL = "https://k58kmt.tdh.io.vn/api";
    private static final String STUDENT_ID = "K225480106025";

    private EditText edtWeight;
    private EditText edtHeight;
    private TextView tvResult;
    private TextView tvEvaluation;
    private Button btnCalculate;
    private Button btnReset;
    private Button btnBack;

    // Dùng luồng nền để gửi dữ liệu lên API
    private final ExecutorService executorService =
            Executors.newSingleThreadExecutor();

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_bmi);

        // Liên kết các thành phần XML với code Java
        edtWeight = findViewById(R.id.edtWeight);
        edtHeight = findViewById(R.id.edtHeight);
        tvResult = findViewById(R.id.tvResult);
        tvEvaluation = findViewById(R.id.tvEvaluation);
        btnCalculate = findViewById(R.id.btnCalculate);
        btnReset = findViewById(R.id.btnReset);
        btnBack = findViewById(R.id.btnBack);

        btnCalculate.setOnClickListener(v -> calculateBmi());
        btnReset.setOnClickListener(v -> resetForm());
        btnBack.setOnClickListener(v -> finish());
    }

    private void calculateBmi() {
        String weightText = edtWeight.getText().toString().trim();
        String heightText = edtHeight.getText().toString().trim();

        // Kiểm tra ô trống
        if (TextUtils.isEmpty(weightText) || TextUtils.isEmpty(heightText)) {
            Toast.makeText(this, R.string.error_empty, Toast.LENGTH_SHORT).show();
            return;
        }

        try {
            // Cho phép nhập 1.7 hoặc 1,7
            double weight = Double.parseDouble(weightText.replace(',', '.'));
            double height = Double.parseDouble(heightText.replace(',', '.'));

            // Kiểm tra dữ liệu phải lớn hơn 0
            if (weight <= 0 || height <= 0) {
                Toast.makeText(this, R.string.error_positive, Toast.LENGTH_SHORT).show();
                return;
            }

            // Công thức BMI
            double bmi = weight / (height * height);

            tvResult.setText(getString(R.string.bmi_result_format, bmi));

            String evaluation;

            if (bmi < 18.5) {
                evaluation = getString(R.string.evaluation_underweight);
            } else if (bmi < 25) {
                evaluation = getString(R.string.evaluation_normal);
            } else if (bmi < 30) {
                evaluation = getString(R.string.evaluation_overweight);
            } else {
                evaluation = getString(R.string.evaluation_obese);
            }

            tvEvaluation.setText(evaluation);

            // Gửi bài toán và kết quả lên API
            sendResultToApi(weight, height, bmi, evaluation);

        } catch (NumberFormatException e) {
            Toast.makeText(
                    this,
                    R.string.error_invalid_number,
                    Toast.LENGTH_SHORT
            ).show();
        }
    }

    private void sendResultToApi(
            double weight,
            double height,
            double bmi,
            String evaluation
    ) {
        executorService.execute(() -> {
            HttpURLConnection connection = null;

            try {
                // Tạo JSON input
                JSONObject input = new JSONObject();
                input.put("weight", weight);
                input.put("height", height);
                input.put("name", "BMI Calculator");

                // Tạo JSON output
                JSONObject output = new JSONObject();
                output.put("ketluan", evaluation);
                output.put("bmi", Math.round(bmi * 100.0) / 100.0);

                // Tạo JSON gửi lên API
                JSONObject payload = new JSONObject();
                payload.put("app_by", STUDENT_ID);
                payload.put("input", input);
                payload.put("output", output);

                URL url = new URL(API_URL);
                connection = (HttpURLConnection) url.openConnection();

                connection.setRequestMethod("POST");
                connection.setConnectTimeout(10000);
                connection.setReadTimeout(10000);
                connection.setDoOutput(true);

                connection.setRequestProperty(
                        "Content-Type",
                        "application/json; charset=UTF-8"
                );

                connection.setRequestProperty(
                        "Accept",
                        "application/json"
                );

                byte[] body = payload
                        .toString()
                        .getBytes(StandardCharsets.UTF_8);

                connection.setFixedLengthStreamingMode(body.length);

                try (OutputStream outputStream = connection.getOutputStream()) {
                    outputStream.write(body);
                }

                int statusCode = connection.getResponseCode();

                InputStream inputStream;

                if (statusCode >= 200 && statusCode < 300) {
                    inputStream = connection.getInputStream();
                } else {
                    inputStream = connection.getErrorStream();
                }

                String responseText = readStream(inputStream);

                if (statusCode >= 200 && statusCode < 300) {
                    JSONObject responseJson = new JSONObject(responseText);

                    int stt = responseJson.optInt("stt", -1);

                    runOnUiThread(() -> {
                        if (stt >= 0) {
                            Toast.makeText(
                                    this,
                                    "Đã gửi API thành công. STT: " + stt,
                                    Toast.LENGTH_LONG
                            ).show();
                        } else {
                            Toast.makeText(
                                    this,
                                    "Đã gửi kết quả lên API",
                                    Toast.LENGTH_SHORT
                            ).show();
                        }
                    });

                } else {
                    runOnUiThread(() ->
                            Toast.makeText(
                                    this,
                                    "API phản hồi lỗi: " + statusCode,
                                    Toast.LENGTH_LONG
                            ).show()
                    );
                }

            } catch (Exception e) {
                runOnUiThread(() ->
                        Toast.makeText(
                                this,
                                "Không thể gửi dữ liệu lên API",
                                Toast.LENGTH_LONG
                        ).show()
                );

            } finally {
                if (connection != null) {
                    connection.disconnect();
                }
            }
        });
    }

    private String readStream(InputStream inputStream) throws Exception {
        if (inputStream == null) {
            return "";
        }

        StringBuilder builder = new StringBuilder();

        try (
                BufferedReader reader = new BufferedReader(
                        new InputStreamReader(
                                inputStream,
                                StandardCharsets.UTF_8
                        )
                )
        ) {
            String line;

            while ((line = reader.readLine()) != null) {
                builder.append(line);
            }
        }

        return builder.toString();
    }

    private void resetForm() {
        edtWeight.setText("");
        edtHeight.setText("");
        tvResult.setText("");
        tvEvaluation.setText("");
        edtWeight.requestFocus();
    }

    @Override
    protected void onDestroy() {
        super.onDestroy();
        executorService.shutdown();
    }
}
```
Nhấn:

Ctrl + S
19. Dữ liệu được gửi lên API

Khi người dùng nhập:

Cân nặng: 60
Chiều cao: 1.7

ứng dụng sẽ gửi JSON gần giống:

{
  "app_by": "K225480106025",
  "input": {
    "weight": 60,
    "height": 1.7,
    "name": "BMI Calculator"
  },
  "output": {
    "ketluan": "Kết luận: Cân nặng hợp lý",
    "bmi": 20.76
  }
}

Nếu API nhận dữ liệu thành công, ứng dụng sẽ hiện thông báo gần giống:

Đã gửi API thành công. STT: 1234
20. Build lại Project

Nhấn:

Ctrl + F9

Kết quả mong đợi:

BUILD SUCCESSFUL

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0cd6eebe-9f45-4bd2-af3c-75176694b984" />


## 21. Bổ sung chuỗi cho màn hình WebView
Bước 21.1. Mở strings.xml

Ở cây thư mục bên trái, mở:

app
→ res
→ values
→ strings.xml
Bước 21.2. Thêm nội dung mới

Thêm các dòng sau trước thẻ đóng:

</resources>

Nội dung cần thêm:

    <!-- Nội dung màn hình WebView -->
    <string name="web_view_title">TRANG THÔNG TIN THAM KHẢO</string>
    <string name="btn_reload">TẢI LẠI TRANG</string>

Bạn đã có chuỗi dùng chung:

<string name="btn_back">QUAY LẠI</string>

nên không cần khai báo lại.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/157e71c9-1d81-4e17-a341-1679c67b0b7e" />

Nhấn:

Ctrl + S
22. Thiết kế giao diện activity_web_view.xml
Bước 22.1. Mở file giao diện

Ở cây thư mục bên trái, mở:

app
→ res
→ layout
→ activity_web_view.xml
Bước 22.2. Chuyển sang chế độ Code

Ở góc trên bên phải vùng chỉnh sửa XML, bấm biểu tượng ba dòng ngang:

Code
Bước 22.3. Xóa XML cũ

Nhấn:

Ctrl + A

sau đó xóa toàn bộ nội dung cũ.

Bước 22.4. Dán XML mới

Dán toàn bộ đoạn sau:

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="12dp">

    <TextView
        android:id="@+id/tvWebViewTitle"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/web_view_title"
        android:textSize="20sp"
        android:textStyle="bold"
        android:gravity="center"
        android:layout_marginBottom="8dp" />

    <WebView
        android:id="@+id/webView"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1" />

    <Button
        android:id="@+id/btnReload"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/btn_reload"
        android:layout_marginTop="8dp" />

    <Button
        android:id="@+id/btnBack"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/btn_back"
        android:layout_marginTop="8dp" />

</LinearLayout>

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8093a377-b897-4d2d-8407-3130e7799a25" />

Nhấn:

Ctrl + S
23. Kiểm tra giao diện WebView

Chuyển sang chế độ:

Design

hoặc:

Split

Giao diện cần có bố cục:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/708ec5e7-db42-4464-80f1-5b71404a051a" />

TRANG THÔNG TIN THAM KHẢO

┌──────────────────────────┐
│                          │
│         WebView          │
│                          │
│                          │
└──────────────────────────┘

[        TẢI LẠI TRANG       ]

[           QUAY LẠI         ]

Trong màn hình thiết kế, vùng WebView có thể chỉ hiển thị một khung trống. Điều này là bình thường. Trang web chỉ được tải khi chạy ứng dụng.

Ý nghĩa của layout_weight

Trong XML có đoạn:

android:layout_height="0dp"
android:layout_weight="1"

Hai thuộc tính này giúp WebView chiếm toàn bộ khoảng trống còn lại trên màn hình, nhưng vẫn dành chỗ cho hai nút bên dưới.

24. Viết code cho WebViewActivity.java
Bước 24.1. Mở file Java

Ở cây thư mục bên trái, mở:

app
→ kotlin+java
→ com.example.bmicalculator
→ WebViewActivity
Bước 24.2. Xóa code tự sinh

Nhấn:

Ctrl + A

sau đó xóa toàn bộ code cũ.

Bước 24.3. Dán code mới

Dán toàn bộ đoạn sau:

package com.example.bmicalculator;

import android.os.Bundle;
import android.webkit.WebSettings;
import android.webkit.WebView;
import android.webkit.WebViewClient;
import android.widget.Button;

import androidx.activity.OnBackPressedCallback;
import androidx.appcompat.app.AppCompatActivity;

public class WebViewActivity extends AppCompatActivity {

    private static final String WEB_URL =
            "https://k58kmt.tdh.io.vn?masv=K225480106025";

    private WebView webView;
    private Button btnReload;
    private Button btnBack;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_web_view);

        // Liên kết các thành phần trong XML với code Java
        webView = findViewById(R.id.webView);
        btnReload = findViewById(R.id.btnReload);
        btnBack = findViewById(R.id.btnBack);

        // Cấu hình WebView
        WebSettings webSettings = webView.getSettings();
        webSettings.setJavaScriptEnabled(true);
        webSettings.setDomStorageEnabled(true);

        // Giữ trang web hiển thị bên trong ứng dụng
        webView.setWebViewClient(new WebViewClient());

        // Mở trang web theo mã sinh viên
        webView.loadUrl(WEB_URL);

        // Tải lại trang hiện tại
        btnReload.setOnClickListener(v -> webView.reload());

        // Đóng Activity để quay lại MainActivity
        btnBack.setOnClickListener(v -> finish());

        // Xử lý nút Back vật lý hoặc thao tác vuốt Back
        getOnBackPressedDispatcher().addCallback(
                this,
                new OnBackPressedCallback(true) {
                    @Override
                    public void handleOnBackPressed() {
                        if (webView.canGoBack()) {
                            webView.goBack();
                        } else {
                            finish();
                        }
                    }
                }
        );
    }

    @Override
    protected void onDestroy() {
        if (webView != null) {
            webView.stopLoading();
            webView.destroy();
        }

        super.onDestroy();
    }
}


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ffc2cc3f-83c5-484d-82e0-c3953dd3a855" />

Nhấn:

Ctrl + S
25. Ý nghĩa code WebView
25.1. Mở trang theo mã sinh viên
private static final String WEB_URL =
        "https://k58kmt.tdh.io.vn?masv=K225480106025";

URL chứa mã sinh viên của bạn để trang web có thể nhận diện ứng dụng đang truy cập.

25.2. Cho phép chạy JavaScript
webSettings.setJavaScriptEnabled(true);

Một số trang web cần JavaScript để hiển thị và xử lý nội dung động.

25.3. Giữ liên kết trong ứng dụng
webView.setWebViewClient(new WebViewClient());

Nếu thiếu dòng này, khi bấm vào một liên kết, Android có thể mở trình duyệt bên ngoài. Khi thêm dòng trên, liên kết tiếp tục được hiển thị trong WebViewActivity.

25.4. Nút tải lại
btnReload.setOnClickListener(v -> webView.reload());

Khi bấm TẢI LẠI TRANG, WebView tải lại nội dung hiện tại.

25.5. Nút quay lại
btnBack.setOnClickListener(v -> finish());

finish() đóng WebViewActivity và quay lại MainActivity.

26. Kiểm tra lại quyền Internet

Bạn đã thêm quyền Internet ở bước trước. Mở:

app
→ manifests
→ AndroidManifest.xml

Kiểm tra hai dòng sau nằm phía trên thẻ <application>:

<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

Nếu đã có rồi thì không cần sửa thêm.

27. Build Project

Nhấn:

Ctrl + F9
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8d112816-2753-4949-9862-28229511e864" />

Kết quả mong đợi:

BUILD SUCCESSFUL

Nếu build thành công, bạn đã hoàn thành code cơ bản của cả 3 Activity:

MainActivity
→ màn hình giới thiệu và điều hướng

BmiActivity
→ tính BMI và gửi kết quả lên API

WebViewActivity
→ hiển thị trang web theo mã sinh viên


## 28. Tạo điện thoại ảo để chạy ứng dụng
Bước 28.1. Mở Device Manager

Ở góc trên bên trái, bấm biểu tượng:

☰

Sau đó chọn:

Tools → Device Manager
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ee8dd4d2-b1a5-4c70-b257-826e87b0f712" />



Theo tài liệu Android, sau khi mở một Project, Device Manager là nơi tạo và quản lý Android Virtual Device, viết tắt là AVD.

Bước 28.2. Tạo thiết bị mới

Trong bảng Device Manager, bấm:

+

sau đó chọn:

Create Virtual Device

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dc31793b-1c93-4ea3-aad8-fec6a7f2eb02" />

Bước 28.3. Chọn mẫu điện thoại

Trong mục:

Phone

chọn một thiết bị phổ biến, ví dụ:

Pixel 6

Sau đó bấm:

Next
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b10eb6d8-7cb2-4bcf-9440-1f264e50a1eb" />

Bạn không nhất thiết phải chọn đúng Pixel 6. Một mẫu Pixel khác cũng sử dụng được.

Bước 28.4. Chọn phiên bản Android

Android Studio sẽ hiển thị danh sách System Image.

Chọn một phiên bản có nút tải xuống, ví dụ:

API 35

hoặc:

API 36
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/81a70692-896c-443c-a07f-cf30f82c19eb" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/63142586-0b9c-4930-92c7-1d8971a53354" />

Nếu bên cạnh phiên bản có biểu tượng tải xuống, bấm vào đó và chờ tải hoàn tất.

Sau đó chọn phiên bản vừa tải và bấm:

Next

Theo hướng dẫn chính thức, quá trình tạo AVD gồm chọn cấu hình phần cứng, chọn system image, kiểm tra cấu hình rồi bấm Finish.

Bước 28.5. Hoàn tất

Giữ nguyên cấu hình mặc định và bấm:

Finish

Điện thoại ảo sẽ xuất hiện trong Device Manager.

29. Chạy ứng dụng
Bước 29.1. Chọn thiết bị

Trên thanh công cụ phía trên Android Studio, bấm vào:

No Devices

Chọn điện thoại ảo vừa tạo, ví dụ:

Pixel 6 API 35
Bước 29.2. Kiểm tra cấu hình chạy

Ngay bên phải danh sách thiết bị, bảo đảm đang chọn:

app
Bước 29.3. Bấm Run

Bấm biểu tượng tam giác màu xanh:

▶

hoặc nhấn:

Shift + F10

Android Studio sẽ:

Khởi động điện thoại ảo
→ Build ứng dụng
→ Cài APK vào điện thoại ảo
→ Mở MainActivity
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ef95e555-15cc-4498-9c4f-98c7e6c28af3" />

Lần đầu khởi động Emulator có thể chậm hơn các lần sau. Android Emulator được tích hợp cùng Android Studio và dùng để kiểm tra ứng dụng trên thiết bị ảo.

30. Kiểm tra từng chức năng
Trường hợp 1. Màn hình chính

Sau khi app mở, bạn cần thấy:

ỨNG DỤNG TÍNH CHỈ SỐ BMI
Sinh viên: Lương Văn Học
Mã sinh viên: K225480106025

[ TÍNH CHỈ SỐ BMI ]
[ XEM THÔNG TIN THAM KHẢO ]
Trường hợp 2. Chuyển sang màn hình tính BMI

Bấm:

TÍNH CHỈ SỐ BMI

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4e85a411-019e-444c-85a5-5b43fd1a06c1" />

Ứng dụng phải mở BmiActivity.

Trường hợp 3. Kiểm tra bỏ trống dữ liệu

Không nhập gì và bấm:

TÍNH BMI

Kết quả mong đợi:

Vui lòng nhập đầy đủ cân nặng và chiều cao
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3e7e752e-ae9a-4a81-aa81-8eb82ce780e0" />

Trường hợp 4. Kiểm tra dữ liệu bằng 0

Nhập:

Cân nặng: 0
Chiều cao: 1.7

Bấm:

TÍNH BMI

Kết quả mong đợi:

Cân nặng và chiều cao phải lớn hơn 0
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a51edfcc-ca7d-4dd9-a69e-032df6bdd525" />

Trường hợp 5. Tính BMI hợp lệ

Nhập:

Cân nặng: 60
Chiều cao: 1.7

Bấm:

TÍNH BMI

Kết quả mong đợi:

Chỉ số BMI của bạn: 20.76
Kết luận: Cân nặng hợp lý

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3a9adea8-73cc-43da-bdd3-dd0423ab2010" />


Nếu kết nối mạng và API hoạt động bình thường, ứng dụng sẽ hiện thêm thông báo gần giống:

Đã gửi API thành công. STT: 1234

Số STT thực tế có thể khác.

Trường hợp 6. Làm mới

Bấm:

LÀM MỚI

Hai ô nhập và kết quả cũ phải được xóa.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9fe699eb-abc5-4a0c-a9ee-98892d88770c" />


Trường hợp 7. Quay lại

Bấm:

QUAY LẠI

Ứng dụng phải trở về màn hình chính.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9fe4e049-f073-47bd-abf7-8c96e32bae19" />


Trường hợp 8. Kiểm tra WebView

Từ màn hình chính, bấm:

XEM THÔNG TIN THAM KHẢO
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2330d4f3-427b-4b6d-bf8f-cd9b217d8b63" />

WebViewActivity phải mở trang:

https://k58kmt.tdh.io.vn?masv=K225480106025

Sau đó kiểm tra:

TẢI LẠI TRANG
QUAY LẠI

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4834a30b-eb5a-4140-b046-b6220798df7e" />

31. Nếu không muốn dùng điện thoại ảo

Bạn cũng có thể dùng điện thoại Android thật.

Trên điện thoại, bật:

Cài đặt
→ Giới thiệu điện thoại
→ bấm nhiều lần vào Số bản dựng
→ mở Tùy chọn nhà phát triển
→ bật Gỡ lỗi USB

Sau đó nối điện thoại với máy tính bằng cáp USB và chấp nhận hộp thoại cho phép gỡ lỗi trên điện thoại. Android Studio có thể chạy và debug ứng dụng trên thiết bị thật thông qua kết nối ADB.

Khi thiết bị xuất hiện thay cho dòng:

No Devices

chọn điện thoại và bấm:

▶ Run













     
