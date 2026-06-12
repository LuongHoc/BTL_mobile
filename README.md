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

# Phần 2. Viết app sử dụng Android Studio
   + Android manifest.xml  => mô tả gì? app cần quyền để do-st: khai báo ntn? để làm gì?
   + vòng đời của 1 ứng dụng android.

     code tự sinh sau khi tạo 1 project: có sẵn hàm onCreate: tại sao???
     
   + Code: java language.

     app cần check xem có quyền để do-st? : code như thế nào? ý nghĩa?
     
     giao diện: (res/layout) mô tả bằng file XML + UI Design review
     
        + thuộc tính text, hoặc các thuộc tính khác: giá trị hardcode => lưu vào nới khác, tham chiếu tới nó:
        + 
          cú pháp của việc tham chiếu là gì?
          
          ưu điểm của việc tham chiếu này?
          
          OS hỗ trợ auto việc lấy giá trị tham chiếu theo LOCATION, LANGUAGE, THEME
          
          việc hỗ trợ auto này giúp app làm được điều gì?
          
        + đối tượng chứa: gộp các đối tượng con lại: cùng 1 quy luật sắp xếp để hiển thị 
          các đối tượng con nằm kề nhau theo chiều dọc | hoặc ngang, gravity
          
     code tương tác với layout: vd hiển thị text
     
          mong muốn text hiển thị phù hợp với thiết lập LOCATION, LANGUAGE, THEME của người dùng
          thì làm ntn? (tránh hardcode)
     
     event (sự kiện) người dùng tác động vào app: CLICK vào button, click vào text,...
     
          với 1 sự kiện nào đó, muốn chạy 1 đoạn code để do-st thì LAYTOUT cần làm gì?
     
              CODE viết như nào (2 cách)
---------------------------
     trong app có các thư mục đặc biệt: Assets
     
     khi sử dụng Window Explorer để copy các files + folder vào trong Assets
     
     thì khi compiler: mọi file này đều đi theo app, nằm trong app
     
     trong app có thể truy cập được đến các file này
     
     cú pháp truy cập vào là gì?
     
     lợi ích của việc app có sẵn các files (offline cũng có)?
     
     ứng dụng: app hướng dẫn việc X

==> tạo app1 sử dụng cơ chế Dữ liệu chuẩn bị trước trong Assets

         format dữ liệu: tuỳ ý, nội dung tuỳ ý
         
         công cụ để hiển thị dữ liệu: tuỳ ý
         
         có cần phải tiền xử lý trước khi hiển thị ko: tuỳ ý.
         
         Sinh viên TỰ ĐẶT RA VẤN ĐỀ => TỰ GIẢI QUYẾT VẤN ĐỀ
         
         MÔ TẢ ĐƯỢC DỮ LIỆU CÓ ĐẶC THÙ GÌ
         
                    DÙNG THUẬT TOÁN NÀO ĐỂ XỬ LÝ DỮ LIỆU (NẾU CẦN)
                    
                    DÙNG ĐỐI TƯỢNG NÀO ĐỂ HIỂN THỊ DỮ LIỆU.
                    
                    (ĐỘ SÁNG TẠO LÀ KO GIỚI HẠN)
------------------------
APP2 (android studio):  tạo app tương đương với Mit App inventor

  app có 3 activity
  
  + activity1: about: about+nút gọi sang 2 activity còn lại
  + activity2: giải toán đơn giản (tuỳ ý). mỗi khi giải xong bài toán: gọi api tại https://k58kmt.tdh.io.vn/api
    để gửi bài toán lên đó
    {app_by:mã số sv, input: {a:1,b:2,c:3,name:"hello tắc kè"},output:{ketluan:"vô nghiệm", abc:"xyz", nghiem:3.14}}
    nhận lại json: {ok:1, stt:1234}
  + activity3: 
    dùng web-view để truy cập từ 
    1 trang web https://k58kmt.tdh.io.vn?masv=mã sv của bạn
# BÀI LÀM

##  Bài toán cần giải quyết

Tính chỉ số BMI

## 1. Tạo dự án

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

### 6.2. Tại sao cần đổi tên thành phần?

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
# A. Lý thuyết

## 1. Tổng quan về Android Studio

### 1.1. Android Studio là gì?

Android Studio là môi trường phát triển tích hợp dùng để xây dựng ứng dụng Android. Công cụ này hỗ trợ lập trình, thiết kế giao diện, kiểm tra lỗi, build ứng dụng và chạy thử trên điện thoại thật hoặc máy ảo Android Emulator.

Trong bài tập này, ứng dụng được viết bằng ngôn ngữ Java. Giao diện được mô tả bằng các file XML trong thư mục:

```text
app/src/main/res/layout
```

### 1.2. Các thành phần chính của một Project Android

Một Project Android cơ bản có cấu trúc:

```text
app
├── manifests
│   └── AndroidManifest.xml
├── java
│   └── com.example.tenungdung
│       └── MainActivity.java
└── res
    ├── layout
    │   └── activity_main.xml
    ├── drawable
    ├── mipmap
    └── values
        ├── strings.xml
        ├── colors.xml
        └── themes.xml
```

Ý nghĩa của một số thư mục:

| Thư mục hoặc file     | Ý nghĩa                                                      |
| --------------------- | ------------------------------------------------------------ |
| `AndroidManifest.xml` | Khai báo thông tin tổng quát, Activity và quyền của ứng dụng |
| `java`                | Chứa code Java xử lý chức năng                               |
| `res/layout`          | Chứa file XML mô tả giao diện                                |
| `res/values`          | Chứa chuỗi, màu sắc và theme                                 |
| `res/drawable`        | Chứa hình ảnh hoặc tài nguyên giao diện                      |
| `assets`              | Chứa file dữ liệu đi kèm ứng dụng                            |

