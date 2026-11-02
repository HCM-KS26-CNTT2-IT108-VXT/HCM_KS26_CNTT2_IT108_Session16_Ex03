## <span style="color: red;"> Bài 3: Xử Lý Sự Cố Giao Diện Website Doanh Nghiệp </span>

### Phần 1: Báo Cáo Phân Tích (I/O)

*1.Nguyên nhân lỗi*

- Qua kiểm tra bằng F12 và tab computed thì chúng ta có thể thấy hai khung bị chồng lên nhau do margin âm và kích thước các phần tử chưa hợp lý.

*2.  Phân Tích Box Model*

- Content : Phần nội dung bên trong.
- Padding : Khoảng cách giữa nội dung và viền, 15px.
- Border: Đường viền, 2px.
- Margin: Khoảng cách bên ngoài, đang có giá trị âm làm hai khung bị lệch.

<u>Nhận diện lỗi:</u>

- Khung nội dung bài học bị chồng lấn với khung Danh sách video.

- Margin đang có giá trị âm (-10px, -28px), làm các khung bị lệch vị trí.

- Padding 15px và Border 2px làm tăng kích thước phần tử.

- Chiều rộng hai khung chưa được tính toán hợp lý, dẫn đến giao diện bị
lệch.

### Phần 2: Thiết kế giải pháp

*1.  Cách khắc phục*

<u>Em đề xuất làm:</u>

- Đưa Margin về 0.

- Giữ Padding ở mức 15px.

- Giữ Border 2px.

- Điều chỉnh chiều rộng hai khung để không bị chồng lên nhau.

- Sử dụng box-sizing: border-box.

*2.  Nếu thay đổi Margin mà không kiểm tra Padding*

- Kích thước phần tử vẫn có thể bị sai, giao diện bị lệch hoặc tiếp tục
chồng lấn vì Padding cũng ảnh hưởng đến kích thước tổng thể.

*3.  Kết quả mong đợi*

- Hai khung hiển thị riêng biệt, không còn chồng lên nhau và giao diện dễ
nhìn hơn.
