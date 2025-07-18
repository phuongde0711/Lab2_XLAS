## 🧪 Lab 2 - Xử lý điểm ảnh: Biến đổi cường độ ảnh

### 👤 Thông tin sinh viên
- **Họ tên:** Lê Hoài Phương
- **MSSV:** 207CT10264
- **Môn học:** Nhập môn Xử lý ảnh số  
- **Giảng viên:** Đỗ Hữu Quân

---

### 📌 Mục tiêu bài Lab
Thực hành các phép biến đổi cường độ ảnh và hàm toán học để thay đổi độ sáng, độ tương phản cũng như chất lượng ảnh số. Các kỹ thuật trong Lab này đóng vai trò nền tảng cho việc:
- Cải thiện chất lượng hình ảnh đầu vào
- Tiền xử lý ảnh cho các bước xử lý sau như phân đoạn, trích đặc trưng

---

### 🛠️ Công nghệ & Thư viện sử dụng
- **Python**: Ngôn ngữ lập trình chính
- **Pillow (PIL)**: Đọc và ghi ảnh
- **NumPy**: Xử lý dữ liệu ảnh dưới dạng mảng
- **Matplotlib**: Hiển thị ảnh trực quan
- **ImageIO**: Đọc ảnh với định dạng phong phú

---

#### Bài 1: Biến đổi cường độ ảnh cơ bản
- **Mục đích:** Lật ngược ảnh bằng phép biến đổi âm bản (`Negative Transformation`)
- **Cách thực hiện:**
  - Đọc ảnh gốc dạng grayscale
  - Áp dụng công thức: `output = 255 - input`
- **Kết quả:** Hiển thị ảnh âm bản của ảnh chim (`bird.png`)

#### Bài 2: Thay đổi độ tương phản bằng Power Law (Hàm mũ)
- **Mục đích:** Nâng cao chi tiết vùng tối hoặc vùng sáng bằng hàm gamma correction
- **Cách thực hiện:**
  - Chuyển ảnh sang mảng `float`, chuẩn hóa [0,1]
  - Áp dụng công thức: `output = c * input^gamma`
  - Dùng `gamma = 5` để làm rõ vùng tối
- **Kết quả:** Ảnh sau khi tăng độ tương phản với gamma

#### Bài 3: Biến đổi logarit
- **Mục đích:** Làm nổi bật chi tiết ở vùng tối
- **Cách thực hiện:**
  - Dùng công thức `output = c * log(1 + input)`
  - Áp dụng chuẩn hóa kết quả về [0,255]
- **Kết quả:** Ảnh với chi tiết vùng tối được tăng cường