---

## 2. File `AndroidManifest.xml`

### 2.1. Vai trò của `AndroidManifest.xml`

`AndroidManifest.xml` là file khai báo thông tin quan trọng của ứng dụng Android. Hệ điều hành đọc file này để biết ứng dụng gồm những thành phần nào và cần sử dụng những quyền gì.

File Manifest thường được dùng để khai báo:

* Tên package của ứng dụng.
* Các Activity.
* Activity khởi động đầu tiên.
* Quyền truy cập Internet, camera, vị trí hoặc bộ nhớ.
* Icon, tên ứng dụng và theme.
* Một số cấu hình liên quan đến hệ điều hành Android.

### 2.2. Khai báo Activity

Ví dụ:

```xml
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
```

Trong đó:

| Thành phần                 | Ý nghĩa                                     |
| -------------------------- | ------------------------------------------- |
| `android:name`             | Tên class Activity                          |
| `android:exported="false"` | Activity chỉ được mở từ bên trong ứng dụng  |
| `MAIN`                     | Đánh dấu Activity khởi động chính           |
| `LAUNCHER`                 | Cho phép mở Activity từ biểu tượng ứng dụng |

### 2.3. Khai báo quyền truy cập

Ứng dụng muốn sử dụng một số chức năng của thiết bị hoặc hệ điều hành phải khai báo quyền trong Manifest.

Ví dụ, ứng dụng BMI cần Internet để gửi dữ liệu lên API và tải trang WebView:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Hai dòng này phải đặt phía trên thẻ:

```xml
<application>
```

Ví dụ đầy đủ:

```xml
<manifest xmlns:android="http://schemas.android.com/apk/res/android">

    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

    <application
        ... >
    </application>

</manifest>
```

### 2.4. Quyền thông thường và quyền nhạy cảm

Không phải quyền nào cũng cần hỏi người dùng khi ứng dụng đang chạy.

#### 2.4.1. Quyền thông thường

Một số quyền chỉ cần khai báo trong Manifest. Hệ điều hành không hiển thị hộp thoại xin phép người dùng.

Ví dụ:

```xml
<uses-permission android:name="android.permission.INTERNET" />
```

Ứng dụng BMI chỉ cần khai báo quyền Internet, không cần viết code xin quyền khi chạy.

#### 2.4.2. Quyền nhạy cảm

Các quyền liên quan đến dữ liệu cá nhân hoặc thiết bị nhạy cảm cần được kiểm tra và xin phép khi chạy ứng dụng.

Ví dụ:

```xml
<uses-permission android:name="android.permission.CAMERA" />
```

Code Java kiểm tra quyền camera:

```java
if (ContextCompat.checkSelfPermission(
        this,
        Manifest.permission.CAMERA
) != PackageManager.PERMISSION_GRANTED) {

    ActivityCompat.requestPermissions(
            this,
            new String[]{Manifest.permission.CAMERA},
            100
    );
}
```

Ý nghĩa:

```text
Kiểm tra quyền camera
→ Nếu chưa được cấp
→ Hiển thị hộp thoại xin quyền
```

---

## 3. Vòng đời của Activity

### 3.1. Activity là gì?

Activity thường đại diện cho một màn hình của ứng dụng Android.

Ví dụ trong ứng dụng BMI:

| Activity          | Màn hình               |
| ----------------- | ---------------------- |
| `MainActivity`    | Màn hình giới thiệu    |
| `BmiActivity`     | Màn hình tính BMI      |
| `WebViewActivity` | Màn hình xem trang web |

### 3.2. Các trạng thái vòng đời chính

Một Activity không chạy liên tục từ đầu đến cuối. Hệ điều hành Android quản lý Activity thông qua các hàm vòng đời.

Các hàm quan trọng:

| Hàm           | Thời điểm được gọi                    | Mục đích thường dùng               |
| ------------- | ------------------------------------- | ---------------------------------- |
| `onCreate()`  | Activity vừa được tạo                 | Khởi tạo giao diện và biến         |
| `onStart()`   | Activity bắt đầu hiển thị             | Chuẩn bị tài nguyên                |
| `onResume()`  | Activity sẵn sàng tương tác           | Tiếp tục thao tác đang tạm dừng    |
| `onPause()`   | Activity mất một phần quyền tương tác | Lưu trạng thái tạm thời            |
| `onStop()`    | Activity không còn hiển thị           | Dừng các công việc không cần thiết |
| `onDestroy()` | Activity bị hủy                       | Giải phóng tài nguyên              |

Sơ đồ đơn giản:

```text
onCreate()
    ↓
onStart()
    ↓
onResume()
    ↓
Người dùng tương tác với ứng dụng
    ↓
onPause()
    ↓
onStop()
    ↓
onDestroy()
```

Nếu người dùng quay lại một Activity đã dừng, Android có thể gọi:

```text
onRestart()
→ onStart()
→ onResume()
```

### 3.3. Tại sao code tự sinh có hàm `onCreate()`?

Khi tạo một Project hoặc Activity mới, Android Studio tự sinh code gần giống:

```java
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
}
```

Lý do là `onCreate()` được gọi khi hệ điều hành tạo Activity. Đây là vị trí phù hợp để:

* Gắn file XML vào Activity.
* Tìm các View theo ID.
* Khởi tạo biến.
* Đăng ký sự kiện click.
* Chuẩn bị dữ liệu ban đầu.

Dòng:

```java
setContentView(R.layout.activity_main);
```

có nghĩa là Activity sử dụng giao diện nằm trong file:

```text
res/layout/activity_main.xml
```

---

## 4. Thiết kế giao diện bằng XML

### 4.1. Vai trò của thư mục `res/layout`

Giao diện ứng dụng thường được khai báo trong các file XML thuộc thư mục:

```text
app/src/main/res/layout
```

Ví dụ:

```text
activity_main.xml
activity_bmi.xml
activity_web_view.xml
```

File XML giúp tách phần giao diện khỏi code xử lý Java.

### 4.2. Các thành phần giao diện cơ bản

Ví dụ một nút bấm:

```xml
<Button
    android:id="@+id/btnCalculate"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:text="@string/btn_calculate" />
```

Ý nghĩa:

| Thuộc tính      | Ý nghĩa                                      |
| --------------- | -------------------------------------------- |
| `android:id`    | Định danh thành phần để Java có thể tìm thấy |
| `layout_width`  | Chiều rộng của thành phần                    |
| `layout_height` | Chiều cao của thành phần                     |
| `android:text`  | Nội dung hiển thị                            |
| `match_parent`  | Kích thước bằng thành phần cha               |
| `wrap_content`  | Kích thước vừa đủ nội dung                   |

### 4.3. Design, Code và Split

Android Studio hỗ trợ ba chế độ chỉnh sửa layout:

| Chế độ   | Chức năng                    |
| -------- | ---------------------------- |
| `Code`   | Viết XML trực tiếp           |
| `Design` | Thiết kế giao diện trực quan |
| `Split`  | Vừa xem XML vừa xem Preview  |

Người lập trình có thể kéo thả thành phần trong giao diện Design hoặc sửa trực tiếp code XML.

---

## 5. Đối tượng chứa và cách sắp xếp giao diện

### 5.1. View và ViewGroup

Các thành phần giao diện như `TextView`, `Button`, `EditText` được gọi là `View`.

Các đối tượng chứa nhiều View con được gọi là `ViewGroup`.

Ví dụ:

```text
LinearLayout
ScrollView
ConstraintLayout
```

### 5.2. `LinearLayout`

`LinearLayout` sắp xếp các View con theo một chiều nhất định.

Ví dụ sắp xếp theo chiều dọc:

```xml
<LinearLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">
</LinearLayout>
```

Giá trị:

```xml
android:orientation="vertical"
```

có nghĩa là các thành phần được xếp từ trên xuống dưới.

Nếu sử dụng:

```xml
android:orientation="horizontal"
```

các thành phần được xếp từ trái sang phải.

### 5.3. Thuộc tính `gravity`

Thuộc tính `gravity` dùng để căn nội dung bên trong đối tượng chứa.

Ví dụ:

```xml
android:gravity="center"
```

Nội dung được căn giữa.

Một số giá trị thường dùng:

| Giá trị             | Ý nghĩa                   |
| ------------------- | ------------------------- |
| `center`            | Căn giữa                  |
| `center_horizontal` | Căn giữa theo chiều ngang |
| `center_vertical`   | Căn giữa theo chiều dọc   |
| `start`             | Căn về đầu                |
| `end`               | Căn về cuối               |

### 5.4. `ScrollView`

`ScrollView` cho phép cuộn màn hình khi nội dung dài hơn kích thước điện thoại.

Ví dụ:

```xml
<ScrollView
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical">
    </LinearLayout>

</ScrollView>
```

---

## 6. Tránh hardcode bằng tài nguyên tham chiếu

### 6.1. Hardcode là gì?

Hardcode là ghi trực tiếp nội dung vào layout hoặc code Java.

Ví dụ:

```xml
android:text="TÍNH BMI"
```

Cách này vẫn chạy được nhưng khó quản lý khi ứng dụng có nhiều màn hình hoặc cần hỗ trợ nhiều ngôn ngữ.

### 6.2. Lưu chuỗi trong `strings.xml`

Nên lưu nội dung vào:

```text
res/values/strings.xml
```

Ví dụ:

```xml
<resources>
    <string name="btn_calculate">TÍNH BMI</string>
</resources>
```

Sau đó tham chiếu từ layout:

```xml
android:text="@string/btn_calculate"
```

### 6.3. Ưu điểm của tài nguyên tham chiếu

Sử dụng tài nguyên tham chiếu có các lợi ích:

* Tránh lặp lại nội dung trong nhiều file.
* Dễ sửa nội dung.
* Hỗ trợ nhiều ngôn ngữ.
* Hỗ trợ các cấu hình màn hình khác nhau.
* Hỗ trợ giao diện sáng và tối.
* Giúp code dễ đọc và dễ bảo trì.

### 6.4. Hệ điều hành tự chọn tài nguyên phù hợp

Android có thể tự động chọn tài nguyên dựa trên cấu hình thiết bị.

Ví dụ hỗ trợ tiếng Việt:

```text
res/values/strings.xml
res/values-vi/strings.xml
```

Ví dụ hỗ trợ giao diện ban đêm:

```text
res/values/colors.xml
res/values-night/colors.xml
```

Ví dụ hỗ trợ giao diện khi xoay ngang:

```text
res/layout/activity_main.xml
res/layout-land/activity_main.xml
```

Khi người dùng thay đổi ngôn ngữ, chế độ sáng tối hoặc hướng màn hình, hệ điều hành lựa chọn tài nguyên phù hợp.

---

## 7. Tương tác giữa code Java và layout

### 7.1. Gắn layout vào Activity

Trong `onCreate()`, sử dụng:

```java
setContentView(R.layout.activity_bmi);
```

Dòng này gắn file:

```text
activity_bmi.xml
```

vào `BmiActivity`.

### 7.2. Tìm thành phần giao diện theo ID

Trong XML:

```xml
<EditText
    android:id="@+id/edtWeight"
    ... />
```

Trong Java:

```java
EditText edtWeight = findViewById(R.id.edtWeight);
```

Sau đó có thể lấy dữ liệu:

```java
String weightText = edtWeight.getText().toString();
```

### 7.3. Hiển thị nội dung lên giao diện

Trong XML:

```xml
<TextView
    android:id="@+id/tvResult"
    ... />
```

Trong Java:

```java
TextView tvResult = findViewById(R.id.tvResult);
tvResult.setText("Kết quả");
```

Tuy nhiên, để tránh hardcode, nên dùng:

```java
tvResult.setText(R.string.evaluation_normal);
```

Hoặc:

```java
String message = getString(R.string.bmi_result_format, bmi);
tvResult.setText(message);
```

### 7.4. Ý nghĩa của `R`

Android tự sinh class `R` để tham chiếu tới tài nguyên.

Ví dụ:

```java
R.layout.activity_main
R.id.btnCalculate
R.string.btn_calculate
```

Ý nghĩa:

| Cú pháp                  | Tài nguyên                |
| ------------------------ | ------------------------- |
| `R.layout.activity_main` | File layout               |
| `R.id.btnCalculate`      | ID của một View           |
| `R.string.btn_calculate` | Chuỗi trong `strings.xml` |

---

## 8. Xử lý sự kiện người dùng

### 8.1. Sự kiện là gì?

Sự kiện là hành động của người dùng đối với ứng dụng.

Ví dụ:

* Bấm Button.
* Chạm vào TextView.
* Nhập dữ liệu.
* Chọn một mục.
* Vuốt màn hình.

Khi một sự kiện xảy ra, ứng dụng có thể chạy một đoạn code tương ứng.

### 8.2. Cách 1: Dùng `setOnClickListener()`

Đây là cách được sử dụng trong ứng dụng BMI.

Trong XML, Button cần có ID:

```xml
<Button
    android:id="@+id/btnCalculate"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:text="@string/btn_calculate" />
```

Trong Java:

```java
Button btnCalculate = findViewById(R.id.btnCalculate);

btnCalculate.setOnClickListener(v -> {
    calculateBmi();
});
```

Ý nghĩa:

```text
Khi người dùng bấm btnCalculate
→ Chạy hàm calculateBmi()
```

### 8.3. Cách 2: Khai báo `android:onClick` trong XML

Trong XML:

```xml
<Button
    android:id="@+id/btnCalculate"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:text="@string/btn_calculate"
    android:onClick="calculateBmiFromXml" />
```

Trong Java:

```java
public void calculateBmiFromXml(View view) {
    // Viết code xử lý tại đây
}
```

Khi người dùng bấm nút, Android gọi hàm:

```java
calculateBmiFromXml()
```

### 8.4. So sánh hai cách xử lý sự kiện

| Cách                   | Ưu điểm                            | Hạn chế                          |
| ---------------------- | ---------------------------------- | -------------------------------- |
| `setOnClickListener()` | Linh hoạt, dễ kiểm soát trong Java | Code dài hơn một chút            |
| `android:onClick`      | Khai báo nhanh trong XML           | Khó quản lý hơn khi ứng dụng lớn |

Trong ứng dụng BMI, sử dụng:

```java
setOnClickListener()
```

giúp tập trung phần xử lý sự kiện trong code Java.

---

## 9. Thư mục `assets`

### 9.1. Vai trò của `assets`

`assets` là thư mục đặc biệt dùng để chứa các file dữ liệu đi kèm ứng dụng.

Ví dụ:

```text
app/src/main/assets
├── huong_dan_bmi.json
├── gioi_thieu.txt
├── index.html
└── images
    └── bmi_chart.png
```

Các file trong `assets` được đóng gói cùng ứng dụng khi build.

### 9.2. Tạo thư mục `assets`

Trong Android Studio:

```text
Nhấp chuột phải vào app/src/main
→ New
→ Folder
→ Assets Folder
```

Sau đó copy file dữ liệu vào thư mục:

```text
app/src/main/assets
```

### 9.3. Đọc file từ `assets` bằng Java

Ví dụ đọc file văn bản:

```java
InputStream inputStream =
        getAssets().open("gioi_thieu.txt");

BufferedReader reader =
        new BufferedReader(
                new InputStreamReader(inputStream)
        );

StringBuilder builder = new StringBuilder();
String line;

while ((line = reader.readLine()) != null) {
    builder.append(line).append("\n");
}

reader.close();

String content = builder.toString();
```

### 9.4. Đọc file trong thư mục con

Nếu file nằm trong:

```text
assets/data/huong_dan_bmi.json
```

thì cú pháp:

```java
getAssets().open("data/huong_dan_bmi.json");
```

### 9.5. Truy cập file HTML trong WebView

Nếu file nằm trong:

```text
assets/index.html
```

có thể hiển thị bằng:

```java
webView.loadUrl("file:///android_asset/index.html");
```

### 9.6. Lợi ích của dữ liệu trong `assets`

Dữ liệu trong `assets` có các ưu điểm:

* Được đóng gói cùng ứng dụng.
* Có thể sử dụng khi không có Internet.
* Phù hợp với tài liệu hướng dẫn offline.
* Có thể lưu file JSON, TXT, HTML hoặc hình ảnh.
* Giữ nguyên cấu trúc thư mục con.
* Dễ sử dụng cho dữ liệu chuẩn bị trước.

### 9.7. Hạn chế

Một số hạn chế:

* Làm tăng kích thước ứng dụng.
* Muốn cập nhật dữ liệu phải build và phát hành lại app.
* Không phù hợp với dữ liệu thay đổi thường xuyên.

---

## 10. Liên hệ với ứng dụng BMI đã xây dựng

### 10.1. Sử dụng `AndroidManifest.xml`

Ứng dụng BMI khai báo:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

để gửi JSON lên API và tải nội dung WebView.

### 10.2. Sử dụng `onCreate()`

Trong mỗi Activity, `onCreate()` được dùng để:

* Gắn layout.
* Tìm View theo ID.
* Khởi tạo Button.
* Đăng ký sự kiện click.
* Tải trang WebView.

### 10.3. Sử dụng XML

Ứng dụng có 3 file layout:

```text
activity_main.xml
activity_bmi.xml
activity_web_view.xml
```

### 10.4. Sử dụng tài nguyên chuỗi

Nội dung được lưu trong:

```text
res/values/strings.xml
```

và tham chiếu bằng:

```xml
@string/ten_tai_nguyen
```

### 10.5. Xử lý sự kiện

Các nút được xử lý bằng:

```java
setOnClickListener()
```

Ví dụ:

```java
btnReset.setOnClickListener(v -> resetForm());
btnBack.setOnClickListener(v -> finish());
```

### 10.6. Gửi dữ liệu lên API

Sau khi tính BMI, ứng dụng gửi JSON bằng phương thức:

```text
POST
```

tới:

```text
https://k58kmt.tdh.io.vn/api/
```

### 10.7. Hiển thị WebView

Ứng dụng tải trang:

```text
https://k58kmt.tdh.io.vn/?masv=K225480106025
```

bằng:

```java
webView.loadUrl(WEB_URL);
```

---

## 11. Kết luận

Qua phần lý thuyết, có thể thấy một ứng dụng Android gồm nhiều thành phần phối hợp với nhau:

```text
AndroidManifest.xml
→ Khai báo Activity và quyền

XML Layout
→ Mô tả giao diện

strings.xml
→ Quản lý nội dung hiển thị

Java Activity
→ Xử lý chức năng và sự kiện

assets
→ Lưu dữ liệu chuẩn bị trước để sử dụng offline
```

Việc tách riêng giao diện, tài nguyên và code xử lý giúp ứng dụng rõ ràng, dễ bảo trì và dễ mở rộng.


# B. Thực hành

# 1. Giới thiệu

## 1.1. Tên đề tài

```text
ỨNG DỤNG TÍNH CHỈ SỐ BMI
```

## 1.2. Thông tin sinh viên

```text
Họ và tên: Lương Văn Học
Mã sinh viên: K225480106025
```

## 1.3. Mục tiêu thực hiện

Ứng dụng được xây dựng bằng **Android Studio**, sử dụng ngôn ngữ **Java** và giao diện **XML**.  

Ứng dụng có chức năng tính chỉ số BMI dựa trên cân nặng và chiều cao, gửi kết quả lên API và hiển thị trang thông tin sinh viên bằng `WebView`.

### 1.4. Cấu trúc ứng dụng

Ứng dụng gồm 3 Activity:

| Activity | Chức năng |
|---|---|
| `MainActivity` | Hiển thị thông tin giới thiệu và chứa nút mở 2 Activity còn lại |
| `BmiActivity` | Nhập cân nặng, chiều cao, tính BMI, phân loại kết quả và gửi JSON lên API |
| `WebViewActivity` | Hiển thị trang web thông tin sinh viên bằng `WebView` |

# 2. Tạo Project Android Studio

## 2.1. Khởi tạo Project mới

Mở Android Studio.

Nếu đang ở màn hình chào mừng, bấm:
```
New Project
```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/d17d7e37-739c-4123-b5a3-4eea11bc05d8" />

### 2.1.1. Chọn mẫu Project

Trong danh sách mẫu, chọn:

Phone and Tablet → Empty Views Activity

Sau đó bấm: Next

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/469019db-344c-42c0-b834-184770de8e23" />

Empty Views Activity:	Dùng Java và file giao diện XML

### 2.1.2. Điền thông tin Project

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

## 2.2. Kiểm tra Project đã tạo thành công

Ở cột bên trái, chọn chế độ hiển thị: ```Android```

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

# 3. Tạo các Activity

## 3.1. Tạo BmiActivity

### 3.1.1. Mở chức năng tạo Activity

Ở cột bên trái, mở:

```
app
└── java
    └── com.example.bmicalculator
```

Nhấp chuột phải vào: ```com.example.bmicalculator```

Chọn:
```
New → Activity → Empty Views Activity
```

Android Studio có thể tự tạo Activity, file layout XML và cập nhật Manifest khi bạn sử dụng thao tác này.

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/6093016f-db78-487b-88cb-c3034bf0e84e" />


### 3.1.2. Cấu hình BmiActivity

Trong cửa sổ hiện ra, nhập:

| Mục | Giá trị |
|------|----------|
| Activity Name | BmiActivity |
| Layout Name | activity_bmi |
| Source Language | Java |
| Launcher Activity | Không chọn |

Bấm: Finish

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f8099754-3f67-4288-914b-d4dd6faf067a" />

## 3.2. Tạo WebViewActivity

Làm tương tự:

Nhấp chuột phải vào:

```
com.example.bmicalculator
```

Chọn:

```
New → Activity → Empty Views Activity
```

Nhập:

| Mục | Giá trị |
|------|----------|
| Activity Name | WebViewActivity |
| Layout Name | activity_web_view |
| Source Language | Java |
| Launcher Activity | Không chọn |

Bấm: Finish

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8233818b-9973-4764-905a-5ca73f2780b6" />

## 3.3. Kiểm tra cấu trúc sau khi tạo 3 Activity

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

```
app → manifests → AndroidManifest.xml
```

Sẽ thấy 3 Activity đã được khai báo:

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/28f80d75-fdb2-44dd-aed8-8cd2e0be5898" />

MainActivity là màn hình khởi động nên có intent-filter chứa MAIN và LAUNCHER. Hai Activity còn lại được mở từ bên trong ứng dụng nên chưa cần intent-filter. Activity không khai báo intent-filter chỉ có thể được khởi chạy bằng Intent tường minh.


# 4. Khai báo trong `AndroidManifest.xml`

## 4.1. Vai trò của `AndroidManifest.xml`

`AndroidManifest.xml` dùng để khai báo:

- Các Activity trong ứng dụng.
- Activity nào được mở đầu tiên.
- Các quyền mà ứng dụng cần sử dụng.
- Một số thông tin cấu hình chung của app.

## 4.2. Khai báo quyền Internet

### 4.2.1. Lý do cần quyền Internet

Ứng dụng cần Internet để:

- Gửi kết quả BMI lên API.
- Hiển thị trang web trong `WebViewActivity`.

### 4.2.2. Thêm quyền vào Manifest

**Mở Manifest**

Ở cây thư mục bên trái, mở:

```
app → manifests → AndroidManifest.xml
```

**Thêm hai dòng quyền**

Ngay bên dưới thẻ mở <manifest> và phía trên <application>, thêm:

```
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/26a2fa33-7fac-4951-bc6c-fd7993d757ce" />

Nhấn:

Ctrl + S

## 4.3. Khai báo các Activity

Nội dung `AndroidManifest.xml`:

```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">

    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.BMICalculator">

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

</manifest>

```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0b51d1e8-e7b7-4450-8dbe-dab91863b496" />

# 5. Khai báo tài nguyên chuỗi trong `strings.xml`

## 5.1. Lý do sử dụng `strings.xml`

Nếu ghi trực tiếp nội dung trong XML, Android Studio sẽ cảnh báo hardcode.  

Để dễ quản lý và hỗ trợ nhiều ngôn ngữ, nội dung hiển thị được lưu trong:

```text
app → res → values → strings.xml
```

## 5.2. Cú pháp tham chiếu chuỗi

Trong XML, tham chiếu chuỗi bằng cú pháp:

```xml
@string/ten_tai_nguyen
```

## 5.3. Nội dung file `strings.xml`

**Mở file strings.xml**

Ở cây thư mục bên trái, bấm:
```
app → res → values → strings.xml
```

**Chuyển sang chế độ Code**

Nếu Android Studio mở giao diện khác, bấm biểu tượng ba dòng ngang ở góc trên bên phải để chuyển sang chế độ viết code.

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

    <!-- Nội dung thông báo và kết quả BMI -->
    <string name="error_empty">Vui lòng nhập đầy đủ cân nặng và chiều cao</string>
    <string name="error_positive">Cân nặng và chiều cao phải lớn hơn 0</string>
    <string name="error_invalid_number">Dữ liệu nhập không hợp lệ</string>

    <string name="bmi_result_format">Chỉ số BMI của bạn: %.2f</string>
    <string name="evaluation_underweight">Kết luận: Thiếu cân</string>
    <string name="evaluation_normal">Kết luận: Cân nặng hợp lý</string>
    <string name="evaluation_overweight">Kết luận: Thừa cân</string>
    <string name="evaluation_obese">Kết luận: Béo phì</string>

    <!-- Nội dung màn hình WebView -->
    <string name="web_view_title">TRANG THÔNG TIN THAM KHẢO</string>
    <string name="btn_reload">TẢI LẠI TRANG</string>
</resources>
```
Nhấn: ```Ctrl + S``` để lưu.

# 6. Thiết kế giao diện MainActivity

## 6.1. Thiết kế giao diện `activity_main.xml`

### 6.1.1. Mở file giao diện

Ở cây thư mục bên trái, mở:

```
app → res → layout → activity_main.xml
```

### 6.1.2. Chuyển sang chế độ viết XML

Ở góc trên bên phải của vùng chỉnh sửa giao diện, chọn: ```Code```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/591c469a-ee5a-4122-b9e3-b69bb5efbc97" />

### 6.1.3. Nội dung file XML

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
Nhấn: ```Ctrl + S```

### 6.1.4 Kiểm tra giao diện

Sau khi dán xong, chọn: ```Design or Split``` để xem trước giao diện.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6b573a14-7ca4-4971-8c0b-809c79a9ae6d" />


## 6.2. Viết code điều hướng trong `MainActivity.java`

### 6.2.1. Mở file Java

Ở cây thư mục bên trái, bấm:

app → kotlin+java → com.example.bmicalculator → MainActivity

Tệp được mở là: ```MainActivity.java```

### 6.2.2. Dán code 

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
Nhấn: ```Ctrl + S``` để lưu file.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4a5befad-09bf-4549-9fa9-ebc7d45bc64b" />


# 7. Xây dựng `BmiActivity`

## 7.1. Thiết kế giao diện `activity_bmi.xml`

### 7.1.1. Thành phần giao diện

Màn hình gồm:

- Ô nhập cân nặng.
- Ô nhập chiều cao.
- Nút tính BMI.
- Nút làm mới.
- Vùng hiển thị BMI.
- Vùng hiển thị kết luận.
- Nút quay lại.

### 7.1.2. Nội dung file XML

**Mở file activity_bmi.xml**

Ở cây thư mục bên trái, mở:

```
app → res → layout → activity_bmi.xml
```

Chuyển sang chế độ viết XML bằng biểu tượng ba dòng ngang ở góc trên bên phải vùng chỉnh sửa.

 **Nội dung file XML**
 
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

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1b7fb6e9-c08e-4cb3-b4c5-23b081e0a3ce" />


Nhấn: ```Ctrl + S```

**Xem giao diện**

Bấm biểu tượng Design hoặc Split ở góc trên bên phải.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3580990a-ad24-431a-b31d-273a51d6e040" />

## 7.2. Viết code xử lý BMI

### 7.2.1. Công thức BMI

```text
BMI = cân nặng / (chiều cao × chiều cao)
```

### 7.2.2. Kiểm tra dữ liệu đầu vào

Ứng dụng kiểm tra:

- Người dùng có bỏ trống ô nhập hay không.
- Cân nặng và chiều cao có lớn hơn `0` hay không.
- Dữ liệu có chuyển đổi được sang kiểu số hay không.

### 7.2.3. Phân loại kết quả

| Giá trị BMI | Kết luận |
|---:|---|
| `< 18.5` | Thiếu cân |
| `< 25` | Cân nặng hợp lý |
| `< 30` | Thừa cân |
| `>= 30` | Béo phì |

## 7.3. Gửi dữ liệu lên API

### 7.3.1. Endpoint

Ứng dụng gửi JSON bằng phương thức `POST` tới:

```text
https://k58kmt.tdh.io.vn/api/
```

### 7.3.2. Cấu trúc JSON gửi đi

```json
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
```

### 7.3.3. Viết code xử lý trong BmiActivity.java

**Mở BmiActivity.java**

Ở cây thư mục bên trái, chọn:

app → kotlin+java → com.example.bmicalculator → BmiActivity

**Dán code xử lý BMI**

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

    private static final String API_URL = "https://k58kmt.tdh.io.vn/api/";
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

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/462d1b46-bf57-4959-934e-a26a6fbde42a" />


Nhấn: ```Ctrl + S```

# 8. Xây dựng `WebViewActivity`

## 8.1. Thiết kế giao diện `activity_web_view.xml`

### 8.1.1. Thành phần giao diện

Màn hình gồm:

- Tiêu đề.
- `WebView`.
- Nút tải lại trang.
- Nút quay lại.

### 8.1.2. Nội dung XML

**Mở file giao diện**

Ở cây thư mục bên trái, mở:

```
app → res → layout → activity_web_view.xml
```

Chuyển sang chế độ Code

Dán toàn bộ đoạn sau:

```
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
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/38fd9a2d-6564-413c-8cf7-fde88efca254" />

Nhấn: ```Ctrl + S```

**Kiểm tra giao diện WebView**

Chuyển sang chế độ:
```
Design hoặc Split
```


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/708ec5e7-db42-4464-80f1-5b71404a051a" />

## 8.2. Viết code `WebViewActivity.java`

### 8.2.1. URL truy cập

```text
https://k58kmt.tdh.io.vn/?masv=K225480106025
```

### 8.2.2. Cấu hình WebView

- Cho phép JavaScript.
- Bật DOM Storage.
- Giữ trang web hiển thị trong ứng dụng.
- Tạo nút tải lại và quay lại.

### 8.2.3. Code hoàn chỉnh

**Mở file Java**

Ở cây thư mục bên trái, mở:

```
app → kotlin+java → com.example.bmicalculator → WebViewActivity
```

**Dán toàn bộ đoạn sau:**

```
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
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9f733a2e-ca10-4d2c-917e-5a7d21d7251c" />


Nhấn: ```Ctrl + S```

# 9. Build và chạy ứng dụng

## 9.1. Build Project

### 9.1.1. Thực hiện Build

Nhấn:

```text
Ctrl + F9
```

### 9.1.2. Kiểm tra kết quả

Thành công, Android Studio hiển thị:

```text
BUILD SUCCESSFUL
```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/b6c17e9c-75bc-47c9-b059-37055dadba81" />

## 9.2. Tạo máy ảo Android

### 9.2.1. Mở Device Manager

Ở góc trên bên trái, bấm biểu tượng: ☰

Sau đó chọn: 
```
Tools → Device Manager
```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/436c8137-fe9d-48ed-ab7d-eb8aee8af71a" />


### 9.2.2. Tạo thiết bị mới

Chọn:

```text
+ → Create Virtual Device
```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/5e8dbe2e-0f02-414a-b731-3fc5298717e6" />


### 9.2.3. Chọn thiết bị

Trong mục:
```
Phone
```
chọn một thiết bị bất kì, ở đây em chọn

```
Pixel 6
```
Sau đó bấm: ```Next```

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/3132bd84-c818-44f2-812b-e7a7b4526d6b" />

### 9.2.4. Chọn phiên bản Android

Android Studio sẽ hiển thị danh sách System Image.

Chọn một phiên bản có nút tải xuống, ở đây em chọn  :

```
API 36
```

<img width="1980" height="986" alt="image" src="https://github.com/user-attachments/assets/e10dc20a-ed95-416e-adf9-f345764b039f" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/63142586-0b9c-4930-92c7-1d8971a53354" />

Nếu bên cạnh phiên bản có biểu tượng tải xuống, bấm vào đó và chờ tải hoàn tất.

Sau đó chọn phiên bản vừa tải và bấm: ```Next```


### 9.2.5. Hoàn tất

Giữ nguyên cấu hình mặc định và bấm: ```Finish```

Điện thoại ảo sẽ xuất hiện trong Device Manager.

<img width="1980" height="1080" alt="image" src="https://github.com/user-attachments/assets/938bdc40-5da5-4add-82e0-98f56e4a24e8" />

# 10. Kiểm tra chức năng

## 10.1. Run

Chọn điện thoại ảo vừa tạo:

```
Pixel 6 API 36
```

Bấm Run

- Bấm biểu tượng tam giác màu xanh: ▶

- Hoặc nhấn: ```Shift + F10```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/871c3fe1-632f-4f1d-977e-309978c0ae83" />


## 10.2. Kiểm tra màn hình chính

### 10.2.1. Nội dung hiển thị

Màn hình chính hiển thị:

```text
ỨNG DỤNG TÍNH CHỈ SỐ BMI
Sinh viên: Lương Văn Học
Mã sinh viên: K225480106025
```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/152befe5-d35a-4d31-8ebf-ff4f449588e3" />

### 10.2.2. Kiểm tra nút điều hướng

Hai nút:

```text
TÍNH CHỈ SỐ BMI
XEM THÔNG TIN THAM KHẢO
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/94249fe3-b89d-4711-a025-fcd58c1948f9" />

***Giao diện TÍNH CHỈ SỐ BMI***

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1cea9ea1-bb99-4712-8748-5779e5b33448" />

***Giao diện XEM THÔNG TIN THAM KHẢO***

## 10.3. Kiểm tra màn hình tính BMI

### 10.3.1. Trường hợp bỏ trống dữ liệu

Không nhập dữ liệu và bấm:

```text
TÍNH BMI
```

Kết quả:

```text
Vui lòng nhập đầy đủ cân nặng và chiều cao
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ed044d97-a719-4f71-a01d-be36997459d4" />

### 10.3.2. Trường hợp nhập giá trị bằng `0`

Nhập:

```text
Cân nặng: 0
Chiều cao: 1.7
```

Kết quả:

```text
Cân nặng và chiều cao phải lớn hơn 0
```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/810d5f66-095e-45d9-ba85-a0157ad6a3f0" />


### 10.3.3. Trường hợp dữ liệu hợp lệ

Nhập:

```text
Cân nặng: 60
Chiều cao: 1.7
```

Kết quả:

```text
Chỉ số BMI của bạn: 20.76
Kết luận: Cân nặng hợp lý
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8bfba984-4135-4689-9caa-d9eff897e11b" />

## 10.4. Kiểm tra gửi API
### 10.4.1. Thông báo gửi thành công

Sau khi tính BMI, ứng dụng hiển thị:

```text
Đã gửi kết quả lên API
```
<img width="1578" height="894" alt="image" src="https://github.com/user-attachments/assets/60d667d3-79cc-47f7-839f-9bc379279867" />

### 10.4.2. Kiểm tra JSON LOG

Trang log hiển thị dữ liệu có:

```text
app_by = K225480106025
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c224d7bd-2145-444f-943b-05cbd504669b" />


## 10.5. Kiểm tra nút làm mới và quay lại

### 10.5.1. Nút làm mới

Bấm:

```text
LÀM MỚI
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5e205d43-e706-4a9b-8c2f-9f94e387e790" />

***Hai ô nhập và kết quả cũ được xóa.***

### 10.5.2. Nút quay lại

Bấm:

```text
QUAY LẠI
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/43ed5a66-175d-42da-8603-9393074b5feb" />

***Ứng dụng trở về màn hình chính.***


## 10.6. Kiểm tra WebView

### 10.6.1. Mở trang tham khảo

Từ màn hình chính, bấm:

```text
XEM THÔNG TIN THAM KHẢO
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c59e99ac-db5a-4235-89b1-c81c097c2275" />


### 10.6.2. Kiểm tra SV LOG

Sau khi WebView tải trang, số lượt truy cập trong `SV LOG` tăng lên.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8433805c-39aa-49cf-941d-7c78728e9a36" />

# 11. Kết quả đạt được

## 11.1. Chức năng đã hoàn thành

Ứng dụng đã đáp ứng các yêu cầu:

- Có 3 Activity.
- `MainActivity` giới thiệu ứng dụng và điều hướng.
- `BmiActivity` kiểm tra dữ liệu, tính BMI và phân loại kết quả.
- Kết quả BMI được gửi lên API bằng phương thức `POST`.
- `WebViewActivity` hiển thị trang web theo mã sinh viên bằng phương thức `GET`.
- `JSON LOG` ghi nhận dữ liệu đã gửi.
- `SV LOG` tăng khi truy cập trang WebView.
- Project build thành công và chạy được trên máy ảo Android.

## 11.2. Kết luận

Qua bài thực hành, em đã xây dựng được một ứng dụng Android hoàn chỉnh bằng Java và XML, biết cách:

- Tổ chức nhiều Activity.
- Thiết kế giao diện bằng XML.
- Sử dụng tài nguyên chuỗi trong `strings.xml`.
- Xử lý sự kiện Button.
- Gửi JSON lên API.
- Hiển thị trang web bằng `WebView`.
- Build và kiểm thử ứng dụng trên Android Emulator.





































     
